# Replicação do Artigo Toxic Language Dataset for Brazilian Portuguese (ToLD-Br)

Repositório para replicação dos experimentos do ToLD‑Br, um dataset com tweets em Português anotados de acordo com diferentes aspectos, como trabalho final para a disciplina de Aprendizagem de Máquina.

[Link para o artigo](https://arxiv.org/abs/2010.04543)

## Datasets

* `ToLD-BR.csv` — cada coluna tem valor de 0 a 3 representando o número de vezes que um exemplo foi sinalizado como tóxico.
* `ToLD-BR_alpha.csv` — anotações não agregadas por classe (valores 0 ou 1) com três colunas por classe.

[Dataset card no Hugging faces](https://huggingface.co/datasets/JAugusto97/told-br)

## Licença

O ToLD-Br está licenciado sob CC BY-SA 4.0 (arquivo `LICENSE_ToLD-Br.txt`).
O código disponível para reprodução dos experimentos está licenciado sob MIT (arquivo `LICENSE_code.txt`).

## Replicação de Experimentos Originais

* ```experiments/data/Nannotator.zip```: Datasets de treino, validação e teste usado nos experimentos, onde N é o número de flags que um exemplo precisa ser rotulado prara ser considerado um tweet tóxico.

### AutoML Baseline

* Descomprimir ```experiments/data/annotatorN.zip``` e executar ```experiments/automl.ipynb```.

### BERT

* Executar ```experiments/classification.ipynb``` no Google Collab com GPU habilitada.

---

## Novos experimentos

A replicação teve enfoque em realizar experimentos incluindo modelos clássicos de machine learning, além dos experimentos com BERT do trabalho original, junto de melhorias nas etapas de pré-processamento, como remoção de acentos, URLs, menções, hashtags, dígitos e pontuação.

### Modelos testados

* Regressão logística (Logistic Regression)
* Naive Bayes (MultinomialNB)
* Árvore de decisão (DecisionTreeClassifier)
* Random Forest
* K-Nearest Neighbors (KNN)
* Ensemble Voting com os modelos citados acima
