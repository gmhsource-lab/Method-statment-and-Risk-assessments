# Method Statement & Risk Assessment Tool

A portable, single-file web app for creating professional Method Statements and Risk Assessments for electrical works. No installation, no internet connection required — just open the HTML file in any browser.

Built for use by electrical contractors and site managers. Outputs a print-ready PDF document including all standard method statement sections, a scored risk assessment, method of works, and a sign-off sheet for operatives.

---

## Features

- **Method Statement** — fill in project details, signatures, emergency contacts, and all standard site safety sections (First Aid, PPE, Safe Isolation, Working at Height, Manual Handling, and more)
- **Risk Assessment** — interactive risk matrix (likelihood × severity) with colour-coded scoring, add unlimited risks with initial and final scores
- **Method of Works** — free-text area for project-specific work sequences and procedures
- **Preview & Print** — generates a complete, formatted document ready to print or save as PDF
- **Sign-off Sheet** — 14-row operative sign-off table with the standard declaration statement
- **Save & Load** — export your document as a `.json` file and reload it later to continue editing
- **Fully portable** — everything is contained in a single `.html` file, no dependencies or server needed

---

## Getting Started

### Option 1 — Use directly

1. Download `method-statement.html`
2. Open it in any modern browser (Chrome, Edge, Firefox, Safari)
3. Fill in your document details across the tabs
4. Click **Print / Export PDF** to save your finished document

### Option 2 — Host on GitHub Pages

1. Fork or clone this repository
2. Go to your repository **Settings → Pages**
3. Under **Source**, select `main` branch and `/ (root)`
4. Click **Save**
5. Your app will be live at `https://yourusername.github.io/your-repo-name/method-statement.html`

> GitHub Pages is free for public repositories and requires no configuration beyond the steps above.

---

## How to Use

### Tab 1 — Method Statement
Fill in the document header information: MS number, date, author, project name, site address, client contact, and duration. The standard method statement sections (First Aid, PPE, Safe Isolation, etc.) are pre-filled with standard text — expand each section to review and edit as needed for your specific project.

### Tab 2 — Risk Assessment
- The **risk scoring matrix** is displayed for reference at the top
- Fill in the location, assessor name, and activity/task
- Click **+ Add Risk** to add a hazard entry
- For each risk, fill in the hazard description, who is affected, existing controls, and select the likelihood and severity to auto-calculate the initial score
- Add your protection measures, then set the final likelihood and severity to generate the residual risk score
- Scores are colour-coded: green (1–2 acceptable), amber (3–4 manage), red (5–6 reduce), dark red (7 unacceptable)

### Tab 3 — Method of Works
Write a detailed, project-specific description of how the works will be carried out — sequence of operations, specific procedures, equipment to be used, etc. This section appears in the printed document after the standard method statement sections.

### Tab 4 — Preview
Displays the complete formatted document exactly as it will print. Use **Print / Export PDF** from the toolbar to open your browser's print dialog — select **Save as PDF** as the destination.

### Saving Your Work
- Click **💾 Save** to download a `.json` file containing all your form data and risk entries
- Click **📂 Load** to restore a previously saved `.json` file
- The `.json` file can be shared with colleagues so they can open and continue editing the same document

---

## Printing Tips

- Use **A4** paper size in your print settings
- Set margins to **minimum** or **none** for best results
- Enable **Background graphics** in print settings to preserve the colour-coded risk scores
- **Save as PDF** is recommended over physical printing for sharing documents digitally

---

## File Structure

```
method-statement.html   # The entire application — single self-contained file
README.md               # This file
```

Everything — HTML, CSS, and JavaScript — lives in the single `.html` file. There are no external dependencies, no build steps, and no server required.

---

## Customisation

The file is plain HTML and can be opened in any text editor. Common things you may want to change:

| What | Where in the file |
|---|---|
| Company name / branding | Search for `Method Statement & Risk Assessment` in the `<title>` and header section |
| Pre-filled standard text | Find the `<textarea>` elements with IDs like `txtComms`, `txtFirstAid`, `txtPPE` etc. |
| Number of sign-off rows | Search for `Array.from({length: 14}` and change `14` to your preferred number |
| Legislation list | Search for `Associated Legislation` to find the list items |
| Accent colour | Change `--accent: #c8390a` in the `:root` CSS variables at the top of the file |

---

## Browser Compatibility

| Browser | Support |
|---|---|
| Chrome / Edge | ✅ Full support |
| Firefox | ✅ Full support |
| Safari | ✅ Full support |
| Mobile browsers | ✅ Responsive layout |

---

## Licence

This project is provided as-is for use by electrical contractors and site managers. You are free to use, copy, and modify this tool for your own business use.

---

*Created with [QuoteForge](https://quoteforge.app)*
