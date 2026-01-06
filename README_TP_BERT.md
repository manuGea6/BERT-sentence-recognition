# TP BERT — Sentiment (FinancialPhraseBank)

Ce dossier contient un TP complet (corrigé) pour entraîner / évaluer un modèle **DistilBERT** sur le dataset **FinancialPhraseBank**.

## Contenu
- `tp_bert_outputs_english_solution.ipynb` : notebook complet (chargement des données, split train/test, tokenization, modèle, entraînement avec Trainer, évaluation).
- `FinancialPhraseBank-v1.0/` : fichiers `Sentences_*.txt` (AllAgree / 75Agree / 66Agree).

## Données (fichiers Sentences_*.txt)
Chaque ligne est de la forme :
`<phrase>@<label>`
où `label ∈ {negative, neutral, positive}`.

## Exécution
1. Installer les dépendances :
```bash
pip install -r requirements.txt
```

2. Lancer le notebook :
```bash
jupyter lab
```
ou dans VS Code / Colab (en uploadant le dossier).

## Changer de split / dataset
Dans le notebook, modifiez la variable :
```python
filename = "FinancialPhraseBank-v1.0/Sentences_75Agree.txt"
```
vers `Sentences_66Agree.txt` ou `Sentences_AllAgree.txt`.

## Notes
- `FREEZE_PRETRAINED_MODEL=True` entraîne uniquement la tête de classification (plus rapide).
- Passez à `False` pour fine-tuner tout DistilBERT.
