# copilot-analytics

## What it does

Data Analyst: profiles CSV/XLSX exports, finds anomalies, duplicates, outliers and trends and explains them plainly.

Part of the **department-copilots** suite: local-only copilots where the employee provides the input, Claude analyses it on the machine, and the employee decides what to do. No CRM, NMS, email or system integrations.

## Install

```bash
claude plugin marketplace add sara-hamza/department-copilots
```

```bash
claude plugin install analytics@department-copilots
```

Drop in the export and ask "find anything unusual". Get back a profile of the data, its quality problems, the outliers and concentrations with the method stated, plain-English findings with caveats, and a chart-ready trend table.

| Command | Use when |
|---|---|
| `/analytics:profile <export>` | First look at a file: DATA PROFILE and DATA QUALITY (missing, duplicates, impossible values) |
| `/analytics:anomalies <export>` | Outliers, concentrations, week-over-week changes, correlations, each with the method used |
| `/analytics:findings <export or prior output>` | Numbered plain-English FINDINGS with evidence and caveats for a non-analyst reader |
| `/analytics:trends <export>` | Period-over-period comparison with the basis stated and a chart-ready table |

Requires `copilot-common` (its spreadsheet-reader profiler does the file reading).

Reference knowledge lives in `skills/data-analyst/references/`. Outlier fences and week-over-week thresholds there are sensible defaults marked `CUSTOMISE`.

The analyst explains what the data shows. It does not claim causes the data cannot support.
