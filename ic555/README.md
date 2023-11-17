# Circuito Oscilador com Timer

## Introdução

Neste projeto trabalharemos com um circuito oscilador e o IC 555 (Timer), que gera pulsos intermitentes de saída com base em unidades de tempo definidas pelos valores de resistores e capacitores. Este tipo de circuito é frequentemente utilizado para criar sinais de temporização, gerar pulsos, ou piscar LEDs em uma taxa ajustável.

## Projeto Esquemático

Neste circuito, o LED piscará intermitentemente com base no tempo definido pelos valores dos resistores R1 e R2, e do capacitor C1. O potenciômetro R2 permite ajustar o período de oscilação. Aqui estão alguns exemplos de cálculos de período:

a) Condição quando o potenciômetro é girado ao máximo para a esquerda (valor mínimo de R2): 

```
T = 0.693 * (10KΩ + 2 * 0Ω) * 10μF
T = 0.693 * 10KΩ * 10μF
T = 69.3ms
```

b) Condição quando o potenciômetro é girado para a posição intermediária:

```
T = 0.693 * (10KΩ + 2 * 50KΩ) * 10μF
T = 0.693 * 110KΩ * 10μF
T = 762.3ms
```

c) Condição quando o potenciômetro é girado ao máximo para a direita (valor máximo de R2):

```
T = 0.693 * (10KΩ + 2 * 100KΩ) * 10μF
T = 0.693 * 210KΩ * 10μF
T = 1448.7ms
```

### Lista de componentes 

- IC 555 Timer
- Resistor R1: 10KΩ
- Resistor R2: 100KΩ (Potenciômetro)
- Capacitor C1: 10uF/16V
- LED
- Resistor limitador de corrente para o LED
- Fonte de alimentação
- Conector de alimentação
- Conector de saída para o LED

- **Nota**: Certifique-se de verificar a polaridade correta do LED e do capacitor e conecte os pinos do IC 555 Timer de acordo com o modo astável.

### Cálculo do Período
O período do oscilador astável com o IC 555 Timer é determinado pela seguinte fórmula:

```
T = 0.693 * (R1 + 2 * R2) * C1
```

- T: Período em segundos
- R1: Resistor em ohms
- R2: Resistor (potenciômetro) em ohms
- C1: Capacitor em farads

## Tarefa: 

Utilize o software EasyEDA para projetar uma placa de circuito impresso (PCB) que acomode os componentes e facilite a montagem do circuito do oscilador com o IC 555.