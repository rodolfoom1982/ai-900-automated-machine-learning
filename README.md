# AI-900: Trabalhando com Machine Learning na Prática no Azure ML
Utilização do serviço Aprendizado de Máquina do Azure para treinar e avaliar um modelo de aprendizado de máquina, seguido da implantação e teste do modelo treinado.

Neste exercício, foi utilizado um dataset público contendo o histórico de aluguel de bicicletas para treinar um modelo. Este modelo prevê o número de bicicletas necessárias em um determinado dia, com base em características sazonais e meteorológicas, para atender à demanda de locação.

# 1ª Etapa) Aprovisionar o serviço de Machine Learning

a) Acessar o Azure Machine Learning
<br><br>
001

b) Criar um Resource Group para armazenar o serviço
002

c) Inserir as configurações do Workspace
--> Informar apenas o campo Name
--> Para os demais, deixar os valores padrões
--> Na sequência, clicar em Review + create
003

d) Crear o serviço
--> Aguardar a mensagem de validação, conforme imagem a baixo, e clicar em Create
004


e) Aguardar a implantação do serviço
--> Quando a mesma estiver concluída, o status <i>Your deployment is complete</i> aparecerá na tela
--> Esta etapa leva alguns instantes para ser concluída
005



# 2ª Etapa) Configurar os modelos de Machine Learning e os conjuntos de dados

a) Abrir o Machine Learning Studio
--> Durante o carregamento, pode ser solicitado, novamente, sua conta do Azure
006

b) Criar um Novo Trabalho de Machine Learning Automatizado
007

c) Preencher as configurações básicas
008

d) Criar o tipo de tarefa
009

e) Criar o ativo de dados
010 até 016

f) Configurar tarefas
017 a 020

g) Configurar computação
021

h) Enviar o trabalho para treinamento 
022
--> Esta ação levará cerca de 15 minutos para ser finalizada
023
--> Este é o status que indica a conclusão do treinamento
024


# 3ª Etapa) Analisar e Testar do Modelo

a) Checar a integridade dos dados
025

b) Checar a conclusão de todas as tarefas
026

c) Identificar o melhor modelo do treinamento
027

d) Checar as métricas deste modelo
028
--> As métricas mais importantes são: predicted_true e residuals
029
--> predicted_true: O gráfico predicted_true compara os valores previstos com os valores verdadeiros.
030
--> residuals: O gráfico de resíduos mostra os resíduos (as diferenças entre os valores previstos e reais) como um histograma
031

e) Implantar e testar o modelo
032
033
--> A implantação leva entre 5 e 10 minutos
034

f) Testar o modelo
035
--> Resultado do teste
O resultado indica a quantidade de bicicletas necessárias para atender à demanda de acordo com a data e as condições meterorógicas informadas
036
