## 📊 Dashboard de Estoque - Contoso

Este projeto apresenta uma análise de estoque utilizando **Power BI**, com foco em identificar **estoques críticos**, **ruptura de produtos** e **impactos financeiros por região, país e loja**.  

A base de dados utilizada é o **ContosoRetailDW**, disponibilizada pela Microsoft, sendo um excelente case para simulação de cenários de **gestão de estoque e logística**.

### 🛠️ Tecnologias e Ferramentas

* **Power BI:** Utilizado para ETL, modelagem e visualização de dados.
* **SQL Server:** Fonte de dados original para as tabelas de fatos e dimensões.
* **Power Query (M):** Usado para a etapa de transformação e enriquecimento dos dados.
---
### ⚙️ Principais Recursos do Dashboard
### 🖼️ Imagens do Projeto
#### Aqui estão as imagens que detalham as etapas do projeto, demonstrando o fluxo de trabalho completo.
---
### **1. Conectando a Tabela de Fatos (FactInventory)**
  <img align="right" width="400"  src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/1%20-%20Conex%C3%A3ofact.png">

* Nesta etapa, a conexão com o **banco de dados SQL Server** é estabelecida para carregar a tabela `FactInventory`.
* Essa tabela de fatos central contém informações críticas sobre o inventário,
   como quantidade em estoque e em pedido.

<br><br>

#### **2. Conectando a Tabela de Dimensão (DimProduct)**
   <img align="right" width="400"  src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/2%20-%20tabela%20de%20dimens%C3%A3o%20DimProduct.png">

* A imagem mostra o carregamento da tabela de dimensão `DimProduct`,
  que traz detalhes sobre os produtos (marca, cor, etc.).
* A consulta SQL permite extrair dados essenciais para contextualizar a análise de inventário.

<br><br>

### **3. Conectando a Tabela de Dimensão (DimStore)**
 <img align="right" width="400"  src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/3%20-%20tabela%20de%20dimens%C3%A3o%20DimStore.png">
 
* Aqui, a tabela de dimensão `DimStore` é carregada, contendo informações sobre as lojas.
* Isso é fundamental para segmentar a análise de dados por local,
 A edição dos pontos de latitude e longitude foi um passo importante para permitir a inclusão de um mapa no dashboard, o que enriquece a análise geográfica.
<br><br>

### **4. Transformação de Dados (DimDate)**
<img align="right" width="400"  src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/4%20-%20transforma%C3%A7%C3%A3o%20de%20dados%20date.png">

* Esta captura de tela destaca a fase de **transformação de dados** no Power Query.
* Colunas referentes as datas exemplo: `Mês` é criada a partir da `DateKey`, um passo crucial para enriquecer o modelo
   e permitir análises de séries temporais.

  <br><br>
### **5. Modelo de Dados (Star Schema)** 
<img align="right" width="350" heigh="250" src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/5%20-%20modelo%20de%20dados%20completo.png?raw=true">

* **Descrição:** A imagem mais importante! Ela exibe o **modelo de dados completo**, organizado em um **Esquema em Estrela (Star Schema)**.
    * **Estrutura do Modelo:** A tabela de fatos `FactInventory` está no centro, conectada às tabelas de dimensão,
        o que demonstra uma sólida compreensão em **modelagem dimensional**.
    * **Base para Relatórios:** Este modelo é a base para a criação de relatórios de BI eficientes,
        escaláveis e de fácil compreensão.

<br><br>
---

### **6.📍 Visão Geral do Dashboard**
<img align="" width="400" src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/Vis%C3%A3o%20geral%201.png?raw=true">

* **Descrição:** O dashboard final transforma dados brutos em insights de negócio. Ele apresenta uma análise completa do inventário e das vendas, com destaque para:
    * **KPIs de Estoque:**  lojas com estoque crítico,  itens cadastrados, e o valor total do estoque  e do custo .
    * **Análise por Classe:** Um gráfico de rosca exibe a quantidade de itens por classe (`Regular`, `Economy`, `Deluxe`), permitindo uma visão rápida da distribuição do estoque.
    * **Evolução de Pedidos:** Um gráfico de linha mostra a evolução mensal de unidades em falta e a quantidade de pedidos de compra, identificando tendências e picos.
    * **Resumo por País:** Uma tabela resume o estoque disponível e a quantidade em falta por país, facilitando a identificação de áreas que precisam de atenção.
    * **Top Lojas:** Um gráfico de barras apresenta o ranking das 10 lojas com mais unidades em falta.
<br>

### **7. Detalhe do Tooltip Personalizado**
<br>
<img align="" width="400" src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/Tooltip.png?raw=true">

* **Descrição:** Esta imagem demonstra a funcionalidade de um tooltip personalizado, um recurso avançado do Power BI.
    * **Análise Detalhada:** Ao passar o mouse sobre os gráficos, um pop-up exibe dados detalhados, como o resumo de custos por região e um gráfico das principais lojas com unidades em             falta.
    * **Melhora a Usabilidade:** Este recurso permite análises mais profundas sem a necessidade de navegar para outra página, tornando o dashboard mais intuitivo.

### **8. Filtros Interativos**
<br>
<img aling="" width="400" src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/Filtros%20Interativos.png?raw=true">

 * **Descrição:** Esta imagem ilustra a funcionalidade de filtros interativos no dashboard.
   * **Personalização da Análise:** Os filtros localizados à esquerda permitem que o usuário personalize a análise de dados com base em critérios como Ano, Continente,
                                     Fabricante e ClassName.
   * **Tomada de Decisão:** A capacidade de filtrar os dados de forma dinâmica é crucial para a tomada de decisões, permitindo a exploração de informações específicas
                              e a obtenção de insights mais aprofundados sobre o desempenho.

### **9. Análise por Região**
<br>
<img aling="" width="400" src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/An%C3%A1lise%20por%20Regi%C3%A3o.png?raw=true">

* **Descrição:** Esta página do dashboard oferece uma **análise detalhada por região**.
    * **KPIs de Estoque:** O painel exibe KPIs importantes, como `Custo de Ruptura de Estoque` e o percentual de `Unid em Falta`.
    * **Visualizações:** Gráficos de barras mostram o ranking de produtos e a média de unidades em falta por loja, ajudando a identificar áreas com problemas de estoque.
    * **Foco Regional:** O dashboard demonstra a capacidade de segmentar dados para uma análise focada em regiões específicas, essencial para a gestão global.

### **10. Funcionalidade de Drill-through**
<br>
<img align="" width="400" src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/Drill%20-%20An%C3%A1lise.png?raw=true">

* **Descrição:** A imagem destaca o uso do recurso de **Drill-through** no Power BI.
    * **Análise Profunda:** O menu de contexto é usado para navegar para uma página de análise detalhada, a partir de um ponto específico do gráfico.
    * **Melhora a Exploração:** Essa funcionalidade permite que o usuário mergulhe em informações mais específicas sem sobrecarregar a tela principal do dashboard, 
                                aprimorando a experiência de exploração dos dados.

### **11. Análise Detalhada por Região**
<br>
<img align="" width="400" src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/An%C3%A1lise%20detalhada.png?raw=true">

* **Descrição:** Esta página do dashboard é um exemplo de **análise detalhada por região**.
    * **Métricas de Inventário:** O painel apresenta métricas-chave como `Unidades em Falta`, `Média Cobertura de Estoque` e `Qtd Em Pedido de compra`.
    * **Análise Temporal e de Custo:** Gráficos de linha e de barras mostram o custo de ruptura de estoque por mês e o custo por loja,
                                      facilitando a identificação de tendências e as áreas que mais impactam o negócio.
    * **Comparativo Anual:** O gráfico de barras `YTD Unidades em Falta` permite a comparação anual do desempenho, uma visualização fundamental para a gestão de estoque.
---

## 🚀 Tecnologias Utilizadas
<div style="display: inline_block">
    <img align="center" alt="SQL" height="40" width="40" src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/logo.png?raw=true">
    <img align="center" alt="Power BI" height="40" width="40" src="https://github.com/Carlosarmendoca/ContosoPortifolio/blob/main/Imagens/1200px-New_Power_BI_Logo.svg.png?raw=true">
---

[Veja meu Dashboard no Power BI](https://app.powerbi.com/view?r=eyJrIjoiNmU4ZjY5MDctNzJkNS00OTljLTgwYmEtNWQ3NTBjMTgyYWZlIiwidCI6ImI1MjVhODJiLTQzMjgtNDUzNC04NmRmLTgyYTk0NmQwODU0ZSJ9)

## 📌 Observações
Este projeto faz parte do meu portfólio em **Análise de Dados**, com foco em **gestão eficiente de estoques**.

