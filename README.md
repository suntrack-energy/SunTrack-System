# ☀️ SunTrack-System

O Sistema Físico será somento um projeto funcional de inicio, antes de aplicarmos o sistema completo com os sistemas Web e microserviços. Ou seja, isso é apenas um protótipo antes de refinar o projeto final.

> Este repositório é dedicado para a atualização do nosso sistema físico que será apresentado futuramente em um vídeo no YouTube.

<br>

## Planejamento do Projeto Físico

### 1. Arquitetura da Maquete

Possível maquete:

<img width="902" height="450" alt="image" src="https://github.com/user-attachments/assets/c26ccbc3-84aa-456e-bb2a-f91a93f5a26d" />

#

### 2. Materiais e Equipamentos para a Maquete
- Base em MDF, acrílico ou isopor (fácil de cortar e pintar).

- Divisórias internas (pode ser em MDF fino ou papelão pluma para leveza).

- Mini móveis (3D printing ou compra pronta, para dar realismo).

- Pintura e iluminação interna (LEDs) para simular luz das lâmpadas.

- Pequenos painéis solares de 5V (opcional, para estética, mas podem gerar energia real para o sistema).

- Mini telhas de EVA ou impressão 3D para estética.

#

### 3. Hardware (cérebro + sensores + atuadores)

#### Microprocessador

- **ESP32** (Modelo com Wi-Fi e Bluetooth integrado);
> Vai gerenciar toda a lógica e comunicação com a interface.

#### Sensores

- **Sensor de luminosidade (LDR ou BH1750)** – para detectar quando as luzes estão ligadas/desligadas.

- **Sensor de temperatura e umidade (DHT22 ou BME280)** – para monitorar ambiente e simular condições para desligamento preventivo.

- **Sensor de corrente (ACS712 ou SCT-013)** – para medir consumo de energia de cada “circuito” da maquete.

- **Sensor de fumaça e gases (MQ-2 ou MQ-135)** – para detecção de incêndio.

- **Sensor de tensão** – para simular queda de luz e leitura do gerador.

- **Botões físicos** – para simular interações manuais (ligar/desligar lâmpada, acionar gerador, etc.).

- **Sensor magnético reed switch** – para simular portas/janelas (segurança).

#### Atuadores

- **Relés de 5V ou módulos de relé 1, 2, 4 ou 8 canais** – para controlar LEDs, tomadas simuladas, etc.

- **LEDs brancos** – para simular iluminação dos cômodos.

- **LED RGB** – para alertas visuais (verde = normal, amarelo = aviso, vermelho = emergência).

- **Mini motor DC** – para simular o gerador.

- **Buzzer** – para alarmes sonoros de segurança.

- **Mini displays OLED ou LCD 16x2/20x4** – para exibir status localmente.

- **Bateria Li-ion 18650 + módulo carregador TP4056** – para simular banco de energia.

#

### 3. Tecnologias e softwares

Programação do ESP32

- Arduino IDE ou PlatformIO para programar o ESP32.

- Bibliotecas para:
  - WiFi

  - MQTT (para comunicação com servidor)
  
  - Controle de sensores (DHT, ACS712, BH1750, etc.)

  - Controle de relés

  - JSON para troca de dados

- Interface de usuário
  - Aplicativo mobile (Flutter, já que você domina) para controle e monitoramento.

  - Alternativa: Painel web com Node-RED ou Home Assistant rodando localmente.

  - Banco de dados: Firebase ou SQLite (dependendo do escopo da demo).

  - Comunicação: MQTT ou HTTP REST API.

#
