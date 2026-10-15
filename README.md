# 🌡️ NM Labs — Sistema IoT de Controle Climático Ativo

Sistema autônomo e inteligente para monitoramento e controle de temperatura e umidade em ambientes sensíveis à descarga eletrostática (ESD).

---

## 📌 Sobre o Projeto

Em laboratórios e linhas de manutenção de eletrônicos, o ar seco e descontrolado aumenta o risco de eletricidade estática, gerando danos em componentes sensíveis, prejuízos e falhas em auditorias.

A **NM Labs** oferece uma solução **não invasiva e de baixo custo**:
* **Monitoramento 24/7:** Leitura contínua de temperatura e umidade.
* **Atuação Autônoma:** Acionamento e ajuste do ar-condicionado via infravermelho (IR) sem alterar a fiação do equipamento.
* **Gestão em Nuvem:** Dashboard em tempo real e exportação de dados para auditoria.

---

## 🛠️ Tecnologias Utilizadas

### **Hardware**
* **Microcontrolador:** ESP32 (Wi-Fi e Bluetooth)
* **Sensores:** Sensor de Temperatura e Umidade DHT22
* **Atuadores:** Módulo Emissor IR (KY-005)
* **Receptor:** Módulo Receptor IR (VS1838B) para cópia de sinais
* **Display/Alimentação:** LCD 16x2 I2C e Fonte de Alimentação 5V

### **Software & Nuvem**
* **Firmware:** C++ / Arduino IDE (ESP32)
* **Front-End:** HTML, CSS, JavaScript
* **Hospedagem Web:** GitHub Pages
* **Back-End / Banco de Dados:** PostgreSQL hospedado no Supabase
* **Comunicação:** API REST (HTTP POST / GET)

---

## ⚡ Funcionalidades Principais

* ✅ **Leitura Contínua:** Coleta contínua dos parâmetros climáticos ambientais.
* ✅ **Controle Ativo:** Ajuste automático do ar-condicionado via IR ao detectar desvios de temperatura/umidade.
* ✅ **Resiliência e Buffering:** Armazenamento local de dados por até 24 horas em caso de queda do Wi-Fi.
* ✅ **Dashboard Web:** Visualização dinâmica dos dados e indicativos visuais de alerta.
* ✅ **Relatórios de Auditoria:** Exportação de históricos em formato CSV.

---

## 🚀 Como Executar o Projeto

### **1. Configuração do Hardware**
1. Conecte o sensor DHT22 e o emissor IR (KY-005) aos pinos digitais configurados no ESP32.
2. Conecte o Display LCD 16x2 via barramento I2C.

### **2. Firmware (ESP32)**
1. Abra o código no **Arduino IDE**.
2. Instale as bibliotecas necessárias (`DHT sensor library`, `IRremoteESP8266`, `WiFi`).
3. Configure as credenciais de rede Wi-Fi e as chaves de acesso da API do Supabase no arquivo de firmware.
4. Faça o upload do código para o ESP32.

### **3. Banco de Dados (Supabase)**
1. Crie um projeto no Supabase e execute o script SQL disponibilizado em `database/schema.sql` para criar a tabela `leituras_ambientais`.
2. Configure as políticas de segurança de linha (RLS).

---

## 👥 Equipe NM Labs

* **Marcio Cavalcante:** Liderança, QA e Programação C++
* **Augusto:** Integração de Hardware e Programação C++
* **Armando:** Desenvolvimento Front-End, Back-End e Banco de Dados
* **Pedro:** Desenvolvimento Front-End, Back-End e Banco de Dados

---

## 📄 Licença

Este projeto foi desenvolvido para fins acadêmicos e de demonstração tecnológica.