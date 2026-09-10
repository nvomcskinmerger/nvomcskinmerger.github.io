# 🎨 NVO MC SKIN MERGER

<p align="center">
  <strong>Advanced Minecraft Skin Merger</strong><br>
  Combine, remix and preview Minecraft skins directly in your browser.
</p>

<p align="center">
  <a href="https://nvomcskinmerger.github.io/">🌐 Live Demo</a> •
  <a href="https://github.com/nvomcskinmerger/nvomcskinmerger.github.io/issues">🐛 Report a Bug</a> •
  <a href="https://github.com/nvomcskinmerger/nvomcskinmerger.github.io">💻 Repository</a>
</p>

---

## ✨ Overview

**NVO MC Skin Merger** is a browser-based Minecraft skin merging tool built for players and creators who want to combine multiple Minecraft skins without opening a desktop image editor.

The project supports traditional 2-skin merging as well as **3 Skin** and **4 Skin** workflows, multiple Minecraft skin resolutions, Minecraft username loading, 2D result previews, 3D character preview, custom body-part selection, history/gallery features and additional experimental merge modes.

The application is designed as a **single-page web application** and can be hosted directly with GitHub Pages.

> **Current release:** `V1.0.0`

---

## 🚀 Features

### 🧩 Multi-Skin Merger

The merger supports up to **4 input skins**.

#### 2 Skin

Use the standard merger modes with Skin 1 and Skin 2.

#### 3 Skin

The 3-skin workflow combines the inputs in stages:

1. Skin 1 + Skin 2 are combined with the existing **50/50 vertical merger**.
2. The intermediate result is combined with Skin 3 using the existing **top/bottom merger** logic.

#### 4 Skin

The 4-skin workflow combines the inputs in stages:

1. Skin 1 + Skin 2 are combined with the existing **50/50 vertical merger**.
2. Skin 3 + Skin 4 are combined with the existing **50/50 vertical merger**.
3. The two intermediate results are combined using the existing **top/bottom merger** logic.

This keeps the multi-skin workflow based on the same merger mechanics rather than introducing a separate split/merge engine.

---

## 🛠️ Merge Modes

The application includes a collection of ready-to-use and advanced merger modes, including:

- **50/50 / Half Merger**
- **3 Skin Merger**
- **4 Skin Merger**
- **Head Swap**
- **Top / Bottom**
- **Arm Swap**
- **Leg Swap**
- **Outer Overlay**
- **Base Only**
- **Front / Back**
- **Blend**
- **Chimera / Random Mix**
- **Body Swap**
- **Alternating Parts**
- **Cross Limb Swap**
- **Gradient Blend**
- **Custom Selective Merger**

The exact available modes may evolve as the merger engine is updated.

---

## 🎯 Custom Selective Merger

The **Custom Selective Merger** allows individual body sections to be selected from Skin 1 or Skin 2.

Supported selections include:

- Head
- Torso / Body
- Right Arm
- Left Arm
- Right Leg
- Left Leg
- Outer / Overlay layer

Overlay parts can also be disabled independently.

Quick actions are available for:

- **All Skin 1**
- **All Skin 2**
- **All Overlays Off**

---

## 🧱 Supported Skin Formats

The merger accepts Minecraft skin PNG files in these formats:

| Format | Support |
|---|---|
| `64×32` | ✅ Supported and converted to the modern `64×64` UV layout |
| `64×64` | ✅ Native |
| `128×64` | ✅ Supported |
| `128×128` | ✅ Native / dedicated processing pipeline |

### Important

When combining skins, the input skins must use the **same compatible format** for the selected merger operation.

The application validates PNG files, dimensions and compatibility before processing.

---

## 👤 Minecraft Username Skin Loading

Instead of uploading a PNG manually, you can enter a Minecraft username and use **Getir / Fetch** to load the player's skin.

Username loading is available for all required multi-skin inputs, including:

- Skin 1
- Skin 2
- Skin 3
- Skin 4

The application validates the username format before attempting to retrieve the skin.

---

## 👁️ Preview System

NVO MC Skin Merger provides multiple ways to inspect the result.

### 2D UV Preview

The merged texture is rendered on a canvas while preserving pixel-art sharpness.

### 3D Preview

The project uses **skinview3d** for Minecraft character visualization and animation.

The 3D viewer can be used to inspect the resulting skin on a Minecraft-style character.

### Animations

Available preview controls include:

- Walk
- Run
- Idle
- Rotate

---

## 🖼️ Result & History

After a merge, the generated skin can be reviewed in the result section.

The project also includes a **History / Gallery** system for signed-in users, allowing saved results to be revisited and reused.

Additional workflow features include:

- Save result to gallery
- Refresh saved history
- Reload saved results
- Use a previous result as Skin 1
- Before / After comparison
- Chained merge workflow

---

## 🔐 Authentication

The application uses **Google Authentication through Firebase Authentication** for account-related features.

Authentication is used for features such as account-based history/gallery functionality and protected result/download workflows.

The merge engine itself is designed to process skin textures in the browser.

---

## 🔒 Privacy

Skin processing is performed in the browser using client-side image/canvas processing.

According to the application's privacy information:

- Uploaded skin files are processed on the user's device/browser.
- Skin files are not intended to be uploaded to NVO servers for merging.
- Google sign-in is handled through Firebase Authentication.
- Account session information is handled through the authentication system.
- Firebase Firestore is used for an anonymous total-merge usage counter.

For the most accurate and current privacy behavior, refer to the Privacy Policy displayed inside the application.

---

## 🧰 Technology

The project is implemented as a browser-based HTML application using web technologies including:

- **HTML5**
- **CSS3**
- **JavaScript**
- **HTML Canvas API**
- **skinview3d** for 3D Minecraft skin preview
- **Firebase Authentication**
- **Firebase Firestore**
- **Google Sign-In**
- **Font Awesome** icons

The project is intentionally lightweight and can be served as a static website.

---

## 📁 Project Structure

The GitHub Pages repository is intentionally simple:

```text
nvomcskinmerger.github.io/
├── index.html
├── favicon.png
├── favicon-512.png
├── apple-touch-icon.png
├── og-preview.png
├── LICENSE
└── README.md
```

The main application is contained in `index.html`, making the project easy to deploy and modify.

---

## 🌐 Running Locally

Because the project is a static web application, it does not require a traditional build system to run the main page.

### Option 1 — Open locally

Clone the repository:

```bash
git clone https://github.com/nvomcskinmerger/nvomcskinmerger.github.io.git
cd nvomcskinmerger.github.io
```

Then open `index.html` in a modern browser.

### Option 2 — Local HTTP server

For the most reliable browser behavior, serve the directory through a local HTTP server.

For example, with Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

---

## 📦 GitHub Pages Deployment

The repository is structured for **GitHub Pages** deployment.

The live site is available at:

**https://nvomcskinmerger.github.io/**

A typical deployment flow is:

1. Push changes to the repository.
2. Keep the main website entry point as `index.html`.
3. Configure GitHub Pages to publish the repository's main branch/root directory.
4. Open the GitHub Pages URL.

---

## 🧪 Browser Compatibility

Use a modern browser with support for:

- HTML5 Canvas
- JavaScript ES6+
- WebGL for the 3D viewer
- Modern browser storage APIs
- HTTPS for production authentication flows

Recommended browsers include recent versions of:

- Google Chrome
- Microsoft Edge
- Mozilla Firefox
- Safari

---

## ⚠️ Known Considerations

### Matching skin formats

Some merger operations require all participating skins to have the same format. If incompatible dimensions are provided, the application will stop the operation rather than silently produce a corrupted texture.

### 3D preview / authentication

Some protected application features may require Google authentication. The 2D canvas merger and core texture-processing workflow are separate from the account system.

### External services

Username-based skin loading, Firebase authentication and 3D preview dependencies rely on external web services/CDN resources. Availability may therefore depend on the user's network, browser and those services.

---

## 🐛 Bug Reports

If you find a problem, please open an issue in the GitHub repository:

**https://github.com/nvomcskinmerger/nvomcskinmerger.github.io/issues**

When reporting a bug, include:

- Browser and version
- Operating system
- Selected merger mode
- Skin resolution(s)
- Whether the skin was uploaded or fetched by username
- The exact error message, if any
- Steps needed to reproduce the problem

Do **not** upload or publish private account information in an issue.

---

## 🤝 Contributing

Contributions, bug reports and feature suggestions are welcome.

Recommended workflow:

1. Fork the repository.
2. Create a feature branch.
3. Make your changes.
4. Test the affected merger modes.
5. Verify both desktop and mobile layouts where possible.
6. Submit a pull request with a clear description of the change.

For merger-engine changes, test at least:

- `64×32`
- `64×64`
- `128×64`
- `128×128`
- 2-skin workflow
- 3-skin workflow
- 4-skin workflow
- Custom Selective Merger

---

## 🗺️ Roadmap

Possible future improvements include:

- Additional multi-skin workflows
- More advanced UV-aware merge operations
- Improved mobile controls
- More preview and animation options
- Additional export options
- Performance improvements for high-resolution skins
- More advanced skin editing tools
- Expanded documentation and tutorials

The roadmap is subject to change as the project develops.

---

## 📜 License

This project is released under the **MIT License**.

See [`LICENSE`](LICENSE) for the complete license text.

Copyright © 2026 **nvomcskinmerger / NVO TEAM**.

---

## ⚖️ Trademark Notice

Minecraft is a trademark of **Mojang AB / Microsoft Corporation**.

NVO MC Skin Merger is an independent project and is **not affiliated with, endorsed by, or sponsored by Mojang or Microsoft**.

Google and the Google logo are trademarks of Google LLC.

---

## 🔗 Links

- 🌐 **Live Site:** https://nvomcskinmerger.github.io/
- 💻 **GitHub:** https://github.com/nvomcskinmerger/nvomcskinmerger.github.io
- 🐛 **Issues:** https://github.com/nvomcskinmerger/nvomcskinmerger.github.io/issues

---

<p align="center">
  <strong>NVO MC SKIN MERGER</strong><br>
  Built for Minecraft skin creators.
</p>
