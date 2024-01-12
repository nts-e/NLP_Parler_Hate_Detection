# NLP_Parler_Hate_Detection


The detection of hate speech on social media is challenging due to the difficulty in obtaining labeled data for training. This study proposes a semi-supervised learning approach using a Zero-Shot model to enhance hate speech detection. Focusing on Parler, a platform known for minimal moderation and increased hate speech, I fine-tuned a BERT-based classifier on a manually annotated dataset of around 10,000 posts. Through iterative steps, I incorporated an unannotated dataset of over 100 million posts, using a BART-based zero-shot model to identify hate against specific groups. The predictions from both models were combined to augment the annotated set, gradually improving the BERT classifier's precision without compromising recall. The approach successfully reduced false positive classifications in hate speech detection on Parler.


<h2>Repository Contents</h2>

1. Jupyter notebooks:

    a.  <b>BERT_benchmark.ipynb</b>:    contains EDA and the training of the benchmark BERT model, trained solely on the originally annotated data.
    
    b.  <b>BERT_iterations.ipynb</b>:   contains the training of the 3rd iteration of the BERT model, trained on the originally annotated data, plus 3 auxiliary sets from the previous iterations.
    
    c. <b>Zero_Shot_train.ipynb</b>:   contains a zero-shot BART based classification model.

    d. <b>p_value_significance_evaluation.ipynb</b>: contains a paired t-test to compare the benchmark vs. our model.

2. Data folder with:

    <ins>CSV files</ins> 
    
    1.  <b>parler_annotated_data.csv</b>:   the originally annotated data.
    
    2. <b>parler_unannotated_predictions_&lt;ITERATION&gt;.csv</b>: the zero shot perdiction of iteration ITERATION.
    
    3. <b>test_predicted_proba_&lt;ITERATION&gt;.csv</b>: the fine-tuned BERT test perdictions for model BERT_&lt;ITERATION&gt;.
    
    4. <b>parler_data000000000000.sampled50000.&lt;ITERATION&gt;.csv</b>: a subset of 10,000 unannotated Parler posts used in iteration ITERATION.

    <ins>Trained models</ins>:
    
    Initially the folder is empty. Please download the model files from [here](https://drive.google.com/drive/u/0/folders/1hefKNzJ-mUCl8FjHa1OUgqDe6z0vQ5QW).
    
    The folder contains:
    
    1.  <b>BERT_0</b>: the trained BERT benchmark model.
    
    2. <b>BERT_&lt;ITERATION&gt;</b>: the trained BERT model after iteration ITERATION.
    


<h2>Running the Code</h2>

__Download the Trained BERT Models__
1. Download the models to ./Data/models from [here](https://drive.google.com/drive/u/0/folders/1hefKNzJ-mUCl8FjHa1OUgqDe6z0vQ5QW).


__Run the Benchmark BERT Model__
1. Open BERT_benchmark.ipynb.
2. Run the notebook. The notebook defaults are set to use the pretrained models. You can train the model from scratch by Editing the Presets section. (LOAD_MODEL_FROM_FILE = False).


_The following 2 sections should be run iteratively:_

__Run the Zero-Shot Model__
1. Open Zero_Shot_train.ipynb.
2. Run the notebook. The notebook defaults are set to run iteration 0, the zero-shot classification on the benchmark model BERT_0, to create the prediction file parler_unannotated_predictions_0. Edit the Presets section to alter the ITERATION number.

__Run the Enriched BERT Model__
1. Open BERT_iterations.ipynb.
2. Run the notebook. The notebook defaults are set to run iteration 3, to create the final (3rd) BERT model BERT_3. Edit the Presets section to alter the ITERATION number.



__Run the Significance Test__
1. Open p_value_significance_evaluation.ipynb.
2. Run the notebook.    
