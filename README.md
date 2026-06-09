Build a professional full-stack Credit Risk Assessment Dashboard based on my machine learning project.

The backend model already exists in Python and predicts loan default probability using ensemble learning models (Bagging, Random Forest, Gradient Boosting, XGBoost, etc.).

I need only the frontend UI and API integration layer.

========================================================
PROJECT GOAL
========================================================

Create a modern fintech-style web application where a loan officer can:

1. Enter borrower information.
2. Submit the application.
3. Receive:
   - Default Probability
   - Risk Score (0-100)
   - Risk Category (Low / Medium / High)
4. View explanation of risk factors.
5. View portfolio-level analytics.

The design should look like a professional banking or fintech platform.

========================================================
TECH STACK
========================================================

Frontend:
- React
- TypeScript
- Tailwind CSS
- Shadcn UI
- Recharts

Backend API:
- FastAPI (assume API already exists)

========================================================
APP STRUCTURE
========================================================

Create the following pages:

--------------------------------------------------------
1. Dashboard
--------------------------------------------------------

Top KPI cards:

- Total Applications
- Average Risk Score
- High Risk Borrowers
- Default Rate

Charts:

- Risk Category Distribution
- Loan Purpose Distribution
- Default Probability Histogram
- ROC-AUC Model Comparison

Recent Applications Table:

Columns:
- Borrower ID
- Risk Score
- Default Probability
- Risk Category
- Status

--------------------------------------------------------
2. Credit Risk Prediction Page
--------------------------------------------------------

Loan Application Form

Fields:

- Credit Policy
- Purpose
- Interest Rate
- Installment
- Log Annual Income
- Debt To Income Ratio
- FICO Score
- Days With Credit Line
- Revolving Balance
- Revolving Utilization
- Inquiries Last 6 Months
- Delinquencies Last 2 Years
- Public Records

Submit Button

When submitted:

Call:

POST /predict

Response:

{
  "default_probability": 0.42,
  "risk_score": 42,
  "risk_category": "Medium Risk"
}

Display results inside premium analytics cards.

--------------------------------------------------------
3. Risk Analysis Page
--------------------------------------------------------

Show:

- Gauge Chart for Risk Score
- Risk Category Indicator
- Probability Meter

Color Scheme:

Green = Low Risk
Yellow = Medium Risk
Red = High Risk

--------------------------------------------------------
4. Explainability Page
--------------------------------------------------------

Show SHAP-style explanations.

Display:

Top Contributing Features

Example:

Interest Rate      +0.22
FICO Score         -0.18
DTI                +0.12
Income             -0.09

Use:

- Horizontal bar charts
- Feature impact cards

--------------------------------------------------------
5. Portfolio Analytics Page
--------------------------------------------------------

Charts:

- Risk Category Distribution
- Default Rate by Risk Category
- Average Risk Score
- Monthly Applications

Include:

- Interactive filters
- Search
- Export CSV Button

========================================================
DESIGN REQUIREMENTS
========================================================

Theme:

Professional Banking Dashboard

Inspired by:

- Bloomberg Terminal
- JPMorgan Analytics
- Goldman Sachs Internal Dashboards
- Stripe Analytics

Color Palette:

Primary:
#0F172A

Secondary:
#1E293B

Accent:
#3B82F6

Success:
#22C55E

Warning:
#F59E0B

Danger:
#EF4444

Design Requirements:

- Fully responsive
- Mobile friendly
- Dark mode
- Smooth animations
- Glassmorphism cards
- Professional typography
- Clean spacing
- Enterprise-level appearance

========================================================
BONUS FEATURES
========================================================

Add:

- Sidebar navigation
- User profile section
- Notifications panel
- Download PDF report button
- Export prediction history
- Loading skeletons
- Error handling
- Toast notifications

========================================================
DELIVERABLE
========================================================

Generate complete React + TypeScript codebase.

Include:

- Folder structure
- Components
- Pages
- Mock API integration
- Dummy data
- Tailwind configuration

The final application should look like a production-grade credit risk assessment platform used by banks and financial institutions.
