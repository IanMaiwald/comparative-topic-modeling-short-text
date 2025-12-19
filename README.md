# Comparando Modelagem de Tópicos em Textos Curtos

Este repositório contém uma implementação comparativa de diversos algoritmos de modelagem de tópicos aplicados a textos curtos, especificamente tweets em português sobre a pandemia de COVID-19.

## Descrição do Projeto

O projeto visa comparar o desempenho de diferentes técnicas de modelagem de tópicos quando aplicadas a textos curtos. Os algoritmos implementados incluem:

- **LDA (Latent Dirichlet Allocation)** - Modelo probabilístico clássico
- **BTM (Biterm Topic Model)** - Modelo baseado em Biterms
- **CRFTM (Contextual Recurrent Fast Topic Model)** - Modelo baseado em redes neurais recorrentes
- **DMM (Dirichlet Multinomial Mixture)** - Modelo de mistura para textos curtos
- **GPU-PDMM** - Versão otimizada para GPU do PDMM
- **LapDMM** - DMM com regularização de Laplacian
- **LSA (Latent Semantic Analysis)** - Análise semântica latente
- **MIGA** - Modelo de inferência baseado em meta-informação
- **MTM** - Modelo baseado em Multiterms
- **NBTMWE** - Modelo baseado em embeddings de palavras
- **NQTM** - Modelo baseado em amostragem negativa
- **PLSA (Probabilistic Latent Semantic Analysis)** - Análise semântica latente probabilística
- **PTM** - Modelo de alocação hierárquica
- **SATM** - Modelo com auto-agregação
- **WNTM** - Modelo baseado em redes de palavras

## Conjunto de Dados

O conjunto de dados utilizado consiste em tweets em português sobre COVID-19 coletados entre março de 2020 e março de 2021. Os dados incluem:

- Mais de 7 milhões de tweets hidratados
- Texto completo dos tweets
- Pré-processamento realizado para limpeza e normalização

### Arquivo de Dados
- `tweets2020-PT-Covid.zip`: Arquivo compactado com os tweets hidratados

## Pré-requisitos

Para executar este projeto, você precisará das seguintes bibliotecas Python:

```
pandas
numpy
gensim
scikit-learn
nltk
spacy
bitermplus
scipy
matplotlib
seaborn
wordcloud
unidecode
```

### Instalação das Dependências

```bash
pip install pandas numpy gensim scikit-learn nltk spacy bitermplus scipy matplotlib seaborn wordcloud unidecode
```

### Instalação do Modelo de Linguagem do SpaCy

```bash
python -m spacy download pt_core_news_sm
```

## Estrutura do Projeto

- `1-filtrando-tweets-pt-br.ipynb`: Filtragem inicial dos tweets em português
- `2-filtrando-apenas-textos-de-tweets-hidratados.ipynb`: Extração dos textos dos tweets hidratados
- `3-pre-processamento-de-textos.ipynb`: Pré-processamento completo dos textos (limpeza, tokenização, lematização, etc.)
- `*.ipynb`: Notebooks individuais para cada algoritmo de modelagem de tópicos

## Como Usar

1. **Pré-processamento dos Dados:**
   - Execute os notebooks de pré-processamento em ordem (1, 2, 3)
   - Isso gerará os dados limpos prontos para modelagem

2. **Execução dos Modelos:**
   - Cada notebook de modelo pode ser executado independentemente
   - Os modelos calculam métricas como perplexidade e coerência
   - Resultados incluem tópicos descobertos e distribuições de palavras

3. **Comparação:**
   - Compare os resultados entre diferentes modelos
   - Métricas de avaliação incluem perplexidade, coerência C_umass e C_w2v

## Resultados Esperados

Cada modelo produz:
- Tópicos com suas palavras mais representativas
- Distribuições de tópicos
- Visualizações quando aplicável

## Licença

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

## Referências

Este trabalho foi desenvolvido como parte de uma pesquisa acadêmica sobre modelagem de tópicos em textos curtos. Os algoritmos implementados são baseados em publicações científicas recentes na área de processamento de linguagem natural.
