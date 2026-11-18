# 🚀 RobloxScripter v4.1 (Extension Version)

**Turn any free web AI chat (DeepSeek, Gemini, ChatGPT, Claude) into an autonomous Roblox Studio agent—with Visual Diff Review, Atomic Auto-Rollback, and 32 built-in tools.**

No API keys. No subscriptions. Zero `npm` or Python dependencies.

---

### 🛡️ Why RobloxScripter? (Built for Real Projects & Challenges)

Giving an AI direct control over Roblox Studio usually ends in broken maps or deleted scripts. **RobloxScripter v4.1** solves this with production-grade safety and token efficiency:

* **🔍 Interactive Visual Diff Review (`Risky` / `All` / `Off`):** Inspect exact red/green line-by-line code changes inside Studio and click **Apply** or **Reject** before anything is modified—or switch to `Off` mode for pure speedrun chaos.
* **↩️ Atomic Batch & Auto-Rollback:** Powered by `ChangeHistoryService`. If 1 out of 10 actions in a batch fails, the entire batch automatically rolls back so your game never breaks halfway.
* **⚡ 32 Specialized Tools (5x Less Token Usage):** Includes `project_snapshot`, `script_outline`, line-range reading, partial find/replace (`edit_script`), themed UI builder (`create_gui`), raycast object scatterer, and an automatic project/backdoor auditor (`verify`).
* **🤖 Autonomous Playtest & Self-Debugging:** Launch an automated `playtest` via `StudioTestService`, capture Server/Client Output errors in real time, and let the AI patch its own bugs in a loop.
* **🔒 Local Security & Backdoor Scanner:** Uses cryptographic session tokens (`X-RS-Token`), strict `Host`/`Origin` anti-DNS-rebinding checks, automatic script stripping on Toolbox assets, and a built-in malicious pattern scanner.
* **📦 1-Click Automated Installer (`install.bat`):** Zero `npm` or Python dependencies—just double-click `install.bat` to install the plugin, launch the bridge server, and open the pairing dashboard automatically.

---

### ⚡ 2-Step Quick Setup (Windows)

*(Prerequisite: Make sure [Node.js 16+](https://nodejs.org) is installed on your PC.)*

#### 1. Run the 1-Click Installer (`install.bat`)
* Extract the downloaded folder and double-click **`install.bat`**.
* It will **automatically**:
  1. Copy the plugin into your Roblox Studio `Plugins` folder.
  2. Start the local bridge server (`127.0.0.1:3030`).
  3. Open the **RobloxScripter Dashboard** in your browser.
* Click **Connect** on the dashboard, then open **Plugins > RobloxScripter** in Studio and click **Allow** when prompted for HTTP access.

*(Note for macOS/Linux users: Manually copy `plugin/RobloxScripterBridge.server.lua` to your Roblox Plugins folder and run `node server/server.js --open`.)*

#### 2. Load the Browser Extension
* Open `chrome://extensions` (Chrome) or `edge://extensions` (Edge).
* Turn on **Developer mode** (top right).
* Click **Load unpacked** and select the `extension/` folder.
* Open DeepSeek, Gemini, ChatGPT, or Claude in your browser and start prompting!

---

### 🧰 Full List of 32 Built-in Tools

| Category | Tools |
| :--- | :--- |
| **Read (10)** | `project_snapshot`, `list_children`, `find_instances`, `get_properties`, `get_selection`, `get_script_source`, `script_outline`, `search_scripts`, `search_toolbox`, `get_output` |
| **Modify (11)** | `create_instance`, `set_properties`, `bulk_set_properties`, `move_instance`, `delete_instance`, `clone_instance`, `set_attributes`, `tag`, `group_instances`, `arrange_instances`, `create_tree` |
| **Script (4)** | `create_script`, `edit_script`, `replace_in_scripts`, `run_luau` |
| **UI (1)** | `create_gui` *(supports `dark`, `light`, `neon` themes & design tokens)* |
| **World (4)** | `terrain` *(including Perlin noise `hills`)*, `set_lighting`, `insert_asset`, `scatter_instances` *(raycast ground-snapping)* |
| **Test (2)** | `verify` *(syntax, loops, unanchored parts & dead remote audit)*, `playtest` |

---

### 📄 License

This project is licensed under the **MIT License** — free to use, modify, and showcase in videos or personal/commercial games.
