# Atividade 8 - KNN, SVM/SVR e Random Forest

## 🎯 Descrição
Notebook completo implementando e comparando três algoritmos de Machine Learning:
- **KNN** (K-Nearest Neighbors)
- **SVM/SVR** (Support Vector Machines)
- **Random Forest**

Aplicados em:
- **Classificação** (dataset Wine)
- **Regressão** (dataset Diabetes)

---

## 🐍 Requisitos de Ambiente

### Versão do Python
- ✅ **Recomendado:** Python 3.9, 3.10 ou 3.11
- ⚠️ **Mínimo:** Python 3.8
- ❌ **Evitar:** Python 3.7 ou inferior, Python 3.12+ (problemas de compatibilidade)

### Bibliotecas Necessárias
- numpy ≥ 1.21.0
- pandas ≥ 1.3.0
- matplotlib ≥ 3.5.0
- seaborn ≥ 0.11.2
- scikit-learn ≥ 1.0.2
- jupyter ≥ 1.0.0
- ipykernel ≥ 6.0.0

---

## 🔧 Instalação

### Opção 1: Usar ambiente virtual existente

Se você já tem um ambiente Python 3.9-3.11 configurado:

```bash
cd "/Users/Rafael-Freitas/Desktop/Estudos"
source venv/bin/activate  # ou outro ambiente que você já tenha
pip install -r requirements_atividade8.txt
```

### Opção 2: Criar novo ambiente virtual

Criar um ambiente dedicado para esta atividade:

```bash
# Navegue até o diretório
cd "/Users/Rafael-Freitas/Desktop/Estudos"

# Crie o ambiente virtual (certifique-se de ter Python 3.9-3.11 instalado)
python3.11 -m venv venv_atividade8

# Ative o ambiente
source venv_atividade8/bin/activate

# Atualize o pip
pip install --upgrade pip

# Instale as dependências
pip install -r requirements_atividade8.txt

# Registre o kernel no Jupyter
python -m ipykernel install --user --name=atividade8 --display-name="Python 3.11 (Atividade8)"
```

### Opção 3: Usar ambiente do Machine Learning (se disponível)

Se você já tem o ambiente `venv_py311` configurado:

```bash
cd "/Users/Rafael-Freitas/Desktop/Estudos/Python/IA/Machine Learning"
source venv_py311/bin/activate
cd "/Users/Rafael-Freitas/Desktop/Estudos"
pip install -r requirements_atividade8.txt
```

---

## ▶️ Como Executar

1. **Abra o Jupyter Notebook ou JupyterLab:**
   ```bash
   cd "/Users/Rafael-Freitas/Desktop/Estudos"
   source venv_atividade8/bin/activate  # ou seu ambiente
   jupyter notebook
   # ou
   jupyter lab
   ```

2. **Abra o arquivo:**
   - `Atividade8_KNN_SVM_RandomForest.ipynb`

3. **Selecione o kernel correto:**
   - No Jupyter Notebook: `Kernel` → `Change Kernel` → `Python 3.11 (Atividade8)`
   - No JupyterLab: Clique no kernel no canto superior direito

4. **Execute a célula de verificação:**
   - Execute a primeira célula de código para verificar se o ambiente está configurado corretamente

5. **Execute as células em ordem:**
   - Use `Shift + Enter` para executar célula por célula
   - Ou `Cell` → `Run All` para executar todas

---

## 📋 Estrutura do Notebook

### Parte 1 - Classificação (Wine Dataset)
1. ✅ Preparação e EDA
2. ✅ Modelagem com KNN, SVM e Random Forest
3. ✅ Métricas e visualizações
4. ✅ Bônus: KMeans e PCA
5. ✅ Análise crítica

### Parte 2 - Regressão (Diabetes Dataset)
1. ✅ Preparação e EDA
2. ✅ Modelagem com KNN Regressor, SVR e Random Forest Regressor
3. ✅ Métricas e visualizações
4. ✅ Bônus: Método do Cotovelo, KMeans e PCA
5. ✅ Análise crítica

### Conclusões Gerais
- Comparação entre classificação e regressão
- Principais aprendizados
- Recomendações práticas

---

## 🔍 Verificação do Ambiente

Após instalar as dependências, execute a célula de verificação no notebook ou execute no terminal:

```python
python3 -c "import sys; print(f'Python: {sys.version}'); import sklearn; print(f'scikit-learn: {sklearn.__version__}'); import numpy; print(f'numpy: {numpy.__version__}'); import pandas; print(f'pandas: {pandas.__version__}')"
```

---

## ⚙️ Recursos Utilizados

- **RandomizedSearchCV** para otimização de hiperparâmetros
- **Pipeline** para organização de pré-processamento + modelo
- **StratifiedKFold** e **KFold** para validação cruzada
- **StandardScaler** para padronização (quando necessário)
- Visualizações ricas (heatmaps, ROC curves, learning curves, etc.)

---

## 📊 Métricas Calculadas

**Classificação:**
- Accuracy
- Macro F1-Score
- ROC-AUC (one-vs-rest)
- Matriz de Confusão

**Regressão:**
- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)
- R² (Coeficiente de Determinação)
- Análise de Resíduos

---

## 🎯 Objetivos Alcançados

✅ Aplicação de KNN, SVM/SVR e Random Forest em classificação e regressão  
✅ Comparação de desempenhos com métricas apropriadas  
✅ Discussão de trade-offs (viés/variância, interpretabilidade, custo computacional)  
✅ Implementação de bônus (KMeans, PCA, método do cotovelo)  
✅ Reprodutibilidade garantida com `random_state=42`

---

## 📝 Arquivos do Projeto

- `Atividade8_KNN_SVM_RandomForest.ipynb` - Notebook principal
- `requirements_atividade8.txt` - Dependências Python
- `README_Atividade8.md` - Este arquivo (instruções)

---

## 🆘 Resolução de Problemas

### Problema: ImportError ao importar scikit-learn
**Solução:** Certifique-se de que está usando Python 3.8+
```bash
python --version
pip install --upgrade scikit-learn
```

### Problema: Kernel não aparece no Jupyter
**Solução:** Registre o kernel novamente
```bash
source venv_atividade8/bin/activate
python -m ipykernel install --user --name=atividade8 --display-name="Python 3.11 (Atividade8)"
```

### Problema: Matplotlib não exibe gráficos
**Solução:** Certifique-se de que está executando no Jupyter (não terminal)
```python
%matplotlib inline  # adicione esta linha no início do notebook
```

---

## 📚 Referências

- [Scikit-learn Documentation](https://scikit-learn.org/stable/)
- [Wine Dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_wine.html)
- [Diabetes Dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_diabetes.html)

---

**Autor:** Rafael Soares  
**Data:** 2025-11-12  
**Versão:** 1.0


