# 📊 Carteiras no Mercado Brasileiro: Aleatórias vs Setoriais vs Markowitz Restrito

👉 **[🔗 Acesse o Dashboard Interativo (GitHub Pages)](https://mhirokitomida.github.io/analise_carteiras_brasil_risco_retorno/)**

---

## 📌 Sobre o projeto

Este projeto investiga como diferentes abordagens de construção de carteiras se comportam no mercado acionário brasileiro.

Foram comparadas estratégias baseadas em:

- 🎲 **Carteiras aleatórias** (diversificação ampla sem regra econômica explícita)  
- 🧱 **Carteiras por setor e subsetor** (concentração temática)  
- ⚖️ **Otimização via Markowitz restrito** (média-variância com limite de peso por ativo)  
- 📊 **Benchmark de mercado (Ibovespa)**  

A análise vai além do retorno puro, incorporando risco, eficiência risco-retorno e testes estatísticos para avaliar a robustez dos resultados.

---

## 🎯 Objetivo

Avaliar, de forma quantitativa e estatística, como diferentes formas de diversificação e concentração produzem perfis distintos de desempenho no mercado brasileiro.

Em especial, o projeto busca investigar:

- 📌 se carteiras aleatórias podem gerar retornos competitivos  
- 📌 se a otimização de portfólio melhora a relação entre retorno e risco  
- 📌 como carteiras concentradas por setor e subsetor se comportam frente a abordagens mais diversificadas  
- 📌 até que ponto as diferenças observadas parecem consistentes dentro da amostra analisada  

---

## 🧠 Metodologia

A análise foi construída em etapas estruturadas:

---

### 1. Construção da base

- Dados históricos de preços ajustados  
- Base consolidada de ativos do mercado brasileiro  
- Inclusão do benchmark (**Ibovespa**)  
- Padronização temporal e alinhamento das séries em período comum  

---

### 2. Geração das carteiras

Foram construídos diferentes grupos de carteiras:

#### 🎲 Carteiras aleatórias
- Mais de **1000 carteiras simuladas**
- Diferentes tamanhos (número de ativos)
- Alta diversidade de combinações

#### 🧱 Carteiras concentradas
- Carteiras por **setor**
- Carteiras por **subsetor**
- Exposição concentrada a grupos específicos do mercado

#### ⚖️ Carteiras otimizadas
- Otimização via **Markowitz restrito**
- Janela de estimação histórica sem look-ahead
- Rebalanceamento periódico
- Restrição de peso máximo por ativo

---

### 3. Simulação das carteiras

Para cada carteira:

- 📈 Cálculo do retorno mensal  
- 📊 Curva de capital acumulada  
- 📉 Drawdown ao longo do tempo  

---

### 4. Métricas de avaliação

Foram calculadas métricas centrais de desempenho e risco:

- 📈 Retorno anualizado  
- 📊 Volatilidade  
- ⚖️ **Sharpe simplificado**  
- 📉 Drawdown máximo  
- 📊 **Sortino simplificado**  
- 📈 Calmar  

> **Observação:** o Sharpe e o Sortino utilizados no projeto são versões **simplificadas**, aplicadas de forma padronizada a todas as estratégias. Isso preserva a comparabilidade relativa entre as carteiras, embora não corresponda exatamente às formulações clássicas com taxa livre de risco explícita.

---

### 5. Análise estatística

Para validar os resultados, foram utilizados:

- **Mann-Whitney** para comparações independentes  
- **Wilcoxon pareado** como teste principal entre Markowitz restrito e a carteira aleatória correspondente  
- **Bootstrap pareado** para estimar a diferença média com intervalo de confiança  
- **Permutação pareada** para reforçar a robustez da evidência  

---

## 📈 Principais Resultados

- O **Markowitz restrito** apresentou o melhor desempenho agregado do projeto  
- O grupo liderou em **retorno anual médio**, **Sharpe simplificado médio** e **drawdown médio menos severo**  
- As carteiras **aleatórias** continuaram fortes e **superaram o Ibovespa** no agregado  
- Carteiras **setoriais e subsetoriais** foram as menos eficientes no agregado  
- Parte do desempenho das carteiras aleatórias continua refletindo o **efeito do acaso** em um universo amplo de combinações  
- A comparação **pareada** reforçou a vantagem do Markowitz restrito sobre as aleatórias correspondentes  

👉 Isso sugere que:

> A diversificação simples já é poderosa —  
> mas, neste estudo, a otimização com restrição de peso produziu o melhor equilíbrio entre retorno e risco.

---

## 📊 Visualizações

O projeto inclui um relatório HTML interativo com:

- 📈 gráfico dinâmico com séries de retorno  
- 🎛️ filtros por tipo de carteira e modo (resumo vs individual)  
- 📊 tabela interativa sincronizada com o gráfico  
- 📉 distribuições de retorno e Sharpe simplificado  
- 📊 boxplots e dispersão risco-retorno  
- 🏆 ranking interativo por métricas  
- 🔍 exploração detalhada das carteiras  

---

## 🌐 Visualização do projeto

👉 https://mhirokitomida.github.io/analise_carteiras_brasil_risco_retorno/

---

## ⚠️ Observações importantes

- A análise utiliza **carteiras simuladas**, não recomendações reais  
- Os resultados são **sensíveis ao período analisado**  
- A otimização de Markowitz restrito depende das estimativas de retorno e covariância  
- Parte dos resultados pode ser influenciada por **variabilidade aleatória**  
- O estudo identifica **associação empírica**, não causalidade  
- O benchmark utilizado foi o **Ibovespa**  
- Algumas carteiras Markowitz com histórico insuficiente foram descartadas das métricas finais por critério mínimo de observações  

---

## 🧠 Principais Aprendizados

- A **diversificação simples** já produz resultados fortes e competitivos  
- As **carteiras aleatórias** superaram o benchmark no agregado  
- Parte desse desempenho reflete o **efeito do acaso**, e não uma superioridade estrutural da aleatoriedade  
- O **Markowitz restrito** liderou o agregado em **retorno anual médio**, **Sharpe simplificado médio** e **drawdown médio**  
- A comparação **pareada** reforçou a vantagem do Markowitz restrito sobre as aleatórias correspondentes  
- Carteiras **concentradas** foram as menos eficientes no agregado  
- A concentração aumentou risco sem compensação proporcional em retorno  
- Os testes estatísticos reforçaram que a vantagem observada do Markowitz restrito sobre as aleatórias correspondentes não parece ser apenas ruído  
- **Sharpe** e **Sortino** foram usados em versões **simplificadas**, preservando a comparabilidade relativa entre as estratégias  
- A escolha da estratégia continua dependendo do objetivo do investidor, mas, neste estudo, o **Markowitz restrito** foi a solução mais forte no agregado  

---

## 🏁 Conclusão

O estudo reforça uma ideia central:

> **Diversificar já ajuda muito, mas otimizar ajudou ainda mais neste recorte.**

As carteiras aleatórias continuaram mostrando que a diversificação ampla pode gerar resultados muito competitivos, inclusive acima do benchmark. No entanto, após os ajustes metodológicos e a revisão da análise, o **Markowitz restrito** passou a se destacar como a abordagem mais completa do projeto, combinando **maior retorno médio**, **melhor eficiência risco-retorno** e **menor severidade média de drawdown**.

Isso não elimina a importância da diversificação simples, nem invalida o papel do acaso em parte do sucesso das carteiras aleatórias. O que o projeto sugere é que, partindo de uma base já diversificada, a **otimização com restrição de peso** conseguiu melhorar ainda mais o equilíbrio entre retorno e risco.

Em termos práticos:

> **a diversificação é poderosa, mas a otimização restrita de pesos foi a estratégia mais robusta no agregado dentro da amostra analisada.**
