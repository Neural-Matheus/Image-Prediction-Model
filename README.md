# Dog-Cat-Classifier usando Convolutional Neural Network (CNN)

## Introdução
Este projeto implementa uma Convolutional Neural Network (CNN) utilizando TensorFlow e Keras para classificar imagens como sendo de um cachorro ou de um gato. O conjunto de dados é dividido em treinamento e teste, contendo imagens de cachorros e gatos.

![Representação de uma CNN](https://cdn.discordapp.com/attachments/1184622679685333042/1193575806614638644/CNN.png?ex=65e49617&is=65d22117&hm=c0dc5387831e70cebb0a2ada953503695b740c81150e029cf1d7ac7456c89dbc&)

## Descrição do Projeto
O objetivo principal é criar um modelo capaz de aprender características distintas entre imagens de cachorros e gatos, possibilitando a classificação correta de novas imagens. A CNN é escolhida devido à sua eficácia no processamento de dados de imagem.

## Preparação do Conjunto de Dados

### Conjunto de Treinamento
- Utiliza um gerador de imagens (`ImageDataGenerator`) para pré-processar as imagens.
- Realiza aumento de dados, incluindo rotação, zoom e inversão horizontal.
- As imagens são redimensionadas para o tamanho desejado (64x64 pixels).
- Cria um conjunto de treinamento (`training_set`) com classes binárias (cachorro ou gato).
- Há um conjunto de 4000 imagens de gatos e cachorros separados por pastas.

### Conjunto de Teste
- Utiliza um gerador de imagens (`ImageDataGenerator`) para pré-processar as imagens, com rescale.
- As imagens são redimensionadas para o tamanho desejado (64x64 pixels).
- Cria um conjunto de teste (`test_set`) com classes binárias (cachorro ou gato).

## Construção da CNN
- Inicializa um modelo sequencial (`Sequential`) do Keras.
- Adiciona duas camadas de convolução (`Conv2D`) com ativação ReLU e camadas de max pooling (`MaxPool2D`).
- Adiciona uma camada de flattening e uma camada densa (`Dense`) para conexão completa.
- A última camada é uma camada de saída com ativação sigmoid para classificação binária.

## Treinamento da CNN
- Compila a CNN com o otimizador Adam, a função de perda binary crossentropy e métricas de acurácia.
- Treina a CNN no conjunto de treinamento (`training_set`) e valida no conjunto de teste (`test_set`) por 25 épocas.

## Realizando uma Única Previsão
- Carrega uma imagem de teste.
- Pré-processa a imagem para o formato adequado.
- Faz uma previsão utilizando o modelo treinado.
- Converte a previsão em uma classe (cachorro ou gato).

## Dependências
Certifique-se de ter as seguintes bibliotecas instaladas:
- TensorFlow: `pip install tensorflow`
- Keras: `pip install keras`

## Contribuindo
Contribuições são bem-vindas! Se você encontrar problemas ou tiver sugestões, sinta-se à vontade para abrir uma issue ou enviar um pull request.
Agradeço pelo seu interesse e contribuição!
