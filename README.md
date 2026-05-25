# My-singing-Monsters-Custom-Anim-Creator
it's not exactly an app, but in this html, you can make animations. For example, I've attached a rig for Cube Cybop, which you can try out. It also supports RU and EN. For more information, please refer to the README
README Create By Gemini
# MSM Anim Creator Pro 🦴

A lightweight, high-fidelity skeletal animation tool tailored for modders and creators of **My Singing Monsters** character rigs. The entire engine and editor are contained within a single self-contained HTML file—no complicated installations, packages, or node modules required!

> **Quick Start:** You can test the engine right away using the pre-configured rig for **Cube Cybop** included in the workspace repository.

---

## 🚀 Features

* **Zero Setup / Single HTML:** Runs entirely inside your browser. Perfect for rapid development and mobile linux environments (like Termux).
* **Skeletal & Sprite Rigging:** Easily create node hierarchies, bind parent-child layers, and animate parts of monsters (eyes, wings, mouths) with smooth interpolations.
* **Sprite Sheets & Frame Links:** Full support for complex state changes on a single node (e.g., swapping frames to create organic eye blinks or mouth shapes).
* **Advanced Layer Management (Z-Index):** Rearrange drawing depths natively within the workspace hierarchy to prevent blinking states or pupils from slipping behind head textures.
* **Precision Keyboard/Mouse Controls:** * **Arrow Keys:** Pixel-perfect adjustments for your nodes.
    * **Shift + Arrows:** Precise rotation tracking.
    * **Spacebar + Drag:** Seamless workspace pan and zoom to catch micro-details.
* **Custom Frame Rates:** Dynamically configure your workspace canvas FPS (perfect for standard 12 FPS MSM animations, or smoother 24/30/60 FPS workflows).
* **Clean Blueprint System:** Quickly hide skeleton lines with a single checkbox to inspect raw visual art outputs without green/blue vector lines in the way.
* **Dual Language Support:** Easily switch between English (**EN**) and Russian (**RU**) natively via the top navigation bar.

---

## 🛠️ How to Use

1.  **Download or Clone** this repository.
2.  Open the `index.html` (or your main application file) directly in any modern desktop or mobile browser.
3.  **To Build a Rig:** Click **"+ Add Node"** (`+ Добавить узел`), choose whether it uses a single sprite or a frame связка (sprite sheet), upload your texture assets, and structure your hierarchy using the Layer control buttons (`▲` / `▼`).
4.  **Animate:** Pick your target frame on the timeline track, adjust node positions via dragging or keyboard arrows, and press **"● Key"** (`● Ключ`) to save keyframes.
5.  **Export & Share:** Use the **Export** action to save your finished animations as local `.msmanim` structural data packages. Use **Import** to load existing templates or pick up where you left off.

---

## 📦 File Ecosystem

The application structures and exports data using a custom JSON structure saved under the `.msmanim` file format:

```json
{
  "bones": [
    {
      "id": "bone_123456789",
      "name": "Head",
      "type": "single",
      "parentId": "none",
      "images": ["data:image/png;base64,..."],
      "x": 400,
      "y": 300,
      "angle": 0,
      "length": 60
    }
  ],
  "keyframes": {
    "0": {
      "bone_123456789": { "x": 400, "y": 300, "angle": 0, "phaseIndex": 0 }
    }
  }
}
