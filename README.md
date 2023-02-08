# NLP_Parler_Hate_Detection

<ins>Repository Contents
1. Jupyter notebooks:

    a.  __BERT_benchmark.ipynb__:    contains EDA and the training of the benchmark BERT model, trained solely on the originally annotated data.
    
    b.  __BERT_iterations.ipynb__:   contains the training of the 3rd iteration of the BERT model, trained on the originally annotated data, plus 3 auxiliary sets from the previous iterations.
    
    c. __Zero_Shot_train.ipynb__:   contains a zero-shot BART based classification model.

    d. __p_value_significance_evaluation.ipynb__: contains a paired t-test to compare the benchmark vs. our model.

2. Data folder with:

    a. CSV files: 
        i.  __parler_annotated_data.csv__:   the originally annotated data ()
        ii. __parler_unannotated_predictions_<ITERATION>.csv__: the zero shot perdiction of iteration ITERATION.
        iii. __test_predicted_proba_<ITERATION>.csv__: the fine-tuned BERT test perdictions for model BERT_<ITERATION>.

    b. Trained models.


<ins>Running the Code

__Download Large Files__
1. Download the models to ./Data/models from [here](https://drive.google.com/drive/u/0/folders/1hefKNzJ-mUCl8FjHa1OUgqDe6z0vQ5QW).
2. Download the Parler unannotated data files that we have used to ./Data/csv_files/ from [here](https://drive.google.com/drive/u/0/folders/1bSeyejnY0XAnd_7HeK3KM5cSszLBKSux).

__Create the Benchmark BERT Model__
1. Open BERT_benchmark.ipynb.
2. Tune the Presets section. Specifcally, keep ITERATION = 0 and set LOAD_MODEL_FROM_FILE = True (if LOAD_MODEL_FROM_FILE will be set to False, the model will be trained again from scratch).


_The following 2 sections should be run iteratively:_

__Run the Zero-Shot Model__
1. Open Zero_Shot_train.ipynb.
2. Tune the Presets section. Specifically, choose ITERATION = 0, 1 or 2, depending on the iteration.

__Create the Enriched BERT Model__
1. Open BERT_iterations.ipynb.
2. Tune the Presets section. Specifcally, set ITERATION = 1, 2 or 3, depending on the next iteration. If you are just evaluating the model.

