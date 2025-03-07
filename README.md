# Fake News Detection

This repository contains a Jupyter Notebook for analyzing and processing a fake news dataset. The dataset is downloaded from Kaggle and processed using Python libraries such as Pandas, Transformers, and Torchmetrics.

## Dataset
The dataset is obtained from Kaggle's [Fake and Real News Dataset](https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset). It consists of two CSV files:
- `Fake.csv`: Contains fake news articles.
- `True.csv`: Contains real news articles.

## Installation
To run the notebook, install the required dependencies using the following command:

```bash
pip install torchmetrics datasets transformers kagglehub pandas
```

## Usage
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/fake-news-detection.git
   cd fake-news-detection
   ```
2. Run the Jupyter Notebook:
   ```bash
   jupyter notebook main.ipynb
   ```

## Notebook Overview
- Downloads the dataset from Kaggle.
- Loads and inspects the dataset using Pandas.
- Combines the fake and real news datasets and assigns labels (0 for real, 1 for fake).
- Fine-tunes a BERT model using the `transformers` library for fake news classification.

## Fine-Tuning with Transformers
The notebook uses the `transformers` library to fine-tune a `BERT` model for sequence classification:

1. **Loading the Pretrained Model and Tokenizer:**
   ```python
   from transformers import AutoModelForSequenceClassification
   from transformers import AutoTokenizer, DataCollatorWithPadding

   checkpoint = "bert-base-uncased"
   tokenizer = AutoTokenizer.from_pretrained(checkpoint)

   model = AutoModelForSequenceClassification.from_pretrained(checkpoint, num_labels=2)
   ```
2. **Setting Up the Optimizer:**
   ```python
   from transformers import AdamW

   optimizer = AdamW(model.parameters(), lr=1e-5)
   ```
3. **Learning Rate Scheduler:**
   ```python
   from transformers import get_scheduler

   num_epochs = 1
   num_training_steps = num_epochs * len(train_dataloader)
   lr_scheduler = get_scheduler(
       "linear",
       optimizer=optimizer,
       num_warmup_steps=0,
       num_training_steps=num_training_steps,
   )
   print(num_training_steps)
   ```

## License
This project is licensed under the MIT License.

