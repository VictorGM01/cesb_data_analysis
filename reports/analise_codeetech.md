# Análise Introdutória - Database Codeetech

## Visão Geral do Dataset

O banco de dados `codee_2022_v11`, o qual foi extraído do dump mysql `Codeetech_Safras_2016_a_2022.sql`, contém informações consolidadas de múltiplas fontes sobre desafios de produtividade de soja no Brasil. O dataset possui **40.382 inscrições** distribuídas em **45.852 propriedades** rurais, abrangendo o período de 2016 a 2022.

## Estrutura Principal

### Tabelas Core

- **inscricao**: Registro principal das inscrições (40.382 registros)
- **propriedade**: Dados das propriedades rurais (45.852 registros)
- **safra_desafio**: Configurações das safras/edições
- **colheita**: Métricas detalhadas de produtividade e qualidade
- **cadastro**: Informações dos participantes

### Dimensões Técnicas

- **tecnologia_agricultura_precisao**: Tecnologias de precisão
- **adubacao**: Diferentes tipos de adubação
- **agroquimico_aplicacao**: Uso de agroquímicos
- **correcao_solo**: Características e correções do solo
- **tratamento_semente**: Qualidade e tratamento de sementes

### Dimensões Geográficas

- **estado**: Distribuição por estados brasileiros
- **cidade**: Localização das propriedades
- **regiao**: Agrupamento regional

## Fontes de Dados

O dataset é composto por dados de **4 fontes principais**:

1. **db02iphytus2016a2018**: 16.101 inscrições (2016-2018)
2. **db03algoritmus2019a2020**: 11.971 inscrições (2019-2020)
3. **db05ciag2022**: 6.867 inscrições (2022)
4. **db04ciag2021**: 5.443 inscrições (2021)

## Distribuição Geográfica

**Top 5 Estados:**

1. Paraná (PR): 12.935 propriedades
2. Rio Grande do Sul (RS): 11.694 propriedades
3. Goiás (GO): 3.515 propriedades
4. Minas Gerais (MG): 3.462 propriedades
5. São Paulo (SP): 2.983 propriedades

**Tamanho médio das propriedades:** 3.028 hectares

## Evolução Temporal

**Inscrições por ano:**

- 2016: 6.796 inscrições
- 2017: 5.363 inscrições
- 2018: 3.942 inscrições
- 2019: 5.224 inscrições
- 2020: 6.747 inscrições
- 2021: 5.435 inscrições
- 2022: 6.875 inscrições

## Variáveis-Chave para Análise

### Produtividade

- **resultados_finais_produtividade_final_kg**: Produtividade final em kg
- **resultados_finais_produtividade_final_sc**: Produtividade final em sacas
- **media_produtividade_atual**: Média de produtividade atual
- **pesagem_perdas_colheita**: Perdas durante a colheita

### Qualidade

- **pesagem_umidade**: Umidade dos grãos
- **impureza**: Nível de impurezas
- **pesagem_quebrados**: Grãos quebrados
- **pesagem_esverdeados**: Grãos esverdeados

### Custos

- **custos_area_audit_custo_total_ha**: Custo total por hectare
- **custos_area_audit_mecanizacao**: Custos de mecanização
- **custos_area_audit_adubacao_corretivos**: Custos de adubação
- **custos_area_audit_defensivos**: Custos de defensivos

### Tecnologia

- **tecnologia_agricultura_precisao**: Tecnologias de precisão
- **tecnologia_colhedora**: Equipamentos de colheita
- **tecnologia_plantadeira_semeadora**: Equipamentos de plantio
- **tecnologia_pulverizador**: Equipamentos de pulverização

## Diferencial do Dataset

### Características Únicas

- **Dados consolidadas** de múltiplas plataformas
- **Série temporal longa** (7 anos de dados)
- **Métricas detalhadas** de qualidade de grãos
- **Informações de custos** por categoria
- **Dados georreferenciados** (latitude/longitude)

## Observações Técnicas

- Dataset consolidado com múltiplas fontes
- Boa cobertura temporal (2016-2022)
- Dados georreferenciados disponíveis
- Métricas detalhadas de qualidade e custos
- Potencial para análise preditiva e prescritiva
- Compatível com outros datasets agrícolas
