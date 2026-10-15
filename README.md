# 🌡️ NM Labs — Sistema IoT de Controle Climático Ativo

Sistema autônomo e inteligente para monitoramento e controle de temperatura e umidade em ambientes sensíveis à descarga eletrostática (ESD)[cite: 1].

---

## 📌 Sobre o Projeto

Em laboratórios e linhas de manutenção de eletrônicos, o ar seco e descontrolado aumenta o risco de eletricidade estática, gerando danos em componentes sensíveis, prejuízos e falhas em auditorias[cite: 1, 2].

A **NM Labs** oferece uma solução **não invasiva e de baixo custo**[cite: 1, 4]:
* **Monitoramento 24/7:** Leitura contínua de temperatura e umidade[cite: 1].
* **Atuação Autônoma:** Acionamento e ajuste do ar-condicionado via infravermelho (IR) sem alterar a fiação do equipamento[cite: 1, 4].
* **Gestão em Nuvem:** Dashboard em tempo real e exportação de dados para auditoria[cite: 1, 2].

---

## 🛠️ Tecnologias Utilizadas

### **Hardware**
* **Microcontrolador:** ESP32 (Wi-Fi e Bluetooth)[cite: 5, 8]
* **Sensores:** Sensor de Temperatura e Umidade DHT22[cite: 5]
* **Atuadores:** Módulo Emissor IR (KY-005)[cite: 5]
* **Receptor:** Módulo Receptor IR (VS1838B) para cópia de sinais[cite: 5]
* **Display/Alimentação:** LCD 16x2 I2C e Fonte de Alimentação 5V[cite: 5]

### **Software & Nuvem**
* **Firmware:** C++ / Arduino IDE (ESP32)[cite: 5, 8]
* **Front-End:** HTML, CSS, JavaScript[cite: 5, 8]
* **Hospedagem Web:** GitHub Pages[cite: 7, 8]
* **Back-End / Banco de Dados:** PostgreSQL hospedado no Supabase[cite: 5, 8]
* **Comunicação:** API REST (HTTP POST / GET)[cite: 7, 8]

---

## ⚡ Funcionalidades Principais

* ✅ **Leitura Contínua:** Coleta contínua dos parâmetros climáticos ambientais[cite: 1].
* ✅ **Controle Ativo:** Ajuste automático do ar-condicionado via IR ao detectar desvios de temperatura/umidade[cite: 1].
* ✅ **Resiliência e Buffering:** Armazenamento local de dados por até 24 horas em caso de queda do Wi-Fi[cite: 2, 6].
* ✅ **Dashboard Web:** Visualização dinâmica dos dados e indicativos visuais de alerta[cite: 2, 7].
* ✅ **Relatórios de Auditoria:** Exportação de históricos em formato CSV[cite: 2, 7, 9].

---

## 🚀 Como Executar o Projeto

### **1. Configuração do Hardware**
1. Conecte o sensor DHT22 e o emissor IR (KY-005) aos pinos digitais configurados no ESP32[cite: 5].
2. Conecte o Display LCD 16x2 via barramento I2C[cite: 5].

### **2. Firmware (ESP32)**
1. Abra o código no **Arduino IDE**.
2. Instale as bibliotecas necessárias (`DHT sensor library`, `IRremoteESP8266`, `WiFi`).
3. Configure as credenciais de rede Wi-Fi e as chaves de acesso da API do Supabase no arquivo de firmware[cite: 8].
4. Faça o upload do código para o ESP32[cite: 5, 8].

### **3. Banco de Dados (Supabase)**
1. Crie um projeto no Supabase e execute o script SQL disponibilizado em `database/schema.sql` para criar a tabela `leituras_ambientais`[cite: 8, 15].
2. Configure as políticas de segurança de linha (RLS)[cite: 7, 8].

---

## 👥 Equipe NM Labs

* **Marcio Cavalcante:** Liderança, QA e Programação C++[cite: 4, 5]
* **Augusto:** Integração de Hardware e Programação C++[cite: 5]
* **Armando:** Desenvolvimento Front-End, Back-End e Banco de Dados[cite: 5]
* **Pedro:** Desenvolvimento Front-End, Back-End e Banco de Dados[cite: 5]

---

## 📄 Licença

Este projeto foi desenvolvido para fins acadêmicos e de demonstração tecnológica.