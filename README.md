# Sistema de Recomendação de Imagens Digitais

Este projeto implementa um sistema de recomendação de roupas baseado na similaridade de imagens, usando um dataset do Kaggle (https://www.kaggle.com/datasets/agrigorev/clothing-dataset-full). Utiliza redes neurais convolucionais (CNNs) pré-treinadas para extrair características visuais das imagens e o algoritmo K-Nearest Neighbors (KNN) para encontrar as mais semelhantes. O sistema recomenda roupas visualmente semelhantes a uma imagem fornecida pelo usuário.

O projeto foi desenvolvido para ser executado em ambientes como o Google Colab, mas pode ser adaptado para outras plataformas.

# Tecnologias Utilizadas
* **TensorFlow / Keras:** Para carregar e utilizar modelos de redes neurais pré-treinadas (EfficientNetB0 e MobileNetV2).

* **Scikit-learn:** Para implementar o algoritmo K-Nearest Neighbors (KNN).

* **Matplotlib:** Para visualização dos resultados (exibição das imagens recomendadas).

* **Pandas e NumPy:** Para manipulação e processamento de dados.

* **Skimage:** Para conversão de cores e extração de histogramas de cores.

* **Kaggle API:** Para download do dataset de roupas.

# Visualização dos resultados:

As imagens recomendadas são exibidas lado a lado com a imagem de consulta. As roupas não são super parecidas por causa do dataset que possui várias roupas em poses/iluminação variadas, mas as roupas que aparecem são praticamente similares.

![exemplo 1](https://github.com/user-attachments/assets/e8a1ae94-1b4b-4925-8795-bbcc7e16465a)<br>
![exemplo 2](https://github.com/user-attachments/assets/164f7284-89ce-4175-ac69-2a99232812f9)<br>
![exemplo 3](https://github.com/user-attachments/assets/b47800ec-cfa3-4e91-9d19-5e015cc0466e)

# Instalação
1. Instale as dependências necessárias:
> !pip install -q kaggle tensorflow numpy pandas scikit-learn matplotlib scikit-image
2. Configure o Kaggle para baixar o dataset:
> Faça o upload do arquivo kaggle.json no Google Colab
3. Baixe e extraia o dataset:
> !kaggle datasets download -d agrigorev/clothing-dataset-full<br>
> !unzip -q clothing-dataset-full.zip -d clothing-dataset

# Funcionamento
O sistema funciona em 4 etapas principais:

* Carrega e processa imagens de um dataset

* Extrai caracteristicas usando uma CNN pre-treinada

* Utiliza KNN para encontrar imagens semelhantes

* Exibe as recomendacoes visuais ao usuario

# Extração de características:

* As características visuais são extraídas utilizando modelos pré-treinados.

* Histogramas de cores são calculados para complementar as características.

# Busca por similaridade:

* O algoritmo KNN é utilizado para encontrar as imagens mais similares com base nas características extraídas.

# Exibição dos resultados:

* Ao executar a função recomendar_roupas(), o usuário seleciona uma imagem de consulta e recebe 5 imagens similares. A imagem de consulta e as recomendações são exibidas lado a lado para comparação visual.




