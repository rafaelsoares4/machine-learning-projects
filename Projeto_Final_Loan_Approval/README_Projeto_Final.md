# Projeto Final - Aplicação de Algoritmos de Machine Learning
## Classificação de Aprovação de Empréstimos

**Autor:** Rafael Sobral
**Dataset:** [Loan Approval Classification Data](https://www.kaggle.com/datasets/taweilo/loan-approval-classification-data)  
**Data:** 2025-11-13

---

## 📋 Descrição do Projeto

Este projeto aplica técnicas de aprendizado de máquina supervisionado (classificação) para prever a aprovação de empréstimos bancários. O projeto segue todas as etapas do pipeline de Machine Learning, desde a exploração de dados até a comparação de modelos e redução de dimensionalidade.

---

## 🎯 Objetivos

1. **Exploração e Análise de Dados (EDA):**
   - Análise exploratória com gráficos e estatísticas descritivas
   - Identificação de valores ausentes, outliers e colunas irrelevantes

2. **Pré-processamento:**
   - Tratamento de dados ausentes
   - Normalização e padronização
   - Codificação de variáveis categóricas
   - Balanceamento de classes (se necessário)

3. **Treinamento de Modelos:**
   - Aplicação de pelo menos 3 algoritmos diferentes
   - Ajuste de hiperparâmetros com validação cruzada

4. **Comparação de Desempenho:**
   - Métricas: Accuracy, F1-Score, ROC-AUC
   - Visualizações comparativas

5. **Redução de Dimensionalidade:**
   - Aplicação de PCA no melhor modelo
   - Comparação antes e depois

---

## 📁 Estrutura do Projeto

```
.
├── Projeto_Final_Loan_Approval.ipynb  # Notebook principal
├── README_Projeto_Final.md            # Este arquivo
├── requirements_projeto_final.txt    # Dependências
└── loan_approval_dataset.csv         # Dataset (baixar do Kaggle)
```

---

## 🚀 Como Executar

### 1. Pré-requisitos

- Python 3.9, 3.10 ou 3.11
- Jupyter Notebook ou JupyterLab

### 2. Instalação das Dependências

```bash
# Criar ambiente virtual (opcional, mas recomendado)
python3.11 -m venv venv_projeto_final
source venv_projeto_final/bin/activate  # Linux/Mac
# ou
venv_projeto_final\Scripts\activate  # Windows

# Instalar dependências
pip install -r requirements_projeto_final.txt
```

### 3. Baixar o Dataset

**Opção 1: Usando Kaggle API**
```bash
# Instalar Kaggle API (se ainda não tiver)
pip install kaggle

# Configurar credenciais (veja: https://www.kaggle.com/docs/api)
# Baixar dataset
kaggle datasets download -d taweilo/loan-approval-classification-data
unzip loan-approval-classification-data.zip
```

**Opção 2: Download Manual**
1. Acesse: https://www.kaggle.com/datasets/taweilo/loan-approval-classification-data
2. Baixe o dataset
3. Coloque o arquivo CSV no mesmo diretório do notebook

### 4. Executar o Notebook

```bash
# Abrir Jupyter Notebook
jupyter notebook Projeto_Final_Loan_Approval.ipynb

# Ou JupyterLab
jupyter lab Projeto_Final_Loan_Approval.ipynb
```

Execute as células em ordem sequencial.

---

## 📊 Estrutura do Notebook

### 1. Exploração e Análise de Dados (EDA)
- Carregamento do dataset
- Análise de valores ausentes e outliers
- Estatísticas descritivas
- Análise de correlações
- Distribuição da variável target

### 2. Pré-processamento dos Dados
- Tratamento de valores ausentes
- Codificação de variáveis categóricas (One-Hot Encoding)
- Normalização (StandardScaler)
- Balanceamento de classes (SMOTE, se necessário)
- Divisão treino/teste (70/30)

### 3. Treinamento de Modelos
- **Modelo 1:** Regressão Logística
- **Modelo 2:** Random Forest
- **Modelo 3:** Support Vector Machine (SVM)
- **Modelo 4:** Gradient Boosting (Bônus)

Todos os modelos utilizam `RandomizedSearchCV` para otimização de hiperparâmetros com validação cruzada (5 folds).

### 4. Comparação de Desempenho
- Tabela comparativa com todas as métricas
- Gráficos de barras comparativos
- Matrizes de confusão
- Curvas ROC

### 5. Redução de Dimensionalidade
- Aplicação de PCA (mantendo 95% da variância)
- Treinamento do melhor modelo com dados reduzidos
- Comparação antes vs. depois do PCA
- Análise dos efeitos sobre desempenho, complexidade e visualização

### 6. Conclusões
- Resumo dos resultados
- Discussão dos achados
- Limitações e melhorias futuras

---

## 📦 Dependências Principais

- `numpy` ≥ 1.21.0
- `pandas` ≥ 1.3.0
- `matplotlib` ≥ 3.5.0
- `seaborn` ≥ 0.11.2
- `scikit-learn` ≥ 1.0.2
- `imbalanced-learn` ≥ 0.8.0 (para SMOTE)

---

## 📈 Métricas Utilizadas

- **Accuracy:** Proporção de predições corretas
- **Precision:** Proporção de predições positivas que são realmente positivas
- **Recall:** Proporção de casos positivos que foram corretamente identificados
- **F1-Score:** Média harmônica entre Precision e Recall
- **ROC-AUC:** Área sob a curva ROC (Receiver Operating Characteristic)

---

## 🔧 Configurações

- **Random State:** 42 (para reprodutibilidade)
- **Validação Cruzada:** StratifiedKFold (5 folds)
- **Divisão Treino/Teste:** 70/30 (estratificada)
- **PCA:** Mantém 95% da variância

---

## 📝 Notas Importantes

1. **Reprodutibilidade:** Todos os processos usam `random_state=42` para garantir resultados reproduzíveis.

2. **Balanceamento:** O notebook verifica automaticamente se as classes estão desbalanceadas e aplica SMOTE se necessário.

3. **Pré-processamento:** 
   - Variáveis numéricas: imputação com média
   - Variáveis categóricas: imputação com moda
   - One-Hot Encoding para variáveis categóricas
   - StandardScaler para normalização

4. **Otimização de Hiperparâmetros:** Utiliza `RandomizedSearchCV` com 30 iterações para cada modelo.

---

## 🎓 Resultados Esperados

Após executar o notebook completo, você terá:

1. ✅ Análise exploratória completa com visualizações
2. ✅ Dados pré-processados e prontos para modelagem
3. ✅ 4 modelos treinados e otimizados
4. ✅ Comparação detalhada de desempenho
5. ✅ Análise de redução de dimensionalidade
6. ✅ Visualizações profissionais para apresentação

---

## 📚 Referências

- Dataset: [Kaggle - Loan Approval Classification Data](https://www.kaggle.com/datasets/taweilo/loan-approval-classification-data)
- Scikit-learn Documentation: https://scikit-learn.org/
- Imbalanced-learn Documentation: https://imbalanced-learn.org/

---

## 👤 Autor

**Rafael Sobral**

---

## 📄 Licença

Este projeto é para fins educacionais.

---

**Última atualização:** 2025-11-13

