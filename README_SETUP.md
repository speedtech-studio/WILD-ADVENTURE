# WILD ADVENTURE — INTERACTIVE JUMANJI MAP (Full-page Google Sites Embed)

This is an independent adventure-map website. **Do not change your working Pixel Explorer Check-In / Google Sheets script.** The already approved Wild Adventure map is the background, and a pixel explorer marker moves through the five checkpoints after a pupil confirms they finished a mission.

## Files
- `index.html` — fully functional map, mission-step controls, avatar animation, self-check, progress indicator, local browser save, and an optional PNG avatar upload.
- `assets/jumanji-adventure-map.png` — exact approved map artwork; **do not change its file name or folder**.

## Step 1: Add the real Google Sites links
Open `index.html` using a text/code editor. Search for `MISSION_URLS`.

```javascript
const MISSION_URLS = {
  1: 'https://sites.google.com/view/YOUR-SITE/mission-1',
  2: 'https://sites.google.com/view/YOUR-SITE/mission-2',
  3: 'https://sites.google.com/view/YOUR-SITE/mission-3',
  4: 'https://sites.google.com/view/YOUR-SITE/mission-4',
  5: 'https://sites.google.com/view/YOUR-SITE/mission-5'
};
```

**Those are examples only:** paste each real, PUBLISHED mission-page URL. Do NOT publish with those fictitious example links. Until URLs are added, the map still lets you test movement and unlocking, but clicking OPEN MISSION will explain that a link is missing.

## Step 2: Publish the map with GitHub Pages (free)
1. Create a GitHub repository for the map, for example `wild-adventure-interactive-map`.
2. Upload `index.html` and the `assets` folder with `jumanji-adventure-map.png` inside it. You can unzip the ZIP first. Preserve folder names.
3. In GitHub, select **Settings → Pages**, then **Deploy from a branch**, `main`, `/ (root)` and Save.
4. GitHub will display your site's actual URL after deployment. Do not guess the URL; open the link that GitHub provides and test it.
5. On mobile, the wide map is intentionally horizontally scrollable for readable checkpoint signs.

## Step 3: Embed as a full page in Google Sites
1. Open your Google Sites editor.
2. Select **Pages → + → Full page embed**.
3. Name it `Adventure Map`.
4. Paste your actual GitHub Pages URL (the published `index.html` page).
5. Publish Google Sites and test the full-page view with a student or test account.
6. Set your check-in Explorer Passport button's destination to the **published Google Sites Adventure Map page** when ready. This is optional and does not require changes to the attendance functions.

## Student flow
1. Press **OPEN MISSION 1** — the real Google Sites mission page opens in another tab, leaving the map available.
2. Complete the activities and submit the required work on that page.
3. Return to the map and tap **I'M DONE HERE!**.
4. Confirm **YES, I'M DONE!** — the explorer moves smoothly to the next checkpoint.
5. Select **OPEN MISSION 2** / **NEXT MISSION** and continue.
6. After Mission 5, the explorer reaches FINISH and a celebration appears.

## Student avatar from check-in
- The map includes the same pixel-style explorer design as the check-in prototype.
- Since GitHub Pages and Apps Script are **different websites/origins**, their browser storage is not directly shared. If pupils downloaded their avatar PNG at check-in, they can select **Explorer options → Use my Explorer Avatar PNG** to display it on this map.
- Avatar PNG and progress are saved locally **if browser storage is permitted**.

## Important limitations
- **A tap on "I'm Done" is self-reported**. It does NOT detect completion in Book Creator, Genially, Wordwall, Padlet, etc.
- The `0/5` indicator measures **pupil self-checks**, not a verified teacher assessment.
- Progress is stored on the device/browser, not Google Sheets. It will not automatically sync to another device, and private/incognito browsing or blocked third-party storage may clear it.
- If the same iPad is shared among pupils, use **Explorer options → Reset mission progress** between pupils, or give them separate devices/browser profiles.
- The attendance spreadsheet and existing Google Apps Script are unchanged.
- All student-facing content is in English; the visual remains Pixel Jumanji and shows no time labels.

## Optional: test before adding links
Run a local server in the folder, e.g. `python -m http.server 8000`, then open `http://localhost:8000`. This preserves the image path. Standalone local previews opened directly may also work, but web hosting is the intended method.

## If you specifically want to paste EMBED CODE
After hosting the map via GitHub Pages, you may use Pages → + → Full page embed → Embed code.
Copy `EMBED_CODE_COPY.txt`, change the `src` to your real published URL, then publish the Google Site.
For the cleanest fit, choose the URL option instead; paste the actual GitHub Pages URL directly.
`FULL_HTML_CODE_COPY.txt` contains all the HTML, CSS and JavaScript, but it still references `assets/jumanji-adventure-map.png`, so that image folder must be hosted beside it.
