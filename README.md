# Gemini Playground Template

This is a pre-configured, lightweight VS Code template designed to spin up isolated development playgrounds. It integrates conversational AI agents, custom Model Context Protocol (MCP) tools, and automated system mounting out-of-the-box.

---

## Features

1. **Automated Terminal Initialization:** 
   Opening any integrated terminal in this folder automatically activates your python virtual environment, sources environment variables, and launches the ADK web server.
2. **Interactive Google Drive Auto-Mounting:**
   On your first terminal start, you will be prompted: *"Would you like to mount your Google Drive? (y/n)"*.
   * Selecting **Yes** launches `rclone` authentication.
   * Selecting **No** creates a persistent opt-out sentinel file (`.gdrive_opt_out`), and you will **never** be prompted again.
   * Once configured, your Drive auto-mounts securely in `~/GoogleDrive` on every single boot transparently.
3. **Preloaded "Data Agent Kit" Skills:**
   The template includes pre-bundled, ready-to-run AI skills inside `.gemini/skills/` (including the GKE and ADK Deployment pipelines).

---

## Getting Started

1. **Clone or copy this folder** to your target playground directory.
2. **Set up your environment:**
   Copy `.env.sample` to `.env` and fill in your details:
   ```bash
   cp .env.sample .env
   ```
3. **Open the folder in VS Code:**
   Open the folder as a workspace. The moment you open an integrated terminal, it will automatically initiate the environment setup and ask you if you want to mount your Google Drive.
