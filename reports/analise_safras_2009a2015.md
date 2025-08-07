### Dump: Dump_Safras_2009a2015_(SQL_Server).dmp

## Visão Geral do Dataset
O banco de dados `Dump_Safras_2009a2015_(SQL_Server).dmp` contém informações sobre o Desafio CESB (Comitê Estratégico Soja Brasil) durante o período de 2009 a 2015. O dataset possui **11.067 inscrições** distribuídas durante o período analisado. Esse dataset é particularmente diferente dos outros dumps, pois abrange um período mais antigo e fornece uma visão histórica das edições do desafio, não possuindo campos e tabelas que estão presentes nos dumps mais recentes.

## Estrutura Principal

### Tabelas Core
- **produtos**: Dados de produtos agrícolas utilizados em cada safra
- **inscricoes**: Registro das inscrições dos participantes
- **usuarios**: Dados dos usuários participantes
- **consultores**: Consultores envolvidos no desafio
- **plantio**: Dados sobre os plantios realizados pelos participantes
- **proprietarios**: Informações de todos os proprietários já registrados em alguma edição
- **colheita**: Métricas detalhadas de produtividade e qualidade
- **safras**: Informações sobre as safras/edições

### Dimensões Técnicas

- **correcao_adubacao**: Correção e adubação do solo
- **Inf_Adubacoes**: Informações sobre adubações
- **Manejo**: Manejo de culturas no cultivo
- **Tecnologia**: Tecnologias utilizadas pelos participantes
- **TiposFertilizantes**: Tipos de fertilizantes utilizados
- **TiposProdutos**: Tipos de produtos utilizados

### Dimensões Geográficas

- **estado**: Distribuição por estados brasileiros
- **município**: Localização das propriedades
- **regioes**: Agrupamento regional

## Distribuição Geográfica

**Top 5 Estados:**

1. Rio Grande do Sul (RS): 866 proprietários
2. Paraná (PR): 609 proprietários
3. Mato Grosso (MT): 297 proprietários
4. Minas Gerais (MG): 180 proprietários
5. Goiás (GO): 171 proprietários

## Evolução Temporal

**Inscrições por ano:**

- 2009: 572 inscrições
- 2010: 160 inscrições
- 2011: 402 inscrições
- 2012: 360 inscrições
- 2013: 346 inscrições
- 2014: 106 inscrições
- 2015: 117 inscrições
- 2016: 105 inscrições

## Variáveis-Chave para Análise

### Qualidade

- **umidade**: Umidade dos grãos
- **impureza**: Nível de impurezas
- **produtividade**: Produtividade por hectare

### Custos e Technologia
- **Custos_Por_SC**: Custos por safra/edição
- **Modelo_Pulver**: Tecnologia de pulverização

## Diferencial do Dataset

### Características Únicas
- Informações mais antigas
- Série temporal mais longa (7 anos)
