# NLP_Parler_Hate_Detection

The repository contains:
1. Jupyter notebooks:
    a.  BERT_benchmark.ipynb:    contains EDA and the training of the initial BERT model, trained solely on the originally annotated data.
    b.  BERT_iterations.ipynb:   contains the training of the last iteration of the BERT model, trained on the originally annotated data, plus 3 sets of unannoated data                                  from the previous iterations. The notebook is tuned by its presets to load the model h5 file we've trained. If a manual run (fit) is                                      required, change the LOAD_MODEL_FROM_FILE and ITERATION preset values.
3. Data folder with CSV files and trained models.


To run the notebooks follow these steps:

__Download Large Files__
1. Download the models to ./Data/models from https://drive.google.com/drive/u/0/folders/1hefKNzJ-mUCl8FjHa1OUgqDe6z0vQ5QW.
2. Download the Parler data
