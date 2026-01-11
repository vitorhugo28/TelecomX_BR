# 📊 Projeto Telecom X: Inteligência de Dados e Análise de Churn

Este projeto consiste em um pipeline completo de análise de dados voltado para a retenção de clientes (**Churn Rate**) na empresa Telecom X. O trabalho abrange desde o processo de **ETL** (Extração, Transformação e Carga) até a geração de **insights estratégicos** para tomada de decisão de negócio.

## 🚀 Visão Geral do Projeto
O objetivo principal foi identificar por que os clientes estão deixando a empresa e qual o impacto financeiro dessa perda. A base de dados original, em formato JSON, foi processada para revelar padrões comportamentais que servirão de base para o treinamento de modelos de **Machine Learning**.

## 🛠️ Tecnologias Utilizadas
* **Linguagem:** Python 3.x
* **Manipulação de Dados:** Pandas e NumPy
* **Visualização:** Matplotlib e Seaborn
* **Ambiente:** Google Colab

## 🔧 Pipeline de Dados (ETL)

1.  **Extração:** Carregamento de dados brutos via API/URL no formato JSON e normalização para estruturas tabulares (DataFrame).
2.  **Transformação:**
    * Tratamento de valores ausentes na coluna `Valor_Total` (conversão de strings vazias para 0).
    * Conversão de tipos de dados (`object` para `float64`).
    * Tradução de rótulos de colunas e categorias para o português (Ex: `customerID` → `ID_Cliente`).
    * **Feature Engineering:** Criação da variável `Qtd_Servicos` para medir a densidade de produtos por cliente.

## 📊 Principais Insights e Gráficos

### 1. Perfil Temporal da Evasão
A análise de distribuição revelou que o **Mês 1** é o ponto de ruptura mais crítico para a operação.
![Distribuição Temporal](https://via.placeholder.com/800x400.png?text=Gráfico+de+Histograma+KDE+dos+Meses+de+Contrato)
*Placeholder: Insira aqui o seu gráfico de histplot salvo.*

### 2. Impacto do Modelo Contratual
Os contratos **mês a mês** representam a grande maioria das perdas. Dos 1.869 cancelamentos, **1.655** vieram deste modelo.
![Churn por Contrato](https://via.placeholder.com/800x400.png?text=Gráfico+Comparativo+de+Tipos+de+Contrato)

### 3. Fatores de Risco de Pagamento
Clientes que utilizam **Cheque Eletrônico** apresentam uma taxa de evasão significativamente maior do que métodos automáticos.

## 📄 Relatório de Impacto Financeiro

| Métrica | Valor |
| :--- | :--- |
| **Base Total de Clientes** | 7.267 |
| **Taxa de Churn** | 25,72% |
| **Prejuízo Acumulado** | R$ 2.862.926,90 |
| **Média de Serviços** | 4,14 por cliente |

## 🏁 Conclusões e Recomendações
Com base nos dados, as ações recomendadas incluem:
1.  **Onboarding Prioritário:** Implementar suporte proativo nos primeiros 90 dias de contrato.
2.  **Migração de Planos:** Incentivar a conversão de contratos mensais para anuais.
3.  **Digitalização de Pagamentos:** Facilitar a migração para métodos de débito automático.

## 🔮 Próximos Passos
* Realizar o **Encoding** das variáveis categóricas.
* Tratar o desbalanceamento das classes.
* Treinar e validar um modelo de **Classificação Binária** (Random Forest ou XGBoost) para prever o risco individual de Churn.

---
**Autor:** Vitor Hugo
