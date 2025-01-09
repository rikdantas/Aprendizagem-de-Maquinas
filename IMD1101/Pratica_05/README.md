# Prática 05
A prática 05 que é relacionada com comitê de classificadores. A base que vai ser usada é a PCA_CNN_VGG19_128_avg que mostrou o melhor desempenho nas últimas duas práticas.

Para ver as informações completas sobre a prática basta acessar o arquivo "Aula_Pratica_Comites.pdf" que está disponível aqui no repositório.

A base utilizada está disponível no link: https://drive.google.com/drive/folders/1aqL9jJOSAXDsgoufgwPLSYuYexJPZRBx?usp=drive_link

## Desenvolvimento da prática
A prática foi toda desenvolvida no notebook [Pratica05_Comitê.ipynb](https://github.com/rikdantas/Aprendizagem-de-Maquinas/blob/main/IMD1101/Pratica_05/Pratica05_Comit%C3%AA.ipynb).
Nele iremos baixar a bases de dados, importá-la e depois aplicar diferentes técnicas de comitê de classificadores.

## Perguntas
Durante cada etapa da prática, vão sendo feitas perguntas, que serão respondidas a seguir:

1. **Compare as tabelas de bagging padrão e bagging com seleção de atributos, analisando seus resultados e responda a seguinte pergunta: Qual o impacto da seleção de atributos no Bagging?**

        Comparando os resultados obtidos no meu experimento, foi possível observar que na bagging com seleção de atributos houve uma melhora na acurácia dos modelos Árvore de Decisão e KNN, enquanto houve uma piora na acurácia dos modelos Naive Bayes e MLP. Portanto, não foi possível concluir nada com relação ao impacto da seleção de atributos.

2. **Compare a tabela do Boosting com as linhas 1 e 3 do Bagging padrão e responda a seguinte pergunta: Quem forneceu a maior acurácia, Bagging ou Boosting?**

        O boosting apresentou uma melhora significativa e um aumento da acurácia do modelo para todos os casos testados.

3. **Compare a tabela do Random Forest com os resultados do Bagging e Boosting e responda a seguinte pergunta: Qual comitê de classificadores está fornecendo a melhor acurácia? Explique sua resposta.**

        Em relação ao bagging, o random forest apresentou uma acurácia melhor em média, mas comparado ao boosting, ainda se manteve pior em questão de acurácia. Logo, até o momento, o comitê que está fornecendo uma maior acurácia é o Boosting.

4. **Compare a tabela do Voting com os resultados do Bagging, Boosting e Random Forest e responda a seguinte pergunta: Qual comitê de classificadores está fornecendo a melhor acurácia? Explique sua resposta.**

        O voting obteve desempenho bem parecido com o random forest, ou seja, foi superior ao bagging, mas continuou atrás, no que diz respeito a acurácia, do boosting.

5. **Compare a tabela do Stacking com os resultados do Bagging, Boosting e Random Forest e responda a seguinte pergunta: Qual comitê de classificadores está fornecendo a melhor acurácia? Explique sua resposta.**

        O Stacking foi o comitê que apresentou a melhor acurácia de todas. Foi o único que apresentou maiores valores de acurácia em testes individuais comparado ao boosting, além de também apresentar uma maior média.
        
## Planilha
Assim como pedido na prática, foi construída uma planilha para analisar melhor a acurácia dos comitês. A planilha pode ser acessada no link a seguir: https://docs.google.com/spreadsheets/d/1Eg9LdWKYg01HcwVdr_A9IvdGRaAlodUfhahmUpIXzVc/edit?usp=sharing.

Com base nas médias foi possível observar uma tendência em que as configurações com o menor learning_rate foram as que apresentaram a melhor acurácia. Já analisando separadamente, a base que mostrou a maior acurácia foi a base "PCA_CNN_VGG19_128_avg" com a técnica 10-fold CV, que mostrou uma acurácia de 74,5%.
