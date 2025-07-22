
# 🧬 ESM Project Integration

This project integrates [EvolutionaryScale's ESM models](https://github.com/facebookresearch/esm) with a custom-built **ExoStack** framework to deliver powerful AI-based **protein analysis and prediction tools**.

---

## 📁 Project Structure

| Path           | Description                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| `esm/`         | Contains the ESM (Evolutionary Scale Modeling) protein language models from Meta AI.  |
| `exostack/`    | Custom ExoStack framework for deploying models and handling inference APIs.           |
| `models/`      | Directory for storing pretrained and fine-tuned model checkpoints.                    |
| `logs/`        | Logs generated during training and inference.                                          |
| `esm3env/`     | Python virtual environment (not committed to Git).                                     |

---

## 🛠️ Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/ESM
   cd ESM
````

2. **Create and Activate Virtual Environment**

   ```bash
   python3 -m venv esm3env
   source esm3env/bin/activate  # On Windows: esm3env\Scripts\activate
   ```

3. **Install Dependencies**

   ```bash
   pip install -r esm/requirements.txt
   ```

4. **(Optional) Install Extra Tools for ExoStack**

   ```bash
   pip install -r exostack/requirements.txt
   ```

---

## 🚀 Usage

### Predict Protein Properties

You can use the CLI or ExoStack APIs to run predictions using ESM models.

```bash
cd esm
python examples/esm1b_toks.py --sequence "MGSSHHHHHHSSGLVPRGSH..." --model esm1b_t33_650M_UR50S
```

> Replace the sequence and model name with your specific use case.

---

## 🧪 Testing & Training

### Fine-tune on Custom Dataset

```bash
python train.py --data-dir ./your_dataset --output-dir ./models/fine_tuned_model
```

### Evaluate Model

```bash
python evaluate.py --model ./models/fine_tuned_model --test-set ./your_test_data.csv
```

---

## 🔐 Environment Variables

Create a `.env` file for sensitive configs (if needed by ExoStack APIs):

```
MODEL_DIR=./models
PORT=8000
LOG_LEVEL=INFO
```

---

## 🌐 Run ExoStack Server

Start the model inference server:

```bash
cd exostack
python server.py
```

Access locally at: `http://localhost:8000`

---

## 📦 Pretrained Models

* `esm1_t6_43M_UR50S`
* `esm1b_t33_650M_UR50S`
* `esm2_t36_3B_UR50D`

Refer to [ESM model zoo](https://github.com/facebookresearch/esm#available-models) for more details.

---

## 🧠 Features

* Fast tokenization and inference
* Plug-and-play API via ExoStack
* Easily extensible for new datasets
* Logs and metrics tracking
* Clean modular codebase

---

## ✅ Requirements

* Python ≥ 3.8
* PyTorch ≥ 1.10
* tqdm, biopython, flask (for APIs)

Install via:

```bash
pip install -r esm/requirements.txt
```

---

## 🙏 Credits

* [Meta AI - ESM](https://github.com/facebookresearch/esm)
* \[Your Name or Team]
* \[ExoStack - Internal Framework or Link if Open Source]

---

## 📄 License

This integration is under the MIT License. Refer to individual folders (`esm/`) for their respective licenses.

---

## 📬 Contact

For questions, contact:
📧 `your.email@example.com`
🐦 Twitter: [@yourhandle](https://twitter.com/yourhandle)

