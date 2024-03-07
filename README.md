# AI-900: Trabalhando com Machine Learning na Prática no Azure ML
Utilização do serviço Aprendizado de Máquina do Azure para treinar e avaliar um modelo de aprendizado de máquina, seguido da implantação e teste do modelo treinado.

Neste exercício, foi utilizado um dataset público contendo o histórico de aluguel de bicicletas para treinar um modelo. Este modelo prevê o número de bicicletas necessárias em um determinado dia, com base em características sazonais e meteorológicas, para atender à demanda de locação.

# 1ª Etapa) Aprovisionar o serviço de Machine Learning

a) Acessar o Azure Machine Learning
<br><br>
![alt text](readmeFiles/gifs/001.gif)

b) Criar um Resource Group para armazenar o serviço
<br><br>
![alt text](readmeFiles/gifs/002.gif)

c) Inserir as configurações do Workspace
--> Informar apenas o campo Name
--> Para os demais, deixar os valores padrões
--> Na sequência, clicar em Review + create
<br><br>
![alt text](readmeFiles/images/003.png)

d) Criar o serviço
--> Aguardar a mensagem de validação, conforme imagem a baixo, e clicar em Create
<br><br>
![alt text](readmeFiles/images/004.png)


e) Aguardar a implantação do serviço
--> Quando a mesma estiver concluída, o status <i>Your deployment is complete</i> aparecerá na tela
--> Esta etapa leva alguns instantes para ser concluída
<br><br>
![alt text](readmeFiles/images/005.png)



# 2ª Etapa) Configurar os modelos de Machine Learning e os conjuntos de dados

a) Abrir o Machine Learning Studio
--> Durante o carregamento, pode ser solicitado, novamente, sua conta do Azure
<br><br>
![alt text](readmeFiles/gifs/006.gif)

b) Criar um Novo Trabalho de Machine Learning Automatizado
<br><br>
![alt text](readmeFiles/gifs/007.gif)

c) Preencher as configurações básicas
<br><br>
![alt text](readmeFiles/images/008.png)

d) Criar o tipo de tarefa
<br><br>
![alt text](readmeFiles/images/009.png)

e) Criar o ativo de dados
<br><br>
![alt text](readmeFiles/images/010.png)
<br><br>
![alt text](readmeFiles/images/011.png)
<br><br>
![alt text](readmeFiles/images/012.png)
<br><br>
![alt text](readmeFiles/images/013.png)
<br><br>
![alt text](readmeFiles/images/014.png)
<br><br>
![alt text](readmeFiles/images/015.png)
<br><br>
![alt text](readmeFiles/images/016.png)

f) Configurar tarefas
<br><br>
![alt text](readmeFiles/images/017.png)
<br><br>
![alt text](readmeFiles/images/018.png)
<br><br>
![alt text](readmeFiles/images/019.png)
<br><br>
![alt text](readmeFiles/images/020.png)

g) Configurar computação
<br><br>
![alt text](readmeFiles/images/021.png)

h) Enviar o trabalho para treinamento 
<br><br>
![alt text](readmeFiles/images/022.png)
--> Esta ação levará cerca de 15 minutos para ser finalizada
<br><br>
![alt text](readmeFiles/images/023.png)
--> Este é o status que indica a conclusão do treinamento
<br><br>
![alt text](readmeFiles/images/004.png)


# 3ª Etapa) Analisar e Testar do Modelo

a) Checar a integridade dos dados
<br><br>
![alt text](readmeFiles/images/025.png)

b) Checar a conclusão de todas as tarefas
<br><br>
![alt text](readmeFiles/images/026.png)

c) Identificar o melhor modelo do treinamento
![alt text](readmeFiles/images/027.png)

d) Checar as métricas deste modelo
<br><br>
![alt text](readmeFiles/images/028.png)
--> As métricas mais importantes são: predicted_true e residuals
<br><br>
![alt text](readmeFiles/images/029.png)
--> predicted_true: O gráfico predicted_true compara os valores previstos com os valores verdadeiros.
<br><br>
![alt text](readmeFiles/images/030.png)
--> residuals: O gráfico de resíduos mostra os resíduos (as diferenças entre os valores previstos e reais) como um histograma
<br><br>
![alt text](readmeFiles/images/031.png)

e) Implantar e testar o modelo
<br><br>
![alt text](readmeFiles/images/032.png)
<br><br>
![alt text](readmeFiles/images/033.png)
--> A implantação leva entre 5 e 10 minutos
![alt text](readmeFiles/images/0034.png)

f) Testar o modelo
<br><br>
![alt text](readmeFiles/gifs/035.gif)
--> Resultado do teste
O resultado indica a quantidade de bicicletas necessárias para atender à demanda de acordo com a data e as condições meterorógicas informadas
<br><br>
![alt text](readmeFiles/images/036.png)


# 4ª Etapa) Limpar o ambiente

É necessário excluir todos os recursos e grupos de recursos após a conclusão deste exercício para que não haja cobranças indevidas no Azure
