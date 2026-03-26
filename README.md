# Personal Portfolio Website

This repository contains a single-page portfolio website built in one file: `index.html`.

Live site (GitHub Pages):
- https://fardinsafi.github.io/personal-portfolio/

## Project Structure

- `index.html`: Entire website (layout, styles, JavaScript interactivity, data for Experience and Projects)
- `resume.pdf`: Resume download file linked from navbar and hero
- `headshot.jpg`: Profile image used in the hero section and social preview metadata
- `prompt.txt`: Original requirements/specification notes

## Quick Start (Edit Locally)

1. Open this folder in VS Code.
2. Edit `index.html`.
3. Open `index.html` in a browser to preview changes.

Tip: The HTML now contains section comments like:
- `===== HERO SECTION ========`
- `===== EXPERIENCE SECTION ========`
- `===== CLIENT-SIDE DATA + INTERACTIONS ========`

Use these markers to jump quickly to the part you want to edit.

## How To Edit Existing Content

### 1) Update Hero Content
In `index.html`, find `===== HERO SECTION ========` and edit:
- Name/title text
- Intro paragraph
- Contact details (email/phone/location)
- CTA links (Resume, LinkedIn, GitHub)

### 2) Update About Section
Find `===== ABOUT SECTION ========` and edit:
- About paragraph
- Education highlights card
- Professional narrative text
- Languages chips

### 3) Update Experience Cards
Find `===== CLIENT-SIDE DATA + INTERACTIONS ========` then the `experienceData` array.

Each item controls one card and modal:
- `company`
- `role`
- `period`
- `summary`
- `bullets` (shown in modal)
- `tech`

### 4) Update Projects Cards
In the same script area, edit `projectsData`.

Each item controls one project card:
- `title`
- `description`
- `tech`

### 5) Update Skills
Find `===== SKILLS SECTION ========` and edit:
- Progress bar labels and percentages
- Tools/domain tags

### 6) Update Education & Achievements
Find `===== EDUCATION & ACHIEVEMENTS SECTION ========` and edit timeline and highlight text.

### 7) Update SEO / Social Preview
Find `===== CORE META / SEO / SOCIAL PREVIEW ========` in `<head>` and update:
- `<title>`
- description/keywords
- Open Graph tags (`og:*`)
- Twitter tags
- canonical URL (if repo/site URL changes)

Also update structured data under `===== STRUCTURED DATA (SCHEMA.ORG PERSON) ========`.

## How To Add a New Section

Example: Add a `Certifications` section.

1. Add a new nav link in desktop and mobile navbar:
- `href="#certifications"`

2. Create a new section block in `<main>`:

```html
<!-- ======== CERTIFICATIONS SECTION ======== -->
<section id="certifications" class="section-block fade-in" aria-labelledby="certifications-title">
  <div class="mb-8">
    <h2 id="certifications-title" class="font-display text-3xl font-bold text-white lg:text-4xl">Certifications</h2>
  </div>
  <div class="grid gap-5 md:grid-cols-2">
    <!-- your cards/items -->
  </div>
</section>
```

3. Add the section id to nav highlight tracking in script:

```js
const sectionIds = ["home", "about", "experience", "projects", "skills", "certifications"];
```

4. Save and test scrolling, active nav state, and mobile menu behavior.

## Git + GitHub Pages Deployment Commands

Run these from the project folder:

```powershell
git status
git add -A
git commit -m "Describe your changes"
git push
```

After pushing, GitHub Pages usually updates in 1-3 minutes.

## First-Time Setup (Only If Needed)

If this folder was not initialized before:

```powershell
git init
git remote add origin https://github.com/FardinSafi/personal-portfolio.git
git branch -M main
git add -A
git commit -m "Initial portfolio commit"
git push -u origin main
```

## Recommended Edit Workflow

1. Make one logical batch of edits.
2. Preview in browser.
3. Run `git status` to verify intended changes only.
4. Commit with a clear message.
5. Push and wait for Pages refresh.

## Troubleshooting

- Changes not visible on live site:
  - Hard refresh the browser (`Ctrl + F5`).
  - Wait 1-3 minutes for Pages deployment.
  - Confirm push reached `main` branch.

- Section link does not highlight in navbar:
  - Ensure section has a unique `id`.
  - Ensure that `id` is present in `sectionIds` in script.

- New section does not animate:
  - Add class `fade-in` to the section or element.

## License

Personal portfolio content and branding are for the owner of this repository.
