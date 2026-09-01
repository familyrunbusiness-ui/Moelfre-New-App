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

## v3.1 visual update
The selected **Letters** button now uses a stronger dark-blue background with white text so it is easier to see at a glance on a phone. No workflow, route, GPS, parcel, or delivery behaviour has been changed.

## v3.2 parcel counter
- Each tap on **Parcel** adds one parcel.
- The button displays the parcel quantity, e.g. `Parcel × 3`.
- **Remove one parcel** appears whenever the count is above zero.
- The dashboard summary shows total parcels.
- Delivery mode and today's selected list show parcel quantities.
- Existing v3.1 parcel selections migrate automatically to a count of 1.

## v3.3 field-delivery improvements
1. **Update GPS** is available on every dashboard stop and on the current delivery card. It stores the phone's current latitude/longitude locally and immediately uses that point for Google Maps routing.
2. **Post Box Number 1–8** are always included in Today's Route, even after **Clear today**.
3. Every stop has a **Collection** toggle. A collection-only address is included in Today's Route.
4. Every stop has a **Heavy & Large** toggle. A Heavy & Large-only address is included in Today's Route.
5. Collection and Heavy & Large markers are shown clearly in delivery mode and in today's route list.
6. GPS updates persist in the app's existing local storage and are not erased by **Clear today**.

## v3.3.1 front-screen cleanup
The **GPS ready** summary field has been removed from the front screen. GPS updating and stored GPS locations remain fully available and unchanged.

## v3.4 stats dashboard
Hidden round start/end base: 52°50'39.1"N 3°02'27.1"W. Adds Start Round, Finish Round, Today/Week/Month/All Time totals and per-round averages, round history, and CSV export. Stats are stored locally in the same browser storage as the app.


## v3.4.2 GPS backup
- Adds **Backup GPS** to export all GPS corrections made on the phone to a JSON backup file.
- Adds **Restore GPS** to import that backup later, including after an app update or when moving to another device.
- Restore replaces only the saved GPS overrides; daily selections, delivered progress, and stats are left alone.
- Includes all v3.4.1 changes, including Start/Finish Round controls together in Today's Route.
