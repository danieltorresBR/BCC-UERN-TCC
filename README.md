---
__

# BCC-UERN-TCC 8-)
Repositório destinado ao versionamento da implementação lógica do Robô que dará origem ao TCC da Graduação em CC. 

Foram utilizados até o momento (26/06/2022):

 - 1 Arduino Uno – placa de microcontrolador baseado no ATmega328, com 14 pinos de entradas/saídas digitais, 6 entradas analógicas e conexão USB;
 - 5 Matriz de LEDs 8×8 com [driver MAX7219](http://pdfserv.maximintegrated.com/en/ds/MAX7219-MAX7221.pdf);
 - Jumpers fêmea-fêmea;
 - Jumpers macho-fêmea;
 - 1 computador (para compilar e fazer o upload do código para o Arduino);

Programação feita na IDE Arduino 1.8.19, onde foi necessário adicionar a biblioteca [LedControl.h](https://github.com/wayoda/LedControl)

---
Detalhes para executar o projeto:

#### Aplicação Python:
Crie um ambiente virtual
```
virtualenv .vozes
```
Ative o ambiente virtual
```
.\.vozes\Scripts\activate 
```
Instale os requirements
```
pip freeze > requirements.txt
```

___

#### Aplicação Arduino:

Por meio da IDE arduino, envie o código para a placa.
___
#### Detalhes Gerais:

A aplicação python deve ser executada de forma concomitante com a aplicação arduino. Entretanto, a aplicação arduino deve ser a primeira a ser executada e imediatamente depois a aplicação python deve ser iniciada.

A ordem de execução das aplicação é de fundamental importância, pois se forem executadas em ordem diferente da descrita os seguintes erros podem acontecer:

Se python for executado antes do arduino:
* será gerado um erro na porta serial causado quando o arduino tentar utilizar a porta serial que já vai está em uso no Python;


Se o python demorar a ser executado:
* será gerado um erro de sincronia na execução das vozes.

mais detalhes podem ser obtidos entrando em contado com <danieltorres@alu.uern.br> ou <danielteodolino@gmail.com> ou <raulparadeda@uern.br>
___

# In English:

## BCC-UERN-TCC 8-)
Repository intended for versioning the logical implementation of the Robot that will give rise to the TCC of the Graduation in Computer Science.

Was used:

 - 1 Arduino Uno – microcontroller board based on the ATmega328, with 14 digital input/output pins, 6 analog inputs and USB connection;
 - 5 8×8 LED matrix with [MAX7219 driver](http://pdfserv.maximintegrated.com/en/ds/MAX7219-MAX7221.pdf);
 - Female-female jumpers;
 - Male-female jumpers;
 - 1 computer (to compile and upload the code to the Arduino);

Programming done in the Arduino IDE 1.8.19, where it was necessary to add the library [LedControl.h](https://github.com/wayoda/LedControl)

---
Details to run the project:

#### Python application:
Create a virtual environment
```
virtualenv .voices
```
Activate the virtual environment
```
.\.voices\Scripts\activate
```
Install the requirements
```
pip freeze > requirements.txt
```

___

#### Arduino application:

In the arduino IDE, send the code to the board.
___
#### General Details:

The python application must run concurrently with the arduino application. However, the arduino application must be the first to be executed and immediately after that the python application must be started.

The execution order of the applications is of fundamental importance, because if they are executed in a different order than the one described, the following errors may occur:

If python runs before arduino:
* an error will be generated in the serial port caused when the arduino tries to use the serial port that is already in use in Python;


If python takes time to run:
* a sync error will be generated when executing the voices.

more details can be obtained by contacting <danieltorres@alu.uern.br> or <danielteodolino@gmail.com> or <raulparadeda@uern.br>