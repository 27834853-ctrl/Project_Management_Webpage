# 硬件项目计划管理看板

A single-file HTML project management dashboard for hardware development, featuring Gantt chart visualization, Excel import/export, and Chinese holiday management.

## Features

- **Gantt Chart** — Visual timeline with per-module color coding and today-line indicator
- **Task Management** — Add, edit, delete tasks with start/end dates, natural days, and workdays
- **Progress Tracking** — Per-task completion percentage with visual progress bars
- **Excel Export** — Exports a multi-sheet workbook: one summary sheet + one sheet per module, with NETWORKDAYS formulas linked to a holiday sheet
- **Excel Import** — Re-imports the exported workbook; module sheets take priority over the summary sheet
- **Holiday Management** — Configure Chinese public holidays and makeup workdays; affects all workday calculations
- **Batch Date Setting** — Set a start date for an entire phase and auto-cascade all task dates
- **Persistent Storage** — All data saved to `localStorage`; survives page refresh

## Usage

Open `index.html` directly in a browser — no server or build step required.

Or visit the live deployment:
**[https://27834853-ctrl.github.io/Project_Management_Webpage/](https://27834853-ctrl.github.io/Project_Management_Webpage/)**

## Workflow

1. Edit tasks via double-click or the **编辑** button
2. Export to Excel for sharing (`导出Excel`)
3. Update dates/progress in Excel, then re-import (`导入Excel`)
4. Use **批量日期** on a phase row to auto-fill all task dates from a single start date

## Tech Stack

- Vanilla HTML / CSS / JavaScript — zero dependencies
- [SheetJS (xlsx)](https://sheetjs.com/) — Excel read/write (loaded via CDN)
