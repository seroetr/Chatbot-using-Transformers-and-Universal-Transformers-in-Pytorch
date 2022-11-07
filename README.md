## Chatbot using Transformers and Universal Transformers in Pytorch
- This  repository helps you understand the practical implemantation of Chatbot using Transformer architecture  as a guidance to beginners.
- You can look at the paper of transformers from https://arxiv.org/abs/1706.03762, if you want theoretical knowledge.

- In order to train the Transformers,  `Cornell Movie-Dialog Corpus` dataset is used, which you can get via https://www.kaggle.com/datasets/rajathmc/cornell-moviedialog-corpus

### Transformers
- Transformers get rid of LSTM and its variances, replace them by transformers.
#### There are 3 key points for transformers
1) `Not sequential` like RNNs, all the input (example sentence) is fed once through the model, calculation is performed one time.
2) `Attention` is generated from the model's own input (self-attention).
3) More than one attention is generated each time (Multi-Head Attention)
- In training, there is no need for something called a timestep anymore, there is no sequence, everything is performed at once.

### Difference between Transformers and Universal Transformers
- Only modification that happens in universal transformers is basically the `recursion`.
- Rather than having N layers, we have N timesteps.
- For example, if we're using 6 layers for a transformers, then all of the parameters of the weights of these 6 layers are shared.
- We don't only have the positional encoding of the sequence, but we also have the `positional encoding of timesteps`.

