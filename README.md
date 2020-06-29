# ProjetoFinal
 Bem vindo ao projeto "Smart Switch", nesse repositório você encontrara os códigos gravados no ESP01 para permitir que fosse executadas todas as funcionalidades propostas, além de esquemáticos que representam a parte física do projeto que pode ser utilizado por pessoas que quiserem reproduzir nossa idéia.
 
 Esse projeto consiste em uma caixa térmica que será usada para esquentar animais que não podem ter exposições a temperaturas muito baixas. Ele irá funcionar da seguinte maneira:
 - O DHT 11 irá monitorar a temperatura e umidade do ambiente e enviará os dados para o nosso servidor MQTT
 - Uma equipe especializada irá monitorar esses dados, quando a temperatura estiver baixa a lâmpada será acionada para que se inicie o aquecimento
 - A lâmpada poderá ser acionada através de comandos enviados para o broker MQTT ou através da dashboard configurada para celulares Android
 - Após o acionamento da lâmpada, as temperaturas continuarão sendo lidas pelo DHT 11, assim, quando atingir a temperatura ideal a lâmpada poderá ser desligada por quem estiver realizando o monitoramento.
 
 
 <b><h1> MATERIAIS UTILIZADOS:</B></h1>
 - ESP8266 (Versão ESP-01):É um microcontrolador com capacidade de conexão WIFI, sendo que não necessita nenhum módulo externo para conectar com a rede sem fio. O chip é de baixo custo e é encontrado soldado em módulos com a antena ou em kits separados de desenvolvimento. Tem o seu funcionamento muito parecido com o do arduino, porém com a vantagem de já possuir o wifi integrado e ter um poder de processamento maior.
 - Fonte de Alimentação:Foi utilizada uma fonte ajustável para Protoboard HW 131. Essa fonte possui uma tensão de entrada de 7,5 a 12V e uma tensão de saída de 3,3 e 5v.
 - Resistores: São componentes eletrônicos que resistem à passagem de corrente elétrica, ou seja, quando são inseridos ocorre uma diminuição na intensidade da corrente elétrica, evitando que o dispositivo queime.
 - Transistor 2N2222: É um transistor de baixa potência e possui polaridade NPN (sinal de saída negativo), é utilizado em muitos projetos que não necessitam de corrente alta, suportando tensões de até 50V e correntes de até 1A.
 - Módulo FTDI: Esse módulo funciona como um conversor, convertendo de USB para serial. Assim, permitindo a comunicação de dispositivos como o ESP 01 com computadores através da porta USB. Possui uma tensão de saída selecionável de 3.3 ou 5v.
 - Módulo relé: São componentes eletromecânicos, ou seja, possuem uma parte elétrica e outra mecânica. São muito utilizados para acionar cargas maiores do que a tensão do microcontrolador. Utilizaremos ele para ligar e desligar a lâmpada, sendo controlado pelo ESP 01.
 - Protoboard: É uma placa pequena que possui trilhas de alimentação que estão interligadas entre si na vertical.
 - Sensor de Umidade e Temperatura DHT11: Esse sensor permite fazer leituras de temperaturas entre 0 a 50 graus celsius e uma umidade entre 20 a 90%.
 <br> <h2> Você pode encontrar todo o detalhamento de como as peças foram interligadas na aba "Esquemáticos"</h2>
 
