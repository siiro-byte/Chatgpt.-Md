# Unit Economics Review

## Purpose
Calculate and interpret the economics of a clearly defined business unit. Show revenue, variable costs, contribution, acquisition cost, retention/payback and break-even where the supplied data supports them; expose assumptions and sensitivity rather than fabricating precision.

## When to use
Use when evaluating pricing, customer or order profitability, acquisition efficiency, subscription economics, service margins, growth sustainability or break-even requirements.

## Required inputs
- Business model and unit to analyse (customer, order, booking, subscription, project, transaction or other)
- Period and currency
- Price/revenue per unit and discounts/refunds
- Variable costs attributable to the unit
- Acquisition spend and acquired customers, if CAC is required
- Repeat purchase, retention, churn or usage data, if lifetime value is required
- Fixed costs and capacity constraints, if break-even is required
- Source, date and definitions for each figure

## Instructions
1. Define the economic unit and analysis period. Ensure all figures use compatible time periods, currencies and denominators.
2. Create an input table with value, unit, period, source and status (actual, estimate, assumption or missing). Do not silently fill gaps.
3. Calculate net revenue per unit: gross price less discounts, refunds, taxes or pass-through amounts as appropriate to the business and accounting definition. State what is included.
4. Calculate variable cost per unit by listing each attributable cost, including payment fees, materials, fulfilment, commissions, delivery, support and other usage-linked costs where applicable.
5. Calculate contribution per unit = net revenue per unit − variable cost per unit. Calculate contribution margin = contribution per unit ÷ net revenue per unit, where net revenue is positive.
6. If acquisition data is supplied, calculate CAC = attributable acquisition spend ÷ number of new customers acquired in the same cohort/period. Explain channel attribution and avoid mixing spend periods with acquisition cohorts.
7. If retention/repeat data supports it, estimate customer lifetime value using a stated method and horizon. Show the retention, margin and discount assumptions; distinguish observed cohort value from a forecast.
8. Calculate CAC payback only when contribution over time and acquisition timing are known. State the payback period and assumptions.
9. Calculate break-even volume only when fixed costs and contribution per unit are known: break-even units = fixed costs ÷ contribution per unit. Explain limitations such as capacity, mixed products and step-fixed costs.
10. Build conservative, base and upside scenarios by varying explicit drivers such as price, conversion, repeat rate, variable cost or CAC. Do not disguise arbitrary assumptions as forecasts.
11. Run sensitivity analysis to identify which variables most affect contribution, payback and break-even. Highlight thresholds at which the model becomes unviable.
12. Interpret implications for pricing, acquisition, retention, fulfilment and scale. Explain where growth may worsen cash flow or service capacity.
13. List missing data and the next measurement needed to improve confidence.

## Expected output
- Unit definition and analysis period
- Input register with sources and data quality
- Revenue and variable-cost breakdown
- Contribution and contribution margin
- CAC, lifetime value and payback where calculable
- Break-even analysis where calculable
- Scenario and sensitivity analysis
- Commercial implications and risks
- Missing data and next measurement priorities

## Quality checks
- Unit, currency, period and denominators are consistent
- Formulas are shown and calculations reproducible
- Actuals, estimates and assumptions are separated
- No metric is calculated when required inputs are missing
- CAC and LTV definitions/cohorts are compatible
- Scenario drivers are explicit and plausible
- Negative contribution and cash-flow risks are not obscured
- Recommendations follow from the calculations and limitations

## Source
Original prompt, informed by management accounting and unit-economics analysis; no upstream prompt text reproduced.

## Testing notes
Scenario: An online seller reports KES 2,000 revenue, KES 1,250 variable costs and KES 30,000 fixed costs, but no acquisition or repeat-purchase data. Observed: Contribution is KES 750 (37.5%); CAC and LTV are withheld; break-even is 40 orders only if costs are complete and compatible. Result: PASS. Limitation: Tax, refunds and omitted costs need confirmation.

## Status
Tested