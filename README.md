# Classificador-Spam
Classificador de e-mails SPAM vs. não SPAM com análise exploratória, TF-IDF e Naive Bayes / Regressão Logística, em Jupyter Notebook (Python + scikit-learn).

# Estrutura:

```
spam-classifier/
├── data/
├── notebooks/
│   └── analise_spam.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

# O porquê de cada parte:

* **data/:** separa dado de código. Se o dataset for grande ou tiver restrição de licença, coloque a pasta no .gitignore e explique no README onde baixar.
* **notebooks/:** como a entrega é só o notebook, não precisa de src/ nem de módulos. Estrutura demais para um trabalho pequeno atrapalha mais do que ajuda.
* **requirements.txt:** quem clonar consegue reproduzir seu ambiente. Gere com pip freeze ou liste só o essencial (pandas, scikit-learn, matplotlib, jupyter).
* **.gitignore:** no mínimo .ipynb_checkpoints/, __pycache__/ e .venv/.

README.md, com poucas seções: o que o projeto faz, o dataset (fonte e tamanho), como rodar (pip install -r requirements.txt + abrir o notebook), principais resultados (F1 e matriz de confusão) e uma linha de contexto, como a disciplina.

# Especiais:

1. Palavras mais indicativas de spam (minha recomendação). Com Regressão Logística você olha os coeficientes do TF-IDF; com Naive Bayes, as probabilidades por classe. Mostre as 15 palavras que mais empurram para “spam” e as 15 para “não spam”. Por quê: prova que o modelo aprendeu algo coerente (como “free” ou “winner”) e não um artefato do dataset. É a parte que mais impressiona, custa uma célula de código e ainda alimenta a seção de análise.
2. Ajuste do limiar de decisão. Por padrão o modelo classifica como spam acima de 50% de probabilidade. Plote a curva precisão × recall e discuta qual limiar faz sentido. Por quê: mandar um e-mail importante para o spam costuma ser pior do que deixar um spam passar, e isso mostra que você pensou no problema real, não só na métrica.

# Dataset

- **Fonte:** [emails.csv](https://www.kaggle.com/datasets/ashutoshkun/emailscsv)
- **Conteúdo:** [nº de e-mails, colunas principais, proporção spam/não spam]
- **Observação:** o dataset não está incluído neste repositório. O notebook
  foi executado no Google Colab com o arquivo carregado a partir do Google
  Drive. Os resultados e gráficos estão salvos nas saídas do notebook.
