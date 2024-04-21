# Projeto de PCB para Amplificador de Áudio

## Introdução

O objetivo é desenvolver o design de uma PCB utilizando o popular LM386, um amplificador de potência versátil e de baixo custo projetado para aplicações de áudio. 

## Componentes Principais

- LM386: Amplificador de áudio de baixa potência.
- C1, C2: Capacitores para estabilização da alimentação e saída.
- R1: Resistor para definir o ganho.
- C3: Capacitor de entrada de áudio.
- Potenciômetro (POT): Para controle de volume.
- C4: Capacitor de desacoplamento.
- Alto-falante: Para a saída de áudio.

## Diagrama Esquemático

- Conecte o pino 2 (inversor) do LM386 ao terra (GND) através de C1.

- O sinal de áudio de entrada é aplicado ao pino 3 (não inversor) através de C3 e do potenciômetro para controle de volume.

- R1 e C2 são conectados entre os pinos 1 e 8 para definir o ganho do amplificador.

- O pino 5 é a saída de áudio, que é conectada ao alto-falante através de C4.

- Os pinos 4 e 6 são respectivamente as conexões de terra (GND) e alimentação (VCC).

## Tarefa:

Consulte o datasheet do LM386 e verifique como pode ser utilizado para desenvolver o projeto. Utilize o software EasyEDA para projetar placas de circuito impresso (PCB) que acomodem os componentes. Considere a disposição eficiente para minimizar interferências e perdas, bem como a implantação de LEDs para sinalizar a operação dos circuitos. 