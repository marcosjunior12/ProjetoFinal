# ProjetoFinal
 Bem vindo ao projeto "Smart Switch", nesse repositório você encontrara os códigos gravados no ESP01 para permitir que fosse executadas todas as funcionalidades propostas, além de esquemáticos que representam a parte física do projeto que pode ser utilizado por pessoas que quiserem reproduzir nossa idéia.
 
 Esse projeto consiste em uma caixa térmica que será usada para esquentar animais que não podem ter exposições a temperaturas muito baixas. Ele irá funcionar da seguinte maneira:
 - O DHT 11 irá monitorar a temperatura e umidade do ambiente e enviará os dados para o nosso servidor MQTT
 - Uma equipe especializada irá monitorar esses dados, quando a temperatura estiver baixa a lâmpada será acionada para que se inicie o aquecimento
 - A lâmpada poderá ser acionada através de comandos enviados para o broker MQTT ou através da dashboard configurada para celulares Android
 - Após o acionamento da lâmpada, as temperaturas continuarão sendo lidas pelo DHT 11, assim, quando atingir a temperatura ideal a lâmpada poderá ser desligada por quem estiver realizando o monitoramento.
 
 
 <b> MATERIAIS UTILIZADOS:</B>
 -ESP8266 (Versão ESP-01):
  -É um microcontrolador com capacidade de conexão WIFI, sendo que não necessita nenhum módulo externo para conectar com a rede sem fio. O chip é de baixo custo e é encontrado soldado em módulos com a 

 
 
