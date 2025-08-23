# HOA Website — Jekyll (GitHub Pages)

A simple, maintenance-friendly HOA site you can host **free** on **GitHub Pages**.
Includes: Home, About, Officers, News/Notices (posts), Contact, and a Pay Dues link.

## Quick Start

1) Create a new GitHub repo and upload these files.
2) In your repo: **Settings → Pages**
   - **Source:** Deploy from a branch
   - **Branch:** `main` and folder `/` (root)
3) Visit the URL GitHub shows (e.g., `https://USERNAME.github.io/REPO/`).

> If you name your repo `USERNAME.github.io`, GitHub will publish at `https://USERNAME.github.io/` and you can leave `baseurl: ""` in `_config.yml`.

## Editing Content
- **News/Notices:** add Markdown files in `_posts/` named `YYYY-MM-DD-title.md`.
- **Officers:** edit `_data/officers.yml`.
- **Pay link & Address:** edit `_config.yml` (`pay_url`, `address`, `title`, `description`).
- **About/Contact:** edit `about.md` and `contact.md`.

## Contact Form
GitHub Pages is static-only. To make the contact form work, sign up for **Formspree** (free tier) and replace `YOUR_FORM_ID` in `contact.md` with your endpoint.

## Custom Domain (optional)
- In repo **Settings → Pages → Custom domain**, enter `yourhoa.org`.
- Then create DNS records at your registrar as GitHub instructs. HTTPS is auto-provisioned.

## Local Preview (optional)
Install Ruby and Jekyll, then:
```bash
gem install bundler jekyll
bundle install
bundle exec jekyll serve
# open http://127.0.0.1:4000
```