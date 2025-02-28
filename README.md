# DMC - Design Mediado por Computador

## Introdução

Bem-vindo ao repositório da disciplina Design Mediado por Computador (DMC). A disciplina aborda os fundamentos do desenho técnico, modelagem 2D e 3D aplicadas à Engenharia da Computação. 

##  O que são placas de circuito impresso (PCIs)?

Uma vez que o projeto de engenharia de um dispositivo eletrônico tenha sido testado com sucesso por meio de simulação e prototipagem em uma protoboard, é hora de fazer a transição para uma PCI. Uma PCI consiste de folhas de cobre laminadas em substratos não-condutores, de modo a criar conexões entre componentes eletrônicos e fornecer suporte mecânico para montagem do dispositivo projetado em um gabinete. O fluxo de trabalho de um projeto de PCI é o seguinte: 

- Desenho do diagrama esquemático
- Elaboração do layout da placa
- Exportação dos arquivos "Gerber"
- Fabricação por empresas especializadas

## Modelagem em Software

Softwares de CAD (Computer-Aided Design) como AutoCAD, Fusion360, Proteus, EasyEDA, Eagle, Altium, KiCad, dentre outros, tornaram-se essenciais para viabilizar a materialização de conceitos, transformando protótipos em produtos funcionais. No contexto do design de PCIs, estes softwares facilitam a montagem de esquemas eletrônicos e a modelagem da PCI, oferecendo ferramentas para:

- Desenho de trilhas de cobre
- Posicionamento de componentes eletrônicos
- Verificação de erros de design (DRC e ERC)

## O que é um Datasheet?

Um datasheet (folha de dados) é um documento técnico que contém informações detalhadas sobre um componente eletrônico, como um microcontrolador, resistor, capacitor, transistor, regulador de tensão, entre outros. Ele é fornecido pelo fabricante e serve como um guia essencial para engenheiros e projetistas de circuitos eletrônicos. Um ótimo serviço de consulta a datasheets de diversos fabricantes é o [www.alldatasheets.com](https://www.alldatasheets.com). 

### Por que os Datasheets são Importantes?

- **Especificações Técnicas** – Contém informações como tensão de operação, corrente máxima, potência dissipada e faixas de temperatura de funcionamento, fundamentais para evitar danos ao componente.
- **Pinos e Funcionalidade** – Apresenta o pinout (mapa de pinos), detalhando quais são as funções de cada terminal do componente, evitando conexões erradas no circuito.
- **Diagramas e Características Elétricas** – Inclui gráficos de desempenho, curvas características, circuitos típicos de aplicação e requisitos elétricos.
- **Tolerâncias e Limites Operacionais** – Define os limites dentro dos quais o componente pode operar sem riscos de falha.
- **Sugestões de Uso** – Muitos datasheets fornecem circuitos de referência e sugestões para integração eficiente dos componentes em projetos.
- **Dimensões e Layout de PCB** – Contém o desenho mecânico do componente, essencial para projetar a footprint correta no CAD (como no EasyEDA).

## Projetos Práticos

Durante este módulo do curso, trabalharemos os seguintes projetos práticos: 

1. [Flip-Flop](/flipflop/)

2. [Oscilador / Temporizador (IC555)](/ic555/)

3. [Conversores DC (LM2596 / LM3862)](/converters/)

4. [Mini-Amplificador de Áudio (LM386)](/lm386/)

5. [Amplificador de Áudio Hi-Fi (TDA2003)](/tda2003/)

6. [Mini-Game (ATTiny - Arduino)](/attiny/)

7. [Estação Meteorológica (ESP32 + BME280)](/bme280/)

## Conclusão

O design de PCIs é uma área de crescente demanda no mercado de trabalho, com aplicações cada vez mais diversificadas e inovadoras, especialmente no campo de IoT e sistemas embarcados. Este curso apresenta os fundamentos para ingressar na área e os conceitos para desenvolvimento de projetos eletrônicos desde a concepção até a implementação e prática em engenharia da computação. 

<!--

Um sistema embarcado é um conjunto de hardware e software dedicado a uma aplicação específica. Exemplos incluem controle de motor em automóveis, dispositivos médicos, eletrodomésticos, sistemas de segurança, entre outros. Atualmente, plataformas populares para prototipagem incluem Arduino e ESP32. 

-->