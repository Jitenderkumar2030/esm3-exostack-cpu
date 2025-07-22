# ESM Project Integration

This project integrates EvolutionaryScale's ESM models and ExoStack to power AI-based protein analysis and predictions.

## Structure

- `esm/` - Contains the ESM protein language model.
- `exostack/` - Custom ExoStack framework for model deployment.
- `models/` - Pretrained and fine-tuned models.
- `logs/` - Training and inference logs.
- `esm3env/` - Virtual environment (not committed).

## Setup

```bash
git clone https://github.com/yourusername/ESM
cd ESM
python3 -m venv esm3env
source esm3env/bin/activate
pip install -r esm/requirements.txt
