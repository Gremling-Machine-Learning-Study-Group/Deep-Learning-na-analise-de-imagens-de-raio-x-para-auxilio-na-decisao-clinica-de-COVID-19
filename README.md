# IA e ciência de dados para apoio a decisão clínica 

Parte 2 do desafio "IA E CIÊNCIA DE DADOS PARA APOIO A DECISÃO CLÍNICA" da Hackathon 'Hackcovid19' do Centro Brasileiro de Pesquisas Físicas, tentamos demostrar a possibilidade de usar um modelo de Deep Neural para gerar diagnosticos em radiografias de pulmão, dado o cenario onde se torna impossivel usar teste rapidos ou teste laboratorais em todos os pacientes, o uso de radiografias para diagnosticar Covid ou qualquer outra enfermidade se torna uma opção viavel.

A implementação de algoritmos de suporte à decisão clínica para imagens médicas enfrenta desafios com confiabilidade e interpretabilidade, estabelecemos aqui uma ferramenta de diagnóstico com base em uma estrutura de aprendizado profundo para a triagem de pacientes com doenças tratáveis como comuns, utilizando aprendizado de maquina profundo, treinamos uma rede neural com uma fração dos dados das abordagens convencionais. Demonstramos ainda a aplicabilidade geral do nosso sistema de IA para o diagnóstico de pneumonia usando imagens de raios-X do tórax. Essa ferramenta pode, em última análise, ajudar a acelerar o diagnóstico e o encaminhamento dessas condições tratáveis, facilitando assim o tratamento anterior, resultando em melhores resultados clínicos.


## ETAPA 1: Discussão e Contextualização:

A inteligência artificial (IA) tem o potencial de revolucionar o diagnóstico e o gerenciamento de doenças, realizando classificações difíceis para especialistas humanos e revisando rapidamente imensas imagens. Apesar de seu potencial, a interpretabilidade clínica e a preparação viável da IA continuam sendo um desafio.

A abordagem algorítmica tradicional da análise de imagens para classificação anteriormente se baseava em:

(1) segmentação de objetos artesanais, seguida por;
(2) identificação de cada objeto segmentado usando classificadores estatísticos ou classificadores de aprendizado de máquina computacionais neurais superficiais projetados especificamente para cada classe de objetos;
(3) classificação da imagem.

A criação e o refinamento de vários classificadores exigiram muitas pessoas qualificadas e muito tempo e eram computacionalmente caros. O desenvolvimento de camadas de redes neurais convolucionais permitiu ganhos significativos na capacidade de classificar imagens e detectar objetos em uma imagem São várias camadas de processamento nas quais os filtros ou convoluções de análise de imagem são aplicados.
   
## ETAPA 2: Dados e Modelo.

O dados foram obtidos do site Kaggle, o teste foi feito para dois datasets, um se tratando de pessoas com pneumonia e o ourro de pessoas com COVID-19 e ambos os teste foi feita um comparaço binaria onde tratamos de ensinar o modelo a diferenciar um pulmão saudavel de um pulmão doente (pneumonia ou Covid).

### Dataset

Na maioria das vezes o nosso maior trabalho e na montagem do dataset, visto que esse já se encobntravam prontos e com uma certa confiabilidade, o projeto se tornou mais simples.

### Modelo

Nosso modelo de Deep Neural se concentra em uma aplicaço rapida mais robusta, onde temos uma grande confiabilidade mas ainda carecemos de mais dados para treinar o mesmo, portanto acreditamos que com o que temos já podemos concluir algo sobre e ainda dizer que podemos sim usar o mesmo para avaliar radiografias.

### Codigo

Nosso codigo esta descrito no notebook python anexo neste repositorio. Note que a titulo de comparação podemos dizer que a melhoria do mesmo está condicionada a uma melhora no dados para treino e maior tempo de treinamento.
  
  **Resultados:**
  
  - No nosso primeiro teste com o dataset 1 tivemos uma acuracia de curácia de teste 91%.
  - No segundo onde o volume de dados era menor 71%.
  
  *Maiores informações vide notebook, lá se encontrar um analise grafica detalhando os processos de perda e acuracia.*
  
## Referencias:

* **"Imagens de radiografia de tórax (Pneumonia)"** https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia; (Visualizado em: 17/05/2020) (Daqui foi obtido o *dataset* 'Chest X-Ray Images (Pneumonia)').

* **"COVID-19 RADIOGRAPHY DATABASE"** https://www.kaggle.com/tawsifurrahman/covid19-radiography-database; (Visualizado em: 17/05/2020) (Daqui foi obtido o *dataset* 'COVID-19 Radiography Database').

* **"Detecting COVID-19 induced Pneumonia from Chest X-rays with Transfer Learning: An implementation in Tensorflow and Keras."** https://towardsdatascience.com/detecting-covid-19-induced-pneumonia-from-chest-x-rays-with-transfer-learning-an-implementation-311484e6afc1; (Visualizado em: 17/05/2020) (Inspiraço para construção deste modelo. GitHub do autor https://github.com/EXJUSTICE/).

