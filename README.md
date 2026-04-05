# 💸 Where My Money Went

> *"Where did it all go?"* — now you'll always know.

A lightweight Progressive Web App (PWA) to track exactly where your money goes each week at the market. Built with vanilla HTML, CSS and JavaScript — no frameworks, no dependencies, works fully offline.

---

## Features

- **Personal shopping list** — build your own dropdown of regular items with usual prices
- **Special items** — add one-off purchases and optionally save them to your list
- **Optional budget** — toggle a weekly budget on or off; see how much you have left in real time
- **Edit your list** — rename, re-categorise or delete any item at any time
- **Trip history** — every week's spending is saved and viewable
- **Excel export** — export any trip or all trips to a `.xlsx` spreadsheet for budgeting
- **Editable app title** — tap the header to rename the app for any use case
- **Offline first** — works with no internet after first load
- **Installable** — installs as a native-feeling app on Android via PWA or APK

---

## Live App

**[Open the app →](https://edmundchow.github.io/where-my-money-went/grocery-tracker.html)**

---

## Files

```
where-my-money-went/
├── grocery-tracker.html     # Main app — all UI and logic
├── manifest.json            # PWA manifest for installability
├── sw.js                    # Service worker for offline support
├── icon-192.png             # App icon (192×192)
├── icon-512.png             # App icon (512×512)
└── README.md                # This file
```

---

## Installation

### Option A — Install in Chrome (Android)

1. Open the [app link](https://edmundchow.github.io/where-my-money-went/grocery-tracker.html) in **Chrome** on your Android phone
2. Tap **⋮ menu** → **Add to Home screen** → **Add**

### Option B — Install as APK

```bash
npm install -g @bubblewrap/cli
bubblewrap init --manifest https://edmundchow.github.io/where-my-money-went/manifest.json
bubblewrap build
```

Transfer `app-release-signed.apk` to your phone and install.

---

## How to Use

### At the market
1. Pick an item from **From my list** dropdown — usual price fills in automatically
2. Adjust price if needed → tap **Add to cart**
3. For one-off items use **Special item** — tick **Save to my list** to keep it
4. When done tap **Save this week's trip**

### Managing your list
- Go to **My List** tab → tap **Edit** to change name, category or price
- Add new items at the bottom without needing to be shopping

### Exporting to Excel
1. Go to **History** tab
2. Choose a trip or **All trips**
3. Tap **Download spreadsheet**

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

- All data stored **locally on your device** using IndexedDB
- No data sent to any server
- No accounts, no sign-up, no tracking

---

## Updating the App

1. Make changes to `grocery-tracker.html`
2. Bump the version in `sw.js` (e.g. `v1` to `v2`)
3. Upload both files to GitHub
4. On phone: **Settings → Apps → Where My Money Went → Storage → Clear Cache**

---

## Roadmap

- [ ] Multiple store support
- [ ] Price comparison between stores
- [ ] Monthly spending summary chart
- [ ] Receipt photo attachment
- [ ] Family sharing / sync
- [ ] Google Play Store release

---

## Google Play Store Listing

### App title
Where My Money Went

### Short description (80 chars)
Track your weekly market spending. Know exactly where your money went.

### Full description
Ever get home from the market and wonder where all your money went?

Where My Money Went is a simple, no-fuss weekly spending tracker designed for real market shoppers. Build your own personal list of regular purchases, add them to your cart with one tap, and always know your running total before you reach the checkout.

FEATURES

✔ Your personal shopping list
Build a dropdown of your regular items with their usual prices. Adding your weekly groceries takes seconds — just pick and tap.

✔ Special items
Buy something out of the ordinary? Log it quickly and choose whether to save it to your list for next time.

✔ Optional weekly budget
Toggle a budget on or off. See your running total and how much you have left — or simply track spending without a limit.

✔ Full trip history
Every week's shop is saved. Go back and see exactly what you spent and on what.

✔ Export to Excel
Export any trip or your entire history to a spreadsheet for your financial budgeting and planning.

✔ Works offline
No internet needed at the market. Everything works offline, every time.

✔ 100% private
Your data stays on your phone. No accounts. No cloud. No tracking. Ever.

✔ Editable app title
Rename the app to anything — Butcher Run, Pharmacy, Hardware Store — it works for any regular weekly purchase, not just groceries.

Simple. Fast. Offline. Private.

### Category
Finance → Personal Finance

### Keywords
grocery tracker, market spending, budget tracker, weekly expenses, shopping list, expense tracker, offline budget, money tracker, farmers market, spending diary

### Suggested price
$1.49 AUD

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

## License

Copyright 2025 Edmund Chow. All Rights Reserved.

This code may not be copied, modified, distributed, or sold without explicit written permission from the author.

---

*Built with love for anyone who has ever wondered where their money went.*
