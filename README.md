# Pretraining-Yourself-Bert-From-Scratch
从头训练MASK BERT

In most cases, the Google pretrained BERT model or a further fine-tuning pretraining model base on it is enough. Howerver, sometimes maybe you want to train a BERT or a small BERT with your specific dataset.  This case is few but it does exist.
This repo provides a mask BERT pretraining code, which has not been implemented in the popular repo of BERT, such as [huggingface](https://github.com/huggingface/pytorch-pretrained-BERT).  Note that in this repo, the next sentence prediction is not jointed to pretraining.  
## How to start
- Preparing your dataset, train and dev, and place them into the data directionary
- Building a vocab as bert_vocab.txt. Note that the vocab should include [PAD] [UNK] [CLS] [SEP]
- Change the bert_config.json. Alternatively, you can change the model size to fit your memory.  Besides, you also should change the vocab_size in the config size to based on your vocab
- python run_pretraining.py