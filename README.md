# Detecção de Anomalia
### Scripts desenvolvidos para as palestras sobre Anomalias

### Índice
  
- [Anomalia Pontual e/ou Global](#anomalia-pontual-global)
  - [Análise, processamento e modelo em Dados Pontuais](#analise-processamento-modelo)
- [Anomalia em Séries Temporais](#anomalia-timeseries)
  - [Análise Exploratória e Processamento](#analise-exploratoria-processamento)
  - [Modelos](#modelos)

## 

<h2 id="anomalia-pontual-global">
  
[Anomalia Pontual e/ou Global](https://github.com/FelipeBorgesC/anomaly-detection-bi/tree/main/Anomaly%20-%20Global)
  
</h2>

Nesta seção é apresentado todas as etapas para desenvolvimento de um Detector de Anomalia pontual. A primeira etapa consiste em visualizar a quantidade de classes existentes no problema, executar o preprocessamento necessário e em seguida o treinamento do modelo.

<h3 id="analise-processamento-modelo">
  
[Análise, processamento e modelo em Dados Pontuais](https://github.com/FelipeBorgesC/anomaly-detection-bi/blob/main/Anomaly%20-%20Global/AnomalyDetection.ipynb)
  
</h3>

- **Análise, preprocessamento e modelo:** Carregamento do dataset, analisar o seu comportamento e treinamento do modelo [`AnomalyDetection.ipynb`](https://github.com/FelipeBorgesC/anomaly-detection-bi/blob/main/Anomaly%20-%20Global/AnomalyDetection.ipynb). 
    
    A base de dados trata-se de um conjunto de amostras de exames de eletrocardiograma. E, nessa base, os dados estão rotulados como normais e anômalos e, apesar dos dados serem de um período de tempo sequencial, a avaliação de anomalia ocorre de uma sequência de tamanho fixo e para uma mesma janela de amostragem. Inicialmente é feita uma análise da base, tanto o tamanho dessa janela de amostragem quanto a quantidade de registros normais e de anomalia. Em seguida é aplicado a normalização desses dados e o treinamento do modelo. Por fim, é executada a avaliação do modelo treinado e os resultados quantitativos. 
 
    - Análise da base de dados
      - Visualização gráfica
      - Exibição da quantidade de registros por classe
    - Preprocessamento dos dados
    - Treinamento do modelo
    - Avaliação do modelo


<h2 id="anomalia-timeseries">
  
[Anomalia em Séries Temporais](https://github.com/FelipeBorgesC/anomaly-detection-bi/tree/main/Anomaly%20-%20Timeseries)
  
</h2>

Abaixo está organizado todas as etapas necessárias para a criação de um Detector de Anomalias em Séries Temporais, desde a análise crítica dos dados brutos, passando pelos processos necessários para organização e pré-processamento dos dados, até o treinamento dos modelos e a otimização de seus parâmetros. Diferentemente da abordagem de detecção de anomalias em registros pontuais ou globais, quando o detector deve levar em consideração a evolução temporal de determinada grandeza, é necessário realizar alguns procedimentos adicionais. Além disso, assim como nos casos de previsão de séries temporais, a etapa mais importante e mais delicada do processo é no momento da organização da base de dados. Definir as taxas de amostragens para criação dos *batches* é crucial para um treinamento adequado dos modelos.

<h3 id="analise-exploratoria-processamento">
  
[Análise Exploratória e Processamento](https://github.com/FelipeBorgesC/anomaly-detection-bi/tree/main/Anomaly%20-%20Timeseries/An%C3%A1lise%20e%20preprocessamento)
  
</h3>

  - **Leitura de sensores:** Análise e Processamento Leitura de sensores [`Analise_Preprocessamento.ipynb`](https://github.com/FelipeBorgesC/anomaly-detection-bi/blob/main/Anomaly%20-%20Timeseries/Analise_Preprocessamento.ipynb). 
    
    A base de dados utilizada para exemplificação desse case é do [dataset 3W](https://github.com/ricardovvargas/3w_dataset) sendo composto por inúmeros arquivos de leitura de sensores já rotulados com classes de eventos. Para o estudo de aula, o foco foi apenas sobre 1 único arquivo para exemplificar o passo a passo de um problema de detecção de anomalias em séries temporais. Nessa etapa o objetivo foi explicar as etapas de análise dos dados do problema e aplicar as diversas etapas de pré processamento necessários em séries temporais.


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
  
[Modelos](https://github.com/FelipeBorgesC/anomaly-detection-bi/tree/main/Anomaly%20-%20Timeseries/Modelo)
  
</h3>

 - **Modelos:** Carregamento do dataset processado e testagem de variados modelos [`Modelos.ipynb`](https://github.com/FelipeBorgesC/anomaly-detection-bi/blob/main/Anomaly%20-%20Timeseries/Modelo/Modelos.ipynb). 
    
    Com a base de dados já processada são testados diversos modelos para a detecção dos momentos de anomalia.
 
    - Modelos
      - Autoencoder simples
      - Autoencoder + SVC
      - Variational Autoencoder
