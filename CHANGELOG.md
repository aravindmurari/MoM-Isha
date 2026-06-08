# Changelog

All changes made after the initial handover to Isha IT are documented here.
Each entry includes the file, the specific change, and any notes relevant for merging.

---

## 2026-06-07

### Email Templates — Tab Order Updated
**File:** `index.html`
**Change:** Moved the "To Your Organization Leader" tab to second position (after Corporations & Organizations). New order: Corporations & Organizations, To Your Organization Leader, Small Group / Friends & Family, Post-Session.

---

### Email Templates — "To Your Organization Leader" Tab Added
**File:** `index.html`
**Change:** Added a new tab to the Email Templates accordion: "To Your Organization Leader". Contains a personalized internal proposal email for volunteers to send to their own manager or team leader requesting an employee wellbeing session. Placeholders: [Leader's Name], [Team Name], [Company Name], [Your Name].

---

### Host a Group Session — Offerings Updated
**File:** `index.html`
**Change:** Removed "Yoga for Workplace · 45 min" from the session offerings list. Updated "Yoga for Health" duration from 1 hr to 75 min. New list: Miracle of Mind Experience Session · 30 min, Yoga for Health · 75 min, Yoga for Mental Well-being · 45 min.

---

## 2026-05-25

### Post-Session Report — Button Link Updated
**File:** `index.html`
**Change:** Updated the "Submit Report" button link from `https://isha.co/bb-kit/session-report` to `https://isha.us/mom-session-report`.

---

## 2026-05-23

### Email Templates — Content Updated from Master Sheet
**File:** `index.html`
**Source:** MoM-Artifacts Master Sheet → Email Templates Google Doc
**Change:** Replaced all previous tabs with 3 tabs matching the current document: Corporations & Organizations (formal proposal letter), Small Group / Friends & Family (personal session invite), and Post-Session (follow-up message with app download link and stay-connected form).

---

### Other Useful Content — Research Summary Removed
**File:** `index.html`
**Change:** Removed the "Sadhguru Center for a Conscious Planet — Research Summary" entry from Other Useful Content.

---

### Outreach Resources — Social Media Captions Section Removed
**File:** `index.html`
**Change:** Removed the Social Media Captions accordion card (Instagram, Facebook, LinkedIn, X tabs) from Outreach Resources entirely.

---

### Session Flow — Section Removed; Quick Reference Card Moved to Session Script
**File:** `index.html`
**Change:** Removed the Session Flow accordion card entirely. The Quick Reference Card PDF link has been added to the Session Script accordion header (alongside the existing Session Script link). The Session Checklist item "Review talking points" has also been renamed to "Review session script".

---

### Session Script — Content Updated from Master Sheet
**File:** `index.html`
**Source:** MoM-Artifacts Master Sheet → Session Script Google Doc
**Change:** Updated the Full Session Script accordion content to match the latest version of the document. Key changes:
- Removed "Waiting Announcement" phase
- "Welcome & Introduction" + "Sadhguru & Isha Intro" merged into a single upfront phase: "Welcome & Sadhguru Introduction" (~3.5 min); intro video now plays at the start, not as an optional late-session segment
- "Interaction" renamed to "Opening Questions" with updated dialogue
- "Introduce Miracle of Mind" updated with new text ("The human mind is a miraculous instrument...")
- "Introduction to Practice" removed as a separate phase
- New phase added: "App Features Walk Thru" (~3 min)
- "Managing Thoughts Video" renamed to "How to Meditate When Thoughts Are Noisy" with new dialogue
- "Closing" updated with new text (10,000 steps analogy, Harvard study reference)
- "Open file" link updated to match the canonical URL from the master sheet

---

### Flyer Generator — Template 1 Updated
**File:** `files/templates/1.png`, `files/templates/1.webp`
**Change:** Replaced Flyer Template 1 with a new design (four-panel photo collage, "FREE & OPEN TO ALL" / "Sadhguru Meditation Experience"). Both the PNG source and the WebP used by the generator have been updated.

---

## 2026-05-18

### Take It Further — Mobile Layout Fixed
**File:** `index.html`
**Change:** The four "Take It Further" cards now stack into a single column on mobile (≤768px) instead of showing as a partial 2-column grid that required horizontal scrolling. Side padding is also reduced on small screens to match the rest of the page.

---

## 2026-05-17

### Session Media — Playlist Order Updated
**File:** `index.html`
**Change:** Moved "Sadhguru & Isha Intro" from position 7 to position 3, immediately after the two Yoga Padhi videos. New order: Yoga Padhi · Waiting Yoga Padhi · Sadhguru & Isha Intro · Intro with Meditation · Managing Thoughts · Participant Experience · App Download QR Code.

---

### Session Media — Auto-Play Removed; Idle Placeholder Added
**File:** `index.html`
**Change:** No video plays automatically when the Session Media card is opened. A "Select a video from the playlist to play" placeholder is shown in the video area until the user clicks a playlist item.

---

### Session Media — Presentation View Behavior
**File:** `index.html`
**Change:** When the Presentation View window is open, videos play only on the presentation screen. The main page shows an overlay: "Video is playing on the presentation screen. Close the presentation view to preview here." When the presentation window is closed, the main page returns to the idle placeholder rather than auto-playing. Opening the Presentation View while a video is already selected on the main page immediately locks local playback and pushes the current video to the presentation screen.

---

### Revisit Training & Find a Session — Icons Added and Layout Updated
**File:** `index.html`
**Change:** Both the "Revisit Training" (🎓) and "Find a session near you" (📍) blocks now have an icon on the left with the text and button stacked to the right, consistent with the Submit Post-Session Report card layout. Button stretch bug also fixed.

---

### Session Script — Renamed from "Talking Points"; Short Session Tab Removed; Tab Renamed
**File:** `index.html`
**Change:** Renamed the "Talking Points" accordion card to "Session Script". Removed the "Short Session" tab. Renamed the "Full Session" tab to "Full Session Script". Updated the "↗ Open file" link label accordingly.

---

## 2026-05-15

### Outreach Resources — Card Order Updated
**File:** `index.html`
**Change:** Reordered cards in Outreach Resources. New order: App Features Guide, Booth Setup, Flyer Templates, Email Templates, WhatsApp Templates, Printables, Other Useful Content. App Features Guide and Booth Setup are now the first two items, above Flyer Templates.

---

### Session Resources — "Find a Session Near You" Moved and Restyled
**File:** `index.html`
**Change:** Moved the "Find a session near you" block from the bottom of the Session Resources section to directly below the "Revisit Training" card. Restyled the link as a solid amber button for greater prominence.

---

### Booth Setup — New Card Added to Outreach Resources
**File:** `index.html`
**Source:** MoM-Artifacts Master Sheet (Section: Promotion > Sub-Section: Booth Setup)
**Change:** Added a new expandable "Booth Setup" card positioned above Flyer Templates in the Outreach Resources accordion. Contains:
- **"↗ Open Guide"** link — published Google Doc (WebURL from master sheet)
- **Embedded video player** — direct Dropbox CDN `<video>` tag

---

### Unfollow Wall — Engagement Guide Link + New Document Added
**File:** `index.html`
**Change:** Renamed existing "Open file" button to "Engagement Guide". Added a second button ("Print Guide") linking to the new published Google Doc URL.

---

### Take It Further — Campus Club Email Updated
**File:** `index.html`
**Change:** "Explore a Campus Club" card email updated from `freeofferings@ishausa.org` to `miracleofmind@ishausa.org`.

---

### Email & WhatsApp Templates — Mobile Copy Button Added
**File:** `index.html`
**Change:** On mobile (≤768px), a "Copy" button now appears at the top of every template panel across Email Templates and WhatsApp Templates so users don't need to scroll past long text to find it. Desktop experience is unchanged.

---

### Session Flow & Session Script — Links Updated from Master Sheet
**File:** `index.html`
**Source:** MoM-Artifacts Master Sheet
**Change:** Updated document links for Session Flow PDF, Quick Reference Card, and Session Script to the latest versions from the master sheet.

---

### Disclaimer Bar — Removed; Hero Logo — Now a Link
**File:** `index.html`
**Change:** Removed the top disclaimer bar ("This is not the official Miracle of Mind website"). Wrapped the MoM logo in an `<a>` tag linking to the official Miracle of Mind page (`https://isha.sadhguru.org/us/en/miracle-of-mind`), opens in a new tab.

---

### Section Headers — Icons Added
**File:** `index.html`
**Change:** Replaced emoji icons with flat inline SVG icons that inherit the section's theme color via `currentColor`.
- Outreach Resources → Phosphor Icons `megaphone-fill` in amber
- Session Resources → Phosphor Icons `flower-lotus-fill` in teal

---

### Hero Stat — Downloads Label Updated
**File:** `index.html`
**Change:** Updated the hero stat label from "Downloads in 15 hrs" to "Downloads in first 15 hrs".

---

## 2026-05-08

### Session Media URLs — Migrated to Isha Dropbox
**File:** `index.html` → `const SM_URLS`
**Change:** All 7 session media entries moved from personal Dropbox folder to Isha Dropbox folder (`1sycc2gff066vuwgx0tci`). Videos are the optimized/faststart versions. `rlkey` updated to the correct file-level key (`ikz1rzvmog4ntns2xhv94tt4k`) for all entries including the QR code image.

---

### Take It Further Cards — Updates
**File:** `index.html`
- Renamed "Offer a Group Session" → "Host a Group Session"
- Replaced Group Session button with email link (`freeofferings@ishausa.org`) preceded by "Email us at" label
- CME card: replaced button with italic "Coming Soon" label in amber
- Campus Club card: removed button, added email + subject line hint with "Email us at" label

---

### Site Walkthrough Video — Added to Nav
**File:** `index.html`
**Change:** Added a "Watch Walkthrough" button to the top nav bar (right side). Opens a full-screen video modal playing `MoM-BBResourceKit-WalkThrough.mp4` from Isha Dropbox. Closes on X button, click-outside, or Escape key.

---

### Session Finder — Coming Soon Page
**Files:** `index.html`, `session-finder.html` (new)
**Change:** Created `session-finder.html` — a styled coming soon page for the MoM session location finder. The "Find a session near you" button in the Session Kit now links to `http://isha.us/MoMsession-finder`.
**Action required (Isha IT):** Map short URL `isha.us/MoMsession-finder` → `session-finder.html`. This page can later be replaced or the short URL redirected to the actual session finder tool.

---

### Firefox Freeze Fix — Video Preload Removed
**File:** `index.html`
**Bug:** The `<video id="smLocalPlayer">` element had a hardcoded `src` pointing to the Yoga Padhi MP4 with no `preload` attribute. Firefox started downloading the video immediately on page load, causing the browser to freeze.
**Fix:** Removed the hardcoded `src` and added `preload="none"`. Video `src` is now set dynamically only when a user clicks a video item.

---

### BoomBuddy Passcode Updated
**File:** `index.html`
**Change:** Updated the BoomBuddy access passcode to `LetsB00M!`.
**Note:** This passcode is shared with volunteers via email upon completion of BoomBuddy training. Update the email template accordingly.

---

### Rebrand — "Booom Buddy" → "Boom Buddy"
**Files:** `index.html`, `session-finder.html`, `flyer.html`, `DEPLOYMENT.md`
**Change:** All instances of "Booom" (3 O's) replaced with "Boom" (2 O's) across all site files to match updated branding.

---

### Other Useful Content — Corporate Presentation Deck Added
**File:** `index.html`
**Change:** Added "Miracle of Mind — Corporate Presentation Deck" as a new entry under Other Useful Content. Links to the Canva deck with a note to make a copy before editing.
