# AI-900: Trabalhando com Machine Learning na Prática no Azure ML

![Static Badge](https://img.shields.io/badge/Status_Projeto:-Concluído_(06/Mar/2024)-green)

![Static Badge](https://img.shields.io/badge/Inteligência_Artificial_(IA)-blue)
![Static Badge](https://img.shields.io/badge/Avaliação_e_Treinamento_de_Modelos_(IA)-blue)

![Static Badge](https://img.shields.io/badge/Microsoft_Azure-orange)
![Static Badge](https://img.shields.io/badge/Azure_Auto_ML-orange)
![Static Badge](https://img.shields.io/badge/Azure_Machine_Learning_Studio-orange)

<br>

## Índice

- [Descrição do Projeto](#Descrição-do-Projeto)
- [Acessos necessários](#Acessos-necessários)
- [Introdução](#Introdução)
- [Aprovisionando o serviço de *Machine Learning*](#Aprovisionando-o-serviço-de-Machine-Learning)
- [Configurando os modelos de *Machine Learning* e os conjuntos de dados](#Configurando-os-modelos-de-Machine-Learning-e-os-conjuntos-de-dados)
- [Analisando e Testando o Modelo](#Analisando-e-Testando-o-Modelo)
- [Conclusão](#Conclusão)
- [Limpar o ambiente](#Limpar-o-ambiente)
- [Certificados / Certificações Associados ao Projeto](#Certificados-/-Certificações-Associados-ao-Projeto)

<br>

## Descrição do Projeto

Este projeto é um dos laboratórios do Bootcamp [Microsoft Azure AI Fundamentals](https://web.dio.me/track/microsoft-azure-ai-fundamentals), promovido através da parceria entre a Microsoft e a Dio.me.

Os alunos deste bootcamp tem, como principal objetivo, se prepararem para o exame de certificação Microsoft AI-900, dominando conceitos como visão computacional, classificação inteligente de imagem e inteligência de documentos com IA, enquanto se familiarizam com as tecnologias da Microsoft Azure.

Este desafio é o de número 1 do bootcamp e consiste na execução prática do seguinte exercício:

- [Aprendizagem de Máquina Automatizada](https://aka.ms/ai900-auto-ml): explorar a automatização de *machine learning* no ***Azure Auto ML***

<br>

## Acessos necessários

Para realizar estes laboratórios, eu precisei criar uma [Subscrição do Microsoft Azure](https://azure.microsoft.com/)

A Microsoft permite criar uma subscrição de teste, na qual vários serviços podem ser experimentados gratuitamente por 12 meses, além de receber $200 para serem utilizados nos primeiros 30 dias.

<br>

## Introdução

O aprendizado de máquina automatizado permite experimentar vários algoritmos e parâmetros para treinar modelos e identificar o melhor para seus dados, seguido da implantação e teste do mesmo.

Neste exercício, utilizei um dataset público contendo o histórico de aluguel de bicicletas para treinar um modelo.

Este modelo previu o número de bicicletas necessárias para atender à demanda de locação em um determinado dia, com base em características sazonais e meteorológicas.

<br>

## Aprovisionando o serviço de *Machine Learning*

1) Como primeiro passo, acessei o **Azure Machine Learning**:

   > ![](readmeFiles/gifs/001.gif)

2) Criei um ***Resource Group*** para armazenar o serviço:

   > ![](readmeFiles/gifs/002.gif)

3) Inserir as configurações do Workspace (preenchi apenas o campo ***Name***. Para os demais, deixar os valores padrões):

   > ![](readmeFiles/images/003.png)

4) Criei o serviço:

   > É necessário aguardar a mensagem de validação, conforme imagem a baixo, e, depois, clicar em ***Create***
  
   > ![](readmeFiles/images/004.png)


5) Aguardei a implantação do serviço:

   > ![](readmeFiles/images/005.png)

<br>

## Configurando os modelos de *Machine Learning* e os conjuntos de dados

1) Abri o **Machine Learning Studio**:

   > **Atenção:** Durante o carregamento, pode ser solicitado, novamente, sua conta do Azure

   > ![](readmeFiles/gifs/006.gif)

2) Criar um Novo Trabalho de Machine Learning Automatizado

   > ![](readmeFiles/gifs/007.gif)

3) Preenchi as configurações básicas:

   > ![](readmeFiles/images/008.png)

4) Criei o tipo de tarefa:

   > ![](readmeFiles/images/009.png)

5) Criei o ativo de dados:
   > ***Tipo de dados***
   >
   > ![](readmeFiles/images/010.png)

   > ***Fonte de dados***
   >
   > ![](readmeFiles/images/011.png)

   > ***URL da Web***
   >
   > ![](readmeFiles/images/012.png)

   > ***Configurações***
   >
   > ![](readmeFiles/images/013.png)

   > ***Esquema***
   >
   > ![](readmeFiles/images/014.png)

   > ***Examinar***
   >
   > ![](readmeFiles/images/015.png)

6) Criei o tipo de dados:
   >
   > ![](readmeFiles/images/016.png)

7) Configurei as tarefas:

   > ![](readmeFiles/images/017.png)

   > ![](readmeFiles/images/018.png)

   > ![](readmeFiles/images/019.png)

   > ![](readmeFiles/images/020.png)

8) Configurei a computação:

   > ![](readmeFiles/images/021.png)

9) Enviei o trabalho para treinamento:
   > **Atenção**: Esta ação levou cerca de 15 minutos para ser finalizada
   
   > ![](readmeFiles/images/022.png)
   
   > ![](readmeFiles/images/023.png)
   
   > ![](readmeFiles/images/024.png)

<br>

## Analisando e Testando o Modelo

1) Chequei a integridade dos dados:

   > ![](readmeFiles/images/025.png)

2) Chequei a conclusão de todas as tarefas:

   > ![](readmeFiles/images/026.png)

3) Identifiquei o melhor modelo do treinamento:

   > ![](readmeFiles/images/027.png)

4) Chequei as métricas do modelo escolhido:

   > ![](readmeFiles/images/028.png)

   As métricas mais importantes são: **predicted_true** e **residuals***

     > ![](readmeFiles/images/029.png)

   *- **predicted_true**: O gráfico predicted_true compara os valores previstos com os valores verdadeiros.*

     > ![](readmeFiles/images/030.png)

   *- **residuals:** O gráfico de resíduos mostra os resíduos (as diferenças entre os valores previstos e reais) como um histograma*

     > ![](readmeFiles/images/031.png)

6) Implantei e testei o modelo

   > ![](readmeFiles/images/032.png)

   > ![](readmeFiles/images/033.png)

   > **Atenção**: A implantação levou entre 5 e 10 minutos*

   > ![](readmeFiles/images/034.png)

7) Testei o modelo

   > ![](readmeFiles/gifs/035.gif)

   O resultado do teste indicou que precisava de 298 bicicletas para atender à demanda de acordo com a data e as condições meterorógicas informadas

   > ![](readmeFiles/images/036.png)

<br>

## Conclusão

Este exercício demonstrou o poder e a eficácia do aprendizado de máquina automatizado.

Ao utilizar um conjunto de dados históricos de aluguel de bicicletas, fui capaz de treinar um modelo para prever com precisão o número de aluguéis esperados em um determinado dia, levando em consideração fatores sazonais e meteorológicos.

Isso ilustra como o aprendizado de máquina pode ser aplicado a problemas do mundo real, fornecendo insights valiosos e permitindo a tomada de decisões informadas.

A capacidade de experimentar vários algoritmos e parâmetros me permitiu identificar o modelo mais eficaz para os dados específicos.

Este é apenas um exemplo do potencial do aprendizado de máquina automatizado e das possibilidades que ele oferece para uma ampla gama de aplicações.

<br>

## Limpando o ambiente

> [!WARNING]
> Após a conclusão do projeto, se não for reaproveitar os recursos utilizados, é aconselhável excluí-los, bem como os grupos de recursos, para que não haja cobranças indevidas na sua Azure Subscription

<br>

## Certificados / Certificações Associados ao Projeto

![](https://github.com/rodolfoom1982/meus-certificados/blob/main/dio-bootcamp-ai-900-azure-ai-fundamentals/trabalhando-com-machine-learning-na-pratica-no-azure-ml)
