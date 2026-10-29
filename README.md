# FreeStream App

A lightweight, zero-dependency web application to search for movies and find global free (ad-supported) and subscription streaming availability across 100+ countries, with instant CSV export.

---

## 🚀 How to Run

### Option 1: Just Double-Click (Zero Install)
You don't need Python, Node.js, or any software installed:
* Simply double-click **`index.html`** to open it in any web browser (Chrome, Edge, Firefox, Safari).

### Option 2: Run a Local Static Server (Optional)
If you prefer running a local server:
```powershell
# Using Python (if available):
python -m http.server 8000

# Or using Node:
npx serve .
```
Then visit `http://localhost:8000`.

### Option 3: Host It Free for Friends & Anyone to Use
You can deploy this folder directly to any free static host:
- **GitHub Pages**: Push this folder to a GitHub repository, enable GitHub Pages in repo settings.
- **Cloudflare Pages / Vercel / Netlify**: Drag-and-drop the `freestream-app` folder or connect your Git repo.

---

## 🔑 TMDB API Token Setup

To allow anyone to use their own credentials without hardcoding yours:
1. When you first open the app, a step-by-step onboarding card guides you to:
   - Create a free account at [themoviedb.org](https://www.themoviedb.org/signup).
   - Generate an **API Read Access Token (v4 auth)** or **API Key (v3)** at [TMDB API Settings](https://www.themoviedb.org/settings/api).
2. Paste the token into the input field and click **Verify & Save Token**.
3. The app tests the token against TMDB directly; if valid, it saves it in your browser's private `localStorage` so you never have to re-enter it.
4. You can edit, verify, or remove the token anytime by clicking the **⚙️ TMDB Status** button in the header.

---

## ✨ Features

- **Zero Dependencies**: Pure HTML5, modern CSS3, and Vanilla JavaScript.
- **Global Country Coverage**: Converts ISO country codes into full country names and flag emojis automatically using standard browser `Intl` APIs (no `pycountry` needed).
- **Free & Subscription Filtering**: Filter by All, Free (with Ads), or Subscription platforms.
- **Provider Logos**: Displays official logos for Netflix, Tubi, Pluto TV, Prime Video, etc.
- **CSV Export**: One-click download of the availability table formatted identically to `freestream.py`:
  - Columns: `Country`, `Platform`, `Type`
  - Filename: `[Movie_Title]_free_streaming_availability.csv`
- **PWA Ready**: Works smoothly on mobile phones, tablets, and desktop computers.
