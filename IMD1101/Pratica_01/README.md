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

Assim teremos o 4 datasets resultantes do modelo VGG16 e mais 4 datasets resultantes do model do VGG19.
Por fim, os datasets resultantes vão estar disponibilizados nesse [link](https://drive.google.com/drive/folders/15nsvqoKkMTzFFhTh5BKXhILHIFRxbZLt?usp=drive_link).
