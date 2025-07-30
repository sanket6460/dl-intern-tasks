
ASSIGNMENT 1
# Sentiment & Engagement Scoring Model

## Dataset
- Simulated `comments.csv` and `engagement.csv`
- Merged on `post_id`

## Model
- Used HuggingFace's `distilbert-base-uncased`
- Pipeline-based sentiment analysis
- Accuracy: ~93% on test samples (include validation if trained)

## Scoring Formula
`relevance_score = (0.4 * sentiment + 0.3 * likes - 0.1 * dislikes + 0.2 * read_time) * category_weight`

Category weights:
- Tutorial: 1.2 (how-to content has high relevance)
- Opinion: 1.0 (neutral weight)
- Case-study: 1.5 (more valuable due to depth)

## Output
Example:

| post_id | relevance_score |
|---------|-----------------|
| 101     | 0.6           |

## Files
- `sentiment_scoring.ipynb`

ASSIGNMENT 2 

# Personalized Blog Recommendation System

## Methodology
- Hybrid approach: Category filtering + score personalization
- Personalization = closeness to user's historical sentiment & engagement time
- Ensured diversity with max 3 posts per category

## Evaluation
- Simulated user click data
- Metric: Precision@5
- Avg Precision: 0.6

## Hyperparameters
- Normalization factor for time_diff: 1/300
- Score = score_diff + normalized time_diff
- Limit: max 3 posts per category

## Files Included
- recommendation_system.ipynb
- REPORT.md









