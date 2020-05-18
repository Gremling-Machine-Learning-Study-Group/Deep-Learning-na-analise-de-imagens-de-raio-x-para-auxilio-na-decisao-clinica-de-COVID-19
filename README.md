# Deep Learning na análise de imagens de radiografias para auxílio na decisão clínica do COVID-19 

Parte 2 do desafio "IA E CIÊNCIA DE DADOS PARA APOIO A DECISÃO CLÍNICA" da Hackathon 'Hackcovid19' do Centro Brasileiro de Pesquisas Físicas, tentamos demonstrar a possibilidade de usar um modelo de Deep Neural para gerar diagnósticos em radiografias de pulmão, dado o cenário onde se torna impossível usar teste rápidos ou teste laboratoriais em todos os pacientes, o uso de radiografias para diagnosticar Covid ou qualquer outra enfermidade se torna uma opção viável.

Parte 1 do projeto: https://github.com/Gremling-Machine-Learning-Study-Group/Estimativa-de-mortes-por-COVID-19-subnotificadas-no-Brasil---D051---HACKCOVID-19/blob/master/README.md

Página do projeto no Devpost: https://devpost.com/software/test_deep_covid-19#updates

Pitch para a Hackathon (Apenas vídeo): https://www.youtube.com/watch?v=8ujmJz6i4YI

A implementação de algoritmos de suporte à decisão clínica para imagens médicas enfrenta desafios com confiabilidade e interpretabilidade, estabelecemos aqui uma ferramenta de diagnóstico com base em uma estrutura de aprendizado profundo para a triagem de pacientes com doenças tratáveis como comuns, utilizando aprendizado de máquina profundo, treinamos uma rede neural com uma fração dos dados das abordagens convencionais. Demonstramos ainda a aplicabilidade geral do nosso sistema de IA para o diagnóstico de pneumonia usando imagens de raios-X do tórax. Essa ferramenta pode, em última análise, ajudar a acelerar o diagnóstico e o encaminhamento dessas condições tratáveis, facilitando assim o tratamento anterior, resultando em melhores resultados clínicos.

## ETAPA 1: Discussão e Contextualização:

A inteligência artificial (IA) tem o potencial de revolucionar o diagnóstico e o gerenciamento de doenças, realizando classificações difíceis para especialistas humanos e revisando rapidamente imensas imagens. Apesar de seu potencial, a interpretabilidade clínica e a preparação viável da IA continuam sendo um desafio.

A abordagem algorítmica tradicional da análise de imagens para classificação anteriormente se baseava em:

(1) segmentação de objetos artesanais, seguida por;
(2) identificação de cada objeto segmentado usando classificadores estatísticos ou classificadores de aprendizado de máquina computacionais neurais superficiais projetados especificamente para cada classe de objetos;
(3) classificação da imagem.

A criação e o refinamento de vários classificadores exigiram muitas pessoas qualificadas e muito tempo e eram computacionalmente caros. O desenvolvimento de camadas de redes neurais convolucionais permitiu ganhos significativos na capacidade de classificar imagens e detectar objetos em uma imagem São várias camadas de processamento nas quais os filtros ou convoluções de análise de imagem são aplicados.
   
## ETAPA 2: Dados e Modelo.

O dados foram obtidos do site Kaggle, o teste foi feito para dois datasets, um se tratando de pessoas com pneumonia e o outro de pessoas com COVID-19 e ambos os teste foi feita uma comparação binária onde tratamos de ensinar o modelo a diferenciar um pulmão saudável de um pulmão doente (pneumonia ou Covid).


### Dataset

Na maioria das vezes o nosso maior trabalho e na montagem do dataset, visto que esse já se encontravam prontos e com uma certa confiabilidade, o projeto se tornou mais simples.

### Modelo

Nosso modelo de Deep Neural se concentra em uma aplicação rápida mais robusta, onde temos uma grande confiabilidade mas ainda carecemos de mais dados para treinar o mesmo, portanto acreditamos que com o que temos já podemos concluir algo sobre e ainda dizer que podemos sim usar o mesmo para avaliar radiografias.

### Código

Nosso código está descrito no notebook python anexo neste repositório. Note que a título de comparação podemos dizer que a melhoria do mesmo está condicionada a uma melhora no dados para treino e maior tempo de treinamento. 

## ETAPA 3: Metodologia

A metodologia deste projeto é bem básica, como todo projeto de Deep Learning necessitamos de um dataset robusto é que valise nosso modelo, portanto o primeiro passo foi esse encontra datasets que atendessem minimamente a isso, após encontrá-los foi montado um workflow para descrever o processos: analise dos dados, pré-processamento,construção da rede, treino, teste e validação e como passo final uma avaliação gráfica dos modelos acerca de sua acurácia.

  **Resultados:**
  
  - No nosso primeiro teste com o dataset 1 tivemos uma acurácia  de teste 91%.
  - No segundo onde o volume de dados era menor 71%.
  
  *Maiores informações vide notebook, lá se encontrar um análise gráfica detalhando os processos de perda e acurácia.*
 **Nota** *: devido a limites computacionais da minha máquina não consegui rodar o modelo por mais tempo.*

## ETAPA 3: Conclusão

Portanto podemos concluir que é sim uma aplicação viável e que futuramente pode ser amplamente empregada em análises preliminares e triagem de paciente com Covid. Com a aumento na coleta de dados podemos treinar modelos melhores e diagnosticar usando técnica até mais simples por métodos de avaliação de imagens.


## Referências:

* **"Imagens de radiografia de tórax (Pneumonia)"** https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia; (Visualizado em: 17/05/2020) (Daqui foi obtido o *dataset* 'Chest X-Ray Images (Pneumonia)').

* **"COVID-19 RADIOGRAPHY DATABASE"** https://www.kaggle.com/tawsifurrahman/covid19-radiography-database; (Visualizado em: 17/05/2020) (Daqui foi obtido o *dataset* 'COVID-19 Radiography Database').

* **"Detecting COVID-19 induced Pneumonia from Chest X-rays with Transfer Learning: An implementation in Tensorflow and Keras."** https://towardsdatascience.com/detecting-covid-19-induced-pneumonia-from-chest-x-rays-with-transfer-learning-an-implementation-311484e6afc1; (Visualizado em: 17/05/2020) (Inspiraço para construção deste modelo. GitHub do autor https://github.com/EXJUSTICE/).

