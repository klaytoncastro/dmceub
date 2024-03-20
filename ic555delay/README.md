# Circuito Temporizador com Atraso IC 555

## Introdução

Neste projeto, exploraremos um circuito temporizador com atraso utilizando o IC 555 (*Timer*). Esse circuito gera atrasos controlados com base em unidades de tempo definidas pelos valores dos resistores e capacitores. O temporizador com atraso é amplamente utilizado em aplicações que exigem atrasos precisos, como sistemas de controle, acionamento de relés e muito mais.

## Projeto Esquemático

Neste circuito, o temporizador com atraso é configurado para fornecer atrasos ajustáveis. Os resistores R1, R2, R3, R4, R5 e R6, juntamente com os componentes adicionais, desempenham um papel crucial no controle dos atrasos. O circuito inclui os seguintes componentes:

- R1: 500kΩ
- R2: 1000kΩ
- R3: 1500kΩ
- R4: 1kΩ
- R5: 10kΩ
- R6: 1kΩ
- LED vermelho 3mm
- CI 555 Timer
- Optoacoplador PC817
- Botão de pressão
- Pino 2 do bloco T
- Pino 3 do bloco T
- Chave liga/desliga tipo DIL de 8 pinos
- Diodo 1N4004 (2 peças)
- Relés
- Fonte de alimentação (adaptador de 12V e energia elétrica PLN 220V AC)

Devido à presença de duas fontes de tensão (um adaptador de 12V e energia elétrica PLN 220V AC), é essencial realizar as conexões com cuidado e conduzir experimentos com precaução.

## Operação do IC 555

O IC 555 pode operar em diferentes modos para atender a diversas necessidades de temporização e oscilação em projetos eletrônicos. A escolha do modo depende da aplicação específica e dos requisitos de temporização do circuito. Abaixo, apresentamos a pinagem que define o modo de operação do IC 555:

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

### Modo Astável

No modo astável, o IC 555 é configurado como um oscilador de forma livre, gerando uma saída periódica que alterna entre estados alto e baixo. Este modo é usado para criar sinais de pulso contínuos, como os usados em piscadores de LEDs, geradores de tom e temporizadores intermitentes. A frequência do sinal de saída é determinada pelos valores dos resistores e capacitores conectados ao circuito. O pino 4 (RESET) é geralmente não conectado, o que permite a operação contínua do oscilador.

### Modo Monoestável

No modo monoestável, o IC 555 é configurado como um temporizador de disparo único. Ele produz um pulso de saída após receber um gatilho externo. Este modo é usado para criar atrasos controlados em resposta a um evento de gatilho externo. O pino 4 (RESET) é frequentemente conectado ao VCC para desativar a função de reinício.

### Modo Biestável (Flip-Flop)

No modo biestável, o IC 555 é configurado como um flip-flop, onde ele possui dois estados estáveis: alto e baixo. Ele é usado para criar uma lógica de comutação simples, onde a saída alterna entre estados alto e baixo em resposta a um gatilho externo. O estado de saída é alterado quando um gatilho externo é aplicado ao pino 2 (TRIG), ou o pino 4 (RESET) é usado para redefinir o estado. Este modo é frequentemente usado em aplicações de chaveamento e circuitos de controle de lógica simples.

## Tarefa: 

Utilize o software EasyEDA para projetar uma placa de circuito impresso (PCB) que acomode os componentes e facilite a montagem do circuito do temporizador com atraso usando o IC 555.

<img src="/img/delay-timer-ic555.png" alt="Circuito Temporizador com Atraso">
