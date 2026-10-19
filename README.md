# Personal academic website

Single-page static site (plain HTML + CSS, no build step), modeled on
[brendacnogueira.github.io](https://brendacnogueira.github.io/).

## Files

| Path | What it is |
|------|------------|
| `index.html` | The whole site: content, styles, and the mobile nav script in one file |
| `images/photo.jpg` | Portrait shown in the hero (800×800 JPEG) |
| `images/photo-placeholder.svg` | Fallback shown only if `photo.jpg` is missing |
| `CV_Vinicius_Lopes.pdf` | Linked from the nav, the hero, the Experience section, and the CV section |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is (no Jekyll processing) |

## Deploy to GitHub Pages

1. On GitHub, create a **public** repository named exactly `vinilopes03.github.io`.
   The name is what makes it a user site.
2. Put the contents of this folder at the root of that repository.
3. Commit and push to the `main` branch:

   ```bash
   git init
   git add .
   git commit -m "Personal website"
   git branch -M main
   git remote add origin git@github.com:vinilopes03/vinilopes03.github.io.git
   git push -u origin main
   ```

4. In the repository, open **Settings → Pages** and confirm the source is
   "Deploy from a branch", branch `main`, folder `/ (root)`. User sites are
   usually enabled automatically.
5. After a minute or two the site is live at `https://vinilopes03.github.io`.

Every later change is just another commit and push.

## Updating content

- **New publication**: copy one `<li class="pub-item">` block in the
  Publications section and edit the title, authors, venue, and the link chips.
- **News**: add an `<li>` at the top of the `news-list`.
- **Google Scholar**: the profile link
  is already in the contact card, the Publications heading, and the footer.
- **Colors**: the `:root` block at the top of the `<style>` section
  (`--accent` is Notre Dame navy, `--gold` is only used as a soft highlight).
- **Sections**: each is a plain `<section>`; delete or reorder them and update
  the matching `<li>` in the nav.
