---
layout: post
title: Useful nlp snippets
---

# Using huggingface NER pipeline
```
from transformers import pipeline

nlp = pipeline("ner")

sequence = "Hugging Face Inc. is a company based in New York City. Its headquarters are in DUMBO, therefore very" \
           "close to the Manhattan Bridge which is visible from the window."

sequence = "I want two slices of pizza from Burger King and a chicken from Mac"

print(nlp(sequence))
# [{'word': 'Burger', 'score': 0.9974039793014526, 'entity': 'I-ORG'}, {'word': 'King', 'score': 0.9990913271903992, 'entity': 'I-ORG'}, {'word': 'Mac', 'score': 0.9886620044708252, 'entity': 'I-ORG'}]
```
