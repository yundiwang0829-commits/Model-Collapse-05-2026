# Slowing down Early Stage Model Collapse in Language Models through Diversity-Enhancing Decoding

Coursework project containing the report, notebooks, datasets, and experiment results for reproducing the experiments.

## Structure

- `codes/`: Google Colab notebooks for dataset preparation and experiment execution.
- `dataset/`: train, validation, and test JSONL datasets.
- `results/`: generated examples and metrics.
- `XQTX8_Report.pdf`: coursework report.
- `CRediT contribution statement.docx`: contribution statement.

## Running the Notebooks

The notebooks are designed to run in Google Colab with a T4 GPU.

- `codes/dataset.ipynb` prepares the Chinese Wikipedia datasets and saves the train, validation, and test sets.
- `codes/main.ipynb` runs the experiments, reads the prepared datasets, and writes outputs to `results/`.
