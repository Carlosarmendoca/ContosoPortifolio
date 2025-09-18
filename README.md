## 📊 Dashboard de Estoque - Contoso

Este projeto apresenta uma análise de estoque utilizando **Power BI**, com foco em identificar **estoques críticos**, **ruptura de produtos** e **impactos financeiros por região, país e loja**.  

A base de dados utilizada é o **ContosoRetailDW**, disponibilizada pela Microsoft, sendo um excelente case para simulação de cenários de **gestão de estoque e logística**.

### 🛠️ Tecnologias e Ferramentas

* **Power BI:** Utilizado para ETL, modelagem e visualização de dados.
* **SQL Server:** Fonte de dados original para as tabelas de fatos e dimensões.
* **Power Query (M):** Usado para a etapa de transformação e enriquecimento dos dados.
---
### ⚙️ Principais Recursos do Dashboard

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

### 🖼️ Imagens do Projeto
Aqui estão as imagens que detalham as etapas do projeto, demonstrando o fluxo de trabalho completo.
---
### **1. Conectando a Tabela de Fatos (FactInventory)**
  <img align="right" width="400"  src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/1%20-%20Conex%C3%A3ofact.png">

* Nesta etapa, a conexão com o **banco de dados SQL Server** é estabelecida para carregar a tabela `FactInventory`.
* Essa tabela de fatos central contém informações críticas sobre o inventário, como quantidade em estoque e em pedido.

<br><br>

---
#### **2. Conectando a Tabela de Dimensão (DimProduct)**
   <img align="right" width="400"  src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/2%20-%20tabela%20de%20dimens%C3%A3o%20DimProduct.png">

* A imagem mostra o carregamento da tabela de dimensão `DimProduct`, que traz detalhes sobre os produtos (marca, cor, etc.).
* A consulta SQL permite extrair dados essenciais para contextualizar a análise de inventário.

<br><br>


### **3. Conectando a Tabela de Dimensão (DimStore)**
 <img align="right" width="400"  src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/3%20-%20tabela%20de%20dimens%C3%A3o%20DimStore.png">
 
* Aqui, a tabela de dimensão `DimStore` é carregada, contendo informações sobre as lojas.
* Isso é fundamental para segmentar a análise de dados por local, demonstrando a importância da **modelagem de dados** para a BI.
  
<br><br>


### **4. Transformação de Dados (DimDate)**
<img align="right" width="400"  src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/4%20-%20transforma%C3%A7%C3%A3o%20de%20dados%20date.png">

* Esta captura de tela destaca a fase de **transformação de dados** no Power Query.
* A coluna `Mês` é criada a partir da `DateKey`, um passo crucial para enriquecer o modelo e permitir análises de séries temporais.

  <br><br>



### **5. Modelo de Dados (Star Schema)** 
<img align="right" width="350"  src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/5%20-%20modelo%20de%20dados%20completo.png?raw=true">



* A imagem mais importante! Ela exibe o **modelo de dados completo**, organizado em um **Esquema em Estrela (Star Schema)**.
* A tabela de fatos `FactInventory` está conectada às tabelas de dimensão, o que demonstra uma sólida compreensão em
* **modelagem dimensional** para criação de relatórios de BI eficientes.
<br><br>




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
