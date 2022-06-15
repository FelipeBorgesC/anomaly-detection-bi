# Detecção de Anomalia
## Scripts desenvolvidos para palestras sobre Anomalias

### Índice
  
- [Anomalia Pontual e/ou Global](#anomalia-pontual-global)
- [Anomalia em Séries Temporais](#anomalia-timeseries)
  - [Análise Exploratória e Processamento](#analise-exploratoria-processamento)
  - [Modelos](#modelos)

## 

<h2 id="anomalia-pontual-global">
  
[Anomalia Pontual e/ou Global](https://github.com/manoelakohler/DataMining/tree/main/01_An%C3%A1liseExplorat%C3%B3ria)
  
</h2>

<h2 id="anomalia-timeseries">
  
[Anomalia em Séries Temporais](https://github.com/FelipeBorgesC/anomaly-detection-bi/tree/main/Anomaly%20-%20Timeseries)
  
</h2>

Abaixo está organizado todas as etapas necessárias para a criação de um Detector de Anomalias em Séries Temporais, desde a análise crítica dos dados brutos, passando pelos processos necessários para organização e pré-processamento dos dados, até o treinamento dos modelos e a otimização de seus parâmetros. Diferentemente da abordagem de detecção de anomalias em registros pontuais ou globais, quando o detector deve levar em consideração a evolução temporal de determinada grandeza, é necessário realizar alguns procedimentos adicionais. Além disso, assim como nos casos de previsão de séries temporais, a etapa mais importante e mais delicada do processo é no momento da organização da base de dados. Definir as taxas de amostragens para criação dos *batches* é crucial para um treinamento adequado dos modelos.

<h3 id="analise-exploratoria-processamento">
  
[Análise Exploratória e Processamento](https://github.com/manoelakohler/DataMining/tree/main/01_An%C3%A1liseExplorat%C3%B3ria)
  
</h3>

  - **Leitura de sensores:** Análise e Processamento Leitura de sensores [`Analise_Preprocessamento.ipynb`](https://github.com/FelipeBorgesC/anomaly-detection-bi/blob/main/Anomaly%20-%20Timeseries/Analise_Preprocessamento.ipynb). A base de dados utilizada para exemplificação desse case é do [dataset 3W](https://github.com/ricardovvargas/3w_dataset) sendo composto por inúmeros arquivos de leitura de sensores já rotulados com classes de eventos. Para o estudo de aula, o foco foi apenas sobre 1 único arquivo para exemplificar o passo a passo de um problema de detecção de anomalias em séries temporais. Nessa etapa o objetivo foi explicar as etapas de análise dos dados do problema e aplicar as diversas etapas de pré processamento necessários em séries temporais.
    - Análise dos dados
      - Comportamento classe de saída
      - Amostragem mínima/máxima
      - Quantidade de atributos
    - Processamento
      - Retirada de colunas nulas
      - Checagem de amostragem mínima
      - Organizar base em formato padrão
      - Extrair *features* com a biblioteca *tsfresh*
      - Armazenar em um arquivo


<h3 id="modelos">
  
[Modelos](https://github.com/manoelakohler/DataMining/tree/main/03_Classifica%C3%A7%C3%A3o)
  
</h3>

 - **Análise de Crédito Bancário:** Entendimento, pré processamento e classificação de uma base de análise de crédito [`Secom.ipynb`](https://github.com/manoelakohler/DataMining/blob/main/02_Pr%C3%A9Processamento/Secom.ipynb). A base de dados contém 2077 exemplos de créditos concedidos ou não. Possui 11 atributos de entrada e 2 classes de saída. A saída indica se o cliente pagou o empréstimo (=1) ou se não pagou (=0). 
 
    - Medidas resumo para análise exploratória      
    - Pré processamento
      - Normalização
    - Inferência (classificação)
      - SVM
      - Árvore de Decisão
      - Random Forest
    - Tuning de hiperparâmetros
      - GridSearch
