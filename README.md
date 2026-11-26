# GPA Atlas

**Academic Performance Intelligence & GPA Planning Dashboard**

GPA Atlas is a lightweight, browser-based academic planning tool designed to help university students track their academic performance, calculate their current GPA, simulate future results, and determine an efficient path toward a target graduation GPA.

The application runs entirely in the browser and requires no backend or installation.

## Features

### Academic Dashboard

- Track current GPA on both 4.0 and 10.0 scales
- Monitor completed and remaining GPA credits
- Visualize cumulative GPA progression by semester
- View semester averages and grade distribution
- Identify lower-performing courses
- Estimate graduation GPA based on planned grades

### Course & Grade Management

- View the complete academic transcript
- Add custom courses
- Edit grades and credits
- Set expected grades for future courses
- Assign course difficulty levels
- Search and filter courses by semester or status
- Exclude non-GPA courses from calculations

OJT is explicitly excluded from GPA calculations.

### GPA Forecasting

GPA Atlas provides a simulation environment for future academic performance.

Students can:

- Set a target graduation GPA
- Calculate the average GPA required for remaining credits
- Assign expected grades to individual courses
- Compare multiple academic scenarios
- Estimate future GPA on both 4.0 and 10.0 scales

The application includes three quick scenarios:

- Safe — 7.5/10
- Baseline — 8.5/10
- Ambitious — 9.5/10

### GPA Optimization

GPA Atlas includes a dynamic-programming-based optimizer that searches for a grade allocation capable of reaching a selected GPA target while minimizing a heuristic effort cost.

The optimization considers:

- Course credits
- Expected grades
- Course difficulty
- Target GPA
- Maximum desired grade

This helps identify which future courses provide the greatest potential impact on the final GPA.

> The optimizer is a planning model, not a prediction of actual academic performance.

## GPA Calculation

Current GPA on the 10-point scale is calculated using a credit-weighted average:

`GPA = Σ(Grade × Credits) / Σ Credits`

Future GPA simulations use the current official GPA together with projected grade points and remaining credits.

The 10-to-4 GPA conversion table is configurable because official conversion policies may differ between universities.

## Data & Privacy

GPA Atlas is **offline-first**.

Academic data is stored locally in the browser using `localStorage`.

No transcript or academic information is uploaded to a server.

The application supports:

- JSON backup
- JSON restore
- CSV export
- Reset to the original dataset

## Tech Stack

- HTML5
- CSS3
- Vanilla JavaScript
- SVG
- Browser LocalStorage
- Dynamic Programming

No frameworks, external backend, database, or build tools are required.

## Run Locally

Clone the repository:

```bash
git clone <your-repository-url>
cd <repository-name>
```

Open:

```text
index.html
```

in any modern web browser.

No dependency installation is required.

## Project Structure

```text
gpa-atlas/
├── index.html
└── README.md
```

The application is intentionally implemented as a single-page standalone HTML application.

## Important Notes

- OJT does not contribute to GPA calculations.
- Future courses without confirmed credits use estimated credits for simulation.
- GPA projections depend on the configured grade-conversion table.
- Retaken or replacement course policies are not automatically inferred.
- Forecasts and optimization results are planning estimates and should not replace official academic records or university regulations.

## Purpose

GPA Atlas was developed as a personal academic decision-support tool for analyzing current performance and planning future coursework using quantitative GPA scenarios.

The project focuses on turning academic transcript data into actionable information rather than displaying grades alone.

## License

This project is intended for educational and personal use.
