# Controle de Azimute para Telescópio (Arduino)

Este projeto utiliza um sensor magnetômetro **QMC5883L** conectado através de um **MPU-6050** (usando I2C Bypass) para determinar a direção horizontal (azimute) de um telescópio.

## 🚀 Funcionalidades Implementadas
- **I2C Bypass Mode:** Configuração do MPU-6050 para permitir comunicação direta com o magnetômetro.
- **Calibração de Hard-Iron:** Algoritmo que identifica os valores máximos e mínimos para centralizar as leituras e eliminar desvios magnéticos.
- **Filtro Passa-Baixa (EMA):** Implementação de um filtro de média móvel exponencial para suavizar a leitura e evitar oscilações bruscas.
- **Compensação de Declinação:** Ajuste configurável para alinhar o norte magnético com o norte geográfico.

## 🛠️ Hardware
- Arduino (Uno/Nano/ESP32)
- Módulo GY-87 ou MPU-6050 + QMC5883L

## 📖 Como usar
1. Ao ligar o sistema, o código entra em modo de calibração por 15 segundos.
2. Gire o sensor em todas as direções (em círculos e oitavos) para mapear o campo magnético local.
3. Após a calibração, o monitor serial exibirá o azimute corrigido de 0° a 360°.# telescopio-azimute-arduino
