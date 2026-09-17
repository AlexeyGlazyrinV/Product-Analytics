# Cookie Cats: Placement A/B Test

## Business context
Cookie Cats is a mobile puzzle game(Tacticle Entertainment). The game has "gates" - points where the player must wait or pay to continue. 
The product team proposed moving the gate from level 30 to level 40, hypothesizing that a longer free path would improve player retention.

## Question
Does moving the gate from level 30 to level 40 affect player retention?

## Data
90 189 players randomly assigned to qgate_30` (control) or `gate_40` (test).
Metrics: Retention D1 (returned next da), Retention D7 (returned after a week).
Source: [Kaggle - Mobile Games A/B Testing (Cookie Cats)](https://www.kaggle.com/datasets/mursideyarkin/mobile-games-ab-testing-cookie-cats)

## Method
- Chi-square test of independence (retention x version) for D1 and D7
- Two-proportion z-test as a cross-check
- 95% confidence intervals on retention rates

  ## Result
  | Metric | gate_30 | gate_40 | Relative change | p-value |
  |--------------------------------------------------------|
  | Retention D1 | 44.8% | 44.2% | -1.3% | 0.074 (not significant) |
  | Retention D7 | 19.0% | 18.2% | **-4.3%** | **0.0016(significant)** |
  Metric 	gate_30 	gate_40 	Relative change 	p-value 
Retention D1 	44.8% 	44.2% 	-1.3% 	0.074 (not significant) 
Retention D7 	19.0% 	18.2% 	-4.3%	0.0016(significant)



  ## Recomendation
  Do not move the gate to level 40. The change shows no upside and causes a statistically significant drop in weekly retention.
