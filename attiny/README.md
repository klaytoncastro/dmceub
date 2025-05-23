# PCB para Minigame usando ATtiny85

## Introdução

Este projeto visa desenvolver o esquemático e a PCB para um Minigame/Keychain usando o microcontrolador ATtiny85, um microcontrolador da Atmel/Microchip, que possui recursos semelhantes aos Arduinos, um pouco mais modestos que o ATmega328P, sendo útil para projetos mais miniaturizáveis, acoplado a um display de matriz de LEDs. Este tipo de dispositivo é ideal para desenvolvimento de jogos portáteis simples, como Space Invaders, configurado em um formato de mini-chaveiro.

## Projeto Esquemático

O design do projeto integra vários componentes eletrônicos para controlar o display de LEDs e facilitar a interação do usuário. Os componentes principais e suas funções são descritos a seguir:

### Componentes Principais

- **ATtiny85**: Microcontrolador que gerencia as interações do jogo.
- **Socket DIP de 8 pinos**: Permite fácil inserção e remoção do ATtiny85.
- **Resistores**: Utilizados para pull-up dos botões de ação.
- **Interruptores**: Controlam a ligação e desligamento do circuito.
- **Conector para bateria CR2032**: Fornece a alimentação do circuito.
- **Conector ISP de 6 pinos**: Utilizado para a programação do ATtiny85.
- **Display de Matriz de LEDs 8x8**: Responsável pela exibição das interações do jogo.

### Diagrama Esquemático

O diagrama esquemático apresenta as conexões entre todos os componentes, destacando a forma como o ATtiny85 se conecta ao display de LEDs e aos outros componentes envolvidos.

## Tarefa

Utilize o software EasyEDA para criar o esquemático do circuito. Inclua todos os componentes necessários e as conexões apropriadas. Se necessário, adicione comentários no esquemático para anotar a função de cada parte do circuito, facilitando a compreensão e a montagem.

### Projeto da PCB

- **Desenvolvimento no EasyEDA**: Converta o esquemático em um layout de PCB usando o EasyEDA.
- **Otimização do Layout**: Organize os componentes de forma a minimizar o espaço ocupado e maximizar a eficiência do circuito.
- **Trilhas e Conexões**: Inclua trilhas adequadas para as conexões e assegure-se de que todas as vias e pads estejam corretamente posicionados.
- **Plano de Terra**: Incorpore uma malha de cobre para o plano de terra, melhorando a estabilidade e reduzindo interferências.

## Imagens Ilustrativas

![Esquemático da PCB](/img/attinny_minigame.png)
![Layout da PCB](/img/attinny_minigame_pcb2.png)