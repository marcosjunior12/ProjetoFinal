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
 - Sensor de Umidade e Temperatura DHT11: Esse sensor permite fazer leituras de temperaturas entre 0 a 50 graus celsius e uma umidade entre 20 a 90%.<br> 
 <b><H1>MÉTODOS UTILIZADOS: </B></H1>
 - Protocolo MQTT: É um protocolo de mensagens destinado a sensores e pequenos dispositivos móveis, seu principal uso é fazer as máquinas trocarem informações, conhecido como Machine-to-machine. Foi inicialmente desenvolvido pela IBM no final dos anos 90, e sua finalidade original era conectar sensores de satélites ou pipelines de petróleo. 
Seu funcionamento é simples, o publicador envia a mensagem ao broker, que enfileira e dispara as informações recebidas aos assinantes (que podem ser diversos aparelhos). Será utilizada a plataforma gratuita “Cloud MQTT”.
-  Nesse projeto será utilizado da seguinte forma:
   - As informações de temperatura e umidade obtidas pelo DHT11 serão mostradas na interface do Cloud MQTT, que serão utilizadas apenas para monitorar essas informações.
   - A lâmpada conectada com o ESP8266 irá receber um subscribe do MQTT broker
   - O interruptor comum irá fazer um Publish no MQTT broker para poder comandar o estado a lâmpada
   - O smartphone android irá receber um subscribe do MQTT broker para saber qual é o status da lâmpada (apagada ou acesa), mas também irá fazer um publish  para poder controlar a lâmpada.
- Gravação do Firmware:
   - Para gravar o firmware no ESP 01, foi utilizado o módulo FTDI para possibilitar a comunicação do ESP com o computador. É importante ressaltar que para o ESP 01 entrar em modo de gravação, é necessário que o pino GPIO0 esteja conectado ao terra, após a gravação estar completa, não é necessário que esse pino esteja conectado.
- Leitura da umidade e temperatura pelo DHT11:
   - O DHT11 pode ser alimentado por uma fonte de 3 até 5V, conectado pelo seu pino VCC (positivo), ground (negativo) e o seu pino de dados, que é conectado ao pino GPIO 2 do ESP 01
- Acionamento do relé:
  - O relé deve ser alimentado por uma fonte de energia de 5V para que seu funcionamento seja correto. Esse objeto, de um lado, possui 3 conectores e do outro lado possui 3 pinos de saídas digitais que serão explicados abaixo:
   - Entrada: É por onde a energia elétrica entra.
   - Normalmente fechada: Significa que quando o relé está desativado, a energia está entrando pelo conector de entrada e saindo pelo conector normalmente fechado.
   - Normalmente aberta: Após o acionamento do relé, ele inverte o conector de saída da energia. Ou seja, a energia está saindo pelo conector normalmente fechado.
   - VCC: o pino positivo é ligado na alimentação de 5V para o funcionamento correto do relé.
   - GND: É ligado ao aterramento do sistema.
   - IN: É um pino que ligado ao ESP 01, controla o ativamento do relé, neste projeto ele é ligado ao transistor 2N2222, pois esse transistor foi utilizado como uma chave para o acionamento do relé.
 <br> <h2> Você pode encontrar todo o detalhamento de como as peças foram interligadas na aba <a href=https://github.com/marcosjunior12/ProjetoFinal/tree/master/Esquemáticos> ""Esquemáticos"</a></h2><br>
 
