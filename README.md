# LS-LLaMA-NER-TR

Turkish Named Entity Recognition system using meta-llama's LLaMA 3.2B model with two distinct architectures:
1. Standard LLaMAForTokenClassification
2. Custom UnmaskingLlamaForTokenClassification

## Technologies Used
- **Core**: Python 3.8
- **NLP**: Transformers, Datasets
- **Optimization**: PEFT (LoRA) version 0.13.2 (will not work if higher)
- **Metrics**: scikit-learn
- **Model**: meta-llama/Llama-3.2-1b-Instruct

## Installation

```bash
# Clone repository
git clone https://github.com/your-org/LS-LLaMA-NER-TR.git
cd LS-LLaMA-NER-TR

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Linux/MacOS
# venv\Scripts\activate  # Windows

# Install dependencies
pip install -r requirements.txt

```

## Configuration

1. **Hugging Face Authentication** (Required for LLaMA access):
```bash
huggingface-cli login
``

## Dataset Format
```python
[
    {
        "tokens": ["İstanbul", "Büyükşehir", "Belediyesi", "'", ...],
        "tags": ["B-LOCATION", "I-LOCATION", "I-LOCATION", "O", ...]
    },
    ...
]
```

## License
Apache License 2.0 - See [LICENSE](LICENSE) for details