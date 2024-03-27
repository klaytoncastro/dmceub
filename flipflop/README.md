# Design PCB: Flip–Flop

## Introdução

Um flip-flop é um circuito eletrônico feito com 2 ou mais LEDs, que ligam e desligam alternadamente com base em unidades de tempo, quando uma fonte de alimentação é fornecida. Seu princípio de funcionamento baseia-se na utilização de um transistor como chave. 

Além disso, este circuito é suportado por outros 2 componentes básicos, resistências e condensadores. Em geral, os capacitores utilizados são do tipo eletrolítico ou ELCO (condensador eletrolítico). A função deste componente é armazenar e liberar carga em uma unidade de tempo.

## Projeto Esquemático

### Lista de componentes

- Led 1: tamanho 5 mm, vermelho
- Led 2: tamanho 5 mm, verde
- R1, R2: 100Ω
- R3, R4: 10KΩ
- C1, C2: 100uF/16V
- Tr 1, Tr 2: BC547
- Bateria tipo botão 9Vdc

**Nota**: Ao montar ou soldar componentes em uma PCB, as pernas dos transistores, diodos, LEDs e ElCo não devem ser invertidas, visto que possuem pólos positivos e negativos voltados para o corpo do componente. Para que não haja danos, atenção aos polos positivo e negativo da fonte de alimentação, principalmente ao transistor. 

### Cálculo

Fórmula para o cálculo do período de tempo que um LED acende em um circuito, ou seja, o tempo de carga e descarga no ElCo, o que faz com que o transistor funcione como uma chave:

```
t = (coeficiente)*R*C
```

- t: tempo em segundos
- Coeficiente: 0,7
- R: resistor em ohms
- C: Capacitor em farads

Para o exemplo acima, pode ser calculado: 

```
R = 56KΩ = 56000 Ω
C = 100μF = 0,0001 F
```

Portanto, o período de tempo em que o LED acende no circuito é de aproximadamente 3,92seg, com base nos valores de resistência, capacitância e o coeficiente dado na fórmula.

### Projeto Esquemático 2

Para alterar o tempo ou tempo, o circuito acima pode ser modificado adicionando um potenciômetro. A seguir está um circuito flip-flop versão 2 com a adição de controle de temporização. A lista de componentes do circuito inclui:

- Led 1: tamanho 3 mm, vermelho
- Led 2: tamanho 3 mm, verde
- R1, R2: 10KΩ
- Resistor variável 100KΩ: 2pcs
- C1, C2: 100uF/16V
- Tr 1, Tr 2 : C9014
- Bateria 9Vcc

No circuito, o tempo de ativação do LED é calculado, ou seja,

```
t = (coeficiente)*(R + Pote)*C
R = 10KΩ = 10000 Ω
Potenciômetro = 100 KΩ = 100000 Ω
C = 100μF = 0,0001 F
```

a) Condição quando o potenciômetro é girado ao máximo para a esquerda (valor do potenciômetro = 0 Ω)

```
t = 0,7 * (10000+0) * 0,0001
= 0,7 * 1
= 0,7 segundos
```

b) Condição quando o potenciômetro é girado para a posição intermediária (valor do potenciômetro = 50.000 Ω)

```
t = 0,7 * (10.000 + 50.000) * 0,0001
= 0,7 * 6
= 4,2 segundos
```

c) Condição quando o potenciômetro é girado ao máximo para a direita (valor do potenciômetro = 100000 Ω)

```
t = 0,7 * (10.000 + 100.000) * 0,0001
= 0,7 * 11
= 7,7 segundos
```

## Atividade 1: 

Utilize o software EasyEDA para projetar uma placa de circuito impresso (PCB) que acomode os componentes e facilite a montagem do circuito Flip Flop: 

<img src="/img/flip_flop.png" alt="Circuito Flip Flop">

## Atividade 2: 

Utilize o software EasyEDA para projetar uma placa de circuito impresso (PCB) que acomode os componentes e facilite a montagem do circuito Flip Flop e acrescente um potenciômetro: 

<img src="/img/flip_flop_potenciometro.png" alt="Circuito Flip Flop com Potênciometro">

XL6009