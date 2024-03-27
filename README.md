# Summary

### [Link to Jupyter Notebook](https://github.com/d-veli/bank_marketing_campaign/blob/main/bank_marketing_classifier.ipynb)

## Objective

In this notebook, we support the business objective of a Portugese banking institution in allocating resources effectively for marketing campaigns. 

Specifically the business wants to maximize successful bank term deposit subscriptions (hereafter referred to as the 'success rate') while minimizing contacts (phone calls) required. 

Put another way, the business is ideally able to better target clients who would be interested in a term deposit so that it can either:
1. deploy the same amount of contacts and yield more term deposits (bigger pot) or
2. deploy less contacts but still yield the same amount of term deposits (if resources are scarce).

## Baseline performance

The success rate baseline currently is:
- 8% when considering the entire campaign database (79.3K), and 
- 11% when naively predicting 'success' for every client, based on imported data (41.1K)

The second point highlights the imbalanced nature of the available data.

## Data Available

The business data available includes 41.1K marketing campaign contacts with clients. It includes features across bank client data, current and previous campaign attributes, and socialeconomic context. Importantly, it includes whether the client subscribed to a term deposit.

## Methodology and Results

From this data, we created the optimal model using the top features correlating to successful calls. The features include:

- **Contact communication type**,
- **Previous campaign outcome**,
- **Last contact month of year**, and
- **Socioeconomic context**:
    - employment variaton rate
    - consumer price index
    - euribor 3 month rate

With this model, we were able to achieve 84% prediction accuracy. 

This effectively allows the business to hit a success rate of 38% which is more than 4X the status quo of 8%. 

Importantly, the model also produces the largest list of prospective clients to contact. In improving economic conditions, this will help maximize the pot assuming resources are available.

## Bottom Line

For every 1000 client contact the business makes, this model can help yield 300 more successful bank term deposit subscriptions. 

While future improvements can further enhance results, this yields measurable benefits if the business adopts the predictive results.

## Next steps and recommendations

To continue improving our models, we propose the business make further data mining investments:
- In the short term: 
    - commit compute resources to allow inclusion of more features
    - tune hyperparameters across a broader parameter surface
- And long term: 
    - collect and include more impactful client specific features

Again, we recommend deploying the current model to yield business benefits right away while the above improvements can be made in the near future.