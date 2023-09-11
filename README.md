# Segmentation - Recency, Frequency, Monetary

## Goal

Perform value-based segmentation on customer order data using a Recency, Frequency, Monetary model.

## Data

~40,000 entries with the following features:
* `customer_id`
* `revenue`
* `most_recent_visit`
* `number_of_orders`
* `recency_days`

## Analysis

RFM model was set up with 3 quantiles for each parameter:
* Recency: 1 (least recent) to 3 (most recent)
* Frequency: 1 (lowest frequency) to 3 (highest frequency)
* Monetary: 1 (least money) to 3 (most money)

Customers were then assigned a segment based on total RFM score:
* Superstar: 8-9
* High Potential: 5-7
* Low Relevance: 1-6

## Results

Summary statistics were generated for the segments.

|                | Recency | Frequency | Monetary |       |
|:--------------:|:-------:|:---------:|:--------:|:-----:|
|  **RFM_level** |   mean  |    mean   |   mean   | count |
|    Superstar   |   80.1  |    12.8   |   108.3  |  6375 |
| High Potential |  171.8  |    9.8    |   97.0   | 26445 |
|  Low Relevance |  306.6  |    7.1    |   78.5   |  7179 |
