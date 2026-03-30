# 📚 BookBites — Bite-Sized Book Learning

A personal learning app that breaks non-fiction books into visual insight cards with spaced repetition, situation challenges, and mastery tracking.

---

## What's Inside

| File | Purpose |
|------|---------|
| `index.html` | The entire app — single file, no dependencies |
| `manifest.json` | PWA config — makes it installable on phone/PC |
| `README.md` | This guide |

---

## STEP 1: Create a GitHub Account (skip if you have one)

1. Go to **https://github.com** and click **Sign Up**
2. Follow the steps — it's free

---

## STEP 2: Create a New Repository

1. Click the **+** button (top right corner) → **New repository**
2. Set these values:
   - **Repository name:** `BookBites` (or any name you prefer)
   - **Public** (must be public for GitHub Pages)
   - **Check** "Add a README file"
3. Click **Create repository**

---

## STEP 3: Upload the App Files

1. In your new repo, click **"Add file"** → **"Upload files"**
2. Drag and drop these 2 files:
   - `index.html`
   - `manifest.json`
3. In the commit message box, type: `Add BookBites app`
4. Click **"Commit changes"**

**Your repo should now have:** `README.md`, `index.html`, `manifest.json`

---

## STEP 4: Enable GitHub Pages

1. In your repo, click the **Settings** tab (top of the page, alongside Code/Issues/Pull requests)

   ⚠️ **Important:** This is the REPO settings (inside your repository), NOT your account settings. The URL should look like: `github.com/YOUR-USERNAME/BookBites/settings`

2. In the left sidebar, click **Pages**
3. Under **"Build and deployment"**:
   - Source: **Deploy from a branch**
   - Branch: **main**
   - Folder: **/ (root)**
4. Click **Save**
5. Wait 2-3 minutes for GitHub to build the site
6. Refresh the Settings → Pages page — you'll see a green banner with your URL:

   ```
   https://YOUR-USERNAME.github.io/BookBites/
   ```

7. Click the URL to verify the app loads

---

## STEP 5: Install as App on Your Phone (Android)

1. Open **Chrome** on your Android phone
2. Go to your GitHub Pages URL: `https://YOUR-USERNAME.github.io/BookBites/`
3. Wait for the page to fully load
4. Tap the **three dots menu (⋮)** at the top right
5. Tap **"Add to Home screen"** (or "Install app" if shown)
6. Name it **BookBites** and tap **Add**
7. The 📚 icon appears on your home screen
8. Open it — it runs full-screen like a native app, no browser bar

---

## STEP 6: Install as App on Your PC (Windows/Mac)

1. Open **Chrome** on your PC
2. Go to your GitHub Pages URL
3. Look for the **install icon** (⊕) in the address bar (right side), OR:
   - Click the **three dots menu (⋮)** → **"Install BookBites..."** or **"Create shortcut..."**
   - If using "Create shortcut", check **"Open as window"**
4. Click **Install**
5. BookBites opens in its own window — no browser tabs or address bar

---

## How to Use BookBites

### Three Screens

- **☀️ Today** — Your morning screen. Shows one concept to carry into the day, your mastery progress, and a check on yesterday's concept.

- **📖 Learn** — Guided chapter-by-chapter learning. Pick a book, work through concepts, rate yourself. Chapters unlock at 60% mastery. Hit "Test My Mastery" to see your strength map.

- **📌 Library** — Pinterest-style board of ALL your concept cards. Filter by theme. Browse your growing knowledge wall.

### Pre-loaded Books

The app comes with 2 books fully loaded:
- **NLP at Work** (8 cards across 6 chapters)
- **Words That Change Minds** (6 cards across 5 chapters)

### Adding More Books

Tap the **+ Add Book** button. The app has a built-in library of these popular books that work instantly (no internet needed):

- Atomic Habits
- Thinking, Fast and Slow
- The 7 Habits of Highly Effective People
- Crucial Conversations
- How to Win Friends and Influence People
- Deep Work
- Start With Why
- Radical Candor
- The Science of Getting Rich
- No B.S. Marketing to the Affluent

For books NOT in the built-in library: if you're connected to the internet and the page is hosted (not opened from a local file), the app will try to generate cards using Claude's AI API. If that fails, it creates placeholder cards.

### Spaced Repetition

Every card has three rating buttons:
- **✅ Got it** — Card appears less frequently (interval increases)
- **🔄 Shaky** — Card comes back sooner for review
- **🆕 Revisit** — Card resets to the beginning

Cards you rate "Got it" three times become **Mastered** (✅).

### Mastery Assessment

Tap **"🧪 Test My Mastery"** on the Today screen to see:
- Overall mastery percentage
- Radar chart showing strength across skill areas
- Gap analysis with recommended next focus
- Specific cards to tackle next

---

## Troubleshooting

### "404 File not found" on phone
- Make sure GitHub Pages is enabled (Step 4)
- Make sure the URL is correct: `https://YOUR-USERNAME.github.io/REPO-NAME/`
- Wait 2-3 minutes after enabling Pages — it takes time to build

### App shows old content after updating files
- Open Chrome on the device
- Press **F12** (PC) to open Developer Tools → Console tab
- Type `resetBookBites()` and press Enter
- The app resets with fresh pre-loaded content

### On phone, can't open console to reset
- Go to Chrome → **Settings → Privacy → Clear Browsing Data**
- Select **"Cookies and site data"** only
- Time range: **All time** → Clear
- Reload the BookBites page

### "Error generating cards" when adding a book
- This happens when the Claude AI API can't be reached
- Built-in library books still work offline
- For other books, try again when connected to internet
- The app must be hosted (GitHub Pages), not opened from local file (file://...)

### How to update the app with a new version
1. Go to your repo on GitHub
2. Click `index.html` → click the **pencil icon** (✏️) to edit
3. Select all (Ctrl+A) → Delete → Paste new content
4. Click **"Commit changes"**
5. Wait 2 minutes, then hard-refresh (Ctrl+Shift+R) on your device
6. Run `resetBookBites()` in console if data structure changed

---

## Technical Details

- **Single file app** — everything is in index.html (HTML + CSS + JS)
- **No server needed** — runs entirely in the browser
- **Data stored in localStorage** — survives page reloads, stays on your device
- **PWA** — installable on Android and desktop via manifest.json
- **Offline capable** — pre-loaded and built-in library books work without internet
- **AI-powered** — can generate cards for any book via Claude API (when online)

---

Built with ❤️ using Claude
