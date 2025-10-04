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

# Análise — Distribuição do Nível de Educação (`education_level`)
![distribuicao](images/education_level.png)

O gráfico apresenta a distribuição dos níveis educacionais no conjunto de dados, destacando as categorias mais representativas e suas implicações para o projeto de *Machine Learning*.

---

###  Principais Resultados

A distribuição concentra-se em três categorias principais, que juntas representam mais de **65%** dos dados:

- **Graduate (30,6%)** — categoria majoritária.  
- **High School (20,4%)** — segunda mais frequente.  
- **Unknown (14,9%)** — terceira mais comum, exigindo tratamento específico.

As categorias **Uneducated (14,6%)** e **College (9,8%)** possuem presença intermediária, enquanto **Post-Graduate (5,3%)** e **Doctorate (4,4%)** são minoritárias.

---

###  Implicações Analíticas

1. **Tratamento de valores "Unknown":** Deve ser imputado ou mantido como categoria própria, pois pode conter informação preditiva.  
2. **Agrupamento de classes raras:** *Post-Graduate* e *Doctorate* podem ser combinadas em uma categoria “Advanced Degrees” para melhorar o aprendizado do modelo.  
3. **Foco nas classes majoritárias:** As análises e segmentações iniciais devem priorizar *Graduate* e *High School*, que representam o perfil predominante dos clientes.

---

Em síntese, o dataset apresenta um público com predominância de formação **média e superior**, mas com **lacunas relevantes de informação educacional**, fator que deve ser cuidadosamente tratado nas etapas de modelagem.

---

# Análise — Distribuição do Estado Civil (`marital_status`)
![distribuicao](images/marital_status.png)

O gráfico exibe a distribuição dos clientes por estado civil, destacando as categorias mais representativas e as implicações para o tratamento dos dados.

---

###  Principais Resultados

A variável apresenta **alta concentração** em duas categorias, que juntas somam **85,2%** dos clientes:

- **Married (46,4%)** — categoria majoritária.  
- **Single (38,8%)** — segunda mais frequente.  

As categorias minoritárias são:  
- **Unknown (7,5%)**  
- **Divorced (7,4%)**

Essas duas últimas possuem proporções semelhantes e representam uma pequena parcela da base.

---

###  Implicações Analíticas

1. **Tratamento da categoria "Unknown":**  
   - Pode ser mantida como uma categoria própria durante a codificação (*One-Hot Encoding*), pois a ausência de informação pode ter valor preditivo.  
   - Alternativamente, pode ser imputada com a moda (*Married*), se houver justificativa sólida.  

2. **Impacto na Modelagem:**  
   - As classes **Divorced** e **Unknown** terão menor influência no treinamento do modelo devido à sua baixa representatividade.  
   - A modelagem deve priorizar a correta diferenciação entre **Married** e **Single**, que dominam a amostra.

---

Em síntese, o estado civil dos clientes é predominantemente **Casado ou Solteiro**, enquanto os dados *Unknown* exigem atenção especial durante o pré-processamento para evitar viés no modelo.

---

# Análise — Distribuição da Categoria de Renda (`income_category`)
![distribuicao](images/income_category.png)

O gráfico apresenta a distribuição dos clientes por faixas de renda, destacando a predominância das classes de **renda baixa e média**.

---

###  Perfil de Renda dos Clientes

A base é dominada por clientes com **renda abaixo de \$80K**, que representam cerca de **67%** do total:

- **Less than \$40K:** 35,0% (classe majoritária)  
- **\$40K – 60K:** 17,9%  
- **\$60K – 80K:** 14,0%  

As faixas de **renda alta** e **dados ausentes** têm menor presença:

- **\$120K +:** 7,3% (classe minoritária)  
- **Unknown:** 10,9% (dados faltantes significativos)

---

###  Implicações Analíticas

1. **Viés de Aprendizado:**  
   O modelo de *Machine Learning* aprenderá padrões dominantes das faixas de **renda baixa e média**, com pouca representatividade das classes mais altas.

2. **Tratamento da Categoria “Unknown”:**  
   Deve ser mantida como categoria própria durante a codificação, pois a ausência de informação pode conter valor preditivo relevante.

3. **Ajuste de Categorias:**  
   Para lidar com o baixo volume da faixa **\$120K +**, pode-se agrupá-la com **\$80K – 120K** em uma categoria única (“\$80K +”), fortalecendo o aprendizado sobre clientes de renda mais alta.

---

Em resumo, o conjunto de dados reflete uma base **majoritariamente de classe média-baixa**, o que requer atenção ao balanceamento e à representação das faixas superiores e dos dados desconhecidos na modelagem.
