# Análise Introdutória - Database CESB Produtores

## Visão Geral do Dataset

O banco de dados `cesb`, o qual foi extraído do dump mariaDB `Dump_Safras_2019a2020_(MariaDB).sql`, contém informações sobre o Desafio CESB (Comitê Estratégico Soja Brasil) durante o período de 2019 a 2020. O dataset possui **28.111 inscrições**.

## Estrutura Principal

### Tabelas Core

- **inscricao_desafio**: Registro principal das inscrições (28.111 registros)
- **propriedade**: Dados das propriedades rurais (23.111 registros)
- **safra_desafio**: Configurações das safras/edições
- **produtividade_obtida**: Métricas de produtividade
- **custo_de_producao**: Análise de custos

- **agroquimico**: Dados relacionados ao uso de agroquímicos (42.843 registros)
- **desafiosoja_inscricao**: Registro principal das inscrições (27.883 registros)
- **produto**: Dados de produtos agrícolas utilizados em cada safra
- **safra**: Coluna de referência para o ano das safras analisadas em cada desafio

### Dimensões Geográficas

Todos os dados geográficos estão dentro da tabela `desafiosoja_inscricao`, que contém dados relacionados a localização das propriedades:

- **property_state**: 9 estados principais
- **property_city**: Localização das propriedades
- **property_size**: Tamanho das propriedades (em hectares)

### Dimensões Técnicas

- **tratamento_semente_agroquimico**: Dados sobre o tratamento de sementes e aplicação de agroquímicos
- **tratamento_semente_produto**: Dados sobre o tratamento de sementes e produtos variados utilizados
- **correcao_solo**: Registro de correção de solo e mineral utilizado

## Distribuição Geográfica

**Top 5 Estados:**

1. Paraná: 8.236 propriedades
2. Rio Grande do Sul: 8.209 propriedades
3. Goiás: 2.056 propriedades
4. Minas Gerais: 1.919 propriedades
5. São Paulo: 1.611 propriedades

## Evolução Temporal

**Inscrições por ano:**

- 2020/2021: 6.766 inscrições
- 2019/2020: 5.221 inscrições
- 2018/2019: 3.942 inscrições
- 2017/2018: 5.571 inscrições
- 2016/2017: 6.603 inscrições