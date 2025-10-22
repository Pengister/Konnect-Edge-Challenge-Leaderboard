# Konnect-Edge-Challenge-Leaderboard
This is the Team leaderboard
# Team Leaderboard Challenge

This project is a live leaderboard for the "Konnect Edge Inter-Cluster Marathon Challenge." It uses Google Sheets as a database, Google Apps Script as a backend API, and GitHub Pages to host the frontend.

## Features

-   Live leaderboard that auto-sorts by highest earnings.
-   Progress bar for each team showing progress to the $5,000 goal.
-   4 medal milestones (🥉, 🥈, 🥇, 🏆) that activate as teams reach them.
-   Live countdown timer for the 30-day challenge.
-   Password-protected `admin.html` page to add new earnings to teams.

## Setup Instructions

### 1. Backend (Google Sheet & Apps Script)

1.  **Create Google Sheet:**
    * Create a new Google Sheet.
    * Rename the first sheet (tab) to `TeamData`.
    * Set up headers in row 1: `TeamName`, `CurrentEarnings`, `ColorHex`.
    * Add your 5 cluster names and their chosen colors (e.g., `#f44336`). Set `CurrentEarnings` to `0`.
    * Create a second sheet (tab) and name it `Config`.
    * In cell `A1` of the `Config` sheet, enter the start date: `October 20, 2025 10:00:00`.

2.  **Create Apps Script:**
    * Go to **Extensions > Apps Script**.
    * Copy the `Code.gs` script (from the previous instructions) into the editor.
    * **Important:** Change `'YOUR_SECRET_PASSWORD'` to your own strong password.
    * Save the script.

3.  **Deploy as Web App:**
    * Click **Deploy > New deployment**.
    * **Type:** Select "Web app".
    * **Execute as:** Select "Me".
    * **Who has access:** Select "Anyone".
    * Click **Deploy**.
    * Authorize the script when prompted.
    * **Copy the "Web app URL"**. You will need this for the next step.

### 2. Frontend (GitHub Pages)

1.  **Create Repository:**
    * Create a new public repository on GitHub (e.g., `konnect-challenge`).

2.  **Add Files:**
    * Create an `index.html` file and paste the code from this guide.
    * Create an `admin.html` file and paste the code from this guide.
    * Create this `README.md` file.

3.  **Paste URL:**
    * Open `index.html` and `admin.html` (either in GitHub or your local editor).
    * Find the line `const WEB_APP_URL = 'PASTE_YOUR_GOOGLE_SCRIPT_URL_HERE';`
    * Paste your copied Web app URL inside the quotes.
    * Commit and save the changes.

4.  **Enable GitHub Pages:**
    * In your GitHub repository, go to **Settings > Pages**.
    * Under "Branch," select your `main` (or `master`) branch and `/(root)` folder.
    * Click **Save**.
    * Your site will be live in a few minutes at `https://<YOUR_USERNAME>.github.io/<YOUR_REPO_NAME>/`.

Your leaderboard is now live! You can view it at the main URL, and the admin page will be at `.../admin.html`.
