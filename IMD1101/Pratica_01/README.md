# Prática 01
Essa prática será dividida em 3 etapas principais:
- Extração de características baseadas em HOG e CNN
- Aplicação do Método PCA
- Aplicação de Técnica Supervisionada - kNN

O DataSet que será utilizado está disponível em: https://www.robots.ox.ac.uk/~vgg/data/pets/

Para ver as informações completas sobre a prática basta acessar o arquivo "Aula_Pratica_kNN.pdf" que está disponível aqui no repositório.

## Extração de características baseadas em HOG e CNN
### HOG
Para a extração de características das referidas imagens, usando o HOG, iremos utilizar a seguinte metodologia:
- Ler as imagens baixadas do site de acordo com o sorteio feito em sala de aula;
- Redefinir o tamanho de cada uma delas para 256 x 256 pixels e 128 x 128 pixels;
- Aplicar o algoritmo de HOG para gerar quatro versões diferentes das imagens.
- Salvar os quatro datasets originários da transformação (em CSV), contendo +/- 800 imagens, sendo 400 imagens de cachorros e 400 imagens de gatos de acordo com o sorteio de cada grupo;

Por fim, os datasets resultantes vão estar disponibilizados nesse [link](https://drive.google.com/drive/folders/1iGMmBWTiGfG9Dwc78zwhgdZn3UcPc0DZ?usp=sharing).

### CNN
Com o CNN iremos utilizar os modelos já treinados VGG16 e VGG 19 para:
- Aplicar os modelos treinados de CNN (VGG16 e VGG19) nas 800 imagens de cada grupo, explorando os valores para pooling (‘avg’ e ‘max’), além de redefinir o tamanho de cada uma das imagens para 256 x 256 pixels e 128 x 128 pixels.

Assim teremos 4 datasets resultantes do modelo VGG16 e mais 4 datasets resultantes do model do VGG19.
Por fim, os datasets resultantes vão estar disponibilizados nesse [link](https://drive.google.com/drive/folders/15nsvqoKkMTzFFhTh5BKXhILHIFRxbZLt?usp=drive_link).

## k-NN
Com todos os datasets em mãos, agora podemos aplicar o método do k-NN. Para isso foi desenvolvido o notebook [Pratica01_kNN.ipynb](https://github.com/rikdantas/Aprendizagem-de-Maquinas/blob/main/IMD1101/Pratica_01/Pratica01_kNN.ipynb). Nesse notebook vai ser aplicado o k-NN variando o número de k entre 1 e 10. Nele serão apresentadas a acurácia para todas as bases e com essa acurácia iremos confeccionar uma tabela para visualizar melhor os resultados. A tabela pode ser acessada por esse [link](https://docs.google.com/spreadsheets/d/1UlzKllE8G0cGAwA62Fd16g7GAmpZRARWVSNIojdOO4k/edit?usp=sharing).

### Resultados
| **Melhores Bases**      | **Piores Bases**       |
|--------------------------|-------------------------|
| CNN_VGG16_256_avg       | CNN_VGG16_256_max      |
| CNN_VGG19_256_avg       | CNN_VGG19_256_max      |
| CNN_VGG19_128_max       | HOG_128_20x20          |
| CNN_VGG16_128_max       | HOG_128_16x16          |
| CNN_VGG19_128_avg       | HOG_256_20x20          |
| CNN_VGG16_128_avg       | HOG_256_20x20          |
