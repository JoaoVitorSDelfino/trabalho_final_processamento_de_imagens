<h1 align="center"> Trabalho Final de Processamento de Imagens </h1>

## Aluno
João Vitor Schiavinato Delfino R.A.: a2453363

## Descrição do Descritor Escolhido (Filtro de Gabor)
Filtro de Gabor atua como um "detector de texturas" sensível a variações de frequência e orientação, permitindo uma análise detalhada da estrutura local da imagem. Essa capacidade o torna especialmente útil em cenários onde a textura e os padrões locais são determinantes para a tarefa de classificação ou detecção, como no diagnóstico assistido por imagens médicas. No geral, há duas principais funcionalidades que o tornam efetivos para a análise de casos de COVID-19:

Detecção de Padrões e Texturas:
Devido à sua capacidade de sintonizar para frequências e orientações específicas, o filtro de Gabor é muito eficaz na identificação de padrões locais como bordas, linhas e texturas. Ao aplicar um banco de filtros de Gabor com diferentes orientações e escalas, é possível extrair uma rica representação das características de textura presentes na imagem.

Localização Espacial:
A multiplicação pela função gaussiana garante que o filtro seja local, ou seja, ele captura informações apenas de uma região específica da imagem. Isso é crucial para manter a localização espacial das características, permitindo que se identifique exatamente onde certos padrões ocorrem.

Durante essa implementação, foi utilizado a configuração padrão de parâmetros.

## Repositório do Projeto
https://drive.google.com/drive/folders/1CpDVlAFIlCbQ1jJvHxpBdqyLnz2z5OHy?usp=sharing

## Classificador e Acurácia
O classificador esclolhido foi o SVM (Support Vector Machine), pelos principais motivos:
- Margem Máxima:
A SVM procura um hiperplano que separa as classes com a maior margem possível, o que ajuda a melhorar a generalização

- Capacidade de Lidar com Dados de Dimensão Moderada:
Os vetores de características obtidos a partir dos filtros de Gabor geralmente não são de altíssima dimensão. A SVM se mostra eficiente nesse contexto, principalmente quando utilizada com kernels (como o RBF) que podem modelar relações não-lineares entre as classes.

- Robustez em Cenários com Conjunto de Dados Limitados:
Em aplicações médicas, como a análise de raios-X para COVID-19, muitas vezes temos um número relativamente pequeno de exemplos. A SVM costuma performar bem mesmo com conjuntos de dados menores, ao contrário de modelos como MLP, que podem exigir mais dados para evitar overfitting.

![image](https://github.com/user-attachments/assets/f50bc17d-5c3e-441f-99cf-9fa8dd580e10)
![image](https://github.com/user-attachments/assets/70bff7ab-95bb-4e6c-b89c-370be453b8a0)
