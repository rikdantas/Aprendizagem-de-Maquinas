# Prática 03
Essa prática será similar a prática 02, porém iremos aplicar a técnica de Naive Bayes nas bases resultantes da primeira prática.

Para ver as informações completas sobre a prática basta acessar o arquivo "Aula_Pratica_NB.pdf" que está disponível aqui no repositório.

As bases estão disponíveis no link: https://drive.google.com/drive/folders/1aqL9jJOSAXDsgoufgwPLSYuYexJPZRBx?usp=drive_link

## Desenvolvimento da prática
A prática foi toda desenvolvida no notebook [Pratica03_NB.ipynb](https://github.com/rikdantas/Aprendizagem-de-Maquinas/blob/main/IMD1101/Pratica_03/Pratica03_NB.ipynb). Nele iremos baixar as bases de dados, importá-las e depois aplicar a técnica de Naive Bayes para dois tipos diferentes de técnicas de treinamento e teste.
São elas o holdout 70/30 e o 10-fold CV (KFold). Também iremos variar o tipo do Naive Bayes (GaussianNB, MultinomialNB e ComplementNB). Os resultados foram salvos em um CSV e guardados na pasta [resultados](https://github.com/rikdantas/Aprendizagem-de-Maquinas/tree/main/IMD1101/Pratica_03/Resultados) desse repositório.

### Planilha
Assim como pedido na prática, foi construída uma planilha para analisar melhor a acurácia do modelo. A planilha pode ser acessada no link a seguir: https://docs.google.com/spreadsheets/d/1kg1E5vMxL9MJRXBRZGRFLOSzllpD9tzWDLpIU9FJvuM/edit?usp=sharing.

Diferente das outras práticas, não foi possível definir um dataset que se teve a maior acurácia com base na média dos três tipos de técnicas utilizados, pois o MultinomialNB e o ComplementNB não conseguem lidar com números negativos e as bases que foram aplicados
o PCA possuem números negativos.

Com isso, o experimento que apresentou o melhor resultado, olhando apenas individualmente, foi o PCA_CNN_VGG19_128_avg com a técnica 10-fold CV que apresentou uma acurácia de 74,3%.