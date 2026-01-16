# 📘 README – Projeto de Análise da Nota Fiscal Paulista (NFP)

## 📌 Contexto
Este projeto utiliza a base **NFP.ftr**, proveniente do projeto **#AMABiliDados**, que contém dados de notas fiscais cadastradas para doação automática à **AMA – Associação de Amigos do Autista**.  
O objetivo é analisar e modelar a propensão de diferentes categorias de notas fiscais gerarem créditos (retorno > 0), aplicando técnicas estatísticas como **WOE (Weight of Evidence)** e **IV (Information Value)**.

---

## 🎯 Objetivo
- Identificar quais categorias de notas possuem maior ou menor probabilidade de gerar créditos.  
- Avaliar a relevância da variável **categoria** na explicação do retorno de crédito.  
- Fornecer insights que possam apoiar modelos preditivos e estratégias de incentivo.  

---

## 📂 Estrutura da Base
| Campo              | Descrição |
|--------------------|-----------|
| **CNPJ emit.**     | CNPJ do emitente da nota |
| **Emitente**       | Nome fantasia do emitente |
| **No.**            | Número da nota fiscal |
| **Data Emissão**   | Data da emissão da nota |
| **Valor NF**       | Valor da nota fiscal |
| **Data Registro**  | Data de registro no sistema |
| **Créditos**       | Valor dos créditos (doação) |
| **Situação Crédito** | Status do crédito (pago, processado etc.) |
| **Ano**            | Ano da emissão |
| **Semestre**       | Semestre da emissão |
| **Retorno**        | Créditos ÷ Valor da nota |
| **flag_credito**   | Indicador se houve crédito positivo |
| **categoria**      | Categoria da nota |

---

## 🛠️ Metodologia
1. **Filtragem dos dados**  
   - Considerar apenas notas a partir de janeiro de 2020.  

2. **Análise exploratória**  
   - Proporção de notas com retorno > 0 por categoria.  
   - Visualização em tabelas e gráficos.  

3. **Cálculo do WOE (Weight of Evidence)**  
   - Evento: nota com retorno > 0.  
   - Não evento: nota sem retorno.  
   - Interpretação:  
     - WOE positivo → categoria mais propensa a gerar crédito.  
     - WOE negativo → categoria menos propensa.  
     - WOE ≈ 0 → categoria neutra.  

4. **Cálculo do IV (Information Value)**  
   - Mede o poder preditivo da variável **categoria**.  
   - Interpretação:  
     - <0.02 → não preditiva  
     - 0.02–0.1 → fraca  
     - 0.1–0.3 → média  
     - 0.3–0.5 → forte  
     - >0.5 → suspeita de overfitting  

---

## 📊 Exemplos de Código

### Filtragem
```python
df['Data Emissão'] = pd.to_datetime(df['Data Emissão'])
df = df[df['Data Emissão'] >= '2020-01-01']
