# 🧬 ESM + ExoStack Integration

This repository integrates [ESM](https://github.com/facebookresearch/esm), EvolutionaryScale's protein language models, with the [ExoStack](https://github.com/Jitenderkumar2030/exostack) platform to enable scalable AI-driven protein analysis, inference, and deployment.

---

## 📁 Project Structure

```

ESM/
├── esm/              # ESM protein language model (submodule)
│   └── esm/          # Core ESM3 model components
├── exostack/         # ExoStack framework for orchestration
│   ├── exo\_agent/    # Custom agent with esm3\_executor
├── models/           # Pretrained / fine-tuned model artifacts
├── logs/             # Logs from training and inference
└── esm3env/          # Python virtual environment (not committed)

````

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone --recurse-submodules https://github.com/yourusername/ESM
cd ESM
````

> ⚠️ **Note:** The `esm/` folder is a Git submodule. Use `--recurse-submodules` to fetch it correctly.

---

### 2. Create and Activate a Virtual Environment

```bash
python3 -m venv esm3env
source esm3env/bin/activate
```

---

### 3. Install Required Dependencies

```bash
# ESM requirements
cd esm
pip install -r requirements.txt
cd ..

# ExoStack requirements
cd exostack
pip install -r requirements.txt
cd ..
```

---

### 4. Run ESM3 Integration via ExoStack

```bash
cd exostack
python exo_agent/esm3_executor.py
```

---

## 🚀 Features

* ⚡ ESM3-powered protein language modeling
* 🔁 Integrated inference pipeline with ExoStack agents
* 📦 Docker-ready setup
* 🌐 Scalable K8s-compatible microservices
* 📈 Model serving + logging

---

## 🧪 Testing

```bash
cd exostack
pytest
```

---

## 🧠 Example Use Case

You can modify `exo_agent/esm3_executor.py` to run predictions using ESM3 and route outputs via ExoStack’s pub-sub or task queue model.

---

## 📝 Contributing

Contributions welcome! Please open issues or PRs.

---

## 📄 License

* ESM code: [MIT License](esm/LICENSE.md)
* ExoStack: [MIT License](exostack/README.md)

