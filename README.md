# 2026 NBA Draft Big Board — Statistical Model vs. Consensus

A data-driven lottery prospect ranking model built using 8 advanced metrics from the 2025-26 college season and 2026 NBA Combine. Compares statistical model output against consensus mock draft positioning to identify over and undervalued prospects.

📊 **[View Interactive Dashboard on Tableau Public](https://public.tableau.com/shared/KRNB98Q3Z?:display_count=n&:origin=viz_share_link)**

---

## Project Overview

Most NBA Draft coverage relies on subjective scouting reports and eye test rankings. This project builds a repeatable, data-driven alternative. I have created a weighted composite score for 20 potential lottery picks based on advanced statistical metrics and combine measurements.

The final ranking blends 70% statistical model output with 30% consensus mock draft positioning, then surfaces the biggest divergences between the two to identify prospects the market may be undervaluing or overvaluing.

---

## Methodology

### Metrics Used

| Metric | Weight | Why It Matters |
|--------|--------|----------------|
| RAPM (Regularized Adjusted Plus-Minus) | 28% | Strongest single predictor of NBA translation |
| eFG% (Effective Field Goal %) | 20% | True shooting efficiency accounting for shot type |
| Blk% + Stl% (Combined) | 20% | Two-way defensive impact and activity rate |
| AST/TO Ratio | 15% | Playmaking quality and decision making |
| USG% (Usage Rate) | 5% | Context for production volume |
| 3PA% (Three Point Attempt Rate) | 5% | Shot profile and fit in modern NBA spacing |
| Wingspan Ratio (Wingspan − Height) | 5% | Defensive versatility and length |
| Max Vertical (Combine) | 5% | Athleticism |

### Age Multiplier

Age is applied as a multiplier on the final composite score, thus rewarding younger prospects outperforming older competition:

- 18 years old → +10% boost
- 19 years old → +5% boost
- 20 years old → neutral
- 21 years old → −5% penalty
- 22 years old → −10% penalty

### Z-Score Normalization

All metrics are normalized to z-scores before weighting to ensure that statistics across different scales are mathematically comparable.

### Blended Final Ranking

Final Score = (Composite Z-Score × 0.70) + (Inverted Mock Rank × 0.30)

Consensus mock draft data sourced from NBA.com and nbadraft.net.

---

## Dashboard Features

- **Big Board** — full lottery ranking sorted by blended final score
- **Divergence Chart** — horizontal bar chart showing big board vs. consensus gap for each prospect (green = undervalued, red = overvalued)
- **Scatter Plot** — model rank vs. mock rank with diagonal reference line; prospects above the line are statistically undervalued
- **Individual Prospect View** — click any player to see their full metric breakdown relative to the group average

---

## Key Findings

- Defensive metrics (Blk%+Stl%) and RAPM together account for nearly half the composite weight, reflecting the modern NBA premium on two-way players
- Age multiplier meaningfully boosts younger prospects posting comparable production to older competition
- Rank Divergence column surfaces the biggest gaps between model output and consensus expectations

---

## Tools Used

`Google Sheets` `Tableau Public` `Z-Score Normalization` `Weighted Composite Modeling` `Sports Analytics`

---

## Data Sources

- [Hoop Explorer](https://hoop-explorer.com/?year=2025%2F26) — season stats
- [NBAdraft.net](https://www.nbadraft.net/nba-mock-drafts/#google_vignette) — mock drafts and athletic measurements

---

## About

Built by Nate Wright — psychology graduate and aspiring data analyst with a background in quantitative research and data analysis.
