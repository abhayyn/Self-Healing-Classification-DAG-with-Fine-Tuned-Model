# Self-Healing-Classification-DAG-with-Fine-Tuned-Model
# Self-Healing Classification DAG with Fine-Tuned Model

An implementation of a self-healing classification pipeline using:
- Fine-tuned DistilBERT model for sentiment analysis
- LangGraph-based workflow with fallback mechanism
- Optional zero-shot classifier backup model

## Features

- Automatic fallback to user clarification when confidence is low
- Optional backup model integration
- Comprehensive logging
- Clean CLI interface

## Setup

1. Clone the repository:
```bash
git clone https://github.com/yourusername/self-healing-classification-dag.git
cd self-healing-classification-dag

##Example Workflow

$ python src/classify.py
Enter text to classify: The movie was painfully slow and boring.

[InferenceNode] Predicted label: Positive | Confidence: 54.0%
[ConfidenceCheckNode] Confidence too low. Triggering fallback...
[FallbackNode] I thought this was Positive, but I'm not sure. Was this actually Negative? (yes/no)
Your answer: yes

Final Label: Negative (Corrected via user clarification)
