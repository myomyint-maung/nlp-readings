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

## Assignment 2
### Language Agnostic BERT Sentence Embedding (ACL 2022)
#### by Fangxiaoyu Feng, Yinfei Yang, Daniel Cer, Naveen Arivazhagan, and Wei Wang

| Problem  | BERT has proven to be an effective approach for generating monolingual sentence representations that capture semantic similarities and enable transfer learning through embeddings, but the application of BERT to create cross-lingual sentence embeddings has not been thoroughly examined.  |
| :---  | :---  |
| Key Related Works  | 1. Massively multilingual sentence embeddings for zeroshot cross-lingual transfer and beyond. (Mikel Artetxe and Holger Schwenk. 2019)  |
|   | 2. SentEval: An evaluation toolkit for universal sentence representations. (Alexis Conneau and Douwe Kiela, 2018)  |
|   | 3. Multilingual universal sentence encoder for semantic retrieval (Yang et. al., 2019)  |
| Solution  | This paper presents a new framework for generating sentence embeddings that are language-agnostic, meaning they can be used to represent sentences in any language. The authors propose a modification to the BERT model that enables it to enhance translation ranking performance through the integration of pre-training and dual encoder finetuning, resulting in a cutting-edge performance on bi-text mining. |
| Result  | The authors show that their method outperforms traditional language-specific models in several cross-lingual sentence classification and semantic similarity tasks. Their models outperform the previous state-of-the-art model, LASER by Artetxe and Schwenk, significantly by acheiving 83.7% bi-text retrieval accuracy over 112 languages to 83.7%, up from 65.5% achieved by LASER. Additionally, their embeddings are competitive in the SentEval sentence embedding transfer learning benchmark.  |

## Assignment 3
### A Closer Look at How Fine-tuning Changes BERT (ACL 2022)
#### by Yichu Zhou and Vivek Srikumar

| Problem  | ...  |
| :---  | :---  |
| Key Related Works  | 1.  |
|   | 2.  |
|   | 3.  |
| Solution  | ...  |
| Result  | ...  |
