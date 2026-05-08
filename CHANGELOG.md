# Changelog

All changes made after the initial handover to Isha IT are documented here.
Each entry includes the file, the specific change, and any notes relevant for merging.

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

// After
const BB_PASS = 'LetsB000M!';
```
**Note:** This passcode is shared with volunteers via email upon completion of BoomBuddy training. Update the email template accordingly.
