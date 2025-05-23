# DMC - Design Mediado por Computador

## Introdução

Bem-vindo ao repositório da disciplina Design Mediado por Computador (DMC). A disciplina aborda os fundamentos do desenho técnico, modelagem 2D e 3D aplicadas à Engenharia da Computação.

## Modelagem em Software

Softwares de CAD (Computer-Aided Design) como AutoCAD, Fusion360, Proteus, EasyEDA, Eagle, Altium, KiCad, TinkerCAD, Blender, dentre outros, são hoje fundamentais para a materialização de conceitos, transformando protótipos em produtos funcionais.

##  O que são placas de circuito impresso (PCIs)?

Uma vez que o projeto de engenharia de um dispositivo eletrônico tenha sido testado com sucesso por meio de simulação e prototipagem em uma protoboard, é hora de fazer a transição para uma PCI.

Uma PCI consiste de folhas de cobre laminadas em substratos não-condutores, de modo a criar conexões entre componentes eletrônicos e fornecer suporte mecânico para montagem do dispositivo projetado em um gabinete. 

O fluxo de trabalho de um projeto de PCI é o seguinte: 

- Desenho do diagrama esquemático
- Elaboração do layout da placa
- Exportação dos arquivos "Gerber"
- Fabricação por empresas especializadas

No contexto do design de PCIs, utilizaremos o EasyEDA, visando a montagem de esquemas eletrônicos e a modelagem da PCI, oferecendo ferramentas para:

- Desenho de trilhas de cobre
- Posicionamento de componentes eletrônicos
- Verificação de erros (DRC - Design Rule Check e ERC - Electrical Rule Check)

<!--

Antes de exportar os Gerber files (arquivos para fabricação), sempre rode o ERC e DRC. Isso evita retrabalho e garante que sua placa funcione como esperado e possa ser fabricada com segurança.

### Electrical Rule Check (ERC) no EasyEDA

No editor de esquemáticos (schematic), você acessa:

> Design > Electrical Rule Check (ERC)

O que ele faz:

Verifica se há pinos flutuantes, conexões erradas ou curto-circuitos lógicos.

Destaca possíveis problemas com bolinhas vermelhas nos pontos de erro.

Lista os erros encontrados em uma janela de relatório.

Exemplos de erros que o ERC detecta:

Saída conectada a outra saída

Entrada desconectada

Pinos de alimentação não conectados ao VCC ou GND

Componentes mal referenciados

### Design Rule Check (DRC) no EasyEDA

No editor de layout da PCB, você acessa:

> Tools > Design Rule Check (DRC)

O que ele faz:

Analisa se o projeto da placa segue as regras mínimas definidas (largura de trilha, espaçamento, distância entre pads, etc).

Mostra os erros graficamente em destaque na placa.

Também lista os erros em uma janela com a opção de navegar até cada um deles.

Você pode configurar as regras em:

Design > Design Rule Settings

Exemplos de erros que o DRC detecta:

Trilhas muito próximas

Pads encostando em trilhas vizinhas

Distância entre via e borda da placa insuficiente


-->

## O que é um Datasheet?

Aa utilizar componentes eletrônicos no projeto da PCI, precisamos consultar seus respectivos datasheets (folha de dados). Datasheets são documentos técnicos que contém informações detalhadas sobre um componente eletrônico, como um microcontrolador, circuito integrado, resistor, capacitor, transistor, regulador de tensão, entre outros. Eles são fornecidos pelo fabricante e servem como um guia para engenheiros e projetistas de circuitos eletrônicos que desejam aplicá-los em seus projetos. Um ótimo serviço de consulta a datasheets de diversos fabricantes é o [www.alldatasheets.com](https://www.alldatasheets.com). 

### Por que os Datasheets são Importantes?

- **Especificações Técnicas** – Contém informações como tensão de operação, corrente máxima, potência dissipada e faixas de temperatura de funcionamento, fundamentais para evitar danos ao componente.
- **Pinos e Funcionalidade** – Apresenta o pinout (mapa de pinos), detalhando quais são as funções de cada terminal do componente, evitando conexões erradas no circuito.
- **Diagramas e Características Elétricas** – Inclui gráficos de desempenho, curvas características, circuitos típicos de aplicação e requisitos elétricos.
- **Tolerâncias e Limites Operacionais** – Define os limites dentro dos quais o componente pode operar sem riscos de falha.
- **Sugestões de Uso** – Muitos datasheets fornecem circuitos de referência e sugestões para integração eficiente dos componentes em projetos.
- **Dimensões e Layout de PCB** – Contém o desenho mecânico do componente, essencial para projetar a footprint correta no CAD (como no EasyEDA).

## Projetos Práticos

No Módulo de Design de PCIs, trabalharemos os seguintes projetos práticos: 

| #  | Tarefa                                                             | Tipo de Aplicação      | Prazo      |
|----|--------------------------------------------------------------------|------------------------|------------|
| 01 | [Flip-Flop (BC547)](/flipflop/)                                    | Circuito Sequencial    | 30/05/2025 |
| 02 | [Oscilador / Temporizador (IC555)](/ic555/)                        | Circuito Temporizador  | 30/05/2025 |
| 03 | [Conversores DC (LM3862)](/converters/)                            | Eletrônica de Potência | 30/05/2025 |
| 04 | [Mini-Amplificador de Áudio (LM386)](/lm386/)                      | Amplificador Analógico | 30/05/2025 |
| 05 | [Amplificador de Áudio Hi-Fi (TDA2003)](/tda2003/)                 | Amplificador Hi-Fi     | 30/05/2025 |
| 06 | [Microcontrolador ESP32 (+BME280)](/bme280/)                       | Estação Meteorológica  | 30/05/2025 |
| 07 | [Mini-Game (ATTiny)](/attiny/)                                     | Mini-Game              | 30/05/2025 |

### Como Exportar e Enviar seu Projeto do EasyEDA? 

Você deve entregar o **arquivo `.zip` do seu projeto criado no EasyEDA**, conforme instruções abaixo.

- Antes de enviar, **renomeie o arquivo `.zip` gerado** com seu nome completo e o nome do projeto.
- **Exemplo**: `FlipFlop_JoaoSilva.zip`
- **Não serão aceitos prints ou capturas de tela. Apenas o `.zip` original gerado pelo EasyEDA.**

<!--
- O envio deve ser feito via [**canal oficial da disciplina** — Moodle, e-mail ou GitHub Classroom] *(especificar o meio)*.
-->

###  Passo a Passo: Gerar o `.zip` para envio

1. **No EasyEDA, localize seu projeto** na barra lateral esquerda.
   - Exemplo: `FlipFlop`, `IC555`, etc.

<img src="/img/EEDA_01.png" alt="Passo 1">


2. **Clique com o botão direito no nome do projeto** e vá até:

>Gerenciar Projeto > Download

<img src="/img/EEDA_02.png" alt="Passo 2">

Isso iniciará o empacotamento do seu projeto.

3. Após clicar em **"Download"**, o EasyEDA vai gerar um `.zip` automaticamente e o levará à página de notificações, onde você poderá baixar o arquivo do projeto. A ferramenta também enviará uma **mensagem para sua conta** com o link para baixar.

<img src="/img/EEDA_03.png" alt="Passo 3">

4. Envie o arquivo baixado via repositório indicado na disciplina do [Moodle](https://salaonline.ceub.br/).

<img src="/img/EEDA_04.png" alt="Passo 4">

<!--

6. [Mini-Game (ATTiny - Arduino)](/attiny/)

7. [Estação Meteorológica (ESP32 + BME280)](/bme280/)

-->

## Conclusão

O design de PCIs é uma área de crescente demanda no mercado de trabalho, com aplicações cada vez mais diversificadas e inovadoras, especialmente no campo de IoT e sistemas embarcados. Este curso apresenta os fundamentos para o desenvolvimento de projetos eletrônicos desde a concepção até a implementação e prática essenciais para ingressar na área.

<!--

Um sistema embarcado é um conjunto de hardware e software dedicado a uma aplicação específica. Exemplos incluem controle de motor em automóveis, dispositivos médicos, eletrodomésticos, sistemas de segurança, entre outros. Atualmente, plataformas populares para prototipagem incluem Arduino e ESP32. 

-->
