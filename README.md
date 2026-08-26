# Moelfre 330-stop GPS route app

This package contains a phone-friendly route tracker built from the supplied 330-stop master route.

## Main features
- Preserves stops 1–330 in the supplied order.
- Shows your live phone GPS position.
- Shows distance to the selected stop.
- `Set this stop to my current GPS position` records a personally verified coordinate.
- Keeps the original coordinate separately and prefers the verified one thereafter.
- Marks stops complete and advances to the next stop.
- Stores progress in browser local storage on that device.
- Exports verified coordinates and completion status to CSV.
- Opens the selected effective coordinate in Google Maps.

## Running it on a phone
Live browser geolocation normally requires a secure HTTPS page. Upload these files to an HTTPS static host such as GitHub Pages, Netlify, Cloudflare Pages, or your own HTTPS server, then open that HTTPS address on your phone and allow location access.

Opening `index.html` directly as `file://` may not allow GPS on some phones.

## Important route note
The line drawn inside this app simply connects the stops in your supplied order. It is not turn-by-turn road routing. Use the Google Maps button when you want external navigation to the currently selected stop.

## Backup
Use **Export progress** regularly. Browser local storage can be lost if site data is cleared or if you move to a different browser/domain.
