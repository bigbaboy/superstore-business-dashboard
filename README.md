# Superstore Business Dashboard

A team academic dashboard for exploring **sales, profitability, customer behavior and returns** with Django and D3.js.

## Business questions

- Which countries, cities and products contribute the most sales?
- Do high-sales products also have strong profit margins?
- How do purchase frequency and average order value differ by customer segment?
- How are discounts and returns associated with commercial outcomes?

## Implemented views

The interface organizes Q1–Q13 and TQ1–TQ3 views. Chart modules cover country/city comparisons, product analysis, customer-segment summaries, purchase-frequency distributions, discount/profit comparisons and product returns. These are descriptive analyses; correlations do not establish that discounts or returns cause the observed profits.

## Repository structure

| Path | Purpose |
| --- | --- |
| `dashboard_app/templates/dashboard_app/index.html` | Dashboard navigation and chart containers |
| `dashboard_app/static/dashboard_app/js/` | D3.js chart modules |
| `dashboard_app/static/dashboard_app/data/Global_Superstore_cleaned_rfm.csv` | Prepared sales/customer dataset |
| `dashboard_app/static/dashboard_app/data/Return.csv` | Return records used by the return analysis |
| `dashboard_app/static/dashboard_app/data/People.csv` | Supporting dataset included in the repository |
| `dashboard_app/views.py` | Render the dashboard page |
| `myproject/` | Django project configuration |

## Run locally

```bash
git clone https://github.com/bigbaboy/-DV118-.git
cd ./-DV118-
python -m venv .venv
```

Activate the environment, then:

```bash
python -m pip install "Django>=5.1,<5.2"
python manage.py migrate
python manage.py runserver
```

Open `http://127.0.0.1:8000/`. This is a suggested local setup based on the source structure; a clean environment has not been tested for this documentation update.

Django serves the page and static assets. The D3 scripts load CSV files for analysis. `staticfiles/` contains collected assets; edit the source files in `dashboard_app/static/` rather than treating both copies as independent source implementations.

## Suggested exploration

1. Start with country or category sales summaries.
2. Compare sales with profit margin before identifying strong-performing products.
3. Inspect customer-segment and purchase-frequency views.
4. Review discount and return views as additional context.

## Limits and future work

- Data cleaning and RFM derivation are not fully reproduced by a separate preparation pipeline in this repository.
- Dataset-specific joins, denominators and missing values should be checked before using charts for decisions.
- No causal finding, production deployment or quantified business improvement is claimed.
- Further work: reproducible data preparation, metric definitions, automated aggregate checks and a documented team contribution breakdown.

**Context:** Academic team project. The dashboard's original page lists three student identifiers.
