# 📝 Text Summarizer

A simple and scalable end-to-end NLP project that performs automatic text summarization using the Hugging Face Transformers library and modern MLOps practices.

---

## 🚀 Features

- 📚 Summarizes large chunks of text
- 🤖 Uses pre-trained Transformer models (`t5-small`, `facebook/bart-large-cnn`, etc.)
- 📦 Packaged as a Python module for reuse
- ✅ Logging & YAML-based configuration management
- 📁 Training pipeline support (data ingestion, model training, evaluation)
- 🛠️ Modular, extensible, and production-ready structure

---

## 📂 Project Structure

```

Text-Summarizer/
├── .github/workflows          # CI/CD via GitHub Actions
├── config/                    # YAML config files
├── logs/                      # Log files
├── notebooks/                 # Jupyter experiments
├── research/                  # Initial experimentation scripts
├── src/
│   └── textSummarizer/
│       ├── **init**.py
│       ├── logging.py
│       ├── components/
│       └── utils/
├── tests/                     # Unit tests
├── main.py                    # Entry point
├── setup.py                   # Install script
├── requirements.txt
└── README.md

````

---

## ⚙️ Installation

1. **Clone the repository**  
```bash
git clone https://github.com/Sumit191105/Text-Summarizer.git
cd Text-Summarizer
````

2. **Create a virtual environment**

```bash
conda create -n textS python=3.10 -y
conda activate textS
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

4. **(Optional) Install in editable mode**

```bash
pip install -e .
```

---

## 🧪 Usage

### 🔹 Running the summarizer

```bash
python -m src.textSummarizer.main
```

or from within Python:

```python
from textSummarizer.pipeline.stage_01_data_ingestion import DataIngestionTrainingPipeline

pipeline = DataIngestionTrainingPipeline()
pipeline.main()
```

---

## 🧾 Example Output

**Input:**

> Alice and Bob had a meeting to discuss the quarterly earnings. They agreed that the revenue had increased by 20% and expenses had decreased significantly.

**Output:**

> Alice and Bob met and discussed improved earnings.

---

## 🧰 Tech Stack

* 🐍 Python 3.10
* 🤗 Hugging Face Transformers & Datasets
* 📜 YAML config
* 🧪 PyTest
* 📦 Box, Ensure
* 🚀 GitHub Actions (CI/CD ready)

---

## 📄 Configuration

All settings (paths, parameters) are managed via YAML in the `config/` directory.

---

## 🔍 Research & Training

Use the `notebooks/` and `research/` folders for fine-tuning and experiments.

You can load the SAMSum dataset like so:

```python
from datasets import load_dataset
dataset = load_dataset("samsum")
```

Or load a saved one:

```python
from datasets import load_from_disk
dataset = load_from_disk("samsum_dataset")
```

---


## 👨‍💻 Author

**Sumit Verma**
[GitHub Profile](https://github.com/Sumit191105)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
