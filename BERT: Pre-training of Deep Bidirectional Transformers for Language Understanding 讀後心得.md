## BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding 讀後心得 (2023/06/08)  
這篇雖然已經出現很久了，正好現在想回頭尋找NLP相關的工作，但需要重新讀過這方面的論文，就從NLP的巨大變革BERT這篇論文開始吧!  

經過Pretrain的Language Model是已被證明可以有效改善許多NLP的相關任務。BERT 是一個使用巨量資料Pretrain的Large Language Model(LLM)。BERT內部使用的是Transformer的架構，其中使用的技巧則為Attention。BERT在Pretrain時使用了兩個技巧。  
1. Masked Language Model  
  在預訓練時會隨機的去Masked一些字詞，模型要去預測原本的字詞是甚麼。目標是讓學出來的表示法可以結合上下文。這樣即可訓練出雙向的(從左至右與從右至左)Transformer (Bidirectional Transformer)。
2. Next Sentence Prediction
  在預訓練時也會同時判斷第二個句子是否在原始文本中與第一個句子連接。
  
經過Pretrain之後，BERT會根據不同的NLP Task去進行Fine-tuning，論文中針對了11種不同的NLP Tasks去進行Fine-tuning並得到了最佳表現。  
其中包含General Language Understanding Evaluation(GLUE)、 Stanford Question Answering Dataset(SQuAD v1.1)、(SQuAD v2.0)和Situations With Adversarial Generations(SWAG)，詳細的數字結果可以去論文中察看。  

總結來說，BERT推出當時，因Language Models的Transfer Learning許多結果證明使用大量且非監督式的預訓練是語言理解系統不可或缺的一部分。且單向的架構已經被提出來了，BERT最特別的是其雙向(Bidirectional)的架構，可以讓表示法包含前後文的含意，使其富含更多的句子資訊。
