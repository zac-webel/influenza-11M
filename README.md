# influenza-11M
Sequence to sequence model generating predicted evolution in the influenza genome. Trained soley on influenza B Yamagata-lineage and generalizes to influenza B Victoria-lineage.

<img src="https://github.com/zac-webel/influenza-11M/assets/118777665/6b9fc254-d859-47e4-9b90-43da3de39ee5" alt="image" width="500" height="350" />

# Abstract
This research project introduces a sequence to sequence language model called influenza_11M. The model, a nucleotide level transformer, attends to an input sequence which is a gene in the Influenza B virus, and outputs a predicted evolved sequence which features several mutations: substitutions, insertions and deletions. The model is trained on less than 45,000 samples from the Yamagata lineage and is tested on 49,000 sequences from the Victoria lineage, scoring roughly 92% accuracy on a completely different lineage and more samples than it was trained on. This project represents the foundation and starting point for application of generative artificial intelligence in the domain of predicting viral evolution. 


# About
This is my resarch capstone project in partnership with the Food and Drug Administration along with Georgetown University. The goal of the research is to gain insights about the evolutionary nature of a viral genome through the lens of deep learning. An encoder-decoder model was selected for several reasons: 
* The ability to analyze the attention scores of the transformed input (base) sequence to understand what the attention mechanism deems as signal in the prediction.
* The ability to analzye a long sequence length (max_length = 2410 tokens)
* Simple architecture that can scale to millions of parameters while training under two hours

# Model
* Total params: 10,716,168
* Trained on Yamagata lineage ... tested on Victoria lineage
* Train (sparse_categorical_crossentropy): loss: 0.1829 - accuracy: 0.9529
* Test: loss: 0.3175 - accuracy: 0.9196
* Epochs: 1
* Batch size: 1
* Train time 5700 on Kaggle P100

# Inference 
* Encoder input: Gene from influenza B
* Decoder input: padded <start> sequence
* Output: Predicted evolved sequence, attention scores along the input sequence

<img width="1296" alt="Screen Shot 2023-07-10 at 9 05 36 PM" src="https://github.com/zac-webel/influenza-11M/assets/118777665/bd819368-2315-4b64-8b33-472cce78bd44">





 
