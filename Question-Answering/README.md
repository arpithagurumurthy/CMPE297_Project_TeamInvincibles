**Question answering** is a language modeling task wherein the model is given a short paragraph or context about some topic and is asked some questions based on the passage. 

For training, we have used the **Stanford Question Answering Dataset (SQuAD) dataset** [https://arxiv.org/abs/1606.05250] which comprises 100,000+ Questions for Machine Comprehension of Text. It is a reading comprehension dataset consisting of questions posed by crowdworkers on a set of Wikipedia articles. 

Some histograms to visualize our SQuAD dataset:

<img src="https://github.com/arpithagurumurthy/CMPE297_Project_TeamInvincibles/blob/595b3021fd689e172a019d1bf45fd35c990f122b/Question-Answering/Screenshots/Answer-Length-Histogram.png">
<img src="https://github.com/arpithagurumurthy/CMPE297_Project_TeamInvincibles/blob/595b3021fd689e172a019d1bf45fd35c990f122b/Question-Answering/Screenshots/Context-Length-Histogram.png">
<img src="https://github.com/arpithagurumurthy/CMPE297_Project_TeamInvincibles/blob/595b3021fd689e172a019d1bf45fd35c990f122b/Question-Answering/Screenshots/Question-Length-Histogram.png">

The main model we have used for this task is Transformers. Specifically, we use the DistilBERT model, pretrained on Masked LM and Next Sentence Prediction, add a new head for question answering, and train the new model for our task.

<img src="https://github.com/arpithagurumurthy/CMPE297_Project_TeamInvincibles/blob/595b3021fd689e172a019d1bf45fd35c990f122b/Question-Answering/Screenshots/DistilBERT-Model.PNG">

**Training:**

<img src="https://github.com/arpithagurumurthy/CMPE297_Project_TeamInvincibles/blob/595b3021fd689e172a019d1bf45fd35c990f122b/Question-Answering/Screenshots/Training.PNG">


**Example:**
<img src="https://github.com/arpithagurumurthy/CMPE297_Project_TeamInvincibles/blob/595b3021fd689e172a019d1bf45fd35c990f122b/Question-Answering/Screenshots/QnA_Example.PNG">


**Tensorboard Logs:**

<img src="https://github.com/arpithagurumurthy/CMPE297_Project_TeamInvincibles/blob/595b3021fd689e172a019d1bf45fd35c990f122b/Question-Answering/Screenshots/Tensorboard-Logs.PNG">


**Evaluation:**

<img src="https://github.com/arpithagurumurthy/CMPE297_Project_TeamInvincibles/blob/595b3021fd689e172a019d1bf45fd35c990f122b/Question-Answering/Screenshots/Evaluation.PNG">


**Evaluation results:**

<img src="https://github.com/arpithagurumurthy/CMPE297_Project_TeamInvincibles/blob/595b3021fd689e172a019d1bf45fd35c990f122b/Question-Answering/Screenshots/Evaluation-results.PNG">
