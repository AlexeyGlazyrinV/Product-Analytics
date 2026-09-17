# Player Behavior & Monetization: Hypothesis Testing

## Business context
A product team wants to know which player segment to prioritize for monetization campaigns -specifically, wether engagement level, game genre or in-game behavior patterns predict who becomes a paying player.

## Question
Which behavioral segments (engagement level, genre, session/activity patterns) are associated with in-game purchase conversion?

## Data
40 034 players
Metrics: EngagementLevel (Low/Medium/High), GameGenre, SessionsPerWeek, AvgSessionDurationMinutes, PlayerLevel, AchievementsUnlocked, PlayTimeHours, InGamePurchases (0/1)
Source: [Kaggle - Predict Online Gaming Behavior Dataset] (https://www.kaggle.com/datasets/rabieelkharoua/predict-online-gaming-behavior-dataset)

## Method
- Chi-square test: EngagementLevel x InGamePurchases
- Chi-square test: GameGenre x InGamePurchases
- Two sample t-test: behavioral metrics, paying vs non-paying players

## Result
| Hypothesis | Test | p-value | Supported |
| :--- | :---: | :---: | :---: |
| Engagement level predicts purchase | Chi-square | 0.225 | No |
| Genre predicts purchase | Chi-square | 0.123 | No |
| Behavioral metrics differ by purchase status | t-test (5 metrics) | all > 0.5 | No |

## Recommendation
None of the tested segments predict purchase conversion in this data.
Recommended agains engagement or genre-based targeting for monetization campaigns, and reframed the hypothesis space toward purchase-flow UX and pricing rather than player-behavior segmentation.
