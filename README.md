# nlp-readings
### Summaries of the papers I read for the NLP course at Asian Institute of Technology

## Assignment 1
### Token Dropping for Efficient BERT Pretraining (ACL 2022)
#### by Le Hou, Richard Yuanzhe Pang, Tianyi Zhou, Yuexin Wu, Xinying Song, Xiaodan Song, and Denny Zhou

| Problem  | Although BERT-type language models are very effective for several NLP tasks, the pretraining processes of those models are computationally expensive. Therefore, there is a need to make the pretraining costs of such models more efficient without degrading their performance on downstream tasks.  |
| :---  | :---  |
| Key Related Works  | 1. ALBERT: A lite BERT for self-supervised learning of language representations (Lan et. al., 2020)  |
|   | 2. Megatron-lm: Training multi-billion parameter language models using model parallelism (Shoeybi et. al., 2019)  |
|   | 3. Large batch optimization for deep learning: Training bert in 76 minutes (You et. al., 2020)  |
| Solution  | The paper identifies unimportant tokens, which are of smallest historical masked language modeling (MLM) losses, in each sequence, and drops them from a BERT model after the first few layers during training. But, the dropped tokens are eventually picked up by the last layer so that the model produces full-length seuqences at the end. |
| Result  | While the token-dropping approach reduces 25% of the pretraining cost of a BERT model, the model's performance on standard downstream tasks are not impaired at all.  |
