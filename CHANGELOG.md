# Changelog

All changes made after the initial handover to Isha IT are documented here.
Each entry includes the file, the specific change, and any notes relevant for merging.

---

## 2026-05-15

### Outreach Resources — Card Order Updated
**File:** `index.html`
**Change:** Reordered cards in Outreach Resources. New order: App Features Guide, Booth Setup, Flyer Templates, Email Templates, WhatsApp Templates, Social Media Captions, Printables, Other Useful Content. App Features Guide and Booth Setup are now the first two items, above Flyer Templates.

---

### Session Resources — "Find a Session Near You" Moved and Restyled
**File:** `index.html`
**Change:** Moved the "Find a session near you" block from the bottom of the Session Resources section to directly below the "Revisit Training" card. Restyled the link as a solid amber button (matching the visual pattern of the Revisit Training button) for greater prominence.

---

## 2026-05-15

### Booth Setup — New Card Added to Outreach Resources
**File:** `index.html`
**Source:** MoM-Artifacts Master Sheet (Section: Promotion > Sub-Section: Booth Setup)
**Change:** Added a new expandable "Booth Setup" card positioned above Printables in the Outreach Resources accordion. Contains:
- **"↗ Open Guide"** link (top-right) — published Google Doc (WebURL from master sheet)
- **Embedded video player** — direct Dropbox CDN `<video>` tag (`dl.dropboxusercontent.com`, file hash `ALPmFro7gTjMBzSWliFVX2Q`, rlkey `ozpzdll9z9ymv07vvv17k3ovk`)

---

### Unfollow Wall — Engagement Guide Link + New Document Added
**File:** `index.html`
**Change:** Renamed existing "Open file" button to "Engagement Guide". Added a second button ("Print Guide") linking to the new published Google Doc URL.

---

### Take It Further — Campus Club Email Updated
**File:** `index.html`
**Change:** "Explore a Campus Club" card email updated from `freeofferings@ishausa.org` to `miracleofmind@ishausa.org`.

---

### Template Labels — Amber Color Applied Across All Three Cards
**File:** `index.html`
**Change:** Template label color (e.g. "Caption 1 — Quote post", "Friends & Family", etc.) updated from `--mom-muted` (#6e665b) to `--vol-amber` (#d4914a) across Email Templates, WhatsApp Templates, and Social Media Captions for better visibility and visual distinction.

---

### Email / WhatsApp / Social Media — Mobile Copy Button Added
**File:** `index.html`
**Change:** On mobile (≤768px), a "Copy" button now appears at the top of every template panel across Email Templates (5), WhatsApp Templates (5), and Social Media Captions (IG×4, FB×2, LinkedIn×2, X×2) so users don't need to scroll past long text to find it. The bottom copy button is hidden on mobile to avoid duplication. Desktop experience is unchanged.

---

### Talking Points — Web URL Updated from Master Sheet
**File:** `index.html`
**Source:** MoM-Artifacts Master Sheet
**Change:** Updated the published Google Doc URL for the Talking Points "Open file" link in the Session Kit.
```
Before: ...2PACX-1vS2vLzhk3sGpuUEOOJ5rFdaG0-nVyT_itKQVMSq0wcTMjOQQxyx8ihWUWXv5D4PaIhjFBaJjq06OVlK/pub
After:  ...2PACX-1vTRKzbV3BDQ4pi9cz7wZpf_O8wZo2hIiVa9LuRdLoaSkpRsCcTNySpNoYmCWfMISUjHHyYwSLptvW3_/pub
```

---

### Session Flow — Links Updated from Master Sheet
**File:** `index.html`
**Source:** MoM-Artifacts Master Sheet
**Change:** Updated both document links in the Session Flow card to the latest versions.
```
Session Flow PDF:
  Before: drive.google.com/file/d/1jTYElEkUqcRFfxiJI2aqCTDFiQ14GGqo
  After:  drive.google.com/file/d/1Q04cA42TFbLMe6iqjU5tDUlYIkVGILbT

Quick Reference Card:
  Before: drive.google.com/file/d/1Q1Ele1flvU78CG2fdBIExb-bx5RTnRUs
  After:  drive.google.com/file/d/14SXhep0eZa1LyEh4NUnZR6ITdV4p37lF
```

---

### Disclaimer Bar — Removed
**File:** `index.html`
**Change:** Removed the top disclaimer bar ("This is not the official Miracle of Mind website"). The MoM logo in the hero section is now a clickable link to `isha.sadhguru.org/us/en/miracle-of-mind` instead.

---

### Hero Logo — Now a Link
**File:** `index.html`
**Change:** Wrapped the MoM logo `<img>` in an `<a>` tag linking to the official Miracle of Mind page (`https://isha.sadhguru.org/us/en/miracle-of-mind`), opens in a new tab.

---

### Section Headers — Icons Added
**File:** `index.html`
**Change:** Replaced emoji icons with flat inline SVG icons that inherit the section's theme color via `currentColor`.
- Outreach Resources → Phosphor Icons `megaphone-fill` in amber (`--c-tool`)
- Session Resources → Phosphor Icons `flower-lotus-fill` in teal (`--c-session`)

---

### Hero Stat — Downloads Label Updated
**File:** `index.html`
**Change:** Updated the hero stat label for clarity.
```
Before: "Downloads in 15 hrs"
After:  "Downloads in first 15 hrs"
```

---

## 2026-05-08

### Talking Points & Session Flow Content Update
**File:** `index.html`
**Source:** Updated Google Drive documents — `MoM-TalkingPoints` and `MOM-SessionFlow-QuickReferenceGuide-1Page.pdf`

**Talking Points — Full Session:**
- Renamed phase "Hand Demonstration" → "Introduce Miracle of Mind"
- Updated dialogue: added "which can assist you in this direction?" and new line "Sadhguru will first explain the science behind the Miracle of Mind meditation, and then guide us through it."

**Talking Points — Short Session (Punya Pooja):**
- Expanded the Closing section to include Inner Engineering content (program description, personal testimony placeholder, and in-person program invite)

**Session Flow:**
- Split old step 5 "Engaging Participants" into two steps: "5 · Interaction" and "6 · Introduce Miracle of Mind"
- Renamed step 6 "Introduce MoM App..." → "7 · Introduction to Practice" (same content, cleaner title)
- Updated step 7 → "8 · Guided Meditation" — duration corrected to ~9 min (was 7 min)
- Updated step 8 → "9 · Sharing" — now specifies taking 2–3 sharings
- Removed old step 13 "Customizing for Audience"
- Renamed old step 12 → "13 · App Download CTA" (concise)
- Updated step 14 "Closing" — added "Do Namaskar"
- Added duration indicators to all step labels (e.g., ~1 min, ~2 min)
- Added "On screen" cues to steps 1, 2, 8, 13

---

### Session Media URLs — Migrated to Isha Dropbox
**File:** `index.html` → `const SM_URLS`
**Change:** All 7 session media entries moved from personal Dropbox folder (`hp1orcoku47w1517cf6ql`) to Isha Dropbox folder (`1sycc2gff066vuwgx0tci`). Videos are the optimized/faststart versions. `rlkey` updated from folder-level key to the correct file-level key (`ikz1rzvmog4ntns2xhv94tt4k`) for all entries including the QR code image.

---

### Take It Further Cards — Updates
**File:** `index.html`
- Renamed "Offer a Group Session" → "Host a Group Session"
- Replaced Group Session button with email link (`freeofferings@ishausa.org`) preceded by "Email us at" label
- CME card: replaced button with "Coming soon" badge
- Campus Club card: removed button, added email + subject line hint with "Email us at" label

---

### Site Walkthrough Video — Added to Nav
**Files:** `index.html`
**Change:** Added a "Watch Walkthrough" button to the top nav bar (right side). Opens a full-screen video modal playing `MoM-BBResourceKit-WalkThrough.mp4` from Isha Dropbox. Closes on X button, click-outside, or Escape key. Removed the redundant "Miracle of Mind App ↗" nav button (same URL already present in the page footer disclaimer).

---

### Session Finder — Coming Soon Page
**Files:** `index.html`, `session-finder.html` (new)
**Change:** Created `session-finder.html` — a styled coming soon page for the MoM session location finder. The "Find a session near you" button in the Session Kit now links to `http://isha.us/MoMsession-finder`.
**Action required (Isha IT):** Map short URL `isha.us/MoMsession-finder` → `session-finder.html`. This page can later be replaced or the short URL redirected to the actual session finder tool.

---

### Firefox Freeze Fix — Video Preload Removed
**File:** `index.html`
**Bug:** The `<video id="smLocalPlayer">` element had a hardcoded `src` pointing to the Yoga Padhi MP4 (15 min) with no `preload` attribute. Firefox started downloading the video immediately on page load, causing the browser to freeze.
**Fix:** Removed the hardcoded `src` and added `preload="none"`. Video `src` is now set dynamically by `smPlay()` only when a user clicks a video item.

---

### BoomBuddy Passcode Update
**File:** `index.html`
**Change:** Updated the BoomBuddy access passcode.
```javascript
// Before
const BB_PASS = 'BoomBuddy123';

// After (updated again later in this session — see below)
const BB_PASS = 'LetsB000M!';
```
**Note:** This passcode is shared with volunteers via email upon completion of BoomBuddy training. Update the email template accordingly.

---

### BoomBuddy Passcode — Updated Again
**File:** `index.html`
**Change:** Passcode updated a second time.
```javascript
// Before
const BB_PASS = 'LetsB000M!';

// After
const BB_PASS = 'LetsB00M!';
```

---

### Rebrand — "Booom Buddy" → "Boom Buddy"
**Files:** `index.html`, `session-finder.html`, `flyer.html`, `DEPLOYMENT.md`
**Change:** All 12 instances of "Booom" (3 O's) replaced with "Boom" (2 O's) across all site files to match updated branding.

---

### CME Card — Coming Soon Text Styling
**File:** `index.html`
**Change:** Replaced the "Coming soon" pill badge on the CME card with a plain italic text label in amber color, matching the card's accent color.

---

### Other Useful Content — Corporate Presentation Deck Added
**File:** `index.html`
**Change:** Added "Miracle of Mind — Corporate Presentation Deck" as a new entry under Other Useful Content. Links to the Canva deck with a note to make a copy before editing.
