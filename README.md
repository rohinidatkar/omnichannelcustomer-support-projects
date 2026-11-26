# Omnichannel Customer Support Projects

Three notebooks that show how a customer support operation can be run and measured across **phone, email and chat**: a response playbook, a CRM-style case tracker with SLA and escalation rules, and a complaint analysis dashboard.

**Skills demonstrated:** voice, email and chat support, effective listening, CRM-style case logging, SLA tracking, escalation, complaint handling and root-cause analysis, Python, SQL-ready data, Excel and Power BI-ready output.

> **About the data:** the case tracker and complaint dashboard use **simulated data** (fixed random seeds), because real customer data cannot be shared. The simulation is designed to behave like a small service desk, so the logic and charts can be demonstrated. The numbers below illustrate the method and are **not real company results**.

## Projects

| # | Notebook | What it covers |
|---|---|---|
| 1 | `01_voice_email_chat_response_playbook.ipynb` | Five-stage response flow, scripts for voice, email and chat, empathy phrases, email etiquette, case-logging template with a completeness check |
| 2 | `02_crm_style_customer_case_tracker.ipynb` | Case logging, P1-P4 priorities, SLA timers, escalation matrix, SLA compliance and open cases past due |
| 3 | `03_complaint_analysis_dashboard.ipynb` | Complaints by category, channel and resolution time; recurring issues (Pareto); CSAT and repeat contacts; recommendations |

## Project 1: Response playbook

![Response flow](charts/response_flow.png)

## Project 2: Case tracker

Simulated results (1,500 cases over 90 days):

| Metric | Value |
|---|---|
| Total cases logged | 1500 |
| Closed | 1440 |
| Open or escalated | 60 |
| First-response SLA met (%) | 95.3 |
| Resolution SLA met, closed cases (%) | 92.0 |
| Average resolution time (hours) | 12.7 |
| Escalation rate (%) | 14.7 |
| Open cases already past SLA due time | 46 |

![SLA by priority](charts/sla_compliance_by_priority.png)
![Cases by channel and priority](charts/cases_by_channel_priority.png)
![Open cases past due](charts/open_cases_past_due.png)

## Project 3: Complaint analysis

Simulated results (2,000 complaints over 6 months):

| Metric | Value |
|---|---|
| Complaints analysed | 2000 |
| Average resolution time (days) | 3.2 |
| Median resolution time (days) | 2.4 |
| Average CSAT (1-5) | 3.67 |
| Repeat-contact rate (%) | 23.0 |

![Pareto](charts/complaints_pareto.png)
![Resolution time by category](charts/resolution_time_by_category.png)
![CSAT and repeat contacts](charts/csat_repeat_by_wait.png)

## How to run

```bash
pip install -r requirements.txt
jupyter notebook
```

Open any notebook and choose **Run All**. Charts are saved to `charts/` and the generated datasets to `data/`.

## Using real data

Replace the simulated data cell in notebooks 2 and 3 with a read of your CRM or complaint export (`pd.read_csv`). The columns used are listed in each notebook, and the analysis and charts run unchanged.
