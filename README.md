# Predição de Churn de Cartão de Crédito
![Capa do projeto](images/Gemini_Generated_Image_z9rgh9z9rgh9z9rg.png)
Este projeto tem como objetivo desenvolver um modelo preditivo para estimar a probabilidade de clientes cancelarem seus cartões de crédito. O cancelamento de clientes (*churn*) é um problema crescente para bancos e operadoras, impactando diretamente indicadores como receita recorrente, valor do tempo de vida do cliente (CLV) e retorno sobre o custo de aquisição (CAC). Antecipar quais clientes têm maior risco de cancelamento permite que a empresa adote ações proativas, oferecendo benefícios, ajustes personalizados ou contato direto para reduzir o churn e melhorar a retenção.  

Os dados utilizados foram obtidos na plataforma Kaggle e incluem informações demográficas, comportamentais, financeiras e de relacionamento com o banco de aproximadamente 10.127 clientes ao longo de seis meses. A variável alvo, *Attrition_Flag*, indica se o cliente cancelou o serviço (1) ou permaneceu ativo (0), sendo que apenas 16,07% dos clientes cancelaram, caracterizando um problema de classificação desbalanceada.  

O projeto segue a metodologia CRISP-DM, contemplando desde a compreensão do problema de negócio, preparação e análise exploratória dos dados, criação de variáveis derivadas, modelagem preditiva até a avaliação dos resultados e geração de insights estratégicos. O objetivo final é fornecer previsões confiáveis que auxiliem a empresa na tomada de decisões e na implementação de medidas que aumentem a retenção de clientes e a sustentabilidade do negócio.

# Ferramentas, Tecnologias e Técnicas Utilizadas no Projeto de Previsão de Churn

## Linguagens de Programação
- **Python** – principal linguagem utilizada para análise de dados, criação de modelos de machine learning, cálculo de métricas e simulações financeiras.  

## Bibliotecas Python
- **Pandas** e **NumPy** – manipulação de dados, cálculos e preparação de datasets.  
- **Matplotlib** e **Seaborn** – visualização de dados e gráficos exploratórios (EDA).  
- **LightGBM** – modelo de classificação utilizado para prever churn, incluindo análise de importância de variáveis (*gain*).  
- **SHAP** – análise interpretativa para entender o impacto de cada variável nas previsões.  
- **Scikit-learn** – métricas de avaliação, pré-processamento e validação cruzada.  

## Ferramentas de Desenvolvimento e Documentação
- **Jupyter Notebook / Google Colab** – desenvolvimento interativo do projeto, com código, visualizações e Markdown.  
- **Markdown** – documentação do projeto e organização de resultados dentro do notebook e README.  
- **Git / GitHub** – versionamento e hospedagem do projeto.  

## Metodologia
- **CRISP-DM** – estrutura utilizada para guiar todas as etapas do projeto: compreensão do negócio, preparação de dados, análise exploratória, modelagem, avaliação de performance e interpretação dos resultados.  

## Técnicas Utilizadas

### 1. Exploração e Análise de Dados (EDA)
- Estatísticas descritivas (média, mediana, desvio padrão).  
- Visualizações gráficas: histogramas, boxplots, gráficos de barras e heatmaps de correlação.  
- Comparação de churn entre diferentes perfis de clientes (demográficos, transacionais e comportamentais).

### 2. Pré-processamento de Dados
- Tratamento de valores ausentes.  
- Codificação de variáveis categóricas (one-hot e label encoding).  
- Criação de variáveis derivadas (ex.: `delta_uso`, mudanças trimestrais de transações e valores).  
- Balanceamento de classes para lidar com desbalanceamento (16,07% de churn).

### 3. Modelagem de Machine Learning
- Classificação supervisionada com **LightGBM**.  
- Validação de modelo: divisão treino/teste e métricas de performance (recall, precision, F1-score, AUC-ROC).  
- Seleção de variáveis mais importantes com *gain* e análise de SHAP para interpretação.

### 4. Análise Financeira e Cenários
- Simulação de ganhos e custos com base em performance do modelo.  
- Cálculo de clientes salvos, receita preservada, custo de campanhas, lucro líquido e ROI.  
- Sensibilidade ao custo de ação, eficácia de retenção e recall.  
- Comparação do modelo com targeting aleatório e projeção para escalabilidade em grandes bases de clientes.  
- Indicadores de controle: EV por cliente, custo médio, percentual de desperdício e elasticidade financeira.

# Problema do Negócio e Objetivos do Projeto

## Problema do Negócio
O cancelamento de clientes (churn) é um desafio crítico para empresas de cartão de crédito, pois impacta diretamente a receita recorrente, o valor do tempo de vida do cliente (CLV) e o retorno sobre o custo de aquisição (CAC). Muitos clientes estão encerrando suas contas, reduzindo a base ativa e aumentando o risco financeiro da empresa.  

Identificar antecipadamente quais clientes têm maior probabilidade de cancelar permite ao banco agir de forma proativa, oferecendo incentivos personalizados, ajustes de limites de crédito ou pacotes de produtos que aumentem o engajamento e a retenção. Sem uma previsão eficaz, as ações de retenção podem ser genéricas, menos eficientes e mais caras.

## Objetivos do Projeto
Este projeto tem como objetivo desenvolver um **modelo preditivo de churn** capaz de estimar a probabilidade de um cliente cancelar o serviço de cartão de crédito. O foco é:

- **Prever clientes com alto risco de churn**, priorizando ações de retenção.  
- **Gerar insights sobre os fatores que influenciam o cancelamento**, como comportamento transacional, engajamento e relacionamento com o banco.  
- **Auxiliar a tomada de decisão estratégica**, permitindo que campanhas de retenção sejam direcionadas, eficientes e financeiramente vantajosas.  
- **Fornecer análises financeiras e projeções** para mensurar o impacto monetário das ações de retenção, avaliando lucro líquido, ROI e sensibilidade a custos e eficácia das campanhas.  

Ao final, o projeto busca transformar dados em ações concretas, reduzindo o churn, aumentando a receita e fortalecendo o relacionamento com os clientes.

# Benefícios do Projeto e Pipeline de Solução

## Benefícios do Projeto
O desenvolvimento de um modelo preditivo de churn oferece uma série de vantagens estratégicas e financeiras para a empresa de cartão de crédito:

1. **Redução de Perdas Financeiras:**  
   Antecipar clientes com alto risco de cancelamento permite implementar ações de retenção direcionadas, preservando receita anual significativa e reduzindo perdas relacionadas a churn.

2. **Otimização de Custos de Marketing e Retenção:**  
   Com a previsão do risco de churn, as campanhas de retenção podem ser direcionadas apenas aos clientes que realmente necessitam de intervenção, aumentando a eficiência e diminuindo gastos desnecessários.

3. **Tomada de Decisão Baseada em Dados:**  
   Insights sobre comportamento transacional, engajamento e relacionamento com o banco permitem decisões estratégicas mais embasadas, como ajustes de limites de crédito, ofertas personalizadas e cross-sell de produtos.

4. **Aumento da Retenção e do Lifetime Value (CLV):**  
   A retenção de clientes de alto valor contribui para aumentar o CLV médio, fortalecendo a base de clientes e garantindo receita recorrente de longo prazo.

5. **Monitoramento Contínuo e Proatividade:**  
   A análise de sinais de alerta em tempo real possibilita ações preventivas, reduzindo churn antes que ocorra e promovendo maior engajamento do cliente.

6. **Suporte à Estratégia de Crescimento:**  
   Clientes engajados são mais propensos a adquirir produtos adicionais e a se tornarem defensores da marca, ampliando o potencial de receita futura.

---

## Pipeline de Solução
O projeto segue uma abordagem estruturada, baseada na metodologia CRISP-DM, integrando análise de dados, modelagem preditiva e avaliação financeira:

1. **Compreensão do Negócio:**  
   - Entendimento do problema de churn e impacto financeiro.  
   - Definição de objetivos estratégicos e métricas de sucesso.

2. **Coleta e Integração de Dados:**  
   - Extração de dados demográficos, financeiros e transacionais dos clientes.  
   - Integração de múltiplas fontes para consolidar o dataset.

3. **Análise Exploratória de Dados (EDA):**  
   - Estatísticas descritivas e visualizações para entender padrões e outliers.  
   - Identificação de relações entre variáveis e churn.

4. **Pré-processamento e Engenharia de Features:**  
   - Tratamento de valores ausentes e inconsistências.  
   - Codificação de variáveis categóricas, normalização e padronização.  
   - Criação de variáveis derivadas, como delta de uso e mudanças trimestrais.  
   - Balanceamento da variável alvo (churn) para melhorar performance do modelo.

5. **Modelagem Preditiva:**  
   - Treinamento de modelos de classificação (LightGBM) para prever churn.  
   - Validação cruzada e otimização de hiperparâmetros.  
   - Avaliação de métricas de performance (recall, precision, F1-score, AUC-ROC).

6. **Interpretação e Insights:**  
   - Análise de importância de variáveis (*gain* e SHAP).  
   - Identificação de fatores críticos que influenciam o churn.  
   - Segmentação de clientes de alto risco.

7. **Avaliação Financeira:**  
   - Simulação de cenários de retenção considerando custo, eficácia e receita preservada.  
   - Cálculo de ROI, lucro líquido, lift financeiro e break-even.  
   - Análise de sensibilidade e projeção para escalabilidade.

8. **Implementação e Monitoramento:**  
   - Integração do modelo em processos de marketing e CRM.  
   - Monitoramento contínuo do churn, eficácia das campanhas e ajustes periódicos.  
   - Dashboards e indicadores de controle para suporte à decisão.

---

**Resumo:**  
Este pipeline garante que o projeto não apenas forneça previsões precisas, mas também traduza os resultados em ações estratégicas e financeiramente mensuráveis, alinhando ciência de dados com objetivos de negócio e resultados tangíveis.

---

# Análises de BoxPlots das Variáveis
![Boxplots](images/boxplot.png)
A imagem apresenta uma série de **diagramas de caixa (boxplots)** que ilustram a distribuição de diversas variáveis quantitativas.  
A análise se concentra em quatro pilares principais: **Tendência Central**, **Dispersão**, **Simetria** e **Outliers**.

---

##  Tendência Central e Dispersão (Mediana e IQR)

A **Mediana** (linha dentro da caixa) e o **Intervalo Interquartil (IQR)** (comprimento da caixa) variam significativamente entre as variáveis:

- **Baixa Dispersão:**  
  Variáveis como a **primeira** e a **nona** (de cima para baixo) apresentam caixas extremamente estreitas, indicando que **50% dos dados estão concentrados em uma faixa de valores muito pequena**.

- **Alta Dispersão:**  
  Outras variáveis — como a **terceira** e aquelas da **metade inferior** — exibem caixas mais longas, sinalizando **maior variabilidade** nos 50% centrais dos dados.

- **Variáveis Codificadas ou Binárias:**  
  Algumas caixas são **minúsculas** e/ou têm a **Mediana muito próxima de um dos limites**, sugerindo que podem representar **features binárias (0/1)** ou **categóricas codificadas** com predominância de um valor.

---

##  Simetria e Assimetria (Skewness)

A posição da **Mediana** dentro da caixa e o comprimento dos **bigodes (whiskers)** revelam a forma da distribuição:

- **Assimetria Positiva (Skewed Right)** — *Forma mais predominante:*  
  A Mediana está frequentemente próxima do **Primeiro Quartil (Q1)**, com o **bigode superior** mais longo.  
  Isso indica que a **cauda da distribuição se estende para valores mais altos**.

- **Distribuições Quase Simétricas:**  
  Algumas variáveis apresentam a Mediana **centralizada** na caixa e **bigodes equilibrados**, sugerindo **distribuições mais balanceadas** (e.g., a **sétima variável**, na metade superior).

---

##  Presença e Distribuição de Outliers

Os **pontos individuais fora dos bigodes** representam **outliers**, e estão presentes em quase todas as variáveis — uma das **características mais marcantes** do dataset.

- **Outliers Unilaterais (Assimetria Reforçada):**  
  Na maioria das variáveis com **assimetria positiva**, os outliers aparecem **acima do bigode superior**, reforçando a tendência de valores extremos altos.

- **Variáveis Fortemente Contaminadas:**  
  Algumas variáveis (e.g., a **terceira horizontal**) exibem **alta concentração de outliers em ambas as extremidades**, indicando dados **altamente dispersos ou ruidosos**.

- **Outliers Discretos e Extremos:**  
  Em certos casos, os outliers se **estendem por uma ampla faixa no eixo**, revelando **grande variabilidade** mesmo fora do intervalo interquartil.

---

###  Conclusão

A análise dos boxplots demonstra um conjunto de dados com **forte heterogeneidade**, **assimetria positiva predominante** e **presença significativa de outliers**.  
Essas características exigem **cuidadoso pré-processamento** antes da modelagem, incluindo possíveis **transformações de escala** e **tratamento de valores extremos**, para garantir resultados estatísticos e preditivos mais robustos.

---

# Análise da Distribuição da Variável Alvo — Churn
![churn](images/churn.png)

Esta análise apresenta a **distribuição da variável alvo (Churn Flag)**, essencial para compreender o comportamento do conjunto de dados antes da modelagem preditiva.

---

##  Distribuição de Clientes

| Categoria | Contagem | Percentual |
| :--- | ---: | ---: |
| **Não Cancelou (0)** | 6.799 | **83.93%** |
| **Cancelou (1)** | 1.302 | **16.07%** |
| **Total** | 8.101 | 100.00% |

O gráfico de barras evidencia um **forte desbalanceamento de classes**, onde apenas **16% dos clientes cancelaram** o serviço.

---

##  Implicações para a Modelagem

O desbalanceamento impacta diretamente a qualidade dos modelos de *machine learning*:

- **Viés do modelo:** tende a prever majoritariamente “Não Cancelou”.
- **Alta taxa de falsos negativos:** dificuldade em identificar clientes que realmente cancelam.
- **Métricas tradicionais (acurácia)** tornam-se pouco informativas.  
  Métricas recomendadas:
  - **Recall** (para capturar a classe minoritária)  
  - **Precision**, **F1-Score** e **ROC AUC**

---

##  Estratégias de Correção

Para lidar com o desequilíbrio da variável alvo, podem ser aplicadas técnicas como:

- **Oversampling (e.g., SMOTE)** — gerar novas amostras sintéticas da classe *Churn*.  
- **Undersampling** — reduzir amostras da classe majoritária.  
- **Ajuste de pesos** — dar maior importância à classe minoritária nos algoritmos (*class_weight*).  
- **Combinação híbrida** — unir over e undersampling para melhor equilíbrio.

---

###  Conclusão

O dataset apresenta um **problema clássico de classificação desbalanceada**, o que torna a **previsão de churn desafiadora**.  
Abordagens adequadas de **balanceamento e avaliação de métricas** serão fundamentais para alcançar um modelo com real poder preditivo.

---

# Análise
![distribuicao](images/education_level)



