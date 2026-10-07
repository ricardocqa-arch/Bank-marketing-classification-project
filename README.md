# Bank Marketing Campaign - Data Science & Business Decision Analysis

Este projeto aborda a otimização de campanhas de marketing bancário utilizando Machine Learning. O foco principal não foi apenas alcançar métricas cegas, mas alinhar o desempenho técnico do modelo com os **objetivos de negócio reais** (maximizar a captação de clientes potenciais minimizando os falsos negativos).

## 🚀 Etapas do Projeto
1. **Data Profiling & Auditoria:** Inspeção de tipos de dados, valores em falta e estatísticas descritivas.
2. **Pré-processamento Avançado:** Tratamento de valores ambíguos (`unknown`), *One-Hot Encoding* e limitação de *outliers* através do método IQR (Capping).
3. **Fase de Experimentação e Teste de Hipóteses:**
   - **Hipótese 1 (Regressão Logística):** Teste de modelo linear com dados escalonados (`StandardScaler`).
   - **Hipótese 2 (SVM):** Teste de margem de separação complexa.
   - *Conclusão:* Modelos lineares focaram-se na classe majoritária, ignorando o desequilíbrio severo dos dados.
4. **Modelo Final Otimizado:** Implementação de uma **Árvore de Decisão** com hiperparâmetros ajustados e `class_weight='balanced'`.

## 📊 Resultados e Conclusão de Negócio
Embora os modelos lineares tenham apresentado uma acurácia aparente de ~89%, a **Árvore de Decisão com pesos balanceados** foi selecionada para produção:
- **Recall de 87% na classe minoritária:** Identificou a esmagadora maioria dos clientes interessados na campanha.
- **Justificação de Negócio:** No setor bancário, o custo de perder um cliente potencial (falso negativo) é muito superior ao incómodo de contactar alguém sem interesse. O modelo foi otimizado para o impacto comercial e não apenas para a acurácia matemática.

## 🛠️ Tecnologias Utilizadas
- Python (Pandas, NumPy, Scikit-Learn)
- Jupyter Notebooks
  
