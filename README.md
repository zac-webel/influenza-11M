# influenza-11M
Sequence to sequence model generating predicted evolution in the influenza genome.


# About
This is my resarch capstone project in partnership with the Food and Drug Administration along with Georgetown University. The goal of the research is gain insights about the evolutionary nature of a viral genome through the lens of deep learning. An encoder-decoder model was selected for several reasons: 
* The ability to analyze the attention scores of the transformed input (base) sequence to understand what the attention mechanism deems as signal in the prediction.
* The ability to analzye a long sequence length (max_length = 2410 tokens)
* Simple architecture that can scale to millions of parameters while training under two hours
