# Projeto de PCB para Amplificador de Áudio com TDA2003

## Introdução

O objetivo deste projeto é desenvolver o design de uma PCB utilizando o TDA2003, um amplificador de potência ideal para aplicações de áudio, especialmente em automóveis. Este CI é conhecido por sua alta eficiência e baixo ruído.

### Componentes Principais

- *TDA2003:* Amplificador de potência para áudio.
- *C1 (10µF):* Capacitor de acoplamento de entrada.
- *C2 (100µF):* Capacitor de desacoplamento de alimentação.
- *C3 (100nF):* Capacitor de desacoplamento de alta frequência.
- *C4 (1000µF):* Capacitor de filtro de saída.
- *C5 (100nF):* Capacitor de bypass de alta frequência.
- *C6 (470µF):* Capacitor de feedback.
- *C7 (39nF):* Capacitor de filtro de alta frequência.
- *R1 (1Ω), R2 (220Ω), R3 (2.2Ω), R4 (39Ω):* Resistores para ajuste de ganho e resposta em frequência.
- *Conectores:* Para alimentação (POWER), entrada de áudio (A-IN) e saída para alto-falante (SPEAKER).

### Diagrama Esquemático:

- *VCC:* Conectar ao pino de alimentação do TDA2003.
- *GND:* Conectar ao pino de terra do TDA2003.
- *SCL:* Conectar ao pino de controle do microcontrolador (se houver).
- *SDA:* Conectar ao pino de controle do microcontrolador (se houver).
- *VIN+ e VIN-:* Conectar à carga cuja corrente será medida.
- *Alimentação:* Conectar os pinos de 5V e GND.
- *I2C:* Conectar SCL e SDA aos pinos correspondentes do INA219.

<!--Display (opcional):* Conectar aos pinos adequados para exibição dos dados.-->

## Tarefa

- Utilize o EasyEDA para desenhar o esquemático conforme o diagrama fornecido.
- Considere a disposição eficiente dos componentes para minimizar interferências e perdas, e a implementação de LEDs para sinalizar a operação dos circuitos.
- Converta o esquemático em layout de PCB e posicione os componentes na PCB de forma otimizada.
- Conecte os componentes utilizando trilhas adequadas.

<img src="/img/tda2003.jpeg" alt="Amplificador de Áudio com TDA2003">

<!--

https://www.youtube.com/watch?app=desktop&v=1e4lOJeqAc8

-->