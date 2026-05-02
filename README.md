# LLM From Scratch

Ce dépôt accompagne la série **"Construire un LLM from scratch"** publiée sur LinkedIn.

L'objectif est de construire un Large Language Model depuis zéro, brique par brique, en implémentant chaque composant à la main. Pas de boîte noire. Pas de magie. Juste du code, des maths, et de la pédagogie.

---

## Structure du dépôt

```
llm-from-scratch/
├── notebooks/
│   └── 01_preprocessing.ipynb   # Tokenisation, BPE, Embeddings, Positional Embeddings
├── README.md
```

---

## Progression de la série

| Episode | Concept | Notebook |
|---------|---------|----------|
| 01 | Tokenisation — introduction et vue d'ensemble | — |
| 02 | Byte Pair Encoding (BPE) | — |
| 03 | Token Embeddings | — |
| 04 | Positional Embeddings | — |
| 05 | Preprocessing complet | `notebooks/01_preprocessing.ipynb` |
| 06 | Mecanisme d'attention | A venir |
| ... | ... | ... |

---

## Notebook 01 — Preprocessing

### Ce que ce notebook implémente

- **Chargement du corpus** : Wikipedia FR + CulturaX FR via Hugging Face (~1GB echantillonne)
- **Nettoyage du texte** : suppression HTML, URLs, normalisation des espaces
- **BPE from scratch** : implementation pedagogique de l'algorithme pas a pas
- **BPE optimise** : entrainement sur le grand corpus avec la librairie HuggingFace Tokenizers
- **Token Embeddings** : matrice d'embedding 50 000 x 512
- **Positional Embeddings** : version fixe (sinus/cosinus) et version apprise (GPT)
- **Pipeline complet** : texte brut → vecteurs enrichis prets pour le Transformer

### Prerequis

```bash
pip install datasets tokenizers torch transformers tqdm huggingface_hub
```

### Authentification Hugging Face

CulturaX est un dataset qui necessite une authentification. Au lancement du notebook, une invite te demandera ton token :

```
Entre ton token Hugging Face : ________
```

Pour obtenir un token :
1. Cree un compte sur https://huggingface.co
2. Va dans Settings → Tokens → New token (type Read)
3. Accepte les conditions d'acces sur https://huggingface.co/datasets/uonlp/CulturaX

### Environnement recommande

| Plateforme | RAM disponible | Recommande |
|------------|---------------|------------|
| Kaggle | 30 GB | Oui |
| Google Colab Pro | 25 GB | Oui |
| Google Colab gratuit | 12 GB | Limite |
| Local | Selon machine | Oui si 16GB+ |

---

## Suivre la série

Les articles sont publiés sur LinkedIn. Chaque episode explique un concept en langage clair avant que le code ne l'implémente.

---

## Auteur

Série construite et publiée en public — **Building in Public**.

---

## Licence

MIT
