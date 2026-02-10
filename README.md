# TOPSIS Based Selection of Best Pre-trained Model for Text Summarization

## Objective
The objective of this project is to apply the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) method to identify the best pre-trained model for Text Summarization based on multiple evaluation metrics.

---

## Task Selected
**Text Summarization**  
(Assigned because roll number ends with **5**)

---

## Models Compared
The following pre-trained summarization models were considered:

- BART-Large-CNN  
- T5-Base  
- Pegasus-XSum  
- DistilBART
- led-base

---

## Evaluation Metrics
To compare models effectively, both quality and efficiency metrics were used:

| Metric | Preference |
|--------|------------|
| ROUGE-1 Score | Maximize |
| ROUGE-2 Score | Maximize |
| ROUGE-L Score | Maximize |
| Inference Time (ms) | Minimize |
|Compression ratio | Minimize |
|Semantic similarity | Maximize |

---

## Methodology

### Step 1: Create Decision Matrix
A performance table was created for all models based on the chosen metrics.

### Step 2: Normalize the Data
The decision matrix was normalized to remove scale differences between metrics.

### Step 3: Apply Weights
These weights sum up to 1.0, reflecting their relative importance in the TOPSIS calculation.

- ROUGE-1: 0.15
- ROUGE-2: 0.15
- ROUGE-L: 0.20 
- Inference Time: 0.15  
- Semantic similarity: 0.25
- Compression ratio: 0.20 

### Step 4: Identify Ideal Best and Ideal Worst
- Ideal Best: Maximum ROUGE scores, Minimum time and size  
- Ideal Worst: Minimum ROUGE scores, Maximum time and size  

### Step 5: Compute TOPSIS Scores
Distances from ideal best and worst solutions were calculated and TOPSIS score was computed.

### Step 6: Rank Models
Models were ranked based on TOPSIS score.

---

## Results

A final ranking table was generated:

- The model with the highest TOPSIS score is selected as the best summarization model.

---

## Result Graph
A bar chart was plotted to visualize the TOPSIS scores of all models.

---

## Conclusion
TOPSIS provides a structured approach to selecting the best pre-trained NLP model when multiple criteria such as accuracy and efficiency must be considered. The best model achieved the highest similarity to the ideal solution.

---
