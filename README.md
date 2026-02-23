# Copilot and Agent Adoption Report Generator

Turn your Power BI Copilot and Agent adoption PDF export into a beautiful, fully-populated, interactive single-page HTML report using Claude AI. No coding required.

## What This Is

This repository gives you everything you need to transform a raw Power BI PDF into a polished, interactive adoption report for stakeholders. The output is a single self-contained HTML file with:

- Executive Summary with live KPIs
- AI Maturity Stage assessment (Stages 1-5)
- Agent Adoption deep-dive with top agent leaderboard
- Teams and Power User rankings
- Copilot Chat usage insights
- Growth Opportunities and Recommendations
- 30-60-90 Day Action Roadmap

See copilot-adoption-example.html for a fully populated report built from a real Power BI export.

---

## Repository Contents

| File | Description |
|------|-------------|
| copilot-adoption-template.html | Start here. Blank HTML template with [placeholder] values |
| copilot-adoption-example.html | Fully populated example (real data, anonymised) |
| PROMPT.md | The complete Claude prompt - copy, paste, run |
| README.md | This guide |

---

## Prerequisites

| Requirement | Details |
|-------------|---------|
| Power BI report | The Copilot and Agent Adoption Power BI template exported as a multi-page PDF |
| Claude AI access | Any of: Claude.ai (browser), Claude Code CLI, or Claude Code extension for VS Code |
| A text editor | VS Code recommended - free at https://code.visualstudio.com |

---

## How to Run - Three Options

### Option A: Claude.ai (Browser) - Easiest

1. Open claude.ai in your browser
2. Start a new conversation
3. Attach your PDF - click the paperclip icon and upload your Power BI PDF export
4. Attach the HTML template - upload copilot-adoption-template.html from this repo
5. Copy the full prompt from PROMPT.md and paste it into the chat
6. Send - Claude will return the populated HTML
7. Copy the HTML from the response and save it as a .html file
8. Open in any browser

---

### Option B: Claude Code CLI - Most Powerful

Claude Code is the official Anthropic CLI that lets Claude read and write files directly on your machine.

#### Step 1 - Install Node.js
Download and install Node.js (v18 or later) from nodejs.org.

#### Step 2 - Install Claude Code

    npm install -g @anthropic/claude-code

#### Step 3 - Get an API Key
1. Go to console.anthropic.com
2. Sign in or create an account
3. Click API Keys then Create Key
4. Copy the key (starts with sk-ant-...)

#### Step 4 - Authenticate

    claude

On first run, Claude Code will prompt you for your API key. Paste it and press Enter.

#### Step 5 - Place your files
Put these two files in the same folder:
- Your Power BI PDF export (e.g., my-copilot-report.pdf)
- copilot-adoption-template.html (from this repo)

#### Step 6 - Run
Open a terminal in that folder, start Claude Code, and paste the full prompt from PROMPT.md.

---

### Option C: Claude Code Extension for VS Code - Best for Developers

#### Step 1 - Install VS Code
Download from code.visualstudio.com.

#### Step 2 - Install the Claude Code Extension
1. Open VS Code
2. Press Ctrl+Shift+X to open Extensions
3. Search for Claude Code (publisher: Anthropic)
4. Click Install

#### Step 3 - Open your project folder
In VS Code, go to File then Open Folder and select the folder with your PDF and HTML template.

#### Step 4 - Open Claude Code panel
Press Ctrl+Shift+P and type Claude Code then select Claude Code: Open.

#### Step 5 - Run the prompt
Paste the full prompt from PROMPT.md, update the file paths, and press Enter.

---

## The Prompt

The full prompt is in PROMPT.md. Before running it, update these two lines at the bottom:

    output the complete, fully populated HTML file html file: C:pathtoyourcopilot-adoption-template.html
    pbi pdf: C:pathtoyourpower-bi-export.pdf

Replace the paths with the actual locations of your files.

---

## Section to PDF Page Mapping

| HTML Section | PDF Source |
|---|---|
| Total Agent Users | Agent Active Users - page 1 or 3 |
| Total Agent Sessions | Sum of all agent sessions - Agents Activity table |
| Active Agents | Agents Health Check - page 6 |
| Organizations | Agent leaderboard unique departments |
| Weekly Sessions Per User | Combined Leaderboard KPI |
| Top Performing Agents | Agents Usage Trends chart - page 3 |
| Teams Leaderboard | Agent User Leaderboard - pages 4-5 |
| AI Maturity Stage | Inferred from adoption signals |
| Chat Usage | Unlicensed Chat pages 9-11 plus M365 Copilot pages 12-14 |
| License Prioritization | Copilot Unlicensed License Prioritization page |

---

## Tips for Best Results

- Export all pages - make sure your PDF includes all report pages (typically 12-14 pages)
- Use the date filter - set your Power BI date range before exporting
- Higher page resolution - use Export then PDF with full-page layout for cleaner text extraction
- Re-run anytime - update the PDF monthly and re-run the prompt to generate a fresh report

---

## Customisation

The HTML template is fully self-contained (no external dependencies). To customise:

- Colors: Edit the CSS variables in the style block at the top of the HTML
- Logo/branding: Add an img tag inside the .header div
- New sections: Duplicate any section block and update the nav link in the sidebar
- Export to PDF: Open the HTML in Chrome, press Ctrl+P, select Save as PDF

---

## Contributing

Pull requests are welcome for:
- Improvements to the HTML template
- A better version of the prompt
- Support for other Power BI report templates

---

## License

MIT - free to use, modify, and share.

---

Built with Claude Code by Anthropic. Template by @Fepilot (https://github.com/Fepilot)