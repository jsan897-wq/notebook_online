# 📓 GitNotebook & Voice Vault

A modern, serverless web application that turns your **GitHub repository** into a personal **cloud notebook, note-taking workspace, and voice recording vault**.

---

## 🌟 Key Features

### 1. 📝 GitHub-Backed Note Taking & Markdown Editor
- **Direct GitHub Repository Commits**: Every time you click **"Save to GitHub"** (or press `Ctrl+S` / `Cmd+S`), your note is committed directly to your GitHub repository using GitHub's official REST API.
- **Rich Markdown Support**: Live side-by-side split preview with headings, checklists, code blocks, tables, blockquotes, and timestamps.
- **Auto-Saved Local Drafts**: Never lose what you type. Your current draft is automatically saved locally in your browser.
- **Notebook Organization**: Organize notes into folders (e.g., `notebooks/`, `work/`, `journal/`).
- **Templates**: Instant templates for Meeting Notes, Daily Journal / Diary, Voice Memo Summaries, and Research Logs.

### 2. 🎙️ Voice Recording Studio & Audio Vault
- **In-Browser Audio Recording**: Record voice memos, meetings, or thoughts directly from your microphone using the HTML5 MediaRecorder API.
- **Live Waveform Visualizer**: Real-time frequency visualizer canvas while recording.
- **Audio Playback**: Listen to your recording immediately in the built-in player.
- **Save Audio to GitHub**: Uploads the recorded audio file (`.webm` or `.mp4`) directly to your repository (e.g., `notebooks/audio/`).
- **Companion Markdown Notes**: Automatically create a linked Markdown note with timestamp and summary alongside the audio recording.

### 3. 📂 Repository Explorer & Notebook Viewer
- **Browse Your Repository**: Lists all notes, voice memos, and files stored in your GitHub repository.
- **Listen to Past Voice Memos**: Audio files stored in your repository can be fetched and played back directly inside the web app (even in private repositories!).
- **One-Click File Upload**: Upload attachments, PDFs, images, or documents straight into your GitHub repository notebook folder.

### 4. 🔒 Privacy & Security First
- **No intermediary backend**: The app runs 100% in your browser.
- **Direct API Calls**: All requests go directly between your browser and `api.github.com`.
- **Local Storage**: Your Personal Access Token (PAT) and settings stay stored securely in your browser's `localStorage`.

---

## 🚀 Quick Start Guide

### Step 1: Open the Application
Simply double-click [`index.html`](index.html) or run `start_website.bat` to launch it in any modern web browser (Chrome, Edge, Firefox, Brave, Safari).

### Step 2: Get a GitHub Personal Access Token (PAT)
To allow the website to read and save files to your GitHub repository:
1. Log in to [GitHub](https://github.com/).
2. Go to **Settings** &rarr; **Developer Settings** &rarr; **Personal access tokens** &rarr; **Tokens (classic)** (or visit [https://github.com/settings/tokens](https://github.com/settings/tokens)).
3. Click **Generate new token (classic)**.
4. Give it a note (e.g., `GitNotebook App`) and check the **`repo`** permission scope (full control of private repositories).
5. Click **Generate token** and copy the token string (`ghp_...`).

### Step 3: Configure the Web App
1. Click the **GitHub: Not Connected** (or Settings icon ⚙️) button in the top right.
2. Enter:
   - **Personal Access Token**: Your `ghp_...` token.
   - **GitHub Username / Org**: Your GitHub username (e.g., `octocat`).
   - **Repository Name**: The repository you want to use as your vault (e.g., `my-notes` or create a new private repo on GitHub).
   - **Branch**: Default is `main`.
   - **Base Vault Directory**: Default is `notebooks`.
3. Click **Test Connection** to verify that your repository is reachable.
4. Click **Save Settings**.

---

## 🎯 How to Use

### Taking and Saving Notes
1. Switch to the **Note Editor** tab.
2. Enter your note title and folder name (e.g. `notebooks`).
3. Write your thoughts using Markdown or plain text. Use the toolbar buttons for easy formatting.
4. Press **"Save to GitHub"** (or hit `Ctrl+S`). The file is committed directly to your GitHub repository!

### Recording and Saving Voice
1. Switch to the **Voice Studio** tab (or click **Record Voice** in the sidebar).
2. Click the large red microphone button to start recording. Speak into your microphone.
3. Click pause or stop when finished.
4. Preview the audio with the player.
5. Enter a title and click **"Save Voice to GitHub"**.
6. If checked, a companion markdown note will also be created with a link to the voice memo.

### Exploring and Playing Past Notes & Voice
1. Use the left sidebar or the **Notebook Viewer** tab to view all files saved in your repository.
2. Click any note to open and edit it.
3. Click any audio file to load and listen to it right in the app.
