# Operating Hours & 10,000-Hour Forecast Dashboard

An Excel-based monitoring and forecasting tool developed to track equipment operating hours and estimate when a required 10,000-hour operating milestone will be reached.

The project combines Excel, VBA automation, configurable operating schedules, planned downtime, and date-based forecasting into a practical monitoring and reporting tool.

> The complete working workbook, VBA source code, formulas, and calculation logic are intentionally not included in this public repository. This repository is presented as a portfolio case study.

---

## Project Overview

Operational milestone forecasting involves more than simply adding accumulated operating hours.

The expected completion date can change when:

- daily operating hours change;
- the number of operating days per week changes;
- planned shutdowns occur;
- maintenance periods are introduced; or
- new actual operating data becomes available.

This dashboard was developed to account for these changing conditions while preserving historical operating schedules and automatically recalculating the forecast.

---

## Dashboard

![Operating Hours Dashboard](screenshots/dashboard.png)

The dashboard provides a consolidated view of:

- latest actual operating date;
- cumulative actual operating hours;
- remaining hours to the 10,000-hour target;
- percentage progress toward the target;
- current operating schedule; and
- estimated 10,000-hour milestone completion date.

The forecast automatically recalculates when actual operating data, operating schedules, or planned downtime are updated.

---

## Workflow

```text
Actual Operating Data
        ↓
Data Import
        ↓
Cumulative Operating Hours
        ↓
Remaining Hours to 10,000
        ↓
Operating Schedule
        +
Planned Downtime
        ↓
Daily Forecast Calculation
        ↓
Estimated 10,000-Hour Date
        ↓
Dashboard
```

---

## Data Import Workflow

![Data Import](screenshots/data-import.png)

Actual operating-hour records can be imported from an external Excel source file using a VBA-assisted import workflow.

This reduces repetitive manual entry and allows the dashboard to be updated as new operating data becomes available.

The imported records are used to determine the latest actual operating date and calculate the cumulative operating hours achieved to date.

---

## Date-Effective Operating Schedule

![Operating Schedule](screenshots/operating-schedule.png)

The tool supports changes in operating conditions over time.

Each schedule entry can define:

- effective date;
- operating hours per day; and
- operating days per week.

A new operating schedule applies only from its effective date forward.

Previously completed periods retain the operating conditions that were applicable at that time. This prevents future schedule changes from altering historical calculations.

For example, the forecast can accommodate a transition from continuous operation to a reduced operating schedule without changing previously completed operating periods.

---

## Planned Downtime

Planned shutdowns and maintenance periods can be entered separately from the normal operating schedule.

During these periods, forecast operating hours are adjusted accordingly.

This allows the projected 10,000-hour milestone date to account for known future interruptions rather than assuming uninterrupted operation.

---

## Forecasting Logic

The forecasting model combines:

1. cumulative actual operating hours;
2. remaining hours required to reach 10,000 hours;
3. date-effective operating schedules;
4. operating hours per day;
5. operating days per week;
6. planned downtime periods; and
7. daily forecasted operating hours.

The model evaluates future operating dates until the remaining required operating hours reach zero.

The corresponding date becomes the estimated 10,000-hour milestone completion date displayed on the dashboard.

Exact formulas, VBA procedures, and detailed calculation logic are intentionally excluded from the public repository.

---

## Key Features

- Cumulative actual operating-hour tracking
- Automatic identification of the latest actual date
- 10,000-hour milestone monitoring
- Percentage progress tracking
- Automatic remaining-hours calculation
- Date-effective operating schedule changes
- Variable operating hours per day
- Variable operating days per week
- Planned shutdown and maintenance handling
- Dynamic milestone-date forecasting
- VBA-assisted data import
- Dashboard-based reporting
- User guidance within the workbook

---

## Workbook Structure

The complete working version contains dedicated worksheets for different parts of the workflow:

| Worksheet | Purpose |
|---|---|
| How to Use | User instructions and workflow guidance |
| Dashboard | Main monitoring and forecast view |
| Inputs | Core calculation inputs and current operating status |
| Import Data | Imported actual operating-hour records |
| Operating Schedule | Date-effective operating schedule configuration |
| Planned Downtime | Planned shutdown and maintenance periods |
| Forecast | Daily forecast calculation engine |

The complete macro-enabled workbook is maintained privately and can be demonstrated when appropriate.

---

## Tools & Technologies

- Microsoft Excel
- VBA
- Excel formulas
- Data validation
- Conditional formatting
- Date-based forecasting
- Automated Excel data import
- Dashboard design

---

## Portfolio Repository

This public repository contains documentation and selected screenshots of the completed project.

To protect the complete implementation, the following are intentionally not publicly distributed:

- macro-enabled working workbook (`.xlsm`);
- VBA source code;
- detailed formulas;
- forecast calculation engine; and
- source data files.

The repository is intended to demonstrate the project's functionality, design, workflow, and technical approach without distributing the complete reusable solution.

---

## Data Privacy

All screenshots and examples presented in this portfolio project use demonstration data.

No confidential company, client, project, or operational information is included.

---

## Author

Regina Grace

Mechanical Engineering • Project Controls • Data & Automation

---

© 2026 Regina Grace. All rights reserved.

This project is provided for portfolio demonstration and professional evaluation purposes. Reuse, redistribution, or commercial use of the project materials is not permitted without permission.