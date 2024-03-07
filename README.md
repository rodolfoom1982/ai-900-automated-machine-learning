# AI-900: Trabalhando com Machine Learning na Prática no Azure ML
Utilização do serviço Aprendizado de Máquina do Azure para treinar e avaliar um modelo de aprendizado de máquina, seguido da implantação e teste do modelo treinado.

Neste exercício, foi utilizado um dataset público contendo o histórico de aluguel de bicicletas para treinar um modelo. Este modelo prevê o número de bicicletas necessárias em um determinado dia, com base em características sazonais e meteorológicas, para atender à demanda de locação.

# 1ª Etapa) Aprovisionar o serviço de Machine Learning

a) Acessar o Azure Machine Learning
<br><br>
[![Watch the video](readmeFiles/videos/001.mp4)

b) Criar um Resource Group para armazenar o serviço
002

c) Inserir as configurações do Workspace
--> Informar apenas o campo Name
--> Para os demais, deixar os valores padrões
--> Na sequência, clicar em Review + create
![alt text](readmeFiles/images/003.png)

d) Crear o serviço
--> Aguardar a mensagem de validação, conforme imagem a baixo, e clicar em Create
![alt text](readmeFiles/images/004.png)


e) Aguardar a implantação do serviço
--> Quando a mesma estiver concluída, o status <i>Your deployment is complete</i> aparecerá na tela
--> Esta etapa leva alguns instantes para ser concluída
![alt text](readmeFiles/images/005.png)



# 2ª Etapa) Configurar os modelos de Machine Learning e os conjuntos de dados

a) Abrir o Machine Learning Studio
--> Durante o carregamento, pode ser solicitado, novamente, sua conta do Azure
![alt text](readmeFiles/images/006.png)

b) Criar um Novo Trabalho de Machine Learning Automatizado
![alt text](readmeFiles/images/007.png)

c) Preencher as configurações básicas
![alt text](readmeFiles/images/008.png)

d) Criar o tipo de tarefa
![alt text](readmeFiles/images/009.png)

e) Criar o ativo de dados
![alt text](readmeFiles/images/010.png)
![alt text](readmeFiles/images/011.png)
![alt text](readmeFiles/images/012.png)
![alt text](readmeFiles/images/013.png)
![alt text](readmeFiles/images/014.png)
![alt text](readmeFiles/images/015.png)
![alt text](readmeFiles/images/016.png)

f) Configurar tarefas
![alt text](readmeFiles/images/017.png)
![alt text](readmeFiles/images/018.png)
![alt text](readmeFiles/images/019.png)
![alt text](readmeFiles/images/020.png)

g) Configurar computação
![alt text](readmeFiles/images/021.png)

h) Enviar o trabalho para treinamento 
![alt text](readmeFiles/images/022.png)
--> Esta ação levará cerca de 15 minutos para ser finalizada
![alt text](readmeFiles/images/023.png)
--> Este é o status que indica a conclusão do treinamento
![alt text](readmeFiles/images/004.png)


# 3ª Etapa) Analisar e Testar do Modelo

a) Checar a integridade dos dados
![alt text](readmeFiles/images/025.png)

b) Checar a conclusão de todas as tarefas
![alt text](readmeFiles/images/026.png)

c) Identificar o melhor modelo do treinamento
![alt text](readmeFiles/images/027.png)

d) Checar as métricas deste modelo
![alt text](readmeFiles/images/028.png)
--> As métricas mais importantes são: predicted_true e residuals
![alt text](readmeFiles/images/029.png)
--> predicted_true: O gráfico predicted_true compara os valores previstos com os valores verdadeiros.
![alt text](readmeFiles/images/030.png)
--> residuals: O gráfico de resíduos mostra os resíduos (as diferenças entre os valores previstos e reais) como um histograma
![alt text](readmeFiles/images/031.png)

e) Implantar e testar o modelo
![alt text](readmeFiles/images/032.png)
![alt text](readmeFiles/images/033.png)
--> A implantação leva entre 5 e 10 minutos
![alt text](readmeFiles/images/0034.png)

f) Testar o modelo
![alt text](readmeFiles/images/035.png)
--> Resultado do teste
O resultado indica a quantidade de bicicletas necessárias para atender à demanda de acordo com a data e as condições meterorógicas informadas
![alt text](readmeFiles/images/0036.png)
