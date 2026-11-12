# LSAT Tracker

A small, single-page web app for tracking LSAT practice test results: scores, trend, and score variance.

No build step, no dependencies, no account. It's one `index.html`.

## Features

- **Log each practice test**: date, PrepTest, scaled score (120–180), blind review score, Logical Reasoning and Reading Comprehension correct/total, and notes
- **Recent average and likely range**: the mean of your last *N* tests, ± one standard deviation
- **Consistency**: standard deviation for recent tests and for all tests
- **Trend**: the slope of a fitted line, in points per test
- **Blind review gain**: average BR minus timed score. A large gap usually points to timing, not understanding
- **Goal tracking**: points to your goal, how many recent tests hit it, and a countdown to test day
- **Charts**:
  - Score over time, with a rolling average and a ±1 SD band
  - LR vs RC accuracy
  - Score distribution
- **Backups**: export to JSON (re-importable) or CSV (for spreadsheets)

## Use it

Open `index.html` in a browser, or host it free with GitHub Pages:

1. Push this repo to GitHub.
2. Go to **Settings → Pages**, choose **Deploy from a branch**, then select `main` and `/ (root)`.
3. Your tracker will be live at `https://<your-username>.github.io/<repo-name>/`.

## Where your data lives

Your tests are saved in your browser's `localStorage`. They stay on your device and are never uploaded. Because of that:

- Data doesn't sync between browsers or devices.
- Clearing site data erases it.

Use **Data → Export backup (JSON)** now and then, and **Import backup** to restore your tests or move them to another device.

## Ideas for later

- Track missed questions by type (flaw, necessary assumption, etc.)
- Section timing
- Sync across devices with a small backend
