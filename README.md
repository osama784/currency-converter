# Syrian Currency Converter — محول العملة السورية

Live demo: **https://syrian-currency-converter.vercel.app**

A small single-page tool for everyday cash handling in Syria. It converts between **old Syrian pounds** (ليرة قديمة) and the **new Syrian pound cash** (نقد جديد) at a fixed rate of 100 old = 1 new, and helps you check whether the cash in your wallet covers what a seller is asking for.

The tool's UI is Arabic and right-to-left; this README is in English.

## Features

- **Two-way conversion** between old lira and new cash — type an amount in either field and the other updates instantly (100 old = 1 new).
- **Payment assistant** (مساعد الدفع): enter the amount the seller asked for (in new or old cash), enter what you have in new cash and old lira, and it shows whether the amount is covered or short, along with a suggested way to pay.
- **Quick-add buttons** for common new-cash denominations (10, 25, 50, 100, 200, 500) to build up your wallet total, plus a reset button to clear everything.

## About the rate

The 100:1 old-to-new ratio is **hardcoded** in the page's JavaScript. There is no exchange-rate API, no live or fetched data, and no other currencies involved — it is a fixed-ratio calculator for old and new Syrian pound cash only. Rates are not updated from any external source.

## Tech stack

- A single static `index.html` containing the markup, inline CSS, and inline vanilla JavaScript.
- No framework, no build step, no dependencies to install.
- Tailwind CSS is loaded from its CDN and the Cairo font from Google Fonts, so styling requires an internet connection; the conversion logic itself is plain inline JavaScript.
- Assets: `dollar-sign.png` (favicon) and `site-screenshot.png` (social preview image).

## Run locally

Open `index.html` directly in a browser, or serve the folder with any static server, e.g.:

```sh
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Credits

Built by محمد هويدي (Muhammad Huwaidi).
