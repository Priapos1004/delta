Dear Students,

I would like to provide you with the details for the second portfolio task.

The deadline for the submission is the 10th of August. We ask you to submit one zip archive (.zip or .7z) including a Jupyter notebook (.ipynb) and a requirements file (.txt). Please also mention the required Python version at the top of the notebook.

You can find the data and hand in your submission via the corresponding module on the main moodle page, just below the previous task. You are provided with 2000 tweets about Bitcoin and a corresponding sentiment score (which is 1/True if positive and 0/False if negative). Your task is to perform sentiment analysis with various suitable approaches and compare their performance. The data are separated into a train set of 1500 tweets and a test set of 500 tweets – both of which are labelled.

The submission should contain the following:

1) Preprocess the text data appropriately for each model.
2) Apply a pre-trained transformer model of your choice for sentiment analysis.
3) Fine-tune a pre-trained transformer model using an existing transformer library (since this is computationally intensive, we recommend using models relying on knowledge distillation).
4) Benchmark the performance of the pre-trained transformer with the following models:
- sentiment dictionary of your choice.
- a TF-IDF vectorizer and a classifier of your choice.
- an RNN language classifier trained with your own embeddings as well as with pre-trained embeddings of your choice.
5) Evaluate all approaches using the labelled test dataset and metrics suitable for the task. This should result in a summary table at the end of the notebook!

Your choice of model and how well you train it are critical for the evaluation of your submission. We expect a well-designed pipeline with appropriate model selection, sound training, and careful evaluation. The notebook should run error-free. Your grade will be based on the implementation of the requirements listed above. While you don't have to provide any explanations or interpretations of results, your code should be well-documented.

Due to the proximity to the end of the semester, we have a hard submission deadline for this task. However, if you are unable to submit on time due to illness or other difficult circumstances, you may still submit late via email along with a doctor's note.


---

We should go a bit beyond the notebooks e.g. the pre-trained model we use. To extend the learned things from the tutorial.

We are allowed to use pre-trained models that were already fine-tuned in the direction of sentiment analysis for faster convergence in the fine-tuning.
