# Axure RP Build Guide — AI-Assisted Operator Monitoring Interface

Use this guide to recreate the core interaction in Axure RP so the portfolio claim is backed by a real Axure prototype.

## 1. Page setup
Create one page named `Operations Console`. Use a desktop canvas around 1440 × 1000. Build the sidebar, metric cards, chart area, AI Analysis card and audit trail as reusable components where practical.

## 2. Dynamic panel: SystemState
Create a dynamic panel named `SystemState` with three states:
- `Normal`
- `Warning`
- `Critical`

Each state should update: System Health, Active Alerts, AI Confidence, AI Analysis title, explanation, recommended action, severity badge and chart appearance.

## 3. Global variables
Create these variables:
- `severity` → Normal / Warning / Critical
- `confidence` → 96 / 87 / 94
- `responseStatus` → Ready / Pending / Acknowledged / Escalated / Dismissed

## 4. Scenario controls
Create three buttons: Normal, Warning and Critical.

OnClick for each button:
1. Set `severity` to the corresponding value.
2. Set `confidence` to its matching value.
3. Set panel state of `SystemState` to the matching state.
4. Set `responseStatus` to Ready for Normal or Pending for Warning/Critical.

## 5. Alert review panel
Create a second dynamic panel named `AlertReview` and place it above the page content as a modal.

Set it hidden by default. The `Review alert` button should:
- Show `AlertReview` with a fade animation.
- Populate confidence, severity and recommended action from the active state.

## 6. Conditional operator actions
Add `Dismiss`, `Acknowledge` and `Escalate` buttons.

Use OnClick cases:
- Dismiss → set `responseStatus = Dismissed`
- Acknowledge → set `responseStatus = Acknowledged`
- Escalate → set `responseStatus = Escalated`

Then hide the modal and update the audit-trail text. This is the key evidence of conditional interaction logic in Axure.

## 7. Adaptive views
Add at least one adaptive view around tablet width. Stack the metric cards and move the AI analysis below the chart. This demonstrates responsive GUI prototyping rather than a static wireframe.

## 8. What to capture for your portfolio
After building it in Axure, export or screenshot:
1. Normal system state.
2. Warning state.
3. Alert Review modal.
4. Interaction pane showing an OnClick conditional case.
5. Dynamic Panel state list (`Normal`, `Warning`, `Critical`).

Then replace the wording “Axure-ready Logic” on the portfolio with “Axure RP” and add one of these screenshots to the case study. At that point you can accurately describe this as hands-on Axure RP experience.
