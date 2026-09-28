# IRD Test Case Generator Dashboard

> ## Test PIN: `280085`

> Enter this six-digit PIN after the loading screen to access the dashboard. The PIN gate appears again whenever the page is refreshed or reopened.

A responsive, browser-based quality assurance dashboard that converts form IRDs, requirement sheets, and change logs into structured test cases. The project also includes a reverse-documentation workflow that can generate an IRD by inspecting HTML and optional JavaScript files.

## Features

- Generate structured test cases from an existing IRD
- Convert only change-log records into targeted regression test cases
- Create an IRD from an HTML form and optional JavaScript files
- Preview generated test cases before export
- Search test cases by ID, field, or scenario
- Filter generated test cases by priority
- Export test cases to a styled Excel workbook
- Export test cases to a multi-page PDF
- Export a generated IRD to Excel
- Dark and light themes with saved preference
- Responsive mobile, tablet, and desktop layout
- Touch-friendly controls and horizontally scrollable tables
- Drag-and-drop file uploads
- Local browser processing without a backend
- GitHub Pages compatible

## Supported Input Formats

The standard IRD workflow and change-log workflow support:

- `.xls`
- `.xlsx`
- `.csv`

The **Create IRD for Your Form** workflow supports:

- `.html` or `.htm` as the required form file
- One or more optional `.js` files

Uploaded JavaScript files are inspected as text and are not executed.

## Project Files

```text
IRD-Test-Case-Dashboard/
├── index.html
├── styles.css
├── script.js
└── README.md
```

All four files should remain in the same directory.

## Run Locally

No installation, package manager, build tool, or local server is required.

1. Download or clone the repository.
2. Keep `index.html`, `styles.css`, and `script.js` together.
3. Open `index.html` in a modern browser.
4. Wait for the loading progress to reach 100%.
5. Enter the test PIN: `280085`.

A local web server may also be used if preferred:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Deploy to GitHub Pages

1. Create a GitHub repository.
2. Upload these files to the repository root:
   - `index.html`
   - `styles.css`
   - `script.js`
   - `README.md`
3. Commit and push the files to the `main` branch.
4. Open the repository **Settings**.
5. Select **Pages**.
6. Under **Build and deployment**, choose **Deploy from a branch**.
7. Select the `main` branch and `/root` folder.
8. Save the configuration.
9. Open the GitHub Pages URL after deployment completes.

No CDN, backend service, database, environment variable, or build command is required.

## Workflow 1: Generate Test Cases from a Full IRD

1. Select or drop an `.xls`, `.xlsx`, or `.csv` IRD in the main upload box.
2. The dashboard detects the most likely worksheet and header row.
3. Form fields or requirements are mapped into test scenarios.
4. Review the generated metrics and test-case table.
5. Search or filter the generated test cases if needed.
6. Export the result to Excel or PDF.

Generated test cases can include:

- Positive scenarios
- Negative scenarios
- Boundary conditions
- Format validations
- Functional validations
- Business-rule validations

## Workflow 2: Convert Change Log to Test Cases

Use this workflow when a form already exists and only changed fields require testing.

1. Select **Convert Change Log to Test Cases**.
2. Upload an `.xls`, `.xlsx`, or `.csv` change-log file.
3. Select **Analyze Change Log**.
4. Review the detected changed fields or requirements.
5. Select **Generate Test Cases**.

Only the records detected in the change log are converted into test cases. A verification reminder is displayed after generation so existing fields can be reviewed separately.

## Workflow 3: Create IRD for Your Form

Use this workflow when a form was created without an IRD.

1. Select **Create IRD for Your Form**.
2. Upload the required HTML file.
3. Optionally upload one or more JavaScript files.
4. Select **Generate IRD**.
5. Review the detected form controls and validations.
6. Select **Export IRD** to download the generated workbook, or select **Generate Test Cases** to continue directly.

The IRD builder can inspect:

- Input controls
- Text areas
- Drop-down lists
- Radio buttons
- Checkboxes
- Date, number, email, URL, and file inputs
- Labels and placeholders
- Required attributes
- Minimum and maximum constraints
- Length constraints
- Pattern attributes
- Accepted file types
- JavaScript validation references
- Validation messages and event handlers where detectable

## Test Case Columns

- **ID:** Unique test-case reference number
- **Field:** Field, requirement, ticket, or functional item being tested
- **Priority:** Importance of executing the test case
- **Scenario:** Behavior or condition being verified
- **Steps:** Ordered actions required to perform the test
- **Test data:** Input, selection, file, or condition used during testing
- **Expected result:** Correct system response after test execution

The Excel test-case export also contains a blank **Solved** column for entering `Yes` or `No`.

## Export Options

### Excel Export

The Excel export includes:

- Styled first-row headings
- White heading text on a dark blue background
- Wrapped cell content
- Vertical test steps within a single cell
- Frozen heading row
- Column filters
- A blank `Solved` column

### PDF Export

The PDF export includes:

- Landscape layout
- Multi-page output
- Repeated table headings
- Wrapped test-case content
- Page numbering
- Black body text

The PDF intentionally excludes the `Solved` column.

## Privacy and Offline Processing

- Uploaded files are processed inside the browser session.
- The dashboard does not upload files to a server.
- No backend or database is used.
- No external JavaScript or CSS library is required.

## Mobile Support

The dashboard supports mobile and tablet use with:

- Responsive navigation
- Compact workflow buttons
- Touch-friendly upload controls
- Responsive modals
- Horizontally scrollable result tables
- Mobile-friendly PIN input
- Responsive Excel and PDF export controls
- Dark and light theme support

## Browser Compatibility

A recent version of one of the following browsers is recommended:

- Microsoft Edge
- Google Chrome
- Mozilla Firefox
- Safari

Some very old browsers may not support the browser APIs used for offline spreadsheet processing and file downloads.

## PIN Security Notice

The PIN gate is intended only for interface testing and light access control. Because this is a static client-side project, the PIN is present in `script.js` and can be viewed by anyone who has access to the source files.

Do not treat the PIN gate as production authentication. Real authentication requires a secure backend or identity provider.

## Current Test PIN

```text
280085
```

## Author

Made by Adarsh Maurya 🚀

