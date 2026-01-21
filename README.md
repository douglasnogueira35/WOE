# 📊 Projeto Final - Credit Scoring com Machine Learning

Este projeto demonstra como aplicar **Machine Learning** para prever **bons e maus pagadores** em uma base de crédito.  
O trabalho foi desenvolvido em **Python** com bibliotecas como **Scikit-Learn, LightGBM, XGBoost e Streamlit**, e inclui análise exploratória, comparação de modelos e implementação de um app interativo.

---

## 🚀 Objetivos
- Construir um pipeline completo de pré-processamento e modelagem.
- Comparar diferentes algoritmos de regressão/classificação.
- Escolher o modelo com melhor desempenho para escoragem.
- Implementar uma interface em **Streamlit** para uso prático.
- Gerar insights de negócio a partir das variáveis mais relevantes.

---

## 🧾 Modelos testados
- **Regressão Linear**
- **Random Forest Regressor**
- **XGBRegressor**
- **LightGBM (modelo final)**

📌 O modelo que mais se destacou foi **Random Forest Regressor**, mas o **LightGBM** foi escolhido para produção por sua eficiência e boa performance.

---

## 📖 Explicações e Insights

### Por que este modelo?
- **Random Forest** apresentou melhor desempenho geral.  
- **LightGBM** foi utilizado para escoragem final pela rapidez e capacidade de lidar com grandes volumes de dados.  
- **XGBoost** mostrou potencial para identificar padrões ocultos, mas com maior custo computacional.

### Insights de Negócio
- O modelo ajuda a identificar perfis de maior risco de inadimplência.  
- Variáveis como **tipo_renda**, **idade** e **posse_de_imóvel** tiveram grande importância.  
- Clientes com renda instável ou sem patrimônio apresentaram maior score de inadimplência.  
- Estratégias de crédito podem ser ajustadas com base nesses resultados.

---

## 📊 Gráficos Comparativos
- Importância das variáveis  
- Distribuição dos scores por **tipo_renda**  
- Curva ROC e métricas (AUC, KS, Gini)

*(insira imagens ou links dos gráficos aqui)*

---

## 🖥️ Aplicação em Streamlit
O app permite:
1. Upload de arquivos CSV.  
2. Escoragem automática com o modelo treinado (`model_final.pkl`).  
3. Visualização dos scores de inadimplência.  
4. Download da base escorada.  

### Rodando localmente
```bash
pip install -r requirements.txt
streamlit run app.py
