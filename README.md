# 🎨 HOUDINI-PACKAGES

A comprehensive suite of customized tools, automations, and OTLS designed to enhance and streamline workflows within [Houdini](https://www.sidefx.com/products/houdini/).

---

## 📦 Package Overview

This repository encompasses a variety of tools and configurations tailored for Houdini users, aiming to boost productivity and provide additional functionalities.

---

## 🛠️ Installation

To integrate these packages into your Houdini environment:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/vijayctamil/HOUDINI-PACKAGES.git
   ```

2. **Set Up the Packages:**
   - Place the cloned directory in a location accessible by Houdini.
   - Ensure that Houdini's environment variables are configured to recognize the new tools and configurations. This can be done by adding the package path to your Houdini environment settings.

---

## 🚀 Usage

Once installed, the customized tools and automations will be available within Houdini.  
Access them through the designated menus or shelves as configured.  
Refer to the individual tool documentation for detailed instructions and best practices.

---

## 📂 Repository Structure

The repository is organized as follows:

```
HOUDINI-PACKAGES/
├── VJ_PIPELINE/             # Contains pipeline-related tools and scripts
├── Editor.json              # Configuration file for editor settings
└── VJ_PIPELINE.json         # Configuration file for the VJ_PIPELINE tools
```

---

## ✏️ Customizing `VJ_PIPELINE.json`

You can modify `VJ_PIPELINE.json` to reflect your local paths and preferences. Here's what each key does:

```json
{
  "hpath": "$VJ_PIPELINE",
  "env": [
    { "VJ_PIPELINE": "<path-to-your-VJ_PIPELINE-folder>" },
    { "HOUDINI_PATH": "$VJ_PIPELINE" },
    { "RND": "<path-to-your-RND-folder>" },
    { "HOUDINI_SPLASH_MESSAGE": "Version: ${HOUDINI_VERSION} \n YOUR NAME HERE" },
    { "HOUDINI_SPLASH_FILE": "$VJ_PIPELINE/splash/YOUR_SPLASH_IMAGE.jpg" },
    { "TEX_SO": "<path-to-sourceimages-folder>" },
    { "CACHE_SO": "<path-to-cache-folder>" },
    { "RENDER_SO": "<path-to-render-folder>" },
    { "SHOTS_SO": "<path-to-shots-folder>" },
    { "RND_SO": "<path-to-local-houdini-rnd-folder>" }
  ]
}
```

> Replace all placeholders like `<path-to-your-folder>` with absolute paths relevant to your setup.

---

## 📝 Customizing `Editor.json`

This file lets you define which text/code editor to launch from within Houdini.

Example:

```json
{
  "env" : [
    {
      "EDITOR" : "C:/Users/ADMIN/AppData/Local/Programs/Microsoft VS Code/Code.exe"
    }
  ]
}
```

You can change the path of `EDITOR` to match your preferred editor's executable path. For example:

- **VS Code (default):**
  ```json
  "EDITOR": "C:/Path/To/VSCode/Code.exe"
  ```
- **Sublime Text:**
  ```json
  "EDITOR": "C:/Program Files/Sublime Text/sublime_text.exe"
  ```

Make sure the path is correct and accessible on your machine.

---

## 🤝 Contributing

Contributions are welcome!  
If you have tools, scripts, or configurations that could benefit the Houdini community, feel free to fork this repository and submit a pull request.

---

## 📄 License

This project is licensed under the MIT License.  
See the [LICENSE](LICENSE) file for details.

---

*Enhance your Houdini experience with these customized packages and tools.*

