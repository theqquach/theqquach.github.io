# theqquach.github.io

Personal site built with [Astro](https://astro.build). Deployed automatically to GitHub Pages on every push to `main`.

## Quick start

```bash
npm install
npm run dev       # → http://localhost:4321
npm run build     # builds to dist/
```

## Editing your content

**All content lives in `src/content/` as YAML files. You never need to touch the page code to update your info.**

| File | What it controls |
|---|---|
| `about.yaml` | Name, bio, hero text, interests, languages, contact links |
| `experience.yaml` | Work and volunteer roles |
| `projects.yaml` | Project cards |
| `education.yaml` | Degrees |
| `skills.yaml` | Skill groups and which ones are highlighted |
| `awards.yaml` | Awards and certifications |
| `uses.yaml` | The /uses page — hardware, software, tools |

### Adding a new job

Open `src/content/experience.yaml` and add a block at the top:

```yaml
- title: Your Job Title
  org: Company Name
  url: https://company.com        # optional
  dates: Jan 2025 — Present
  type: work                      # "work" or "vol"
  bullets:
    - First responsibility
    - Second responsibility
```

### Adding a new project

Open `src/content/projects.yaml` and add a block:

```yaml
- title: My New Project
  tag: Machine Learning           # see tag options in the file header
  description: >
    What the project does, methods used, and what you learned.
  stack: [Python, pandas, sklearn]
  url: https://github.com/theqquach/my-project
```

### Highlighting a skill

In `src/content/skills.yaml`, add `hot: true` to any item:

```yaml
- name: PyTorch
  hot: true
```

### Updating your photo

Replace `public/avatar.png` with your new photo. Keep the filename the same.

### Updating your CV

Drop your PDF into `public/uploads/resume.pdf`.

## Deployment

Push to `main` → GitHub Actions builds the site → deploys to GitHub Pages automatically.

**First-time setup:**
1. Go to your repo → Settings → Pages
2. Set Source to **GitHub Actions**
3. Push any commit — the workflow in `.github/workflows/deploy.yml` handles the rest

## Structure

```
theqquach.github.io/
├── src/
│   ├── content/          ← EDIT THESE
│   │   ├── about.yaml
│   │   ├── experience.yaml
│   │   ├── projects.yaml
│   │   ├── education.yaml
│   │   ├── skills.yaml
│   │   ├── awards.yaml
│   │   └── uses.yaml
│   ├── layouts/
│   │   └── Base.astro    ← nav, footer, shared HTML
│   ├── pages/
│   │   ├── index.astro   ← home page
│   │   └── uses.astro    ← /uses page
│   └── styles/
│       └── global.css    ← colours, fonts, shared styles
├── public/
│   ├── avatar.png        ← your photo
│   └── uploads/
│       └── resume.pdf    ← your CV
├── astro.config.mjs
└── package.json
```
