# Al-Folio Setup for Dongxin Guo (bettyguo.github.io)

## Quick Setup (5 minutes)

### Step 1: Create Repository from Template
1. Go to https://github.com/alshedivat/al-folio
2. Click the green **"Use this template"** → **"Create a new repository"**
3. Name it exactly: `bettyguo.github.io`
4. Set it to **Public**
5. Click **Create repository**

### Step 2: Enable GitHub Actions
1. Go to your new repo: `github.com/bettyguo/bettyguo.github.io`
2. **Settings → Actions → General → Workflow permissions**
   - Select "Read and write permissions"
   - Check "Allow GitHub Actions to create and approve pull requests"
   - Click Save
3. Go to **Actions** tab → Enable workflows if prompted

### Step 3: Drop in These Customized Files
Clone your repo locally:
```bash
git clone git@github.com:bettyguo/bettyguo.github.io.git
cd bettyguo.github.io
```

Copy these files from this package, **replacing** the defaults:

| Source File                        | Destination (in your repo)         |
|------------------------------------|------------------------------------|
| `_config.yml`                      | `_config.yml` (replace)            |
| `_pages/about.md`                  | `_pages/about.md` (replace)        |
| `_pages/publications.md`           | `_pages/publications.md` (replace) |
| `_pages/cv.md`                     | `_pages/cv.md` (replace)           |
| `_pages/projects.md`               | `_pages/projects.md` (replace)     |
| `_bibliography/papers.bib`         | `_bibliography/papers.bib` (replace)|
| `_news/announcement_sigir.md`      | `_news/` (add, delete defaults)    |
| `_news/announcement_ijcai.md`      | `_news/` (add)                     |
| `_news/announcement_lics.md`       | `_news/` (add)                     |
| `_news/announcement_icdcs.md`      | `_news/` (add)                     |
| `_news/announcement_acl.md`        | `_news/` (add)                     |

### Step 4: Add Your Profile Photo
Download your GitHub avatar (or use a professional headshot) and save it as:
```
assets/img/prof_pic.jpg
```
Your GitHub avatar URL: https://avatars.githubusercontent.com/u/13963138?v=4

### Step 5: Delete Default Sample Content
Remove the template's sample content that you don't need:
```bash
# Remove default news items
rm _news/announcement_1.md _news/announcement_2.md _news/announcement_3.md

# Remove default blog posts (optional, keep if you want blog examples)
rm _posts/*.md

# Remove default project pages
rm _projects/*.md
```

### Step 6: Deploy
```bash
git add -A
git commit -m "Initial customization"
git push
```

Wait ~2 minutes for GitHub Actions to build. Then:
1. Go to **Settings → Pages**
2. Set Source: **Deploy from a branch**
3. Set Branch: **gh-pages** / **(root)**
4. Click Save

Your site will be live at: **https://bettyguo.github.io**

---

## Post-Setup Customization

### Replace papers.bib with Your Real Publications
The included `papers.bib` has placeholder entries. To get your real ones:

1. Go to https://scholar.google.ca/citations?user=Zz_d_8UAAAAJ&hl=en
2. Select all publications → Export → BibTeX
3. Replace `_bibliography/papers.bib` with the exported file
4. For papers you want on the homepage, add `selected={true}` to the entry
5. For venue badges, add `abbr={SIGIR}` (or IJCAI, LICS, etc.)
6. For code links, add `code={https://github.com/...}`
7. For paper PDFs, add `pdf={filename.pdf}` and put the PDF in `assets/pdf/`

### Add Your CV
1. Export your CV as PDF
2. Put it in `assets/pdf/CV.pdf`
3. Edit `_pages/cv.md` and uncomment `cv_pdf: CV.pdf`

### Optional: Custom Domain
If you buy a domain (e.g., `dongxinguo.com`):
1. Settings → Pages → Custom domain → enter your domain
2. At your DNS provider, add a CNAME record: `www` → `bettyguo.github.io`
3. Add four A records pointing to GitHub's IPs:
   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153

### Optional: Local Preview with Docker
```bash
docker compose up
```
Then open http://localhost:8080

---

## File Structure Reference
```
bettyguo.github.io/
├── _config.yml              # Main site configuration
├── _pages/
│   ├── about.md             # Homepage
│   ├── publications.md      # Auto-generated from BibTeX
│   ├── cv.md                # CV page
│   └── projects.md          # Projects grid
├── _bibliography/
│   └── papers.bib           # Your publications (BibTeX)
├── _news/                   # News/announcements
├── _posts/                  # Blog posts (optional)
├── _projects/               # Project pages
├── assets/
│   ├── img/
│   │   └── prof_pic.jpg     # Your photo
│   └── pdf/                 # PDFs (CV, papers)
└── _data/
    └── cv.yml               # CV data (if using YAML format)
```
