# Booom Buddy Resource Kit — Deployment Guide

This document is intended for the Isha IT team to assist with hosting this project on the official Isha web infrastructure.

---

## Overview

The Booom Buddy Resource Kit is a **fully static website** — no backend, no database, no build step required. It consists of plain HTML, CSS, and JavaScript files that can be served from any standard web server or CDN.

**Live reference:** `https://aravindmurari.github.io/MoM-Isha`

---

## File Structure

```
MoM-Isha/
├── index.html              # Main volunteer hub page
├── present.html            # Presentation view (full-screen video player)
├── flyer.html              # Flyer generator tool
├── files/
│   ├── hero-bg.png         # Hero section background image
│   ├── sadhguru-signature.avif  # Sadhguru signature image (hero section)
│   ├── MoM_Email_Templates.docx
│   ├── MoM_Social_Media_Captions.docx
│   └── templates/
│       ├── 1.png  …  12.png    # Flyer templates (original, high-res)
│       └── 1.webp …  12.webp   # Flyer templates (optimized WebP for display)
```

---

## Deployment Requirements

### Hosting
- Any static file server works (Apache, Nginx, Cloudflare Pages, etc.)
- **HTTPS is required** — the offline video caching feature uses IndexedDB and `fetch()`, which are blocked on plain HTTP in modern browsers.
- No server-side processing needed.

### CORS
The flyer generator draws template images onto an HTML Canvas element and exports them as PNG. For this to work, the template images (`files/templates/*.webp`) must be served from the **same origin** as the HTML pages. No special CORS configuration is needed as long as all files are hosted together on the same domain.

---

## External Dependencies

### Fonts (Google Fonts CDN)
Loaded via `<link>` tags in the `<head>`. No action needed unless the hosting environment blocks external CDN requests, in which case fonts should be self-hosted.
- `Trirong` (italic serif — used for headings and quotes)
- `Inter` (sans-serif — used for body text)

### MoM Logo Image
Loaded from Sadhguru's CDN:
```
https://static.sadhguru.org/d/46272/1739879389-group-1597883432.png
```
This can be downloaded and self-hosted if preferred.

---

## Session Media Videos

Videos are currently hosted on **Dropbox** and streamed directly via `<video>` elements. The URLs are defined in `index.html` in a JavaScript object called `SM_URLS` (search for `const SM_URLS`).

**Recommendation:** Move the video files to Isha's own CDN or media server and update the URLs in `SM_URLS` accordingly. The videos have already been optimized with the MP4 `faststart` flag for faster browser playback.

Current videos:
| Key | File |
|-----|------|
| `yoga-padhi` | 1_MoMEx_Yogapadhi_15min.mp4 |
| `waiting-yp` | 2_MoMEx_waitingYP_4min.mp4 |
| `intro-med` | 4_MoMIntroandMeditation.mp4 |
| `managing` | 5_MoM_post_video.mp4 |
| `participant` | MoM-ParticipantSharing.mp4 |
| `qr-code` | QRcode.png |
| `sg-isha` | 6__MoMEx_SGIshaIntro_3mi.mp4 |

To update, find `const SM_URLS` in `index.html` and replace the Dropbox URLs with the new hosted URLs.

---

## Access Control (BoomBuddy Gate)

Part of the site (Session Resources section) is protected by a client-side passcode. The passcode is defined near the top of the `<script>` block in `index.html`:

```javascript
const BB_PASS = 'BoomBuddy123';
```

Update this to the finalized passcode before go-live. This passcode is also shared with volunteers via email upon completion of BoomBuddy training.

> Note: This is client-side access control intended to add a friction layer, not cryptographic security. It is appropriate for this use case.

---

## Cross-Window Communication (Presentation View)

`present.html` is designed to be opened in a second browser window/screen during a session. It communicates with `index.html` via `localStorage` (key: `smCurrentVideo`). This works entirely in the browser with no server involvement.

---

## Google Drive Links

Several downloadable resources (Talking Points, Session Flow PDF, printables) link directly to Google Drive. These links are embedded in `index.html` as `href` attributes. They can be updated to point to Isha-hosted equivalents by searching for `drive.google.com` in `index.html`.

---

## What to Update Before Go-Live

| Item | Where | Action |
|------|--------|--------|
| Video URLs | `index.html` → `const SM_URLS` | Replace Dropbox URLs with Isha CDN URLs |
| BoomBuddy passcode | `index.html` → `const BB_PASS` | Set to finalized passcode |
| Google Drive doc links | `index.html` → search `drive.google.com` | Optionally migrate to Isha-hosted docs |
| Footer URL reference | `index.html` → footer | Update GitHub Pages URL to Isha domain |

---

## No Build Step

There is no npm, no bundler, no compilation. To deploy:

1. Copy all files to the web server root (or a subdirectory).
2. Ensure the server serves `index.html` as the default document.
3. Verify HTTPS is active.
4. Test the flyer generator (canvas export) and video playback.

That's it.
