# 📊 Dashboard de Estoque - Contoso

Este projeto apresenta uma análise de estoque utilizando **Power BI**, com foco em identificar **estoques críticos**, **ruptura de produtos** e **impactos financeiros por região, país e loja**.  

A base de dados utilizada é o **ContosoRetailDW**, disponibilizada pela Microsoft, sendo um excelente case para simulação de cenários de **gestão de estoque e logística**.

## 📄 Descrição do Projeto

Este projeto é uma demonstração de habilidades em Business Intelligence (BI), focando na análise de dados de inventário e vendas de uma empresa de varejo fictícia. 
O objetivo é transformar dados brutos em insights estratégicos, usando o Power BI para modelagem e visualização. 
O projeto cobre desde a conexão com o banco de dados até a construção de um modelo de dados robusto e a transformação de dados para análises futuras.


## 🛠️ Tecnologias e Ferramentas

* **Power BI:** Utilizado para ETL, modelagem e visualização de dados.
* **SQL Server:** Fonte de dados original para as tabelas de fatos e dimensões.
* **Power Query (M):** Usado para a etapa de transformação e enriquecimento dos dados.

---

## ⚙️ Principais Recursos do Dashboard

- 📍 **Visão Geral:**  
  - Total de lojas em situação crítica.  
  - Quantidade de itens cadastrados.  
  - Estoque disponível e custo total do estoque.  
  - Evolução mensal de unidades em falta vs. pedidos de compra.  

- 🌍 **Análise por País:**  
  - Estoque crítico consolidado.  
  - Percentual de unidades em falta por região.  
  - Top 10 lojas com maior número de unidades em falta.  

- 🏪 **Análise por Região e Loja:**  
  - Drill-through para detalhamento de cada região.  
  - Impacto médio por loja vs. unidades em falta.  
  - Custos de ruptura de estoque por loja.  

- 🔎 **Filtros Interativos:**  
  - Ano e mês.  
  - Continente e país.  
  - Fabricante.  
  - Classificação do produto (Regular, Economy, Deluxe).  


### **1. Conectando a Tabela de Fatos (FactInventory)**
* **Descrição:** Nesta etapa, a conexão com o **banco de dados SQL Server** é estabelecida para carregar a tabela `FactInventory`. Essa tabela de fatos central contém informações críticas sobre o inventário, como quantidade em estoque e em pedido.
* **Imagem:**
    ![Conexão da Tabela FactInventory](https://i.imgur.com/GjQJm4b.png)

---

### **2. Conectando a Tabela de Dimensão (DimProduct)**
* **Descrição:** A imagem mostra o carregamento da tabela de dimensão `DimProduct`, que traz detalhes sobre os produtos (marca, cor, etc.). A consulta SQL permite extrair dados essenciais para contextualizar a análise de inventário.
* **Imagem:**
    ![Conexão da Tabela DimProduct](https://i.imgur.com/FwF3f3o.png)

---

### **3. Conectando a Tabela de Dimensão (DimStore)**
* **Descrição:** Aqui, a tabela de dimensão `DimStore` é carregada, contendo informações sobre as lojas. Isso é fundamental para segmentar a análise de dados por local, demonstrando a importância da **modelagem de dados** para a BI.
* **Imagem:**
    ![Conexão da Tabela DimStore](https://i.imgur.com/8QGj3Qp.png)

---

### **4. Transformação de Dados (DimDate)**
* **Descrição:** Esta captura de tela destaca a fase de **transformação de dados** no Power Query. A coluna `Mês` é criada a partir da `DateKey`, um passo crucial para enriquecer o modelo e permitir análises de séries temporais.
* **Imagem:**
    ![Transformação da Tabela DimDate](https://i.imgur.com/k9J5jR1.png)

---

### **5. Modelo de Dados (Star Schema)**
* **Descrição:** A imagem mais importante! Ela exibe o **modelo de dados completo**, organizado em um **Esquema em Estrela (Star Schema)**. A tabela de fatos `FactInventory` está conectada às tabelas de dimensão, o que demonstra uma sólida compreensão em **modelagem dimensional** para criação de relatórios de BI eficientes.
* **Imagem:**
    ![Diagrama do Modelo de Dados](https://i.imgur.com/V9X9eXh.png)

## 🖼️ Screenshots

### Visão Geral do Dashboard

---

### Resumo da Região - Japan

---

### Filtros Interativos

---

### Análise por Região

---

### Análise Detalhada por Região


---

## 🚀 Tecnologias Utilizadas
- Power BI  
- SQL (para tratamento e consultas no banco de dados ContosoRetailDW)  
- Power Query (ETL)  
- DAX (cálculo de medidas e indicadores)  

---

## 📌 Observações
Este projeto faz parte do meu portfólio em **Análise de Dados aplicada à Engenharia de Manutenção e Logística**, com foco em **gestão eficiente de estoques**.

---
👨‍💻 Desenvolvido por [Carlos Alberto Rodrigues de Mendonça](https://github.com/)  
