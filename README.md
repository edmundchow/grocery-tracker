# 🛒 Saturday Market Tracker

A lightweight Progressive Web App (PWA) to track your weekly grocery spending at the market. Built with vanilla HTML, CSS and JavaScript — no frameworks, no dependencies, works fully offline.

---

## Features

- **Personal grocery list** — build your own dropdown of regular items with usual prices
- **Special items** — add one-off purchases and optionally save them to your list
- **Optional budget** — toggle a weekly budget on or off; see how much you have left in real time
- **Edit your list** — rename, re-categorise or delete any item at any time
- **Trip history** — every Saturday's shop is saved and viewable
- **Excel export** — export any trip or all trips to a `.xlsx` spreadsheet for budgeting
- **Editable app title** — tap the header to rename the app (e.g. Butcher Run, Pharmacy)
- **Offline first** — works with no internet after first load
- **Installable** — installs as a native-feeling app on Android via PWA or APK

---

## Screenshots

| Shopping | My List | History |
|---|---|---|
| Add items from your list or as specials | Edit, add or delete grocery items | View past trips and export to Excel |

---

## Live App

**[Open the app →](https://edmundchow.github.io/grocery-tracker/grocery-tracker.html)**

Or install it on Android — see [Installation](#installation) below.

---

## Files

```
grocery-tracker/
├── grocery-tracker.html     # Main app — all UI and logic
├── manifest.json            # PWA manifest for installability
├── sw.js                    # Service worker for offline support
├── icon-192.png             # App icon (192×192)
├── icon-512.png             # App icon (512×512)
└── README.md                # This file
```

---

## Installation

### Option A — Install directly in Chrome (Android)

1. Open [the app link](https://edmundchow.github.io/grocery-tracker/grocery-tracker.html) in **Chrome** on your Android phone
2. Tap the **⋮ menu** → tap **Add to Home screen**
3. Tap **Add** — the app icon appears on your home screen

### Option B — Install as APK (Android)

Generate a proper APK using [Bubblewrap](https://github.com/GoogleChromeLabs/bubblewrap):

```bash
npm install -g @bubblewrap/cli
bubblewrap init --manifest https://edmundchow.github.io/grocery-tracker/manifest.json
bubblewrap build
```

Transfer the generated `app-release-signed.apk` to your phone and install it.

> **Note:** You will need [Node.js](https://nodejs.org) installed. When prompted for Play Billing, select **No**.

---

## How to Use

### Adding items at the market

1. Open the app and go to the **Shopping** tab
2. Pick an item from the **From my list** dropdown — the usual price fills in automatically
3. Adjust the price if needed, then tap **Add to cart**
4. For a one-off item, use the **Special item** section — tick **Save to my list** to keep it for future use
5. When done, tap **Save this week's trip**

### Managing your list

- Go to the **My List** tab
- Tap **Edit** next to any item to change its name, category or usual price
- Tap **Add new item** at the bottom to add items directly without shopping

### Exporting to Excel

1. Go to the **History** tab
2. Choose a specific trip or **All trips** from the dropdown
3. Tap **Download spreadsheet** — saves a `.xlsx` file to your device

---

## Categories

| Colour | Category |
|---|---|
| 🟢 Green | Produce |
| 🔴 Red | Meat |
| 🔵 Blue | Dairy |
| 🟡 Amber | Bakery |
| 🟣 Purple | Pantry |
| ⚫ Grey | Other |

---

## Data & Privacy

- All data is stored **locally on your device** using IndexedDB
- No data is sent to any server
- No accounts, no sign-up, no tracking
- Clearing your browser/app data will erase your history

---

## Tech Stack

| Technology | Purpose |
|---|---|
| HTML / CSS / JavaScript | App UI and logic |
| IndexedDB | Permanent local data storage |
| Service Worker | Offline support and caching |
| Web App Manifest | PWA installability |
| SheetJS (xlsx) | Excel file export |
| Bubblewrap | Android APK generation |
| GitHub Pages | Free hosting |

---

## Updating the App

If you have the APK installed and want to update:

1. Make your changes to `grocery-tracker.html`
2. Upload the updated file to this GitHub repo
3. Wait ~2 minutes for GitHub Pages to update
4. On your phone: **Settings → Apps → Market Tracker → Storage → Clear Cache**
5. Reopen the app — it will load the latest version

To rebuild the APK after changes:
```bash
bubblewrap build
```

> Keep your `android.keystore` file and password safe — you need them to rebuild.

---

## Roadmap

- [ ] Multiple store support (Woolworths, Coles, IGA)
- [ ] Price comparison between stores
- [ ] Receipt photo attachment
- [ ] Monthly spending summary chart
- [ ] Family sharing / sync
- [ ] Google Play Store release

---

## License

Copyright © 2025 Edmund Chow. All Rights Reserved.

This code may not be copied, modified, distributed, or sold without explicit written permission from the author.

---

## Support

If you find this app useful, consider buying me a coffee ☕

*Built with ❤️ for Saturday market shoppers.*
