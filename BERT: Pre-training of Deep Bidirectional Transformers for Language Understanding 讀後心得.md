## BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding 讀後心得 (2023/06/08)  
這篇雖然已經出現很久了，正好現在想回頭尋找NLP相關的工作，但需要重新讀過這方面的論文，就從NLP的巨大變革BERT這篇論文開始吧!
經過Pretrain的Language Model是已被證明可以有效改善許多NLP的相關任務。BERT 是一個使用巨量資料Pretrain的Large Language Model(LLM)。
BERT內部使用的是Transformer的架構，其中使用的技巧則為Attention。BERT在Pretrain時使用了兩個技巧  
1. Masked Language Model  
  在預訓練時會隨機的去Masked一些字詞，模型要去預測原本的字詞是甚麼。目標是讓學出來的表示法可以結合上下文。這樣即可訓練出雙向的(從左至右與從右至左)Transformer (Bidirectional Transformer)。
2. Next Sentence Prediction
  在預訓練時也會同時判斷第二個句子是否在原始文本中與第一個句子連接
