# 🚚 Dashboard de Análise Logística | Power BI

Este projeto é um dashboard completo para a análise de performance de uma operação logística. O objetivo é fornecer uma visão clara dos principais KPIs (Indicadores-Chave de Performance), identificar gargalos, monitorar custos e rastrear a eficiência das entregas.

**Arquivo do projeto:** Você pode baixar o arquivo `.pbix` original deste repositório para explorar a modelagem de dados, as fórmulas DAX e o tratamento no Power Query.

---

## 🎯 Objetivo do Projeto

O dashboard foi projetado para responder a perguntas críticas de negócio:
* Qual é o nosso Custo Total e Custo Médio por entrega?
* Estamos entregando no prazo? (Análise de OTIF - On-Time In-Full)
* Quais rotas ou motoristas são mais eficientes ou mais caros?
* Quais são os principais motivos de atraso nas entregas?

---

## 🛠️ Ferramentas Utilizadas
* **Power BI Desktop:** Desenvolvimento do dashboard e relatórios.
* **Power Query (Editor de Consultas):** Para todo o processo de ETL (Extração, Transformação e Carregamento).
* **DAX (Data Analysis Expressions):** Para a criação de métricas e KPIs avançados.

---

## 🔬 O Processo: ETL e Modelagem

1.  **Extração e Transformação (Power Query):**
    * Os dados (fictícios) foram importados de múltiplas fontes (planilhas Excel/CSV).
    * Realizei a limpeza e transformação dos dados: tratamento de valores nulos, padronização de texto e criação de colunas condicionais (ex: "Status da Entrega" baseado na data de entrega vs. prazo).

2.  **Modelagem de Dados (Modelo Estrela):**
    * Criei um modelo de dados relacional (esquema estrela) para otimizar a performance das consultas.
    * **Tabelas Fato:** `fEntregas`
    * **Tabelas Dimensão:** `dCalendario`, `dMotoristas`, `dVeiculos`, `dRotas`

3.  **Criação de Métricas (DAX):**
    * Desenvolvi métricas essenciais para a análise, como:
        * `Total de Entregas`
        * `Custo Total = SUM(fEntregas[Custo])`
        * `Taxa OTIF (%) = DIVIDE( [Entregas no Prazo], [Total de Entregas] )`
        * `Custo Médio por Entrega = DIVIDE( [Custo Total], [Total de Entregas] )`

---

## 📊 O Dashboard

### Visão Principal (Dashboard Analítico)
A tela principal oferece uma visão geral da operação, com os principais KPIs em destaque e análises de custo e performance.

![Visão Principal do Dashboard de Logística](dashboard-1.png)

### Análise Interativa (Filtros)
Para provar a interatividade, a imagem abaixo mostra o dashboard filtrado para um **Tipo de Veículo** e **Motorista** específicos. Note como todos os visuais se adaptam para refletir a seleção, permitindo uma análise detalhada.

![Dashboard com Filtro Aplicado](dashboard-2.png)

---

## 📬 Contato
* **Karla Renata** - [LinkedIn](https://www.linkedin.com/in/karlarenata-rosario/)
* **Portfólio Principal** - [karlarenatadev.github.io/portfolio-karla-renata/](https://karlarenatadev.github.io/portfolio-karla-renata/)
