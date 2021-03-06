# Synthetic-Text-Generation

This repository deals with implemnetaions of various Deep Learning based sentiment laden text generation.

***VariationalSentimentTextGeneration_IMDB.ipynb*** file deals with implementing the concepts of text generation as mentioned in the paper by Bowman et al., 2015,
augmented with the concept of Highway networks (Srivastava, 2015) for better quality, gramatically coherent text.
I have used two different models for generating the the two sentiments (pos and neg), which are exact replica of each other except for the training data.
This implementatiopn also deals with bypassing the posterior collapse problem often faced by vae models for text generation, using beta-loss term, highway nets and removal of teacher forcing in decoder.


***conditional_vae.ipynb*** implements how a single vae can be used to generate sentiment laden text from a single model, conditioned on the sentimnent. _z_ vector sampled from latent space is concatenated with the condition _c_, and _(z,c)_ fed to the decoder. Experiments show how the latent space is entangled and the generated sentences show mode collapse as a result of it.



***TSMH.ipynb*** is the implementation of the <a href="https://arxiv.org/pdf/2011.12334.pdf"> paper </a>, "Language Generation via Combinatorial Constraint Satisfaction: A Tree Search Enhanced Monte-Carlo Approach", with some subtle modifications. These modifications include introduction of multithreading for faster sentence generation (mcmc methods are pretty slow, as they require time to _burn in_) and modifying the Metropolis-Hastings condition slightly.

