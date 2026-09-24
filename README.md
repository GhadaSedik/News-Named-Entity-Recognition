# News Named Entity Recognition

## Overview

A Natural Language Processing project for identifying and analyzing named entities in news articles.

The project focuses on extracting entities such as:

* People
* Organizations
* Locations
* Other named entities

Two approaches are explored:

1. Model-based Named Entity Recognition using spaCy
2. Rule-based Named Entity Recognition using spaCy Matcher

## Dataset

CoNLL-2003 English Named Entity Recognition Dataset.

The dataset contains news text annotated with named entity labels.

The dataset is downloaded using KaggleHub.

## Technologies

* Python
* Pandas
* NumPy
* spaCy
* Matplotlib
* KaggleHub
* spaCy Matcher
* spaCy EntityRuler / NER Pipeline

## Named Entity Recognition

Named Entity Recognition (NER) is an NLP task used to identify important entities in text and classify them into predefined categories.

Examples include:

* Person names
* Organizations
* Locations
* Dates
* Miscellaneous entities

## Model-Based NER

spaCy's pre-trained English NER pipeline was used to automatically detect entities in news text.

The project uses:

* `en_core_web_sm`
* `en_core_web_md`

The extracted entities are analyzed and grouped by their entity labels.

## Rule-Based NER

A rule-based approach was also implemented using spaCy's `Matcher`.

A custom pattern was created to identify organization names followed by common organization suffixes such as:

* Inc
* Corp
* Ltd
* Company

Example:

```text
Apple Inc
Microsoft Corp
Google Company
```

This demonstrates how domain-specific rules can complement statistical NER models.

## Entity Analysis

The project analyzes the detected entities and provides:

* Extracted entities
* Entity labels
* Entity frequencies
* Entity counts
* Comparison between different spaCy models

## Visualization

The project includes visualizations of:

* Entity frequency
* Most common entity types
* Named entities extracted from the text

spaCy's visualization tools can also be used to highlight entities directly within the text.

## Model Comparison

Two spaCy English models are compared:

* `en_core_web_sm`
* `en_core_web_md`

The comparison demonstrates how different pre-trained models can produce different entity recognition results.

## How to Run

Install the required libraries:

```bash
pip install -r requirements.txt
```

Download the spaCy models:

```bash
python -m spacy download en_core_web_sm
python -m spacy download en_core_web_md
```

Then open:

`News_NER.ipynb`

Run the notebook cells sequentially.

The dataset will be downloaded automatically using KaggleHub.

## Project Structure

```text
News-Named-Entity-Recognition/
├── News_NER.ipynb
├── README.md
└── requirements.txt
```

## Note

The dataset is not included in this repository. It is downloaded automatically through KaggleHub.

This project demonstrates both statistical and rule-based approaches to Named Entity Recognition and how custom rules can be used to handle specific patterns in text.
