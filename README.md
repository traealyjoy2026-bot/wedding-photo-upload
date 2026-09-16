# Trae & Aly Wedding Photo Upload Wrapper

This static page embeds the Google Apps Script upload page in a third-party page.
The QR code should eventually point to the GitHub Pages URL, not directly to script.google.com.

## GitHub Pages setup
1. Create a PUBLIC GitHub repository named `wedding-photo-upload`.
2. Upload `index.html` to the repository root.
3. Open Settings > Pages.
4. Under Build and deployment:
   - Source: Deploy from a branch
   - Branch: main
   - Folder: /(root)
5. Save.
6. Wait for GitHub Pages to publish.
7. The expected URL for the GitHub user OfficerJ306 is:
   https://officerj306.github.io/wedding-photo-upload/

## Apps Script requirement
Your Apps Script doGet() must return the HTML output with:
.setXFrameOptionsMode(HtmlService.XFrameOptionsMode.ALLOWALL)

Because your HTML file is named lowercase `index`, use:
HtmlService.createHtmlOutputFromFile("index")

After any Apps Script change, deploy a new web-app version.
