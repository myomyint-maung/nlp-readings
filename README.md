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

| Problem  | The effects of fine-tuning on the underlying embedding space of BERT is relatively less understood because the research on those effects is restricted to a few studies that do not comprehensively examine the effects.  |
| :---  | :---  |
| Key Related Works  | 1. What happens to BERT embeddings during fine-tuning? (Merchant et. al., 2020) |
|   | 2. On the interplay between fine-tuning and sentence-level probing for linguistic knowledge in pre-trained transformers (Mosbach et. al., 2020) |
|   | 3. Investigating learning dynamics of BERT fine-tuning (Hao et. al., 2020) |
| Solution  | To provide a comprehensive understanding of how fine-tuning affects BERT, the authors of the paper propose a new methodology that compares the internal representations of the model before and after fine-tuning using experiments on five NLP tasks, which cover both syntactic and semantic predictions. They evaluate how fine-tuning affects different layers and heads of BERT as well as different NLP tasks.  |
| Result  | The study finds that fine-tuning impacts significantly on BERT's internal representations. It is observed that the spatial similarity between the traning and test sets for each representation decrease as a result of fine-tuning and that fine-tuning may not always improve performance. Additionally, it is discovered that fine-tuning does not cause arbitrary changes to the representations and that the adjustments of the internal representations are task-dependent.   |

## Assignment 4
### BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding (2018)
#### by Jacob Devlin, Ming-Wei Chang, Kenton Lee and Kristina Toutanova

| Problem  | Existing pre-trained language models are unidriectional and that imposes restrictions on the choice of pre-training architectures which could be sub-optimal or even harmful when applied to downstream NLP tasks.   |
| :---  | :---  |
| Key Related Works  | 1. Attention Is All You Need (Vaswani et al., 2017)  |
|   | 2. Deep Contextualized Word Representations (Peters et al., 2018)  |
|   | 3. Improving Language Understanding with Unsupervised Learning (Radford et al., 2018)  |
| Solution  | The authors of the paper propose a new approach to pre-trained language representations called Bidirectional Encoder Representations from Transformers (BERT) to resolve the constraints of unidirectionality in existing pre-trained language models. By pre-training on a big corpus of text using a masked language model (MLM) objective, which randomly masks some words and needs the model to predict them based on the surrounding context, BERT overcomes the context-dependent nature of language. Additionally, BERT uses a "next sentence prediction" task to train the model to comprehend the connections between sentences.  |
| Result  | BERT shows to be effective for both feature-based and fine-tuning approaches and outperforms existing state-of-the-art language models on various NLP tasks, including all General Language Understanding Evaluation (GLUE) tasks as well as question answersing and commonsense inference.   |
