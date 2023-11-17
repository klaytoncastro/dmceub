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

### Operação do IC 555

O IC 555 é um componente versátil que pode operar em diferentes modos para atender às necessidades de temporização e oscilação em projetos eletrônicos. A escolha do modo depende da aplicação específica e dos requisitos de temporização do circuito. Na tabela abaixo, temos a pinagem que define o modeo de operação do IC 555: 

| Terminal | Nome            | Aplicação                                           |
|----------|-----------------|-----------------------------------------------------|
| 1        | GND             | Terra (ground)                                     |
| 2        | TRIG, TR        | Gatilho ou disparo (trigger) - Ativa o biestável interno e a saída com um valor de tensão baixo (menos de 1/3 de VCC). |
| 3        | OUT             | Saída (output) - Mantém-se em +VCC durante um intervalo de tempo. |
| 4        | RESET, R, RST   | Reinício (reset) - Permite interromper um intervalo de temporização com um pulso de reinício. |
| 5        | CTRL, CONT, CV  | Tensão de controle (control voltage) - Possibilita o acesso ao divisor interno de tensão (2/3 de VCC). |
| 6        | TH, THR, THRES  | Limiar ou Limite (threshold) - Desativa o biestável interno e a saída com um valor de tensão alto (mais de 2/3 de VCC). |
| 7        | DIS, DISCH      | Descarga (discharge) - Utilizado para descarregar o capacitor conectado a este terminal. |
| 8        | VCC, V+         | Tensão positiva da fonte - Deve estar entre +5V e +15V. |

- **Modo Astável**:

No modo astável, o IC 555 é configurado como um oscilador de forma livre, gerando uma saída periódica que alterna entre estados alto e baixo. Este modo é usado para criar sinais de pulso contínuos, como os usados em piscadores de LEDs, geradores de tom e temporizadores intermitentes. A frequência do sinal de saída é determinada pelos valores dos resistores e capacitores conectados ao circuito. O pino 4 (RESET) é geralmente não conectado, o que permite a operação contínua do oscilador.

- **Modo Monoestável**:

No modo monoestável, o IC 555 é configurado como um temporizador de disparo único. Ele produz um pulso de saída após receber um gatilho externo. Este modo é usado para criar atrasos controlados em resposta a um evento de gatilho externo. O pino 4 (RESET) é frequentemente conectado ao VCC para desativar a função de reinício.

- **Modo Biestável (Flip-Flop)**:

No modo biestável, o IC 555 é configurado como um flip-flop, onde ele possui dois estados estáveis: alto e baixo. Ele é usado para criar uma lógica de comutação simples, onde a saída alterna entre estados alto e baixo em resposta a um gatilho externo. O estado de saída é alterado quando um gatilho externo é aplicado ao pino 2 (TRIG), ou o pino 4 (RESET) é usado para redefinir o estado. Este modo é frequentemente usado em aplicações de chaveamento e circuitos de controle de lógica simples.


## Tarefa: 

Utilize o software EasyEDA para projetar uma placa de circuito impresso (PCB) que acomode os componentes e facilite a montagem do circuito do oscilador com o IC 555.