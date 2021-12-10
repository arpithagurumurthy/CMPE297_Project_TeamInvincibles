**Question answering** is a language modeling task wherein the model is given a short paragraph or context about some topic and is asked some questions based on the passage. 

For training, we have used the **Stanford Question Answering Dataset (SQuAD) dataset** [https://arxiv.org/abs/1606.05250] which comprises 100,000+ Questions for Machine Comprehension of Text. It is a reading comprehension dataset consisting of questions posed by crowdworkers on a set of Wikipedia articles. 

The main model we have used for this task is Transformers. Specifically, we use the DistilBERT model, pretrained on Masked LM and Next Sentence Prediction, add a new head for question answering, and train the new model for our task.

