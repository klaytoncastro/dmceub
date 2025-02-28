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

## Regulador LM2596

O **LM2596** é um regulador de tensão monolítico integrado ideal para o design de conversores step-down (Buck). Ele pode fornecer uma carga de **3,0 A** com excelente regulação de linha e carga. Opera a **150 kHz**, permitindo componentes de filtro menores em comparação com reguladores de menor frequência.

### Principais Características:
- Faixa de Saída Ajustável: **1.23 V – 37 V**
- Corrente de Saída Garantida: **3.0 A**
- Faixa de Entrada: **até 40 V**
- Oscilador Interno de **150 kHz**
- Proteções Contra Superaquecimento e Limite de Corrente
- Operação em Modo Standby de **80 µA**

## Tarefa:
1) Pesquise sobre o CIs **LM2596** e veja como podem ser utilizados para desenvolvimento de conversores de tensão.
2) Utilize o **EasyEDA** para projetar as PCBs.
3) Como exemplo, segue abaixo uma aplicação típica para conversão de saída com LM2596:  

<!--
 e **LM3862** pesquisa
-->

![LM2596 - Conversor de tensão de saída ajustável](/img/lm2596.png)
