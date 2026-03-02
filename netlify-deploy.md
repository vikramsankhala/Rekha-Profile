# Deploy Rekha Sankhala Website to Netlify

## Prerequisites

1. **Place Rekha.mp4** in this folder (`c:\Users\I762844\Documents\Rekha\`) alongside `index.html` before deploying.
2. A [Netlify account](https://www.netlify.com/) (free tier works).

---

## Option A: Drag & Drop (Easiest)

1. **Create deploy folder**:
   - Copy `index.html`, `netlify.toml`, and `Rekha.mp4` into a single folder.
   - Ensure `Rekha.mp4` is in the same folder as `index.html`.

2. **Deploy**:
   - Go to [app.netlify.com](https://app.netlify.com/)
   - Click **"Add new site"** → **"Deploy manually"**
   - Drag the folder containing `index.html`, `netlify.toml`, and `Rekha.mp4` into the drop zone
   - Wait for the deploy to finish

3. **Result**:
   - Your site will be live at a URL like `https://random-name-123.netlify.app`
   - You can change the site name in **Site settings** → **Domain management**

---

## Option B: Netlify CLI

1. **Install Netlify CLI**:
   ```powershell
   npm install -g netlify-cli
   ```

2. **Log in**:
   ```powershell
   netlify login
   ```

3. **Deploy** (from the Rekha folder):
   ```powershell
   cd "c:\Users\I762844\Documents\Rekha"
   netlify deploy --prod
   ```

   When prompted:
   - **Publish directory:** `.` (current directory)

---

## Option C: Git (Continuous Deployment)

1. Push this project to a Git repository (GitHub, GitLab, Bitbucket).

2. In Netlify:
   - **Add new site** → **Import an existing project**
   - Connect your Git provider and select the repo
   - **Build settings:**
     - **Base directory:** (leave empty)
     - **Build command:** (leave empty)
     - **Publish directory:** `.`

3. Add `Rekha.mp4` to the repo and push. Netlify will redeploy automatically.

---

## Video File Size

- Netlify free tier allows up to **100 MB per file**.
- If `Rekha.mp4` is larger, consider:
  - Compressing the video (e.g., [HandBrake](https://handbrake.fr/))
  - Hosting the video elsewhere (e.g., Vimeo, YouTube) and embedding it in `index.html`

---

## Video Player Features

- **Play/Pause** – button and native controls
- **Mute/Unmute** – toggle audio
- **Fullscreen** – expand video to fullscreen
- **Native controls** – built-in controls (seek, volume, etc.)
