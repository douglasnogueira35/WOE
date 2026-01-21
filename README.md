# 📊 Projeto Final - Modelagem Preditiva de Crédito

Este projeto aplica **Machine Learning** para prever inadimplência e apoiar decisões estratégicas em crédito.  
Foram testados diferentes modelos de regressão, avaliados com métricas de mercado e comparados em termos de desempenho e interpretabilidade.

---

## 🚀 Objetivos
- Construir e avaliar modelos de regressão para previsão de risco.  
- Comparar métricas de performance (R², RMSE, MAE).  
- Identificar variáveis mais relevantes para orientar decisões estratégicas.  
- Gerar insights práticos para uso em instituições financeiras.  

---

## 🧾 Modelos Avaliados

| Modelo                  | R²     | RMSE       | MAE       |
|--------------------------|--------|------------|-----------|
| Linear Regression        | 0.483  | 14208.62   | 8193.65   |
| Random Forest Regressor  | 0.765  | 9572.11    | 5156.61   |
| XGBRegressor             | 0.373  | 15645.36   | 6417.50   |

---

## 📖 Justificativa da Escolha dos Modelos
- **Linear Regression**: modelo básico e interpretável, útil para relações lineares simples.  
- **Random Forest Regressor**: captura interações complexas entre variáveis e é robusto contra ruído.  
- **XGBRegressor**: modelo de boosting que otimiza erros residuais, excelente para alta performance em regressão.  

---

## 🎯 Insights Estratégicos
- O **Random Forest Regressor** apresentou o melhor desempenho geral (maior R² e menor RMSE/MAE).  
- Para reduzir erro, deve-se priorizar o modelo com menor RMSE ou MAE.  
- Modelos complexos como **XGBoost** ajudam a identificar padrões ocultos, mesmo quando não são os melhores em métricas globais.  
- A análise das variáveis mais importantes orienta gestores a tomar decisões antecipadas, ajustando limites de crédito e monitorando perfis de maior risco.  

---

## ✅ Conclusão
O projeto demonstrou como diferentes algoritmos podem ser aplicados em **Credit Scoring**.  
O **Random Forest Regressor** se destacou como o modelo mais eficiente para prever novos dados, equilibrando performance e robustez.  
A integração das métricas (R², RMSE, MAE) com a análise de variáveis fornece uma base sólida para decisões estratégicas em instituições financeiras.  

---
