# influenza-11M
Sequence to sequence model generating predicted evolution in the influenza genome.

![image](https://github.com/zac-webel/influenza-11M/assets/118777665/6b9fc254-d859-47e4-9b90-43da3de39ee5)


# About
This is my resarch capstone project in partnership with the Food and Drug Administration along with Georgetown University. The goal of the research is gain insights about the evolutionary nature of a viral genome through the lens of deep learning. An encoder-decoder model was selected for several reasons: 
* The ability to analyze the attention scores of the transformed input (base) sequence to understand what the attention mechanism deems as signal in the prediction.
* The ability to analzye a long sequence length (max_length = 2410 tokens)
* Simple architecture that can scale to millions of parameters while training under two hours
