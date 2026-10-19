# Dave Palarion Portfolio — Live Visitor Counter

This GitHub Pages website includes a live **Visitors online now** count and **Total website visits** counter. The numbers are real Firebase Realtime Database data; no fake initial counts.

## Required one-time Firebase setup

1. Visit https://console.firebase.google.com/ and create a Firebase project.
2. Add a **Web app** in Project settings. Copy its Firebase config values into `firebase-config.js` (including `databaseURL`).
3. Under **Build → Authentication → Sign-in method**, enable **Anonymous** authentication.
4. Under **Build → Realtime Database**, create a database (choose a nearby region if offered). Copy its database URL into `firebase-config.js`.
5. Under Realtime Database **Rules**, paste the contents of `database.rules.json` and **Publish**. Do not leave the database in unrestricted test mode.
6. Under Authentication → Settings → Authorized domains, ensure `davepalarion.github.io` is added if needed.
7. Upload `index.html`, `profile.jpg`, and `firebase-config.js` to the root of your public `davepalarion.github.io` repository. (The rules JSON is applied in Firebase Console, not hosted as your database rules.)
8. In GitHub repository Settings → Pages, deploy from `main` branch and root. Open https://davepalarion.github.io .

## Counting behavior

- **Total visits:** increments once per tab session, so refreshing the same tab does not add another visit. Opening a new tab or session adds a visit. This is *not* a unique-person count.
- **Online visitors:** counts Firebase anonymous-authenticated connected sessions, updated in real time via Realtime Database presence. Disconnects may take a short time to register. Multiple tabs sharing the same anonymous identity may count as one online visitor.
- **Important:** Client-side counters can be inflated by automated traffic or malicious users; this is suitable for a personal portfolio, not trusted analytics. Firebase may charge if free usage limits are exceeded.
- Before Firebase is configured, counters show a dash and a setup note rather than invented data.
