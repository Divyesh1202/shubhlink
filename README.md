# ShubhLink — Personalized WhatsApp Wishes

Free static website for personalized text greetings, including Birthday, Good Morning, Daily Suvichar, Nava Vichar, Good Night, Festivals, Friendship, Anniversary, Congratulations, and Good Afternoon.

## Run on your computer or mobile

- Extract the ZIP.
- Open `index.html` in Chrome/Edge to test the design.
- Enter recipient and sender names, choose a message and press **WhatsApp પર મેસેજ મોકલો**.
- To share a *website link*, the site MUST be published on a public HTTPS URL first. From a local file, text sharing works but personalized links cannot be used by friends.

## Free GitHub Pages publishing

1. Sign in to [github.com](https://github.com) and create a **public** repository, e.g. `shubhlink`.
2. Upload the **contents of this folder** (not its parent folder) to the repository's root.
3. Repository → Settings → Pages → Source: **Deploy from a branch** → Branch `main` → Folder `/ (root)` → Save.
4. Open the GitHub Pages address when publishing is complete (e.g. `https://YOUR_USERNAME.github.io/shubhlink/`). Do not share a guessed URL before verifying publication.
5. Try creating a name-based wish; its WhatsApp message contains the personal greeting **and** the hosted link.

## Setup for owner before public launch

- Replace `ShubhLink` brand if you prefer a different name. 
- Add a real **contact email** to `about.html` and `privacy.html` before launch.
- Check the Privacy Policy before enabling tracking, hosting analytics, third-party adverts or external APIs.
- `data.js` stores all the sample original wish texts; you can add/edit them and maintain the category groups.
- Existing wishes rotate for the daily quote based on the local device's date; for truly *new* content every day you will need to add templates or connect a moderated content system.
- WhatsApp preview for an individually named URL is *generic* on static hosting (the WhatsApp **message text itself is personalized**). Personalized link-preview images require backend/edge rendering.

## AdSense and earning revenue

No advertisements are enabled in this initial version. **Google AdSense application and approval are separate**; neither approval nor revenue is guaranteed. Before applying, launch the website, add useful original content, complete legal/contact information, comply with policy and monitor real visitor interest. Never encourage fake ad clicks, forced sharing, paid traffic exchanges or automated views.

Official Google documentation:
- Eligibility: https://support.google.com/adsense/answer/9724
- Invalid traffic: https://support.google.com/adsense/answer/1348729
- ads.txt: https://support.google.com/adsense/answer/12171244

When approved, add the exact AdSense code and approved ads.txt seller line supplied in **your** account. Do not use a fabricated publisher ID. Ensure ads are separated from the WhatsApp sharing button to prevent accidental ad clicks.

## Implementation

Plain HTML, CSS, and JavaScript. No build, paid service or server required. Uses Google Fonts (optional network request) and `localStorage` to remember sender name and language locally. All name/message inputs use `textContent` rather than injecting HTML. URLs containing names are visible to anyone with the link. Offline PNG card generation uses Canvas, but actual output depends on the device/browser Gujarati font support.
