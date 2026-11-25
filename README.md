# Employee OT Minutes Calculator with Client-Side OCR (Vercel Edition)

Multi-employee Overtime (OT) Minutes & Payroll Calculator with **100% browser-based OCR** (`Tesseract.js` + `PDF.js`) calibrated for **KIJO 6902** electronic time cards, scanned PDFs, and mobile photos.

## Features
- **Client-Side PDF & Photo OCR (`Tesseract.js v5` + `PDF.js v3`):** Upload multi-page scanned time card PDFs (e.g., Days 1–15 on Page 1, Days 16–31 on Page 2) or camera photos (`.jpg`, `.png`, `.webp`) directly in the browser—zero server uploads required.
- **Image Pre-Processing Pipeline:** Renders PDFs at high DPI (2.8x) and applies contrast enhancement & grid-line suppression before OCR for crisp dot-matrix digit recognition.
- **KIJO 6902 Time Card Parser & Review Table:** Automatically extracts Employee Name, Month, Year, daily Clock-In/Out timestamps, `SUNDAY`, `PH`, `MRSM`/Leave remarks, cleans alignment digits (`807:16` -> `07:16`), and lets you verify/edit rows before importing.
- **KIJO Shift & OT Rule Engine:** Weekday (`08:30–17:30`), Half-Day Saturday (`08:30–13:00`), Sunday (`2.0x`), Public Holiday (`3.0x`), overnight midnight crossovers, grace periods, and rounding.
- **Multi-Employee Rollup & Excel Export:** Aggregates OT minutes, OT hours, late minutes, and weighted OT hours per employee with one-click `.xlsx` export.

## Deploy to Vercel
1. Extract this folder and push to GitHub/GitLab/Bitbucket, or run `npx vercel --prod` inside the folder.
2. Vercel detects `vercel.json` and deploys `public/index.html` immediately.
