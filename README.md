# Tran Trung Bac — Portfolio

Personal portfolio hosted at https://trungbac11.github.io/.
Static HTML/CSS/JavaScript; no build step required.

## Enable GitHub Pages (one time)

Settings → Pages → Source: Deploy from a branch → main → / (root) → Save.

## Add your CV and images

On GitHub open the relevant folder, choose **Add file → Upload files**, upload, and commit to `main`. Use these exact names, including case, or update `config.js` to match your filenames:

| Asset | Path |
| --- | --- |
| CV PDF | `assets/cv/Tran-Trung-Bac-CV.pdf` |
| Avatar | `assets/images/avatar/avatar.jpg` |
| Sacombank logo | `assets/images/companies/sacombank.png` |
| CDC project image | `assets/images/projects/cdc.jpg` |
| Music project image | `assets/images/projects/music.jpg` |
| VietGreen project image | `assets/images/projects/vietgreen.jpg` |
| Video retrieval image | `assets/images/projects/video.jpg` |

CV view/download buttons become active when the PDF exists. The viewer opens inside the page, with an external viewer link for browsers that do not support embedded PDFs. No PDF has been included yet.

Images fall back to the TB monogram, S monogram, or pipeline diagrams until uploaded. The avatar is cropped to a circle; company logos and project images use `object-fit: contain` so the full image is visible. PNG, JPG, WebP, and SVG are supported by updating the paths in `config.js`.

This is a static site: upload files through GitHub, not through a public visitor upload form. All files you put in this public repository are publicly accessible.

## Edit content

- Personal information, Education, Experience, Skills, and Recognition: `index.html`.
- Project descriptions and detail dialogs: `projects` array in `index.html`.
- CV and image paths: `config.js`.
- Styles and responsive layout: `<style>` in `index.html`.

## Preview locally

Run `python -m http.server 8000` from this folder, then open http://localhost:8000/. Use HTTP instead of opening the file directly so CV availability checks work.
