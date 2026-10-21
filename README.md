# 📊 Neo Designer Tracker

**Upload a project spreadsheet, see how every designer is performing.**

A browser-based dashboard that turns an Excel or CSV project report into workload charts, a designer leaderboard, a deadline calendar, and a filterable project table. It is built for design team leads who want a quick read on who handled what, and when.

🔗 **Live demo:** [neo designer performence tracker](https://samanway-koley.github.io/neo-designer-tracker/)

![Status](https://img.shields.io/badge/status-active-brightgreen)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3.3-7952B3?logo=bootstrap&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?logo=chartdotjs&logoColor=white)

---

<img width="2880" height="1670" alt="image" src="https://github.com/user-attachments/assets/a97d31e8-c0e5-4fc6-b641-b59a3518d770" />

---

## ✨ Features

- **Spreadsheet import** — Load `.xlsx`, `.xls`, or `.csv` reports straight in the browser; no server or upload step.
- **Summary metrics** — See total matching projects, solo-designer projects, team projects, and total involvement effort at a glance.
- **Designer leaderboard** — Ranks designers by project completion density, with a podium for the top three and a list for the rest. Switch between All Time, This Month, and This Week.
- **Workload charts** — Compare individual assignment volume and combined team split workload side by side.
- **Deadline calendar** — Browse month by month, with a project counter on each day and click-to-filter by date.
- **Flexible filtering** — Filter by year and month, or switch to a custom date range.
- **Team member pills** — Narrow every view to one designer with a single click.
- **Tabbed project table** — Switch between All Together, Combined Deadlines, and Individual Deadlines. The table shows project name, target deadline, final delivery date, designer, and developer, with 20 rows per page.
- **Access portal** — A login screen gates the dashboard before any data is shown.
- **Responsive layout** — The sidebar collapses on desktop and slides in on mobile, and charts resize to fit.

## 🖥️ How It Works

1. Open the app and sign in on the access portal with a User ID and password.
2. Upload an Excel or CSV tracking report from the sidebar. [SheetJS](https://sheetjs.com/) parses it client-side into an in-memory dataset.
3. Choose a filter mode: Standard (year and month) or Date Range (start and end date).
4. Optionally select a team member pill to focus on one designer.
5. The dashboard recalculates the summary cards, leaderboard, and charts from the filtered rows. Chart.js redraws the individual and combined workload charts.
6. Click a day on the deadline calendar to narrow the table to that date.
7. Switch tabs to view all projects, team-handled projects, or solo-handled projects, and page through the results.

All processing happens locally in the browser. Uploaded data is never sent to a server.

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Markup & logic | HTML5, vanilla JavaScript |
| UI framework | [Bootstrap 5.3.3](https://getbootstrap.com/) |
| DOM scripting | [jQuery 3.7.1](https://jquery.com/) |
| Spreadsheet parsing | [SheetJS (xlsx 0.18.5)](https://sheetjs.com/) |
| Charts | [Chart.js](https://www.chartjs.org/) |
| Typography | [Montserrat (Google Fonts)](https://fonts.google.com/specimen/Montserrat) |
| Hosting | [GitHub Pages](https://pages.github.com/) |

## 📁 Project Structure

```text
neo-designer-tracker/
├── index.html              # Entire app: markup, styles, and JavaScript
├── README.md               # Project documentation
└── .github/
    └── workflows/          # GitHub Actions workflow configuration
```

## 🚀 Getting Started Locally

There is no build step. The app is a single static HTML file, and all dependencies load from CDNs.

```bash
# Clone the repository
git clone https://github.com/Samanway-Koley/neo-designer-tracker.git
cd neo-designer-tracker

# Option 1: open directly in your browser
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows

# Option 2: serve it locally
python3 -m http.server 8000
# then visit http://localhost:8000
```

> ⚠️ An internet connection is required on first load, since Bootstrap, jQuery, SheetJS, Chart.js, and Google Fonts are loaded from CDNs.

> ⚠️ The login credentials are defined as plain strings in the client-side JavaScript. Treat the portal as a convenience gate, not real security, and don't upload sensitive data to a public deployment.

## 👤 Author

**Samanway Koley**

- GitHub: @Samanway-Koley
- LinkedIn: Samanway Koley
- Email: samanway.koley@gmail.com
