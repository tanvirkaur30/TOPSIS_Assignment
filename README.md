## Methodology

The TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) method is a
Multi-Criteria Decision Making (MCDM) technique used to rank alternatives based on multiple
conflicting criteria.

The methodology followed in this project is explained step-by-step below.

### Step 1: Construction of Decision Matrix
The input dataset is read from a CSV file.  
- Rows represent different alternatives.
- Columns represent different decision criteria.
The first column contains the names of alternatives and is excluded from calculations.


### Step 2: Normalization of Decision Matrix
Since criteria may have different units and scales, normalization is required.
Vector normalization is used as follows:

rᵢⱼ = xᵢⱼ / √(Σxᵢⱼ²)

This step converts all criteria values to a comparable scale.


### Step 3: Weight Assignment
Each criterion is assigned a weight based on its importance.
The normalized matrix is multiplied by the corresponding weights to obtain the weighted
normalized decision matrix.


### Step 4: Identification of Ideal Best and Ideal Worst
For each criterion:
- If the impact is positive (+), the maximum value is taken as the ideal best and the
  minimum as the ideal worst.
- If the impact is negative (-), the minimum value is taken as the ideal best and the
  maximum as the ideal worst.


### Step 5: Distance Calculation
The Euclidean distance of each alternative from:
- Ideal Best solution
- Ideal Worst solution
is calculated.


### Step 6: TOPSIS Score Calculation
The TOPSIS score for each alternative is calculated using:

Score = Distance from Ideal Worst / (Distance from Ideal Best + Distance from Ideal Worst)

A higher score indicates a better alternative.


### Step 7: Ranking of Alternatives
Alternatives are ranked in descending order of TOPSIS scores.
The alternative with Rank 1 is considered the most preferred.

## Result Table

After applying the TOPSIS algorithm, a result table is generated in CSV format.
The result table contains the following columns:

- Alternative Name
- TOPSIS Score
- Rank

### Interpretation:
- TOPSIS Score indicates the relative closeness of an alternative to the ideal solution.
- Higher TOPSIS score implies better performance.
- Rank 1 represents the best alternative based on given criteria, weights, and impacts.

This table allows easy comparison of all alternatives and helps in selecting the most
appropriate option.
## Result Graph

A bar graph is plotted to visualize the TOPSIS scores of different alternatives.

### Graph Description:
- X-axis represents the alternatives.
- Y-axis represents the TOPSIS score.
- Each bar corresponds to the TOPSIS score of an alternative.

### Purpose of the Graph:
- Provides a visual comparison between alternatives.
- Helps in understanding relative performance at a glance.
- Clearly highlights the best and worst alternatives.

The alternative with the tallest bar has the highest TOPSIS score and is ranked as the best
choice according to the decision criteria.
## Web Application URL

The TOPSIS web application is deployed using Flask and exposed via ngrok.

🔗 **Live Web App:**  
https://epicondylian-shera-nonmonistically.ngrok-free.dev/

## Conclusion

The TOPSIS method provides a structured and objective approach for decision making involving
multiple criteria. This project successfully demonstrates the implementation of TOPSIS using
Python, including data preprocessing, score computation, ranking, and visualization.

The result table and graph together provide both numerical and visual insights, making the
decision-making process transparent and easy to interpret.













