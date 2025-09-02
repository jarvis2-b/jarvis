# Jarvis-Lite (Full)

This project is a ready-to-push Electron app with:
- Chat UI + webview
- Wake-word voice input ("Hey Jarvis") using the Web Speech API
- Text-to-speech replies
- IPC bridge to call OpenAI API (you provide API key at runtime)
- electron-builder config and GitHub Actions workflow to produce installers

## Quick local run
1. Install Node.js (v18+) and npm.
2. Extract the ZIP.
3. In the project folder run:
   ```bash
   npm install
   npm start
   ```
4. Paste your OpenAI API key into the app (top-left) and use the 🎤 button to enable wake-word listening.

## Build installers via GitHub Actions
1. Create a new GitHub repo and push these files.
2. On GitHub, Actions will run the included workflow and produce build artifacts in the Actions run page.
3. Download the produced installer for your platform.

## Security notes
- Do not check in your OpenAI API key. Store it locally or in a secure vault.
- The app sends messages to OpenAI; usage will consume your OpenAI credits.

## Customization
- To change the wake word, edit renderer.js and replace 'hey jarvis' checks.
- To use a local model instead of OpenAI, replace the IPC handler in main.js.

