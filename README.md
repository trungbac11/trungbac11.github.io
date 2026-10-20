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

## Education logo and credential links

The HCMUS logo is stored at `assets/images/education/hcmus.png`; change the school’s `logo` path inside `education` in `config.js` to replace it. Source: https://hcmus.edu.vn/he-thong-nhan-dien-thuong-hieu/. The logo is shown without cropping or recoloring.

Paste your own credential links into `certificateLinks` in `config.js`: `scudem`, `spring-school`, `aiesec`, `datathon`. For Google Drive use a file sharing link, and configure viewer access so visitors can open it. Drive file links open an embedded preview with a link to the original document; other HTTPS credential links open in a new tab. Empty links leave View credential disabled.



## Add another school

Edit the `education` array in `config.js`. Copy the existing school object, insert a comma between entries, and change `name`, `degree`, `detail`, `period`, `logo`, and `highlights`. Upload the school logo under `assets/images/education/`. Schools display in list order; put your most recent school first. You do not need to edit `index.html` or change the layout. A commented NYCU template is included, but is not part of your actual education record. Only enter confirmed study details when using it for your public portfolio.
