# influenza-11M
Sequence to sequence model generating predicted evolution in the influenza genome. Trained soley on influenza B Yamagata-lineage and generalizes to influenza B Victoria-lineage.

![image](https://github.com/zac-webel/influenza-11M/assets/118777665/6b9fc254-d859-47e4-9b90-43da3de39ee5)


# About
This is my resarch capstone project in partnership with the Food and Drug Administration along with Georgetown University. The goal of the research is gain insights about the evolutionary nature of a viral genome through the lens of deep learning. An encoder-decoder model was selected for several reasons: 
* The ability to analyze the attention scores of the transformed input (base) sequence to understand what the attention mechanism deems as signal in the prediction.
* The ability to analzye a long sequence length (max_length = 2410 tokens)
* Simple architecture that can scale to millions of parameters while training under two hours

# Model
* Total params: 10,716,168
* Trained on Yamagata lineage ... tested on Victoria lineage
* Train (sparse_categorical_crossentropy): loss: 0.1610 - accuracy: 0.9602
* Test: loss: 0.2173 - accuracy: 0.9465
* Epochs: 1
* Batch size: 1
* Train time 4968s on Kaggle P100

# Inference 
* Encoder input: Gene from influenza B
* Decoder input: padded <start> sequence

<img width="1296" alt="Screen Shot 2023-07-10 at 9 05 36 PM" src="https://github.com/zac-webel/influenza-11M/assets/118777665/bd819368-2315-4b64-8b33-472cce78bd44">

 
