# Utopian Studies Website

Video lessons and resources from Dr. Mmeskerem Lechisa — *Utopian Thoughts in the Bible*.

## Site Structure

```
utopian-studies/
├── index.html              ← Homepage
├── course.html             ← Course overview & lesson list
├── about.html              ← Research & publications
├── books.html              ← Recommended reading
├── enroll.html             ← Registration page
├── css/
│   └── style.css           ← All styles
├── js/
│   └── nav.js              ← Mobile nav toggle
└── lessons/
    ├── 000-introduction.html
    ├── 000-questions-and-concerns.html
    ├── 001-lesson-1a.html
    ├── 002-lesson-1b.html
    ├── 003-lesson-1c.html
    └── 004-lesson-2.html
```

## Deploy to GitHub Pages

### Step 1 — Create a GitHub repository

1. Go to [github.com](https://github.com) and sign in
2. Click **+** → **New repository**
3. Name it: `utopia` (or anything you like)
4. Set visibility to **Public**
5. Click **Create repository**

### Step 2 — Upload the files

**Option A — GitHub web interface (easiest):**
1. In your new repo, click **Add file** → **Upload files**
2. Drag the entire `utopian-studies` folder contents into the upload area
3. Make sure the folder structure is preserved (css/, js/, lessons/ folders)
4. Commit the files

**Option B — Git command line:**
```bash
cd utopian-studies
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/utopia.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages

1. Go to your repo → **Settings** → **Pages** (left sidebar)
2. Under **Source**, select **Deploy from a branch**
3. Choose branch: **main**, folder: **/ (root)**
4. Click **Save**

Your site will be live at:
`https://YOUR_USERNAME.github.io/utopia/`

(Takes about 1–2 minutes to go live after saving.)

---

## Adding a Video to a Lesson

In each lesson file (e.g. `lessons/000-introduction.html`), find the `video-placeholder` div and replace its contents with a YouTube embed:

```html
<div class="video-placeholder">
  <iframe
    src="https://www.youtube.com/embed/YOUR_VIDEO_ID"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>
```

Replace `YOUR_VIDEO_ID` with the ID from your YouTube URL (the part after `v=`).

## Adding a New Lesson

1. Copy `lessons/000-introduction.html`
2. Rename it (e.g. `lessons/005-lesson-3.html`)
3. Update the title, lesson number, description, and prev/next navigation links
4. Add it to the lesson list in `course.html`

---

*Built with plain HTML, CSS, and JavaScript — no frameworks, no build tools.*
