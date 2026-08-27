# Moelfre Daily Round Planner — v3

This is a separate app from v2.

## Daily workflow
1. Search or scroll the full 330-house list.
2. Tap Letters and/or Parcel for each destination.
3. Use Selected only to review the day's work.
4. Press Create today's route.
5. Work through the selected stops in the original round order.
6. Mark each stop Delivered; the app advances to the next selected stop.
7. Open individual houses or route legs in Google Maps when needed.

## GPS data
The app uses the uploaded field-verification export.
Verified coordinates are preferred. If a stop has no verified coordinate, its original first-pass coordinate is retained as a fallback and shown as approximate.

## Hosting alongside v2 on GitHub Pages
To keep v2 untouched, create a folder named `v3` in the same GitHub repository and put:
- index.html
- manifest.webmanifest
- sw.js

inside that folder.

If your current v2 app is:
`https://USERNAME.github.io/REPOSITORY/`

then v3 should be:
`https://USERNAME.github.io/REPOSITORY/v3/`

The dashboard selections and delivered progress are stored in that browser/device using local storage.
