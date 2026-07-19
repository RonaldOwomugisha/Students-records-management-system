# Student Academic Records System

A responsive, browser-based academic records management interface developed as a course assignment for **Programming for Mechanical Engineers**. The project was prepared by a student pursuing a **Bachelor of Engineering in Automotive and Power Engineering** under the **Department of Mechanical and Production Engineering, Kyambogo University**. The application manages student profiles, semester results, GPA and CGPA calculations, academic classifications, reports, transcripts, CSV import and CSV export.

## Academic context

- **Course unit:** Programming for Mechanical Engineers
- **Programme:** Bachelor of Engineering in Automotive and Power Engineering
- **Department:** Mechanical and Production Engineering
- **Institution:** Kyambogo University
- **Academic year:** 2025/2026
- **Student registration number:** 24/U/APD/11369/PD

This repository represents a course assignment and frontend demonstration. It is not an official Kyambogo University information system.

## Repository contents

- `index.html` — complete frontend application
- `sample_students.csv` — sample import file
- `CODE_REVIEW.md` — review findings, corrections, and remaining production requirements
- `.nojekyll` — tells GitHub Pages to serve the repository as a plain static site

## Run locally

Open `index.html` in a modern browser. For behavior closest to GitHub Pages, use a small local web server rather than opening the file directly.

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Publish with GitHub Pages

### Easiest method: GitHub website

1. Download and extract `student-records-github-ready.zip` on your computer.
2. Sign in to GitHub and select **New repository**.
3. Give the repository a clear name such as `student-records-system`.
4. Select **Public** when using GitHub Free. Do not initialize the repository with another README because this package already contains one.
5. Select **Create repository**.
6. On the empty repository page, select **uploading an existing file**, or use **Add file → Upload files**.
7. Open the extracted `student-records-github` folder and upload its contents. `index.html` must be in the repository root, not inside another nested folder. Do not upload only the ZIP archive.
8. Confirm that the repository root contains `index.html`, `README.md`, `CODE_REVIEW.md`, `sample_students.csv`, and `.nojekyll`.
9. Enter a commit message such as `Initial Student Records System release`, then select **Commit changes**.
10. Open **Settings → Pages**.
11. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
12. Select the `main` branch and `/ (root)`, then select **Save**.
13. Return to **Settings → Pages** after deployment. GitHub displays the published site address there.

For a normal project repository, the address is usually:

```text
https://YOUR-USERNAME.github.io/student-records-system/
```

A first deployment or a later update can take several minutes to appear. When updating the website, upload the revised files to the same repository and commit them to `main`; GitHub Pages will publish the new version automatically.

### Common deployment checks

- The entry filename must be exactly `index.html`, using lowercase letters.
- `index.html` must be at the top level of the selected publishing folder.
- Use `main` and `/ (root)` for this package.
- Do not upload confidential or real student records to the public repository.
- If the site shows an older version, use a hard refresh with `Ctrl + F5`.

## Printing performance

The Print command creates a lightweight temporary print document containing only the currently active dashboard, report, register, or transcript view. Interactive controls, hidden panels, animations, web fonts, and navigation elements are excluded. This substantially reduces the time required for the browser to prepare print preview, especially for transcripts. Very long transcripts can still take longer because the browser must paginate every course table and page.

## Browser data behavior

Student records and activity history are stored in the current browser using `localStorage`.

- Changes survive page refreshes on the same browser and device.
- Data is not synchronized between browsers or devices.
- Clearing browser site data removes the records.
- To restore the initial sample dataset after using **Clear All**, run the command below in the browser console and reload:

```javascript
localStorage.removeItem('kyu-srms-state-v2');
location.reload();
```

## CSV import format

The importer requires these headings:

- `Name`
- `Reg Number`

These headings are optional:

- `Programme`
- `Year`
- `Email`

Quoted values and commas inside quoted values are supported. Invalid registration numbers, invalid email addresses, duplicate records, and files larger than 2 MB are rejected or skipped.

## Important production limitation

GitHub Pages hosts static frontend files only. This version is suitable for demonstrations, assessment, interface review, and controlled local use. It is not a secure multi-user university ERP.

A real production deployment handling official student records still requires:

- authenticated user accounts
- role-based permissions
- a secure backend API
- a managed database
- server-side validation
- encrypted transport and protected secrets
- audit logs that users cannot alter
- backups and recovery procedures
- privacy, records-retention, and institutional compliance controls

Do not place real confidential student records in a public GitHub repository or rely on browser storage as the official system of record.
