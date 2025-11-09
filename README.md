# 📊 Análise de Concentração Populacional nas Capitais Brasileiras

Este projeto realiza uma **análise estatística** sobre a concentração populacional nas capitais dos estados brasileiros utilizando o **Teste Z** para proporções. O objetivo é testar a hipótese de que as capitais concentram mais da metade da população do estado, identificando padrões de distribuição demográfica no Brasil.

> Verificar, através de métodos estatísticos rigorosos, se existe evidência significativa de que as capitais brasileiras concentram uma proporção populacional maior que 50% em relação ao total do estado, utilizando dados oficiais do IBGE de 2021.

## 🔬 Metodologia

### Teste de Hipótese

O projeto utiliza o **Teste Z para proporções** com as seguintes hipóteses:

- **H₀ (Hipótese Nula)**: A proporção da população na capital é igual a 50% (p = 0.5)
- **H₁ (Hipótese Alternativa)**: A proporção da população na capital é maior que 50% (p > 0.5)

### Estatística do Teste

A estatística Z é calculada pela fórmula:

$$Z = \frac{p_1 - p_0}{\sqrt{\frac{p_0(1-p_0)}{n}}}$$

Onde:
- $p_1$ = proporção da população na capital
- $p_0$ = 0.5 (proporção sob H₀)
- $n$ = população total do estado

### Critério de Decisão

- **Nível de significância (α)**: 0.05 (5%)
- **Teste unilateral à direita**
- **Rejeita-se H₀** se p-valor < 0.05

## 📊 Fonte de Dados

Os dados utilizados são provenientes do **Instituto Brasileiro de Geografia e Estatística (IBGE)**, referentes ao ano de **2021**, contendo informações sobre:

- População de todos os municípios brasileiros
- Códigos IBGE dos municípios
- Identificação das capitais estaduais

**Arquivo**: `dados_municipios.xlsx`

## 🛠️ Tecnologias Utilizadas

- **Python 3.x**
- **Pandas**: Manipulação e análise de dados
- **SciPy**: Cálculos estatísticos (distribuição normal)
- **Matplotlib**: Visualização de dados
- **Seaborn**: Gráficos estatísticos
- **Jupyter Notebook**: Ambiente de desenvolvimento interativo

## 📈 Resultados

O notebook gera:

1. **Tabela completa** com estatísticas para todos os estados:
   - População da capital
   - População do restante do estado
   - Proporções (p1, p2)
   - Estatística Z
   - P-valor
   - Decisão do teste

2. **Resumo textual** indicando para cada estado:
   - ✅ Estados onde a capital concentra significativamente mais população
   - ❌ Estados onde não há evidência de concentração na capital

3. **Gráfico de barras** mostrando o percentual de população nas capitais, ordenado do maior para o menor

## 🔍 Interpretação dos Resultados

- **Z > Z_crítico (1.645) e p-valor < 0.05**: 
  - Há evidência estatística significativa de que a capital concentra mais de 50% da população
  
- **Z ≤ Z_crítico ou p-valor ≥ 0.05**: 
  - Não há evidência suficiente para afirmar que a capital concentra mais de 50% da população

## 📁 Estrutura do Projeto

```
ztest-population-distribution/
│
├── teste_z_populacional.ipynb    # Notebook principal com a análise
├── dados_municipios.xlsx          # Dados do IBGE (não incluído no repositório)
└── README.md                      # Este arquivo
```

## 📝 Notas Importantes

- Os dados são referentes ao ano de **2021**
- O Distrito Federal é tratado como um estado especial (capital = estado)
- A análise considera apenas estados com dados completos