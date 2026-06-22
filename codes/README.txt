# Slowing down Early Stage Model Collapse in Language Models through Diversity-Enhancing Decoding

The code is used for reproducing the experiment of "Slowing down Early Stage Model Collapse in Language Models through Diversity-Enhancing Decoding".

The code is run in Google Colab with T4 GPU. "dataset.ipynb" is used to prepare Chinese Wikipedia datasets for the experiment. It will save the training, validation and test sets in the drive.

"main.ipnb" is used to run the experiments. It reads the datasets from the drive, and restores results in a "results" file in the drive after running the notebook.