# Projeto de Estação Meteorológica com ESP32 e Sensor BME280

Este projeto descreve a criação de uma estação meteorológica simples utilizando o ESP32 como controlador principal e o sensor BME280 para medição de temperatura, umidade, pressão e altitude, cujo propósito é monitorar as condições climáticas em tempo real. 

## 1. Design Esquemático

O esquemático para este projeto envolverá a integração do ESP32 com o sensor BME280 via comunicação I2C. Podemos adicionar componentes de suporte como resistores, conectores e um display ou LEDs indicativos.

### Componentes Principais

*ESP32*: Microcontrolador com capacidade Wi-Fi e Bluetooh integrada, sendo ideal para aplicações modernas de IoT.

*BME280*: Sensor de temperatura, umidade, pressão e altitude que opera entre 3,3 V a 5 V.

*Resistor de Pull-up*: 4.7 kΩ para as linhas I2C (SDA e SCL).

*Conector USB*: Para programação e alimentação do ESP32.

*LEDs*: Para indicação de status de operação.

*Capacitores*: 100 nF perto dos pinos de alimentação do ESP32 e BME280 para estabilidade.

*Botão de Reset*: Para reinicialização manual do ESP32.

### Ligação dos Componentes:

*Alimentação*: O ESP32 e o BME280 são alimentados com 3,3 V diretamente do regulador de bordo do ESP32. Conecte os pinos de alimentação (VCC e GND) do ESP32 e do BME280. 

*Comunicação I2C*: Ligue as linhas SDA e SCL do BME280 aos pinos I2C correspondentes no ESP32. 

- SDA: Conectado ao pino 21 do ESP32.
- SCL: Conectado ao pino 22 do ESP32.

*LEDs*: conectados via resistores limitadores de corrente a pinos GPIO disponíveis.

*Botão de Reset*: Conectado ao pino EN (enable) do ESP32. 

### Revisão e Ajustes:

Revise as conexões para garantir que não haja erros. Use a ferramenta de verificação de erros do EasyEDA para isso. 

## 2. Layout da PCB

### Organização dos componentes:

- Use a função `Convert Project to PCB` para transformar o esquemático em um layout de PCB.

- Centralize o ESP32: Como o microcontrolador principal, ele deve estar acessível e bem posicionado para facilitar o acesso a todos os pinos. 

- Posicione o BME280: Coloque este sensor em uma área que minimize a interferência térmica e eletrônica, ou seja, ele deve estar suficientemente distante de fontes de calor como reguladores de tensão ou o próprio microcontrolador para evitar leituras erradas.

- LEDs e Botão de Reset: posicione-os nas bordas da placa para fácil acesso.

### Roteamento:

- Trilhas de Alimentação: Assegure que as trilhas de alimentação sejam suficientemente largas para a corrente esperada.

- Trilhas de Sinal: As linhas I2C terão trilhas mais estreitas e serão mantidas o mais curtas possível para evitar interferência e perda de sinal. Evite caminhos longos e cruzamentos com outras trilhas.

- Plano de Terra: Implemente um plano de terra para estabilidade e redução de ruídos. A camada de terra é essencial reduzir a interferência e melhorar a estabilidade da operação dos componentes.

### Verificação do Layout:

Revise o layout do PCB com as ferramentas de DRC (Design Rule Check) para garantir que todas as normas de design estão sendo seguidas.

## Preparação para Fabricação

### Geração de Arquivos Gerber:

Prepare os arquivos Gerber, que são necessários para a fabricação do PCB. Certifique-se de incluir todas as camadas necessárias.

### Visualização 2D e 3D:

Use a ferramenta de visualização 2D e 3D do EasyEDA para verificar o aspecto final da PCB antes da fabricação.

## 3. Conclusão

Este projeto de estação meteorológica utiliza o ESP32 e o sensor BME280 para fornecer uma solução eficaz e econômica para monitoramento climático. 