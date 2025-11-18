# Relatório REPA - Projeto Final
## Aplicação de Algoritmos de Machine Learning em Classificação de Aprovação de Empréstimos

**Autor:** Rafael Sobral  
**Disciplina:** Inteligência Artificial  
**Instituição:** [Nome da Instituição]  
**Data:** Novembro 2025

---

# 1. INTRODUÇÃO

## 1.1 Contextualização

O setor financeiro tem enfrentado desafios significativos na avaliação de risco de crédito e na tomada de decisões sobre aprovação de empréstimos. Tradicionalmente, essas decisões eram baseadas em análises manuais e regras pré-definidas, processos que podem ser demorados, subjetivos e propensos a erros humanos. Com o advento da era digital e o crescimento exponencial de dados disponíveis, as instituições financeiras têm buscado soluções mais eficientes e precisas para otimizar seus processos de concessão de crédito.

A avaliação de risco de crédito é fundamental para a saúde financeira das instituições bancárias, pois impacta diretamente na taxa de inadimplência e, consequentemente, na rentabilidade e estabilidade do negócio. Decisões incorretas podem resultar em perdas financeiras significativas, seja por aprovar empréstimos para clientes de alto risco ou por rejeitar clientes que seriam bons pagadores. Nesse contexto, a aplicação de técnicas de aprendizado de máquina (Machine Learning) surge como uma ferramenta promissora para auxiliar na tomada de decisões mais precisas e objetivas.

## 1.2 Problemática

O processo de aprovação de empréstimos envolve a análise de múltiplas variáveis relacionadas ao perfil do solicitante, tais como renda, histórico de crédito, idade, situação empregatícia, entre outras. A complexidade dessa análise aumenta quando consideramos a interação entre essas variáveis e a necessidade de identificar padrões que podem não ser evidentes através de métodos tradicionais.

As instituições financeiras enfrentam o desafio de equilibrar dois objetivos aparentemente contraditórios: maximizar a aprovação de empréstimos para aumentar receita e minimizar o risco de inadimplência para proteger o capital. Métodos tradicionais de análise podem ser limitados na capacidade de identificar padrões complexos e relações não-lineares entre as variáveis, resultando em decisões subótimas.

Além disso, o volume crescente de solicitações de empréstimos torna inviável a análise manual detalhada de cada caso, exigindo soluções automatizadas que sejam capazes de processar grandes volumes de dados de forma rápida e eficiente, mantendo ou melhorando a qualidade das decisões.

## 1.3 Justificativa

A aplicação de algoritmos de Machine Learning para classificação de aprovação de empréstimos apresenta várias vantagens em relação aos métodos tradicionais. Primeiro, esses algoritmos são capazes de aprender padrões complexos a partir de dados históricos, identificando relações não-lineares que podem não ser evidentes para analistas humanos. Segundo, uma vez treinados, os modelos podem processar novas solicitações de forma instantânea, permitindo respostas rápidas aos clientes e aumentando a eficiência operacional.

Terceiro, os modelos de Machine Learning podem ser continuamente atualizados com novos dados, permitindo que se adaptem a mudanças no perfil dos clientes e nas condições econômicas. Quarto, a aplicação de múltiplos algoritmos e a comparação de seus desempenhos permite identificar a melhor abordagem para o problema específico, considerando métricas como acurácia, precisão, recall e área sob a curva ROC (ROC-AUC).

Por fim, a redução de dimensionalidade através de técnicas como Análise de Componentes Principais (PCA) pode não apenas melhorar a eficiência computacional, mas também revelar insights sobre quais características são mais relevantes para a decisão de aprovação, contribuindo para a interpretabilidade do modelo.

## 1.4 Objetivos

### 1.4.1 Objetivo Geral

Aplicar técnicas de aprendizado de máquina supervisionado (classificação) para desenvolver modelos preditivos capazes de classificar solicitações de empréstimos como aprovadas ou rejeitadas, utilizando múltiplos algoritmos de Machine Learning e comparando seus desempenhos através de métricas apropriadas.

### 1.4.2 Objetivos Específicos

1. Realizar uma análise exploratória completa dos dados (EDA), identificando padrões, correlações, valores ausentes, outliers e características relevantes do dataset de aprovação de empréstimos.

2. Implementar um pipeline robusto de pré-processamento de dados, incluindo tratamento de valores ausentes, codificação de variáveis categóricas, normalização de variáveis numéricas e balanceamento de classes quando necessário.

3. Treinar e otimizar pelo menos três algoritmos diferentes de classificação (Regressão Logística, Random Forest, Support Vector Machine), utilizando validação cruzada e ajuste de hiperparâmetros para garantir a melhor performance de cada modelo.

4. Comparar o desempenho dos modelos utilizando métricas apropriadas para classificação binária, incluindo acurácia, precisão, recall, F1-Score e área sob a curva ROC (ROC-AUC), apresentando os resultados em tabelas e gráficos comparativos.

5. Aplicar técnicas de redução de dimensionalidade (PCA) no modelo de melhor desempenho e comparar os resultados antes e depois da redução, analisando os efeitos sobre o desempenho, complexidade computacional e capacidade de visualização dos dados.

6. Discutir criticamente os resultados obtidos, identificando o melhor modelo, analisando limitações e propondo melhorias futuras para o sistema de classificação.

## 1.5 Estrutura do Relatório

Este relatório está organizado da seguinte forma: a Seção 2 apresenta a fundamentação teórica sobre os algoritmos de Machine Learning utilizados e as técnicas de pré-processamento aplicadas. A Seção 3 descreve a metodologia adotada, incluindo detalhes sobre o dataset, as etapas de pré-processamento, os algoritmos selecionados e as métricas de avaliação. A Seção 4 apresenta os resultados obtidos, incluindo análises exploratórias, desempenho dos modelos e comparações. A Seção 5 discute os resultados de forma crítica, analisando as implicações práticas e as limitações do estudo. Por fim, a Seção 6 apresenta as conclusões, síntese dos principais achados e sugestões para trabalhos futuros.

---

**Nota:** Esta é a introdução do relatório REPA. As demais seções (Metodologia, Resultados, Discussão e Conclusão) serão desenvolvidas após a execução completa do notebook e obtenção dos resultados finais.

