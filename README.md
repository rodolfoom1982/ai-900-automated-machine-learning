# AI-900: Trabalhando com Machine Learning na Prática no Azure ML
Utilização do serviço Aprendizado de Máquina do Azure para treinar e avaliar um modelo de aprendizado de máquina, seguido da implantação e teste do modelo treinado.

Neste exercício, foi utilizado um dataset público contendo o histórico de aluguel de bicicletas para treinar um modelo. Este modelo prevê o número de bicicletas necessárias em um determinado dia, com base em características sazonais e meteorológicas, para atender à demanda de locação.

## 1ª Etapa) Aprovisionar o serviço de Machine Learning

1) Acessar o Azure Machine Learning:
<br><br>
![alt text](readmeFiles/gifs/001.gif)

2) Criar um Resource Group para armazenar o serviço:
<br><br>
![alt text](readmeFiles/gifs/002.gif)

3) Inserir as configurações do Workspace
<br>&emsp;*- Informar apenas o campo **Name***
<br>&emsp;*- Para os demais, deixar os valores padrões*
<br>&emsp;*- Na sequência, clicar em **Review + create***
<br><br>
![alt text](readmeFiles/images/003.png)

4) Criar o serviço:
<br>&emsp;*- Aguardar a mensagem de validação, conforme imagem a baixo, e clicar em **Create***
<br><br>
![alt text](readmeFiles/images/004.png)


5) Aguardar a implantação do serviço:
<br>&emsp;*- Quando a mesma estiver concluída, o status **Your deployment is complete** aparecerá na tela*
<br>&emsp;*- Esta etapa leva alguns instantes para ser concluída*
<br><br>
![alt text](readmeFiles/images/005.png)



## 2ª Etapa) Configurar os modelos de Machine Learning e os conjuntos de dados

1) Abrir o Machine Learning Studio
<br>&emsp;***Atenção:** Durante o carregamento, pode ser solicitado, novamente, sua conta do Azure*
<br><br>
![alt text](readmeFiles/gifs/006.gif)

2) Criar um Novo Trabalho de Machine Learning Automatizado
<br><br>
![alt text](readmeFiles/gifs/007.gif)

3) Preencher as configurações básicas:
<br><br>
![alt text](readmeFiles/images/008.png)

4) Criar o tipo de tarefa:
<br><br>
![alt text](readmeFiles/images/009.png)

5) Criar o ativo de dados:
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

6) Configurar tarefas:
<br><br>
![alt text](readmeFiles/images/017.png)
<br><br>
![alt text](readmeFiles/images/018.png)
<br><br>
![alt text](readmeFiles/images/019.png)
<br><br>
![alt text](readmeFiles/images/020.png)

7) Configurar computação:
<br><br>
![alt text](readmeFiles/images/021.png)

8) Enviar o trabalho para treinamento:
<br><br>
![alt text](readmeFiles/images/022.png)
<br>&emsp;*- Esta ação levará cerca de 15 minutos para ser finalizada*
<br><br>
![alt text](readmeFiles/images/023.png)
<br>&emsp;*- Este é o status que indica a conclusão do treinamento*
<br><br>
![alt text](readmeFiles/images/004.png)


## 3ª Etapa) Analisar e Testar do Modelo

1) Checar a integridade dos dados:
<br><br>
![alt text](readmeFiles/images/025.png)

1) Checar a conclusão de todas as tarefas:
<br><br>
![alt text](readmeFiles/images/026.png)

3) Identificar o melhor modelo do treinamento:
![alt text](readmeFiles/images/027.png)

4) Checar as métricas deste modelo:
<br><br>
![alt text](readmeFiles/images/028.png)
<br>&emsp;*- As métricas mais importantes são: **predicted_true** e **residuals***
<br><br>
![alt text](readmeFiles/images/029.png)
<br>&emsp;*- **predicted_true**: O gráfico predicted_true compara os valores previstos com os valores verdadeiros.*
<br><br>
![alt text](readmeFiles/images/030.png)
<br>&emsp;*- **residuals:** O gráfico de resíduos mostra os resíduos (as diferenças entre os valores previstos e reais) como um histograma*
<br><br>
![alt text](readmeFiles/images/031.png)

5) Implantar e testar o modelo
<br><br>
![alt text](readmeFiles/images/032.png)
<br><br>
![alt text](readmeFiles/images/033.png)
<br>&emsp;*- A implantação leva entre 5 e 10 minutos*
![alt text](readmeFiles/images/0034.png)

6) Testar o modelo
<br><br>
![alt text](readmeFiles/gifs/035.gif)
<br>&emsp;*- Resultado do teste*
<br>&emsp;*- O resultado indica a quantidade de bicicletas necessárias para atender à demanda de acordo com a data e as condições meterorógicas informadas*
<br><br>
![alt text](readmeFiles/images/036.png)


## 4ª Etapa) Limpar o ambiente

É necessário excluir todos os recursos e grupos de recursos após a conclusão deste exercício para que não haja cobranças indevidas no Azure
