# Dave Palarion | Personal Portfolio

Welcome to my personal portfolio website! This site highlights my background, technical interests, projects, and photo gallery.

🌐 **Live website:** [davepalarion.github.io](https://davepalarion.github.io)  
💻 **GitHub:** [@davepalarion](https://github.com/davepalarion)

## About Me

I am an aspiring **Computer Engineer and IT Support Engineer** with a strong interest in hardware, software, networking, troubleshooting, and technical support.

I am passionate about solving technical challenges, maintaining reliable IT systems, and providing effective solutions that improve productivity and efficiency.

With a commitment to continuous learning and professional growth, I aim to enhance my technical expertise, stay updated with emerging technologies, and contribute to the success of an organization through dependable IT support and innovative solutions.

## Website Features

- **Responsive design** for desktop, tablet, and mobile devices
- **Light and Dark Mode** toggle with matching colors
- **Interactive constellation background** that responds to cursor movement and changes color with the theme
- **Animated navigation** with clean hover underlines
- **Profile photo** with a subtle, borderless glow
- **About Me, Skills, Projects, and Contact** sections
- **Modern photo gallery** with hover animations and full-screen photo viewing
- **Manual photo navigation** (automatic slideshow is disabled)
- **Firebase-powered visitor counters** for online visitors and total visits, once configured

## Technologies

- HTML5
- CSS3
- JavaScript
- Firebase Authentication and Realtime Database (for visitor counters)
- GitHub Pages (hosting)

## Run Locally

1. Download or clone this repository:

   ```bash
   git clone https://github.com/davepalarion/davepalarion.github.io.git
   ```

2. Open `index.html` in a browser. For features that require a web origin, such as Firebase, use a local web server instead.

3. To run a simple local server with Python:

   ```bash
   python -m http.server 8000
   ```

4. Visit `http://localhost:8000`.

## Publish with GitHub Pages

1. Create a public GitHub repository named `davepalarion.github.io`.
2. Upload your website files, including `index.html`, `profile.jpg`, and any gallery images referenced in the HTML.
3. Open **Settings → Pages** in the repository.
4. Under **Build and deployment**, select **Deploy from a branch**, choose `main` and `/(root)`, then save.
5. Once deployment finishes, visit [https://davepalarion.github.io](https://davepalarion.github.io).

## Firebase Visitor Counter Setup

The online and total-visit counters require Firebase configuration; they will not show real visitor counts until setup is complete.

1. Create a project in the [Firebase Console](https://console.firebase.google.com/).
2. Register a Web app and copy its Firebase configuration.
3. Enable **Anonymous Authentication** and create a **Realtime Database**.
4. Apply appropriate Realtime Database security rules for the counter implementation. Do not enable unrestricted public writes.
5. Add the configuration to the website's Firebase configuration file or script, matching the implementation in `index.html`.
6. Publish the updated files to GitHub Pages and test the counters in two separate browsers.

> **Note:** Total visits are not necessarily unique people, and online visitor counts can be approximate. Public counters should be treated as informational rather than tamper-proof analytics.

## Photo Gallery

The gallery contains a **Friends & Memories** photo. The homepage profile photo is intentionally excluded from the gallery. To add more images, upload the image files and add matching gallery entries to `index.html`.

## Customization

Edit `index.html` to update the text, projects, links, colors, and gallery items. Keep image paths consistent with the files in your repository.

## Contact

- GitHub: [github.com/davepalarion](https://github.com/davepalarion)
- Portfolio: [davepalarion.github.io](https://davepalarion.github.io)

---

© 2026 Dave Palarion. Built for GitHub Pages.
