# Market Basket Analysis with Apriori Algorithm

This Python project implements Market Basket Analysis using the Apriori Algorithm. The analysis is performed on a market dataset to discover associations between products purchased by customers. Additionally, the project utilizes the Apyori library for association rule mining and includes data visualization using Seaborn, Matplotlib, and WordCloud.

## Requirements

- Python 3.x
- Pandas
- Matplotlib
- Seaborn
- WordCloud
- Apyori

Install the required libraries using:

```bash
pip install pandas matplotlib seaborn wordcloud apyori
```


### Dataset

The dataset (market_data.csv) should be in the project directory. Ensure it has the necessary transaction data for market basket analysis.


## Usage

1. Clone the repository:

```bash
git clone https://github.com/your-username/market-basket-analysis.git
```

2. Navigate to the project directory:

```bash
cd market-basket-analysis
```


3. Run the script:

```bash
python market_basket_analysis.py
```
Adjust the file path in the script if your dataset is located elsewhere.


## Results

The script outputs association rules based on the specified parameters for minimum support, minimum confidence, minimum lift, and minimum length. Visualizations include a WordCloud showing the most popular items and a Seaborn count plot displaying the frequency of the most popular items.

## Parameters

- **min_support**:  Minimum support threshold for itemsets.
- **min_confidence**: Minimum confidence threshold for association rules.
- **min_lift**: Minimum lift threshold for association rules.
- **min_length**: Minimum number of items in an association rule.

## Visualizations

### WordCloud
**Caption:** Most popular items bought first by the customers.

### Frequency of Most Popular Items
**Caption:** Frequency of most popular items.




## Example

```python
association_rules = apriori(records, min_support=0.0045, min_confidence=0.2, min_lift=3, min_length=2)
association_results = list(association_rules)

# Print the first association rule
print("Rule: " + str(list(association_results[0][2][0][0])) + " -> " + str(list(association_results[0][2][0][1])))
print("Support: " + str(association_results[0][1]))
print("Confidence: " + str(association_results[0][2][0][2]))
print("Lift: " + str(association_results[0][2][0][3]))
```
Adjust the parameters based on your dataset and analysis requirements.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Apyori Library](https://github.com/ymoch/apyori) for providing a convenient implementation of the Apriori Algorithm.
- [Seaborn Library](https://seaborn.pydata.org/) for data visualization.
- [WordCloud Library](https://github.com/amueller/word_cloud) for creating WordCloud visualizations.

