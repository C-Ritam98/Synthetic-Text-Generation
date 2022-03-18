# Synthetic-Text-Generation

This repository deals with implemnetaions of various Deep Learning based sentiment laden text generation.

VariationalSentimentTextGeneration_IMDB.ipynb file dela with implementing the concepts of text generation as mentioned in the paper by Bowman et al., 2015,
augmented with the concept of Highway networks (Srivastava, 2015) for better quality, gramatically coherent text.
I have used two different models for generating the the two sentiments (pos and neg), which are exact replica of each other except for the training data.
This implementatiopn also deals with bypassing the posterior collapse problem often faced by vae models for text generation, using beta-loss term, highway nets and removal of teacher forcing in decoder.
```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
