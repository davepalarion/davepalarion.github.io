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

Visitor counters are displayed in the upper-right of the website header. Firebase setup is still required for live values.

## Mobile view and light/dark theme
The layout adapts automatically to phone screens. Use the theme button in the navigation bar to switch between light and dark mode. It remembers the selection on the same browser, and initially follows device preference. Firebase counters remain in the footer and require configuration.

## Constellation colors
In light mode the constellation uses dark navy stars and lines; in dark mode it keeps the original blue glow. The change updates instantly with the theme toggle.

## Coordinated theme palette
Buttons, cards, navigation, tags, footer counters and animated accents now use consistent dark/light CSS variables. Light mode has navy constellation lines; dark mode has luminous blue lines.

## iOS-inspired glass navigation
The navigation now uses frosted glass blur, translucent panels, a sliding active-link indicator, hover animations, and a stronger floating shadow while scrolling. It supports both themes, phones, and reduced-motion preferences.

## Modern animated navigation
The glass navigation has an entrance animation, a soft sweeping highlight, a sliding active-section indicator on desktop, and an animated hamburger menu on phones. It supports keyboard navigation and reduced-motion settings.

## Navigation hover animation
On desktop, hovering or keyboard-focusing a navigation link moves the glass highlight pill smoothly under that link. The selected section is restored when the pointer leaves. Mobile navigation uses a simple touch highlight. Reduced-motion settings are respected.

Navigation update: removed the iOS glass hover highlight and sliding pill. Links now use a simple animated underline, with the responsive mobile menu retained.

Profile glow: light mode uses a stronger muted royal-blue halo to complement the pale blue background; dark mode uses cyan-blue. Reduced-motion settings are respected.

## Photo Gallery
The Gallery section includes your existing profile.jpg and two placeholders. To add photos, upload images (for example photo2.jpg) beside index.html, then replace a gallery-placeholder div in index.html with: <button class="gallery-photo" type="button" data-full="photo2.jpg" data-caption="My Photo"><img src="photo2.jpg" alt="My Photo" loading="lazy"><span>My Photo</span></button>. The lightbox automatically supports the new photo. Do not upload private photos you do not want publicly visible.

## Modern animated gallery
The gallery now features elevated photo cards, smooth zoom and reveal animations, responsive layout, and an animated full-screen viewer with swipe support on touchscreens. Add more photos by copying an existing `.gallery-photo` button in `index.html` and updating its `src`, `data-full`, and caption. Reduced-motion settings are respected.
