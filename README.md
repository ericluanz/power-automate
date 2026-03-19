# 📊 Automação de Relatórios CSV com Power Automate

Este projeto apresenta um fluxo desenvolvido em **Power Automate** para automatizar o processamento de relatórios em formato **CSV**, transformando dados brutos em informações estruturadas e evitando retrabalho manual.

---

## 🎯 Objetivo do Fluxo

Automatizar a leitura, tratamento e registro de dados provenientes de arquivos CSV, garantindo:
- Padronização das informações
- Eliminação de processos manuais
- Prevenção de dados duplicados
- Maior confiabilidade operacional

---

## 🧰 Tecnologias Utilizadas

- Power Automate (Cloud Flow)
- SharePoint
- SharePoint List (base de dados)
- Ações de dados:
  - Create file
  - Get file content
  - Compose
  - Parse JSON
- Controle de fluxo:
  - Apply to each
  - Condition (validação de dados)

---

## ⚙️ Desafios Técnicos Enfrentados

- Conversão eficiente de CSV para JSON
- Tratamento de arquivos com múltiplas linhas
- Prevenção de duplicidade sem impacto de performance
- Padronização de dados inconsistentes

---

## 🔄 Descrição do Funcionamento

### 1️⃣ Gatilho do Fluxo
O fluxo é iniciado automaticamente a partir do recebimento de um e-mail contendo um arquivo CSV em anexo.  
O arquivo é salvo em uma pasta específica no SharePoint/OneDrive, acionando o início do processamento automatizado..

---

### 1️⃣ Percorrendo os arquivos (Apply to each)
O fluxo inicia processando cada arquivo CSV encontrado no local configurado, permitindo o tratamento automático de múltiplos relatórios.

---

### 2️⃣ Leitura do conteúdo do CSV
Para cada arquivo:
- O conteúdo é obtido integralmente
- Os dados são preparados para tratamento interno

---

### 3️⃣ Tratamento e transformação
- Uso de ações **Compose** para organizar os dados
- Conversão do conteúdo CSV em uma estrutura adequada
- Ação **Parse JSON** para transformar os dados em objetos estruturados

---

### 4️⃣ Consulta de dados existentes
Antes de criar novos registros:
- O fluxo consulta a base de dados (SharePoint List)
- Verifica se o registro já existe

---

### 5️⃣ Validação e controle de duplicidade
- ✅ Caso o item **não exista**: um novo registro é criado
- ❌ Caso o item **já exista**: o fluxo ignora a criação

Esse controle garante integridade e evita duplicações na base.

---

## 🧠 Conceitos Aplicados

- Processamento em lote
- Transformação de dados (CSV → JSON)
- Validação condicional
- Boas práticas de automação
- Organização e legibilidade do fluxo

---

## ✅ Resultados

- Automatização completa da importação de relatórios CSV
- Redução significativa de esforço manual
- Maior confiabilidade e consistência dos dados
- Processo escalável e reutilizável

---

## 📸 Visual do Fluxo

As imagens abaixo demonstram a estrutura do fluxo no Power Automate:

<img width="358" height="781" alt="image" src="https://github.com/user-attachments/assets/530d4648-21da-434d-b636-512efb98ad9b" />

---

