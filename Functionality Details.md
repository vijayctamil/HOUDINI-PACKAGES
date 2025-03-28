# 🔍 Detailed Feature Documentation – HOUDINI-PACKAGES

This document provides deeper insight into each core feature bundled with the `HOUDINI-PACKAGES`. Use it as a technical reference or onboarding guide.

---

## 🎨 1. Automatic ACES Setup

**Purpose:**
- Automatically sets up the OCIO environment to use the ACEScg color pipeline in Houdini.

**How It Works:**
- On Houdini startup, environment variables like `OCIO` are pointed to the studio ACES config.

**Required:**
- ACES config folder (e.g., `config.ocio` from OCIO v1.2 or v2).

**Customization:**
Update your environment in `VJ_PIPELINE.json`:
```json
{ "OCIO": "<path-to-aces-config/config.ocio>" }
```

---

## ⚙️ 2. Custom Environmental Variables

**Purpose:**
- Centralized control over production paths, cache, textures, etc.

**Common Variables:**
- `CACHE_SO`, `TEX_SO`, `RENDER_SO`, `SHOTS_SO`, `RND_SO`

**How to Customize:**
Edit `VJ_PIPELINE.json` to point to your local pipeline structure.

---

## 🌅 3. Custom Splash Screen and Message

**Purpose:**
- Personalizes the Houdini launch experience with team branding and helpful text.

**Setup:**
- Modify splash image path and message inside `VJ_PIPELINE.json`
```json
{
  "HOUDINI_SPLASH_FILE": "$VJ_PIPELINE/splash/custom.jpg",
  "HOUDINI_SPLASH_MESSAGE": "Studio Version: ${HOUDINI_VERSION}\nArtist: John Doe"
}
```

---

## 📝 4. External Editor Setup

**Purpose:**
- Allows you to open .py, .json, .otl or shelf files directly in your editor from Houdini.

**Configured via:** `Editor.json`

**Example:**
```json
{
  "env": [
    { "EDITOR": "C:/Program Files/VS Code/Code.exe" }
  ]
}
```

---

## 🏗️ 5. Customizable Pipeline-based Startup File

**Purpose:**
- Provides a ready-to-use `.hip` scene with base setup for rendering, caching, naming conventions, camera rigs, and lights.

**Default Includes:**
- `/obj` layout
- Standard camera and render settings
- A null named after the scene for version control

**Customize:**
- Replace the default startup `.hip` with your own in the configured startup folder.

---

## 🧰 6. VJ Shelf – Dedicated Houdini Shelf Tools

**Purpose:**
- Custom shelf filled with tools tailored for production tasks like quick cache setups, environment linking, light rig drops, etc.

**How to Access:**
- Located under `VJ Shelf` in Houdini’s shelf tabs.

**Customization:**
- Add/remove tools via the shelf .shelf file in your pipeline folder.

---

## 🧩 7. VJ Digital Assets (OTLS) in TAB Menu

**Purpose:**
- A collection of HDAs designed for reusability and optimized workflows.

**Where to Find:**
- Press `Tab` in network editor ➝ Go to **VJ** tab.

**Examples:**
- `vj_cache_switcher.hda`: toggle between render/cache modes.
- `vj_auto_material.hda`: procedural material assignment.

**Install Path:**
Make sure the otl directory is included in:
```json
{ "HOUDINI_OTLSCAN_PATH": "$VJ_PIPELINE/production otls;&" }
```

---

Need help integrating or customizing these features? Start a discussion or create an issue on the main [GitHub Repo](https://github.com/vijayctamil/HOUDINI-PACKAGES).

Stay tuned — more tools and features are on the way 🚀

