# Support Rescue Dogs Playgroup Automation via CCAS Compatibility Apps Scripts

The Playgroup team has made a fantastic contribution to the dogs' welfare and growth. Since restarting Playgroups in 2024 based on DPFL methodology, many great lessons for handlers and dogs have emerged.

This project brings those behind-the-scenes moving parts to life through the **DPFL Dashboard**, a suite of Google Sheets and Apps Script functions designed for animal shelter enrichment monitoring and storytelling.


---

## 🚀 Project Goals

### 1. **Shelter Impact**
Create a presentation device to show shelter leadership the impact of playgroups on kennel operations.  
**Key Feature**: Tracks which dogs work together using timestamped sessions to measure overlap in the yard.

### 2. **Adopter Awareness**
Generate a live slideshow to showcase yard activity for volunteers, staff, and the public.  
**Key Feature**: Dynamic Dog Profile Cards projected on monitors with real-time updates on yard participation.

---

## 📊 Sheets + Scripts Overview

| Feature | Description |
|--------|-------------|
| `outputPlaygroupOverlapHeatmap()` | Generates a conditional-format heatmap of dog overlaps based on session timestamps |
| `updateDogLog()` | Maintains historical dog session records including new and alumni tagging |
| `updateActivityLog()` | Aggregates daily yard activity: total dogs, minutes, and date keys |
| `highlightMostSocialDogsByWeek()` | Identifies top 3 most social dogs per week based on overlap duration |
| `removeActivityLogDuplicates()` | Removes duplicate rows from `ActivityLog` using `DateKey` with logic for PGDog priority |
| `YardIO Dashboard` | Real-time dashboard to monitor current dogs in the yard, time in yard, and queue state |

---

## 🧠 Design Concepts

- **No change to current PG workflow**: Tracks and analyzes behavior passively through timestamp overlap
- **Focus on duration**: More time in yard = better welfare. Script tracks total yard time with precision
- **Modular design**: Each function handles a specific enrichment or tracking workflow
- **Resilience against data drift**: Scripts adapt to column shifts and scope logic using named ranges

---

## 🔧 Technical Notes

- Built entirely in Google Sheets + Apps Script
- Relies on named ranges (`DogLog`, `DogHistoryLog`, `ProgressLog`, `PGyardList`, `Session`)
- Time zone-sensitive logging for session overlap
- Output location for dashboards is in `Stats` or `YardIO` tabs
- Uses `Utilities.formatDate()` and custom week logic

---

## 📎 Recommended Tools

- [GitHub + Clasp](https://github.com/google/clasp) for Apps Script version control
- Google Apps Script IDE for real-time debugging
- Windows `Win + .` shortcut for emoji in Sheets 💡

---

## 👏 Acknowledgements

Huge thanks to the PG Team for their heart, hustle, and high-fives in making this project possible. This dashboard is for you—and the dogs who count on your time, patience, and presence.

---

*For documentation feedback or technical collaboration, feel free to open a pull request or log an issue.*
