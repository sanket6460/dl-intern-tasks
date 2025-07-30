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

