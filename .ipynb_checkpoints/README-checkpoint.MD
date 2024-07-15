---

## Optimizing Text Summarization Using Transformer Variants

### How to Use the Code
1. Unzip the file `liputan6_data.zip`.
2. Start running the code from `1_Data_Preparation_EDA_Preprocessing.ipynb`.
3. Proceed with files `2_final_Bert2Bert.ipynb`, `2_final_bert2gpt.ipynb`, `2_final_panggi_t5_model.ipynb`.

### Introduction
This project utilized a large-scale summarization dataset sourced from Liputan6.com, as used in the Koto et al. (2020) research. Liputan6.com covers diverse topics and events primarily in Indonesia, spanning a decade from October 2000 to October 2010.

Liputan6.com is an Indonesian online news portal established in August 2000, covering topics such as politics, business, sports, technology, health, and entertainment. As of the time of writing, Liputan6.com ranks 9th in Indonesia and 112th globally according to Alexa's website ranking.

### Problem
The challenge is to provide users with concise and informative summaries of news articles or larger texts, preserving key ideas and essential information.

### Solution
We employed pre-trained language models to generate text summarizations across the dataset using diverse transformer-based models.

### Business Metrics
- Revenue Growth
- Cost Reduction
- Customer Acquisition
- Time Saved
- Clarity and Readability

### ML Metrics
- Rouge1
- Rouge2
- RougeL
- RougeLsum

### Data Definition
The dataset comprises over 200,000 documents of articles and their summarizations collected over a decade—from October 2000 to October 2010—to create a large-scale summarization corpus, totaling 215,827 document–summary pairs.

Each data point includes:
- `id` - data ID
- `url` - news URL
- `clean_article` - cleaned news content
- `clean_summary` - abstractive summary
- `extractive_summary` - extractive summary

### Data Preprocessing

- **REMOVE “Liputan6. com, [teks]:” from the Text**
  Example: Liputan6. com, Jakarta:

- **REMOVE “day and date patterns” from the text**
  Example: Selasa (15/5)

- **REMOVE the format "(<Initial>/<Author Name> and <Author Name>)" from the text**
  Example: (ICH/Tris Wijayanto dan Agus Ginanjar)

- **REMOVE '[baca: ...]' from the Text**
  Example: [baca: Ledakan Bom Mewarnai Malam Pergantian Tahun….]

### Model Experimentation
- Bert2bert
- Bert2GPT
- T5

### Results

| Model     | Rouge1  | Rouge2  | RougeL  | RougeLsum |
|-----------|---------|---------|---------|-----------|
| BERT2BERT | 0.4029  | 0.2528  | 0.3642  | 0.4029    |
| BERT2GPT  | 0.4018  | 0.2562  | 0.3658  | 0.4018    |
| T5        | 0.3134  | 0.1622  | 0.2678  | 0.2680    |

---