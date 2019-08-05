# Atulalizar Frimware do modulo ESP8266-01

**Materiais necessários**

​	*1 placa arduino UNO*

​	*1 modulo ESP8266-01*

​	*8 Jumpers M-M*



**Softwares e Arquivos necessários**

​	*esp8266_flasher.exe*

​	*AI-v0.9.5.0 AT Firmware*

​	*Arduino IDE*



**Procedimento**

1º Remover micro controlador do arduino UNO, usaremos ele como se fosse uma placa FTDI para gravarmos o frimware no modulo

2º Faça as ligações do arduino com fome imagem abaixo

![](<https://github.com/gabrielmarini/Arduino-ESP8266-01/blob/master/Circuito.png>)



3.3v do arduino no barramento positivo da protoborad

GND do arduino no barramento negativo da protoboard

RX do arduino (0) no RX do modulo ESP

TX do arduino (1) no TX do modulo ESP

GND do modulo ESP no barramento negativo da protoboard

VCC do modulo ESP no barramento positivo da protoborad

CH do modulo ESP no barramento positivo da protoboard

GPIO 0 do modulo ESP no barramento negativo da protoborad



3º Abra o esp8266_flasher e selecione o arquivo Bin e a porta ao qual o arduino está conectado ao computador, para verificar qual porta o arduino está conectado você pode abrir a IDE e verificar no menu Ferramentas > Porta

![](<https://github.com/gabrielmarini/Arduino-ESP8266-01/blob/master/Flash-Downloader.PNG>)

4º Clique em download e espere o procedimento de gravação acabar, pronto Frimware  atualizado!



Para testar se a atualização foi realizada  com sucesso, desligue o arduino do PC e remova o pino GPIO 0 do barramento negativo, ligue o arduino novamente no PC, abra a IDE e logo após o monitor serial com a velocidade de 9600 e digite o comando AT

![](<https://github.com/gabrielmarini/Arduino-ESP8266-01/blob/master/Comando.PNG>)

