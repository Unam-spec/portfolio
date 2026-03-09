# UNAM — Content Creator Portfolio

> Personal portfolio website for **Unam Matheatau** — content creator based in Johannesburg, South Africa.  
> Built with vanilla HTML, CSS, and JavaScript. No frameworks, no dependencies, no build step.

🔗 **Live site:** `https://yourusername.github.io/your-repo-name` ← update this after deploying

---

## 🚀 Quick Deploy (GitHub Pages)

1. Create a new GitHub repository (e.g. `portfolio`)
2. Upload `index.html` (rename `unam-portfolio.html` → `index.html`)
3. If you have a video file, upload it to the same repo
4. Go to **Settings → Pages**
5. Under **Source**, select `Deploy from a branch` → `main` → `/ (root)`
6. Click **Save** — your site will be live in ~60 seconds

---

## 📁 File Structure

```
/
├── index.html          ← the entire site (rename from unam-portfolio.html)
├── video1.mp4          ← your uploaded video (optional, same folder)
└── README.md           ← this file
```

---

## ✏️ How to Update Content

All editable content lives in the **`CONFIG` block** at the very top of `index.html`.  
Open the file in VS Code and edit only that section — nothing else needs to change.

```js
const CONFIG = {

  // Personal details
  name:     "Unam Matheatau",
  email:    "unam.hii@gmail.com",
  location: "Johannesburg, ZA",

  // Social handles
  tiktok:    { handle: "@unam_.hii", url: "https://tiktok.com/@unam_.hii" },
  instagram: { handle: "@unam_.m",   url: "https://www.instagram.com/unam_.m/" },

  // Stats — just change the "value" fields
  stats: [
    { platform: "TikTok · @unam_.hii", value: "6K", label: "Followers" },
    ...
  ],

  // Videos — see below for how to add/update
  videos: [ ... ],

  ...
}
```

---

## 🎬 Adding / Updating Videos

There are 3 video slots. Each one has a `type` — either `"file"`, `"tiktok"`, or `"instagram"`.

### Local video file (`type: "file"`)
1. Put your `.mp4` file in the same folder as `index.html`
2. In the CONFIG, set `src` to the filename:
```js
{ type: "file", src: "myclip.mp4", tag: "Featured · Direct Upload" }
```

### TikTok video (`type: "tiktok"`)
1. Go to your TikTok video → **Share → Copy Link**
2. The URL looks like: `https://www.tiktok.com/@unam_.hii/video/7312345678901234567`
3. Paste the full URL into `src`:
```js
{ type: "tiktok", src: "https://www.tiktok.com/@unam_.hii/video/7312345678901234567", tag: "TikTok · @unam_.hii" }
```

### Instagram Reel (`type: "instagram"`)
1. Open your Reel → tap **three dots → Copy Link**
2. The URL looks like: `https://www.instagram.com/reel/ABC123xyz/`
3. Paste the full URL into `src`:
```js
{ type: "instagram", src: "https://www.instagram.com/reel/ABC123xyz/", tag: "Instagram · @unam_.m" }
```

### Adding more videos
Copy any `{ }` block inside `videos: [ ]` and paste it below the last one.

### Removing a video
Delete the entire `{ }` block for that video.

---

## 📊 Updating Your Stats

Find the `stats` array in CONFIG and change any `value` field:

```js
stats: [
  { platform: "TikTok · @unam_.hii", value: "6K",     label: "Followers"       },
  { platform: "TikTok · avg per video", value: "1K",   label: "Avg. Views"      },
  { platform: "TikTok · avg per video", value: "16.12%", label: "Viral Rate"    },
  { platform: "TikTok · avg per video", value: "13.14%", label: "Engagement Rate" },
  { platform: "Instagram · @unam_.m",  value: "5K",    label: "Followers"       },
  { platform: "Instagram · avg per post", value: "11K", label: "Avg. Reach"     },
  { platform: "Instagram · avg per post", value: "2.1K", label: "Avg. Engagements" },
  { platform: "Instagram · avg per post", value: "11.37%", label: "Engagement Rate" },
],
```

---

## 🔧 Local Preview

No server needed for most things. Just open `index.html` directly in your browser.

> ⚠️ **Exception:** Local video files won't play if you just double-click the HTML file in some browsers due to security restrictions. To preview with video working, run a local server:

```bash
# If you have Python installed
python -m http.server 8000
# Then open http://localhost:8000 in your browser
```

Or install the **Live Server** extension in VS Code and click **Go Live** in the bottom bar.

---

## 🎨 Customisation Notes

| What | Where in `index.html` |
|---|---|
| All content & data | `CONFIG` block (top of file) |
| Colors | `:root` CSS variables (~line 50) |
| Fonts | Google Fonts `<link>` tag + `font-family` in CSS |
| Layout / styling | CSS section (between `<style>` tags) |
| Page sections | HTML body (search for `<!-- 01 ABOUT -->` etc.) |

The accent color is `#00e5ff` (cyan). To change it, find `--accent: #00e5ff;` in the `:root` block and replace the hex.

---

## 📬 Contact

**Unam Matheatau**  
📧 unam.hii@gmail.com  
🎵 TikTok: [@unam_.hii](https://tiktok.com/@unam_.hii)  
📸 Instagram: [@unam_.m](https://www.instagram.com/unam_.m/)
