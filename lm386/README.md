<!--

https://www.ti.com/lit/ds/symlink/lm386.pdf



https://blog.novaeletronica.com.br/lm386-o-pequeno-grande-amplificador/

LM386 – O pequeno Grande Amplificador

O LM386 , também conhecido com JRC386 é um dos circuitos integrados amplificadores mais usados, a razão é bem simples, sua versatilidade, baixo custo e consumo. Um amplificador, como o próprio nome diz,  amplifica, aumenta o sinal em x vezes, dependendo de sua configuração, no caso do LM386,  é um amplificador de áudio. Ele é bem diferente dos amplificadores operacionais como o LM741, esses tem exigências diferentes de configuração e uso, já o LM386 é um amplificador de áudio nato, ou seja ele foi projetado para ser um amplificador de áudio.

Marshall 

Para se ter ideia da grandiosidade do LM386, o maior e melhor fabricante de amplificadores, a Marshall, utiliza em seus a amplificadores miniatura modelo MS-2 e MS-4  como saída um circuito integrado NJM386 fabricado pela CCI.

LM386

Características do LM386

O LM386 é um amplificador de potência projetado para uso em aplicações de baixo consumo e baixa tensão. Sua configuração de amplificador é de  Classe AB,  ele consiste em um CI de 8 pinos duplo em linha, DIP-8, com 3 tipos básicos que são  LM386N-1 , LM386N-3 e LM386N-4 , o mais comum desses é o LM386N-1. O ganho é fixado internamente em 20 vezes por razões técnicas, mas a adição de uma resistência externa ou um  capacitor entre os pinos 1 e 8 irá aumentar o ganho de saída em até 200 vezes.

A corrente de repouso é bem baixa, consumindo menos de 30mW com alimentação de 5 Volts, o que o torna ideal para circuitos alimentados por pilhas ou baterias. Chamado de CI de amplificador de potência de baixa tensão, ele foi considerado a joia para projetos amadores onde se precisa de um bom amplificador de áudio com a vantagem de ter poucos componentes , baixo consumo e baixa tensão.

circuito interno equivalente ao lm386

Sua resistência de entrada é de 50k OHMs e a impedância de saída é de 8 OHMs nas versões  LM386N-1  e LM386N-3 e 32 OHMs na versão LM386N-4. O consumo de corrente de repouso é se 4mA  e a sua  distorção é muito baixa, 0,2% (AV = 20, VS = 6V, RL = 8 [Ohm], PO = 125mW, f = 1 kHz) .

Pinagem do LM386
pinagem lm386

Pino 1: Ganho
Pino 2: Entrada –
Pino 3: Entrada +
Pino 4 : Terra
Pin 5: Vout (Saída)
Pino 6 : Vs (Power )
Pino 7 : Bypass
Pino 8 : Ganho

Os pinos 1 e 8 são de controle de ganho. Quando não estiver conectado (NC), o ganho do amplificador é de 20 vezes. Adicionando um capacitor 10uF entre eles o ganho passa a 200 vezes. Valores intermediários e um resistor vão variar o ganho como descrito no datasheet,  veremos abaixo.

O pino 2 é a entrada negativa (GND)  geralmente vai a terra ou – .

O pino 3 é a entrada positiva ou seja, a entrada do sinal  para ser amplificado. Um potenciômetro 10K Ohms antes do pino que ajusta o nível de sinal de entrada, ou seja, um controle de volume.

O Pino  4 (GND – Terra) e o pino 6  (Vs +VCC)  são as entradas de alimentação para a amplificação, um capacitor eletrolítico de no minimo 100uF entre eles perto do CI evita oscilações indesejadas.

O pino 5 é a saída do amplificador. O capacitor eletrolítico de 250uF filtra o componente DC e os restantes AC vam para o alto-falante. Um capacitor de 0.05uF e um resistor de 10 ohm  do pino 5 para o terra  é usado para evitar oscilações de alta frequência.

O pino 7 é chamado de bypass (desvio) , mas a folha de dados não fornece qualquer detalhe adicional sobre ele ou seu uso. Mas tecnicamente serve para diminuir o ruido ( zumbido ) de entrada e também diminuir a distorção de
inter-modulação. Ele isola o estágio de entrada de alto ganho do ruído da fonte de alimentação. Um capacitor de de 100nF a 10uF podem ser usados nesse pino.

Abaixo temos uma tabela com as características principais dos tipos de LM386
Chip Nome	Min Tensão	Max Tensão	Energia mínima de saída	 Potência
LM386N-1	4 Volts	12 Volts	250 mW	325 mW
LM386N-3	4 Volts	12 Volts	500 mW	700 mW
LM386N-4	5 Volts	18 Volts	700 mW	1.000 mW
 

Circuito típico do amplificador LM386 com ganho de 20 Vezes
LM386 ganho 20x

Abaixo um circuito amplificador usando o LM386 com ganho de 20 Vezes, requer o minimo de componentes externos, isso o torna compacto e simples.

Circuito típico do amplificador LM386 com ganho de 50 Vezes
 

LM386 ganho 50x

Esse é o esquema do LM386 para um ganho de 50 vezes, além do capacitor entre o pino 1 e 8 é usado um resistor de 1K2 Ohms para limitar o ganho. Outra mudança é a colocação de um capacitor  para o terra no pino 7 que é o ByPass para evitar instabilidades no circuito, isso deve ser feito sempre que o ganho for maior que 20 vezes.

Circuito típico do amplificador LM386 com ganho de 200 Vezes
 

LM386 ganho 200x

Variando o ganho do LM386
Para fazer com que o LM386 seja amplificador mais versátil, os dois pinos 1 e 8 são usados para controle de ganho. Com os pinos 1 e 8 aberto, sem componente algum o ganho e de 20 vezes ou 26 dB. Mas se um capacitor é colocado entre os pino 1 a 8, a configuração interna é ignorada, e o ganho vai subir para 200 vezes ou 46 dB. Se colocarmos um resistor em série com o capacitor, o ganho pode ser ajustado para qualquer valor de 20x e 200x.

Vemos que o LM386 é um circuito integrado amplificador ideal para montagens amadoras e profissionais. Ele é um CI que não deve faltar na bancada, e junto com o 555 faz um par perfeito de componentes multiuso.

-->

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