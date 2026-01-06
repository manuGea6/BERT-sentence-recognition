# TP BERT — Financial Sentiment Classification (Financial PhraseBank)

## Objectif
Fine-tuner un modèle de type BERT (ex. DistilBERT) pour classifier le sentiment de phrases financières en **positive / neutral / negative** à partir du dataset **Financial PhraseBank** (fichiers `Sentences_*Agree.txt`).

## Contenu
- Notebook principal : `tp_bert_outputs_english_solution.ipynb`
- Données : `FinancialPhraseBank-v1.0/`
  - `Sentences_66Agree.txt`
  - `Sentences_75Agree.txt`
  - `Sentences_AllAgree.txt`
- `requirements.txt`

## Structure
.
├── tp_bert_outputs_english_solution.ipynb
├── FinancialPhraseBank-v1.0/
│ ├── Sentences_66Agree.txt
│ ├── Sentences_75Agree.txt
│ └── Sentences_AllAgree.txt
└── requirements.txt


## Installation
```bash
python -m venv .venv
# Linux / macOS
source .venv/bin/activate
# Windows (PowerShell)
# .venv\Scripts\Activate.ps1

pip install -r requirements.txt
```

### Lancement

  Ouvrir le notebook et exécuter les cellules dans l’ordre :
  
  Chargement + parsing des fichiers Sentences_*
  
  Split train/val/test
  
  Tokenization
  
  Fine-tuning (Transformers)
  
  Évaluation (Accuracy, F1 macro)
  
  Inference sur exemples

### Notes

  Les fichiers Sentences_*Agree.txt servent de support : ils contiennent des phrases annotées.
  
  Le notebook est compatible CPU (plus lent) et GPU (recommandé).

### Auteur

  Manuela Fongang-Kengne
