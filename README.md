# 5DATA004C-DATA-SCIENCE-PROJECT-LIFECYCLE-_climate_risk_analytics

# Aethelgard Re Climate Risk Analytics

Data science pipeline for the 5DATA004C (Data Science Project Lifecycle) deferred/referred
individual coursework. Acting as a consultant for the fictitious reinsurance client
**Aethelgard Re**, this project investigates which global warming drivers most strongly
predict rising temperature anomalies, and what that implies for catastrophic risk pricing.

## Summary of findings

- All candidate warming drivers correlate strongly with the temperature anomaly (Pearson r
  0.89–0.94), but are also almost perfectly correlated with **each other** (VIF up to ~4.9×10¹⁰),
  confirming the severe multicollinearity the project brief anticipated.
- `ghg_emissions` (raw CO₂-equivalent emissions) was retained as the sole regression predictor,
  since the other drivers are statistically derived attributions of the same underlying series.
- A baseline linear model (trained 1950–2005, tested 2006–2021) achieves MAE ≈ 0.13°C but a
  **negative R²** on the test set — the model systematically underestimates 2006–2021 because
  warming has accelerated relative to the earlier fitted trend. This is reported as a genuine
  finding with direct actuarial implications (Aethelgard Re should not rely on flat linear
  trend lines to price catastrophic risk).
- The model projects the global temperature anomaly rising from ~0.71°C (2022) to ~0.85°C (2031),
  treated as a conservative lower bound given the acceleration finding above.

See the accompanying report for the full analysis, actuarial translation and individual
reflection.
