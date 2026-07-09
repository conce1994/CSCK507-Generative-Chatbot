# Dataset

This project uses the **Ubuntu Dialogue Corpus**, a large-scale conversational dataset containing approximately 930,000 two-person Ubuntu support conversations.

## Dataset Contents

The dataset consists of the following files:

- `dialogueText.csv`
- `dialogueText_196.csv`
- `dialogueText_301.csv`
- `toc.csv`

These files are **not included** in this repository because of their size.

## How to Obtain the Dataset

1. Download the Ubuntu Dialogue Corpus from the source provided by the project team or the official distribution. Dataset available here: https://www.kaggle.com/datasets/rtatman/ubuntu-dialogue-corpus
2. Place the downloaded CSV files inside this `data/` folder.

The folder should have the following structure:

```text
data/
├── dialogueText.csv
├── dialogueText_196.csv
├── dialogueText_301.csv
└── toc.csv
```

Once the files are placed in this directory, the notebooks can be executed without modification.
