# 🎨 NVO MC SKIN MERGER

::: {align="center"}
### Next-Generation Minecraft Skin Merger

**Combine • Remix • Preview • Export Minecraft Skins --- directly in
your browser.**

[🌐 Live Demo](https://nvomcskinmerger.github.io/) · [💻
GitHub](https://github.com/nvomcskinmerger/nvomcskinmerger.github.io) ·
[🐛 Report a
Bug](https://github.com/nvomcskinmerger/nvomcskinmerger.github.io/issues)

![Version](https://img.shields.io/badge/version-V1.0.0-8A2BE2?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-success?style=for-the-badge)
![Platform](https://img.shields.io/badge/platform-Web-blue?style=for-the-badge)
![Minecraft](https://img.shields.io/badge/Minecraft-Skins-62B47A?style=for-the-badge)
:::

------------------------------------------------------------------------

## 🖼️ Preview

```{=html}
<p align="center">
```
`<img src="./og-preview.png" alt="NVO MC Skin Merger preview" width="900">`{=html}
```{=html}
</p>
```
> **NVO MC Skin Merger** is a browser-based Minecraft skin creation and
> merging studio focused on fast workflows, detailed skin manipulation,
> multi-skin composition, previewing and exporting.

------------------------------------------------------------------------

## 📌 Table of Contents

-   [✨ What is NVO MC Skin Merger?](#-what-is-nvo-mc-skin-merger)
-   [🚀 Highlights](#-highlights)
-   [🧩 Skin Merger System](#-skin-merger-system)
-   [🎯 Supported Merge Modes](#-supported-merge-modes)
-   [🎨 Custom Selective Merger](#-custom-selective-merger)
-   [👤 Minecraft Username → Skin](#-minecraft-username--skin)
-   [📐 Supported Skin Formats](#-supported-skin-formats)
-   [🧊 3D Preview & Animation](#-3d-preview--animation)
-   [🖼️ Preview, Compare & Result
    Workflow](#-preview-compare--result-workflow)
-   [🔐 Authentication & History](#-authentication--history)
-   [🛡️ Privacy](#-privacy)
-   [⚡ How to Use](#-how-to-use)
-   [💻 Technology](#-technology)
-   [📂 Repository Structure](#-repository-structure)
-   [🌐 GitHub Pages Deployment](#-github-pages-deployment)
-   [🧪 Validation & Compatibility](#-validation--compatibility)
-   [🐛 Troubleshooting](#-troubleshooting)
-   [🤝 Contributing](#-contributing)
-   [🗺️ Roadmap](#️-roadmap)
-   [📄 License](#-license)
-   [⚠️ Trademark Notice](#️-trademark-notice)

------------------------------------------------------------------------

## ✨ What is NVO MC Skin Merger?

**NVO MC Skin Merger** is an advanced, browser-first Minecraft skin
merger designed for players, skin artists, server owners, content
creators and anyone who wants to experiment with Minecraft character
textures without opening a traditional image editor.

The project brings multiple workflows together in one interface:

-   Two-skin merging
-   Three-skin composition
-   Four-skin composition
-   Body-part swapping
-   Overlay/base manipulation
-   Random/chimera-style combinations
-   Custom selective merging
-   Minecraft username-based skin loading
-   2D texture previews
-   3D character preview
-   Animation controls
-   Result comparison
-   History / gallery workflows
-   PNG output

> **Current release:** `V1.0.0`

------------------------------------------------------------------------

## 🚀 Highlights

  Capability                      Status
  ------------------------------ --------
  2 Skin Merger                     ✅
  3 Skin Merger                     ✅
  4 Skin Merger                     ✅
  50/50 Merger                      ✅
  Top / Bottom Merger               ✅
  Body-part based merging           ✅
  Custom Selective Merger           ✅
  Minecraft username loading        ✅
  Multiple skin resolutions         ✅
  2D preview                        ✅
  3D preview                        ✅
  Character animation               ✅
  Before / After comparison         ✅
  History / Gallery                 ✅
  PNG export                        ✅
  Google authentication             ✅
  GitHub Pages compatible           ✅
  Single-page application           ✅
  No desktop software required      ✅

------------------------------------------------------------------------

# 🧩 Skin Merger System

The project extends the original merger workflow without replacing its
underlying mechanics.

## 2️⃣ Two Skin Merger

The classic workflow uses:

-   **Skin 1**
-   **Skin 2**
-   A selected merger mode
-   Generated result

The application works with Minecraft UV layouts instead of treating
skins as ordinary flat images.

------------------------------------------------------------------------

## 3️⃣ Three Skin Merger

The three-skin workflow is intentionally chained:

``` text
Skin 1 ─┐
        ├── 50/50 Vertical ──┐
Skin 2 ─┘                    │
                             ├── Top / Bottom ──> RESULT
Skin 3 ──────────────────────┘
```

### Processing order

1.  Skin 1 + Skin 2
2.  Existing 50/50 vertical merger
3.  Intermediate result + Skin 3
4.  Existing top/bottom merger
5.  Final result

This is a staged composition workflow --- **not a separate split/merge
engine**.

------------------------------------------------------------------------

## 4️⃣ Four Skin Merger

The four-skin workflow uses two parallel 50/50 combinations followed by
the existing top/bottom operation:

``` text
Skin 1 ─┐
        ├── 50/50 Vertical ──┐
Skin 2 ─┘                    │
                             ├── Top / Bottom ──> FINAL
Skin 3 ─┐                    │
        ├── 50/50 Vertical ──┘
Skin 4 ─┘
```

### Processing order

1.  Skin 1 + Skin 2 → 50/50 result
2.  Skin 3 + Skin 4 → 50/50 result
3.  First intermediate result + second intermediate result
4.  Existing top/bottom merger
5.  Final result

------------------------------------------------------------------------

# 🎯 Supported Merge Modes

Current mode families include:

### Core

-   `50/50 / Half`
-   `Top / Bottom`
-   `Head Swap`
-   `Body Swap`
-   `Arm Swap`
-   `Leg Swap`
-   `Arms + Legs Swap`
-   `Head + Legs Swap`
-   `Head + Torso Swap`

### Texture / Overlay

-   `Base Only`
-   `Outer Overlay`
-   `Reverse Overlay`
-   `Front / Back`
-   `Blend`
-   `Checker Blend`
-   `Gradient Blend`

### Advanced

-   `Alternating Parts`
-   `Cross Limb Swap`
-   `Chimera / Random Mix`
-   `Custom Selective Merger`

### Multi-Skin

-   `3 Skin Merger`
-   `4 Skin Merger`

The available mode list may evolve with future merger-engine releases.

------------------------------------------------------------------------

# 🎨 Custom Selective Merger

The **Custom Selective Merger** provides finer control than a single
predefined merge mode.

Instead of choosing one global operation, body regions can be controlled
individually.

``` text
Choose base body
       ↓
Select Skin 1 / Skin 2
       ↓
Control overlay layers
       ↓
Preview the composition
       ↓
Generate final texture
```

Quick actions include:

-   **All Skin 1**
-   **All Skin 2**
-   **Overlays Off**

Individual body-part controls can be cycled through supported source
states.

------------------------------------------------------------------------

# 👤 Minecraft Username → Skin

A local PNG is not always necessary.

The application supports entering a Minecraft username and retrieving
the associated skin.

``` text
Minecraft username
        ↓
      GETIR
        ↓
Fetch skin
        ↓
Load into Skin slot
        ↓
Preview
        ↓
Merge
```

The same interaction model is available for the additional inputs used
by the 3- and 4-skin workflows.

> Username fetching depends on the external profile/skin services used
> by the application and normal browser/network availability.

------------------------------------------------------------------------

# 📐 Supported Skin Formats

The application validates Minecraft skin dimensions before processing.

  Resolution     Supported
  ------------- -----------
  `64 × 32`         ✅
  `64 × 64`         ✅
  `128 × 64`        ✅
  `128 × 128`       ✅

The merger detects the active skin format and prevents incompatible
combinations where required.

Minecraft skins are structured UV maps, so the engine needs to preserve:

-   Texture coordinates
-   Body regions
-   Arm/leg layouts
-   Base layers
-   Overlay layers
-   Resolution scaling

------------------------------------------------------------------------

# 🧊 3D Preview & Animation

NVO MC Skin Merger goes beyond a flat PNG preview.

The application includes a 3D skin viewer workflow with character
animation controls such as:

-   🚶 Walk
-   🏃 Run
-   🧍 Idle
-   🔄 Rotate

The purpose is to inspect the final skin as an actual Minecraft
character rather than only checking the UV texture.

------------------------------------------------------------------------

# 🖼️ Preview, Compare & Result Workflow

After merging, the application can provide:

-   Generated PNG result
-   UV output preview
-   Result information
-   Before / After comparison
-   3D character inspection
-   Reusing the generated result as Skin 1
-   Downloading the final texture

### Chained workflow

``` text
Skin 1 + Skin 2
      ↓
   RESULT
      ↓
Use Result as Skin 1
      ↓
Upload new Skin 2
      ↓
   NEXT MERGE
```

This makes repeated experimentation much faster.

------------------------------------------------------------------------

# 🔐 Authentication & History

The application integrates Google authentication through Firebase.

Account-related functionality can include:

-   History / Gallery
-   Saved results
-   Re-accessing generated results
-   Download-related protected functionality

The basic merger workflow is designed to remain useful without requiring
authentication for every operation.

### History / Gallery

The gallery workflow is designed around:

-   Saving generated results
-   Loading previous results
-   Refreshing the gallery
-   Reusing saved textures
-   Deleting saved entries

------------------------------------------------------------------------

# 🛡️ Privacy

The project includes an in-app privacy/legal information layer.

Skin processing is designed around browser-side workflows wherever
possible.

The application's privacy text states that uploaded skin files are
processed on the user's device rather than being treated as files that
must be uploaded to an NVO server.

Google authentication is handled through Firebase Authentication.

> If you fork or modify the project, review the privacy/legal text again
> whenever you change storage, analytics, authentication or external
> services.

------------------------------------------------------------------------

# ⚡ How to Use

### 1. Open the application

**https://nvomcskinmerger.github.io/**

### 2. Select a mode

Choose:

-   Standard 2-skin mode
-   3 Skin Merger
-   4 Skin Merger
-   Advanced merger
-   Custom Selective Merger

### 3. Add skins

You can:

-   Upload PNG files
-   Enter Minecraft usernames
-   Preview loaded skins
-   Check detected model/format information

### 4. Merge

Select the desired operation and start the merger.

For 3- and 4-skin workflows, the application follows the predefined
staged process automatically.

### 5. Inspect

Review the result using:

-   2D texture view
-   UV output
-   Before / After comparison
-   3D viewer

### 6. Export

Download the generated PNG when the required account/authentication
conditions are satisfied.

------------------------------------------------------------------------

# 💻 Technology

NVO MC Skin Merger is intentionally lightweight and browser-oriented.

### Front end

-   HTML5
-   CSS3
-   JavaScript
-   Canvas API

### Rendering

-   HTML Canvas
-   WebGL-based 3D skin viewer workflow
-   Minecraft UV texture mapping

### Services

-   Firebase Authentication
-   Firebase-related history/usage functionality
-   External Minecraft skin/profile retrieval services

### Hosting

-   GitHub Pages

### Architecture

The main application is designed as a single-page web application with
the primary application contained in:

``` text
index.html
```

This makes deployment straightforward and avoids requiring a traditional
Node.js/PHP server for the static front end.

------------------------------------------------------------------------

# 📂 Repository Structure

``` text
nvomcskinmerger.github.io/
│
├── index.html
├── LICENSE
├── og-preview.png
├── favicon.png
├── favicon-512.png
└── apple-touch-icon.png
```

  File                     Purpose
  ------------------------ ---------------------------
  `index.html`             Main web application
  `og-preview.png`         Social/Open Graph preview
  `favicon.png`            Browser favicon
  `favicon-512.png`        Large favicon/app icon
  `apple-touch-icon.png`   Apple touch icon
  `LICENSE`                MIT License

------------------------------------------------------------------------

# 🌐 GitHub Pages Deployment

The project is designed for static hosting.

1.  Fork or clone the repository.
2.  Open **Settings → Pages**.
3.  Select the desired branch.
4.  Select the repository root as the publishing source.
5.  Save.
6.  Wait for GitHub Pages to publish the site.

Because the front end is browser-based, no traditional server deployment
is required for the main application.

------------------------------------------------------------------------

# 🧪 Validation & Compatibility

The merger validates important input conditions before processing.

### Input validation

The application can reject:

-   Non-PNG files
-   Invalid PNG data
-   Unsupported dimensions
-   Oversized files
-   Incompatible skin formats
-   Unreadable image data

### Browser requirements

The project is intended for modern browsers supporting:

-   HTML5 Canvas
-   Modern JavaScript
-   WebGL for 3D preview
-   Modern File APIs
-   Browser storage/session capabilities

Recommended browsers:

-   Chrome
-   Edge
-   Firefox
-   Safari

------------------------------------------------------------------------

# 🐛 Troubleshooting

## Merge button does not work

Check:

1.  All required skin slots are loaded.
2.  3 Skin mode has Skin 1--3 ready.
3.  4 Skin mode has Skin 1--4 ready.
4.  Skin formats are compatible.
5.  PNG files are valid Minecraft skin textures.
6.  The browser console does not report a JavaScript error.

### 3 Skin

``` text
Skin 1 ✅
Skin 2 ✅
Skin 3 ✅
     ↓
   MERGE
```

### 4 Skin

``` text
Skin 1 ✅
Skin 2 ✅
Skin 3 ✅
Skin 4 ✅
     ↓
   MERGE
```

## Username skin does not load

Possible causes:

-   Invalid Minecraft username
-   Player does not exist
-   External skin service unavailable
-   Browser/network restrictions
-   Temporary third-party outage

Try uploading the PNG manually.

## 3D preview does not appear

Check:

-   WebGL availability
-   Browser hardware acceleration
-   Browser console errors
-   Authentication requirements for the current feature
-   Whether a generated result exists

## Skin looks incorrect

Make sure the input is a genuine Minecraft skin layout and that the
source skins use compatible resolutions/layouts.

------------------------------------------------------------------------

# 🧠 Design Philosophy

NVO MC Skin Merger is built around five principles.

### 1. Preserve existing merger mechanics

New workflows should extend the existing merger engine rather than
unnecessarily replacing it.

### 2. Texture-aware processing

Minecraft skins are structured UV maps. Operations should respect that
structure.

### 3. Fast browser workflows

The intended flow is:

``` text
Skin → Merge → Preview → Export
```

without requiring desktop image-editing software.

### 4. Progressive complexity

Beginners can use simple merger modes while advanced users can move
into:

-   Custom selection
-   Overlay control
-   Multi-skin workflows
-   3D inspection
-   Chained results

### 5. Creator-first UX

The interface is designed for rapid experimentation instead of forcing
creators through a complicated image-editing workflow.

------------------------------------------------------------------------

# 🤝 Contributing

Contributions are welcome.

## Suggested workflow

``` bash
git clone https://github.com/nvomcskinmerger/nvomcskinmerger.github.io.git
cd nvomcskinmerger.github.io
```

Then:

1.  Create a branch.
2.  Make your changes.
3.  Test the affected merger modes.
4.  Test multiple resolutions.
5.  Test 3/4-skin workflows if relevant.
6.  Test username loading if relevant.
7.  Test 3D preview if relevant.
8.  Open a pull request.

### Bug reports should include

-   Browser and version
-   Operating system
-   Skin resolution
-   Merger mode
-   Number of skins
-   Steps to reproduce
-   Console error, if any
-   Screenshot/video when useful

------------------------------------------------------------------------

# 🗺️ Roadmap

Potential future improvements:

-   [ ] More advanced texture controls
-   [ ] More multi-skin composition modes
-   [ ] Improved 3D editing
-   [ ] More precise layer controls
-   [ ] Additional export options
-   [ ] Better mobile editing workflow
-   [ ] More preview customization
-   [ ] Expanded gallery capabilities
-   [ ] More advanced skin analysis
-   [ ] Performance improvements for large textures
-   [ ] Additional creator-focused tools

The roadmap may change as the project evolves.

------------------------------------------------------------------------

# 📊 Project Status

**Current version:** `V1.0.0`

Repository:

https://github.com/nvomcskinmerger/nvomcskinmerger.github.io

Live application:

https://nvomcskinmerger.github.io/

------------------------------------------------------------------------

# 📄 License

This project is released under the **MIT License**.

See [`LICENSE`](./LICENSE) for the complete license text.

Copyright © 2026 **NVO MC Skin Merger / nvomcskinmerger**

------------------------------------------------------------------------

# ⚠️ Trademark Notice

Minecraft is a trademark of **Mojang AB / Microsoft Corporation**.

NVO MC Skin Merger is an independent project and is **not affiliated
with, endorsed by, sponsored by, or officially connected to Mojang or
Microsoft**.

Google and the Google logo are trademarks of Google LLC.

------------------------------------------------------------------------

# 💙 Credits

Built for the Minecraft skin creation community by **NVO MC Skin
Merger**.

If this project helps you create skins, consider giving the repository a
⭐ on GitHub.

::: {align="center"}
[![GitHub
Stars](https://img.shields.io/github/stars/nvomcskinmerger/nvomcskinmerger.github.io?style=for-the-badge&logo=github)](https://github.com/nvomcskinmerger/nvomcskinmerger.github.io)
[![GitHub
Issues](https://img.shields.io/github/issues/nvomcskinmerger/nvomcskinmerger.github.io?style=for-the-badge&logo=github)](https://github.com/nvomcskinmerger/nvomcskinmerger.github.io/issues)

### ⭐ Star the project if you find it useful!

**NVO MC SKIN MERGER --- V1.0.0**

*Merge your skins. Build your character. Create something unique.*
:::
