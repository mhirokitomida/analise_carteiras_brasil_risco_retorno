# 📊 Carteiras no Mercado Brasileiro: Aleatórias vs Setoriais vs Markowitz

👉 **[🔗 Acesse o Dashboard Interativo (GitHub Pages)](https://mhirokitomida.github.io/analise_carteiras_brasil_risco_retorno/)**

---

## 📌 Sobre o projeto

Este projeto investiga como diferentes abordagens de construção de carteiras se comportam no mercado acionário brasileiro.

Foram comparadas estratégias baseadas em:

- 🎲 **Carteiras aleatórias** (diversificação sem viés)  
- 🧱 **Carteiras por setor e subsetor** (concentração)  
- ⚖️ **Otimização via Teoria de Portfólio de Markowitz**  
- 📊 **Benchmark de mercado (Ibovespa)**  

A análise vai além do retorno puro, incorporando risco, eficiência e testes estatísticos para avaliar a robustez dos resultados.

---

## 🎯 Objetivo

Avaliar, de forma quantitativa e estatística, se existe evidência de que:

- 📌 Carteiras aleatórias podem gerar retornos competitivos  
- 📌 A otimização de portfólio melhora a eficiência risco-retorno  

Além disso, o projeto busca entender:

- O impacto da **diversificação vs concentração**  
- A diferença entre **retorno absoluto e qualidade do retorno**  
- Se os resultados observados são **robustos ou fruto do acaso**  

---

## 🧠 Metodologia

A análise foi construída em etapas estruturadas:

---

### 1. Construção da base

- Dados históricos de preços ajustados  
- Base consolidada de ativos do mercado brasileiro  
- Inclusão do benchmark (**IBOVESPA**)  
- Padronização temporal e limpeza dos dados  

---

### 2. Geração das carteiras

Foram construídos diferentes grupos de carteiras:

#### 🎲 Carteiras aleatórias
- Mais de 1000 carteiras simuladas  
- Diferentes tamanhos (número de ativos)  
- Alta diversidade de combinações  

#### 🧱 Carteiras concentradas
- Carteiras por **setor**  
- Carteiras por **subsetor**  
- Representam exposição concentrada  

#### ⚖️ Carteiras otimizadas
- Otimização via Teoria de Portfólio de Markowitz  
- Janela de estimação sem look-ahead  
- Rebalanceamento periódico  

---

### 3. Simulação das carteiras

Para cada carteira:

- 📈 Cálculo do retorno mensal  
- 📊 Curva de capital acumulada  
- 📉 Drawdown ao longo do tempo  

---

### 4. Métricas de avaliação

Foram calculadas métricas fundamentais:

- 📈 Retorno anualizado  
- 📊 Volatilidade  
- ⚖️ Sharpe Ratio  
- 📉 Drawdown máximo  
- 📊 Sortino e Calmar  

---

### 5. Análise estatística

Para validar os resultados:

- Teste de **Mann-Whitney**  
- Teste de **Wilcoxon pareado**  
- **Bootstrap** (intervalos de confiança)  
- **Teste de permutação**  

---

## 📈 Principais Resultados

- Carteiras **aleatórias** apresentaram maior retorno médio anual  
- O modelo de **Markowitz** apresentou maior eficiência risco-retorno (Sharpe superior)  
- O **drawdown** foi menor nas carteiras otimizadas  
- Carteiras **setoriais e subsetoriais** foram as menos eficientes no agregado  
- Parte do desempenho das carteiras aleatórias reflete o **efeito do acaso** em um grande conjunto de combinações  

👉 Isso sugere que:

> A diversificação simples já é poderosa —  
> mas eficiência e controle de risco exigem otimização.

---

## 📊 Visualizações

O projeto inclui um relatório HTML interativo com:

- 📈 Gráfico dinâmico com séries de retorno  
- 🎛️ Filtros por tipo de carteira e modo (resumo vs individual)  
- 📊 Tabela interativa sincronizada com o gráfico  
- 📉 Distribuições de retorno e Sharpe  
- 📊 Boxplots e dispersão risco-retorno  
- 🏆 Ranking interativo por métricas  
- 🔍 Exploração detalhada das carteiras  

---

## 🌐 Visualização do projeto

👉 https://mhirokitomida.github.io/analise_carteiras_brasil_risco_retorno/

---

## ⚠️ Observações importantes

- A análise utiliza **carteiras simuladas**, não recomendações reais  
- Resultados são **sensíveis ao período analisado**  
- A otimização de Markowitz depende das estimativas de retorno e covariância  
- Parte dos resultados pode ser influenciada por **variabilidade aleatória**  
- O estudo identifica **associação empírica**, não causalidade  
- O benchmark utilizado foi o **IBOVESPA**  

---

## 🧠 Principais Aprendizados

- A **diversificação simples** já produz resultados competitivos  
- Carteiras **aleatórias** superaram o benchmark no agregado  
- Parte desse desempenho reflete o **efeito do acaso**, não uma superioridade estrutural  
- O modelo de **Markowitz** melhora significativamente a eficiência risco-retorno  
- O Markowitz apresentou **Sharpe mais alto** e **menor drawdown**  
- Carteiras **concentradas** foram as menos eficientes  
- A concentração aumenta risco sem compensação proporcional  
- Os testes estatísticos indicam que as diferenças não são apenas ruído  
- Retorno e eficiência são dimensões distintas — não apontam o mesmo vencedor  
- A escolha da estratégia depende do objetivo do investidor  

---

## 🏁 Conclusão

O estudo reforça uma ideia central:

> Não existe uma estratégia única superior em todas as dimensões analisadas.

Carteiras aleatórias se destacaram em retorno médio, enquanto o modelo de Markowitz se destacou em eficiência e controle de risco.

Além disso, o papel do acaso não deve ser ignorado. Em um universo amplo de carteiras, algumas combinações naturalmente se destacam, o que ajuda a explicar parte do desempenho das carteiras aleatórias. Isso não significa que investir de forma aleatória seja a melhor estratégia, mas sim que a diversificação, combinada com variabilidade, pode gerar resultados competitivos.

Em termos práticos:

> Diversificar já é poderoso —  
> otimizar melhora a eficiência —  
> e a melhor estratégia depende do equilíbrio entre retorno e risco.
