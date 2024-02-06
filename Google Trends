# Data = Google Trends, BigQuery Public Data 

## What is the time frame of the dataset?

SELECT 
  min(week) as earliest_week, max(week) as latest_week
FROM
  bigquery-public-data.google_trends.top_terms

## List all the searched terms in alpahbetical order.
SELECT 
  term
FROM
  bigquery-public-data.google_trends.top_terms
GROUP BY term

## Which terms are ranked in the top 5?
SELECT
  *
FROM
  bigquery-public-data.google_trends.top_terms
WHERE
  rank <=5

## What are the minumum, maximum, and average scores of the top 5 searched terms?
SELECT
  min(score) as min_score, 
  max(score) as max_score,
  avg(score) as avg_score
FROM
  bigquery-public-data.google_trends.top_terms
WHERE
  rank <=5 

## Which terms were searched with a top 5 rank and a score over 20?
SELECT
  *
FROM
  bigquery-public-data.google_trends.top_terms
WHERE
  rank <=5 and score >=20

## Which of these terms were searched the most times?
SELECT 
  count(*) as Count, term
FROM
  bigquery-public-data.google_trends.top_terms
WHERE
  rank <=5 and score >=20
GROUP BY 
  term
ORDER BY 
  Count desc

## What terms were searched the most from the state of NY?
SELECT 
  count(*) as Count, term
FROM
  bigquery-public-data.google_trends.top_terms
WHERE
  dma_name like '%NY'
GROUP BY
  term
ORDER BY
  Count desc
