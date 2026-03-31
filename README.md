# 📚 BookBites v3 — Bite-Sized Book Learning

A personal learning app that breaks non-fiction books into visual insight cards with spaced repetition, situation challenges, and mastery tracking.

**What's new in v3:** PDF upload, compressed book storage, on-demand AI card generation, SVG icons on cards, responsive desktop/mobile layout.

---

## Files

| File | Purpose |
|------|---------|
| `index.html` | The entire app — single file |
| `manifest.json` | PWA config for phone/PC installation |
| `README.md` | This guide |

---

## Deploy to GitHub Pages

### Step 1: Create repository
- Go to github.com → click **+** → **New repository**
- Name: `BookBites` (or any name)
- **Public** → Check "Add a README" → **Create**

### Step 2: Upload files
- Click **Add file** → **Upload files**
- Drag in: `index.html` and `manifest.json`
- Click **Commit changes**

### Step 3: Enable GitHub Pages
- Go to repo **Settings** → **Pages** (left sidebar)
- Source: **Deploy from a branch**
- Branch: **main** / **/ (root)** → **Save**
- Wait 2-3 minutes → your URL appears:
  `https://YOUR-USERNAME.github.io/BookBites/`

### Step 4: Install on phone
- Open URL in **Chrome** on Android
- Tap **⋮** → **Add to Home screen**
- Opens full-screen like a native app

### Step 5: Install on PC
- Open URL in **Chrome**
- Click **install icon** in address bar (or ⋮ → Install BookBites)
- Opens in its own window

---

## How to Use

### Adding Books

**Option 1 — Upload PDF** (best quality)
- Tap **+ Add** → select **Upload PDF**
- Pick any PDF from your device
- App extracts text, detects chapters, generates AI-powered cards
- Book content stored compressed in your browser — works offline after setup

**Option 2 — Generate with AI** (no file needed)
- Tap **+ Add** → select **Generate with AI**
- Enter book title → Claude generates cards from its knowledge
- Built-in library includes: Atomic Habits, Deep Work (more being added)
- Works best when hosted on GitHub Pages (API needs HTTPS)

### Three Screens

- **☀️ Today** — Morning card with insight, story anchor, situation challenge, and today's action
- **📖 Learn** — Chapter-by-chapter progression. Cards unlock as you master earlier ones (60% threshold)
- **📌 Library** — Pinterest-style board of all your concepts. Filter by theme

### Spaced Repetition

Rate each card:
- **Got it** → interval increases, appears less often
- **Shaky** → comes back sooner
- **Revisit** → resets to beginning

3x "Got it" = Mastered (✅)

### Mastery Assessment

Tap **🧪 Test My Mastery** for:
- Overall mastery percentage
- Strength map by skill area (communication, leadership, etc.)
- Weakest areas identified with specific cards to focus on

---

## Troubleshooting

**Reset all data:** Open browser console (F12) → type `resetBookBites()` → Enter

**PDF upload not working:** Make sure the file is a real PDF (not a scanned image PDF). The app extracts text — if the PDF is all images, there's no text to extract.

**AI generation fails:** This requires internet + HTTPS (GitHub Pages). Won't work from local file:// URLs. Built-in fallback library still works offline.

**Old data from previous version:** Run `resetBookBites()` in console to clear and start fresh.

---

Built with ❤️ using Claude
