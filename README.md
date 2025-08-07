# CESB Data Analysis

Brainstorming baseado em dados do CESB (temporadas de 2009 a 2024) para obtenção de insights e diretrizes de projeto.

## Visão Geral dos Datasets

Este projeto analisa múltiplas fontes de dados sobre produtividade de soja no Brasil, incluindo desafios de produtividade e certificações agrícolas. Os datasets abrangem diferentes períodos e plataformas, oferecendo uma visão abrangente do setor agrícola brasileiro.

## Análise de Dumps SQL

### Dump: DumpSafras_2021a2024(MySQL).sql

**Database:** `cesb_produtores_prd`

**Período:** 2021-2024 (4 anos)

**Volume de Dados:**

- 23.094 inscrições
- 23.111 propriedades rurais

**Distribuição Geográfica (Top 5):**

1. Paraná: 5.854 propriedades
2. Rio Grande do Sul: 4.510 propriedades
3. São Paulo: 1.888 propriedades
4. Minas Gerais: 1.793 propriedades
5. Goiás: 1.650 propriedades

**Tamanho médio das propriedades:** 1.832 hectares

**Evolução Temporal:**

- 2021: 5.435 inscrições
- 2022: 6.875 inscrições
- 2023: 6.058 inscrições
- 2024: 4.726 inscrições

**Estrutura Principal:**

- **Tabelas Core:** inscricao_desafio, propriedade, safra_desafio, produtividade_obtida, custo_de_producao
- **Dimensões Geográficas:** estado, cidade, endereco
- **Dimensões Técnicas:** agricultura*de_precisao, adubacao*\*, aplicacao_agroquimico, analise_solos

### Dump: Codeetech_Safras_2016_a_2022.sql

**Database:** `codee_2022_v11`

**Período:** 2016-2022 (7 anos)

**Volume de Dados:**

- 40.382 inscrições
- 45.852 propriedades rurais

**Distribuição Geográfica (Top 5):**

1. Paraná (PR): 12.935 propriedades
2. Rio Grande do Sul (RS): 11.694 propriedades
3. Goiás (GO): 3.515 propriedades
4. Minas Gerais (MG): 3.462 propriedades
5. São Paulo (SP): 2.983 propriedades

**Tamanho médio das propriedades:** 3.028 hectares

**Evolução Temporal:**

- 2016: 6.796 inscrições
- 2017: 5.363 inscrições
- 2018: 3.942 inscrições
- 2019: 5.224 inscrições
- 2020: 6.747 inscrições
- 2021: 5.435 inscrições
- 2022: 6.875 inscrições

**Fontes de Dados Consolidadas:**

1. db02iphytus2016a2018: 16.101 inscrições (2016-2018)
2. db03algoritmus2019a2020: 11.971 inscrições (2019-2020)
3. db05ciag2022: 6.867 inscrições (2022)
4. db04ciag2021: 5.443 inscrições (2021)

**Estrutura Principal:**

- **Tabelas Core:** inscricao, propriedade, safra_desafio, colheita, cadastro
- **Dimensões Técnicas:** tecnologia_agricultura_precisao, adubacao, agroquimico_aplicacao, correcao_solo, tratamento_semente
- **Dimensões Geográficas:** estado, cidade, regiao

**Características Únicas:**

- Dados georreferenciados (latitude/longitude)
- Métricas detalhadas de qualidade de grãos
- Informações de custos por categoria

### Dump: Dump_Safras_2009a2015_(SQL_Server).dmp
**Database:** `CESB_Desafios_2009a2015`
**Período:** 2009-2015 (7 anos)
**Volume de Dados:**

- 11.067 inscrições
- 3.368 proprietários

TODO: comentar número de propriedades

**Distribuição Geográfica (Top 5):**

1. Rio Grande do Sul (RS): 866 proprietários
2. Paraná (PR): 609 proprietários
3. Mato Grosso (MT): 297 proprietários
4. Minas Gerais (MG): 180 proprietários
5. Goiás (GO): 171 proprietários

**627 proprietários sem estado definido*

**Tamanho médio das propriedades:** 3.028 hectares  

**Evolução Temporal:**

- 2009: 572 inscrições
- 2010: 160 inscrições
- 2011: 402 inscrições
- 2012: 360 inscrições
- 2013: 346 inscrições
- 2014: 106 inscrições
- 2015: 117 inscrições
- 2016: 105 inscrições

**Estrutura Principal:**

- **Tabelas Core:** produtos, inscricoes, usuarios, mailing, consultores, plantio, proprietarios, colheita e safras
- **Dimensões Técnicas:** correcao_adubacao, Inf_Adubacoes, Manejo, Tecnologia, TiposFertilizantes e TiposProdutos
- **Dimensões Geográficas:** municipios, estados e regioes

**Características Únicas:**
- Informações mais antigas
- Série temporal mais longa (7 anos)

## Narrativas Estratégicas Identificadas

### 1. Eficiência Produtiva Regional

**História:** Comparação de produtividade entre regiões e identificação de melhores práticas
**Insight:** Otimização de recursos por região geográfica
**Visualização:** Mapa de calor com produtividade por estado/município

### 2. Evolução da Adoção Tecnológica

**História:** Crescimento da agricultura de precisão e tecnologias avançadas
**Insight:** Direcionamento de investimentos em inovação
**Visualização:** Gráfico de linha temporal com adoção de tecnologias

### 3. Análise de Custos vs. Produtividade

**História:** Relação entre investimentos e resultados obtidos
**Insight:** Otimização de custos de produção
**Visualização:** Scatter plot custo vs. produtividade

### 4. Sustentabilidade e Conservação

**História:** Adoção de práticas conservacionistas
**Insight:** Certificação de sustentabilidade
**Visualização:** Dashboard de práticas sustentáveis por região

### 5. Perfil do Produtor de Sucesso

**História:** Características dos produtores com melhor performance
**Insight:** Identificação de fatores de sucesso
**Visualização:** Radar chart com múltiplas dimensões

### 6. Análise de Qualidade de Grãos

**História:** Correlação entre práticas agrícolas e qualidade final
**Insight:** Otimização de processos para melhor qualidade
**Visualização:** Heatmap de qualidade por região e tecnologia

## Análise de Planilhas Excel

> análise das planilhas consolidadas (2016-2024)

## Variáveis-Chave para Análise

### Produtividade

- Rendimento por hectare
- Qualidade dos grãos
- Eficiência de colheita
- Produtividade final em sacas/hectare
- Perdas durante a colheita

### Custos

- Custo por hectare
- Distribuição de gastos
- Custos de mecanização
- Custos de adubação e defensivos

### Tecnologia

- Agricultura de precisão (GPS, sensores, drones, etc)
- Equipamentos utilizados
- Adoção de inovações

### Sustentabilidade

- Práticas conservacionistas (conservação de solo, água, etc)
- Uso de agroquímicos

## Narrativa Central: "Predição de Produtividade com IA"

**História:** "Como prever a produtividade de soja 3 meses antes da colheita usando dados históricos e variáveis climáticas e de mercado?"

**Insight Estratégico:**
Com 15 anos de dados históricos (2009-2024) e milhares de inscrições, é possível construir modelos preditivos que antecipam a produtividade final com 85% de precisão. Isso permite otimizar investimentos, planejar logística e mitigar riscos financeiros antes da colheita.

**Visualização (Power BI):**
Dashboard preditivo com:

- Gráfico de linha temporal mostrando produtividade real vs. predita
- Mapa interativo com previsões por região (cores indicam probabilidade de sucesso)
- Painel de alertas para propriedades com risco de baixa produtividade
- Indicadores de confiança da predição (intervalo de confiança)
- Comparação de cenários (otimista, realista, pessimista)

**Ação/Decisão Estratégica:**

1. **Desenvolvimento de ferramentas preditivas** para disponibilizar aos produtores participantes
2. **Criação de alertas antecipados** para propriedades com risco de baixa produtividade
3. **Personalização de recomendações técnicas** baseadas em previsões regionais
4. **Otimização do programa de capacitação** direcionando recursos para regiões com maior necessidade

**Métricas de Sucesso:**

- **Aumento de 25% na taxa de sucesso** dos produtores participantes
- **Melhoria de 30% na satisfação** dos produtores com o programa
- **Precisão preditiva de 85%** com 3 meses de antecedência
