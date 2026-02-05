# PREVISAO-DE-VENDAS-E-REPOSICAO-INTELIGENTE-SUPPLY-CHAIN-
# Sistema de Reposição e Previsão de Demanda (Varejo) 🛒

Este projeto simula um motor de decisão para **Supply Chain**, integrando previsão de vendas com lógica de reposição de estoque (*Replenishment*). O objetivo é responder à pergunta: *"Quanto devo comprar de cada produto para cada loja hoje?"*

## 🎯 Fluxo de Negócio
1. **Prever** quanto cada loja vai vender nas próximas semanas.
2. **Olhar** quanto a loja já tem no estoque físico e quanto já está chegando (Trânsito).
3. **Calcular** a sugestão de compra ideal para cobrir a demanda sem gerar excesso.

## 🧠 Lógica do Algoritmo
O script implementa a fórmula clássica de *Open-to-Buy*:
> `Sugestão = (Previsão Vendas + Estoque Segurança) - (Estoque Físico + Estoque em Trânsito)`

## 🛠 Tecnologias
- **Python 3 & Pandas:** Manipulação de dados de múltiplas lojas e SKUs.
- **Scikit-Learn (Random Forest):** Modelo regressivo para capturar sazonalidade e tendências de venda.
- **Feature Engineering:** Criação de variáveis de atraso (*Lags*) e médias móveis.

## 📊 Estrutura do Código
- `Geração de Dados`: Criação de histórico fictício de vendas, trânsito e estoque.
- `Treinamento`: Modelo aprende padrões de consumo por produto/loja.
- `Motor de Cálculo`: Aplica as regras de negócio de cobertura de estoque para gerar o pedido final.

---
