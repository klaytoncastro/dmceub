# Projeto de PCB para Conversores Step Up, Step Down e Step Boost

## Introdução

Neste projeto trabalharemos com o desenvolvimento de PCBs para os tipos principais de conversores DC-DC: Step Up, Step Down e Step Boost. Esses circuitos são fundamentais em eletrônica de potência para alimentação de dispositivos que requerem tensões diferentes da fornecida pela fonte de alimentação. Cada tipo de conversor tem sua aplicação, desde aumentar a tensão de entrada (Step Up), reduzi-la (Step Down) ou combinar ambas as funções em diferentes cenários (Step Boost). 

## Projeto Esquemático

O design de cada conversor envolverá componentes específicos para manipular a tensão de entrada e alcançar a saída desejada. A seguir, os componentes principais e suas configurações para cada tipo de conversor:

### Step Up (Elevador)

O conversor Step Up aumenta a tensão de entrada para uma tensão de saída maior, mantendo a potência quase constante. A operação é controlada pelo IC1, que regula a abertura do transistor Q1 para armazenar energia no indutor L1 e transferi-la para a carga através do capacitor C1.

**Componentes principais:**

- L1: Indutor
- C1: Capacitor de saída
- D1: Diodo Schottky
- Q1: Transistor MOSFET
- R1: Resistor para feedback de tensão
- IC1: CI controlador de Boost

### Step Down (Redutor)

O conversor Step Down reduz a tensão de entrada para uma tensão de saída menor. A energia é armazenada no indutor L2 pelo fechamento do transistor Q2 e depois liberada para a carga. O IC2 regula esse processo para manter a tensão de saída desejada.

**Componentes principais**:

- L2: Indutor
- C2: Capacitor de saída
- D2: Diodo Schottky
- Q2: Transistor MOSFET
- R2: Resistor para feedback de tensão
- IC2: CI controlador de Buck

### Step Boost (Elevador-Redutor)

O conversor Step Boost pode aumentar ou diminuir a tensão de entrada conforme necessário. Sua operação depende do controle do IC3, que ajusta o ciclo de trabalho do transistor Q3 para alternar entre modos de elevação e redução, utilizando L3 e C3 para estabilizar a saída.

**Componentes principais**:

- L3: Indutor
- C3: Capacitor de saída
- D3: Diodo Schottky
- Q3: Transistor MOSFET
- R3: Resistor para feedback de tensão
- IC3: CI controlador de Boost-Buck

## O que é um Datasheet?

Um datasheet (folha de dados) é um documento técnico que contém informações detalhadas sobre um componente eletrônico, como um microcontrolador, resistor, capacitor, transistor, regulador de tensão, entre outros. Ele é fornecido pelo fabricante e serve como um guia essencial para engenheiros e projetistas de circuitos eletrônicos.

### Por que os Datasheets são Importantes?

- Especificações Técnicas – Contém informações como tensão de operação, corrente máxima, potência dissipada e faixas de temperatura de funcionamento, fundamentais para evitar danos ao componente.
- Pinos e Funcionalidade – Apresenta o pinout (mapa de pinos), detalhando quais são as funções de cada terminal do componente, evitando conexões erradas no circuito.
- Diagramas e Características Elétricas – Inclui gráficos de desempenho, curvas características, circuitos típicos de aplicação e requisitos elétricos.
- Tolerâncias e Limites Operacionais – Define os limites dentro dos quais o componente pode operar sem riscos de falha, como a máxima corrente suportada por um LED ou a tensão de ruptura de um transistor.
- Sugestões de Uso – Muitos datasheets fornecem circuitos de referência e sugestões para integração eficiente dos componentes em projetos.
- Dimensões e Layout de PCB – Contém o desenho mecânico do componente, essencial para projetar a footprint correta no CAD (como no EasyEDA).

### Exemplo de Aplicação
Ao projetar uma PCB no EasyEDA, você precisa escolher um regulador de tensão como o LM7805. O datasheet deste componente informará:

- O pino de entrada (Vin), de saída (Vout) e o terra (GND).
- A corrente máxima que ele pode fornecer sem superaquecer.
- A necessidade de dissipadores de calor dependendo da carga.
- O encapsulamento e footprint correto para a sua PCB.

Portanto, consultar datasheets evita erros de projeto e garante que os componentes sejam utilizados corretamente, assegurando eficiência e confiabilidade na placa de circuito impresso.

## Tarefa:

1) Pesquise sobre os CIs LM2596 e LM3862, verifique seus datasheets no site [www.alldatasheet.com](https://www.alldatasheet.com) e veja como podem ser utilizados para desenvolver um projeto de conversão de tensão. 

2) Utilize o software EasyEDA para projetar placas de circuito impresso (PCB) que acomodem os componentes para cada tipo de conversor. Considere a disposição eficiente dos componentes para minimizar interferências e perdas, bem como a implantação de LEDs para sinalizar a operação dos circuitos. 

3) Uma aplicação genérica como exemplo: 

<img src="/img/lm2596.png" alt="LM2596 - Conversor de tensão de saída ajustável">

<!-- XL6009 -->

<!-- <img src="/img/delay-timer-ic555.png" alt="Circuito Temporizador com Atraso"> -->

<!-- Este é um comentário que não será exibido na saída final. -->
