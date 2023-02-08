# NLP_Parler_Hate_Detection

<ins>Repository Contents
1. Jupyter notebooks:

    a.  BERT_benchmark.ipynb:    contains EDA and the training of the initial BERT model, trained solely on the originally annotated data.
    
    b.  BERT_iterations.ipynb:   contains the training of the last iteration of the BERT model, trained on the originally annotated data, plus 3 sets of unannoated data                                  from the previous iterations.

    Note: The notebook is tuned by default to load the h5 file we've trained. If a manual training (fit) is required, change the LOAD_MODEL_FROM_FILE and ITERATION in the Presets section.     
    
3. Data folder with CSV files and trained models.


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

