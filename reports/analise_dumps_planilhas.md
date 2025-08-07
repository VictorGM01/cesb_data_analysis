# Análise de Dumps e Planilhas do CESB

## Visão Geral dos Dumps

Os dumps do CESB são conjuntos de dados extraídos de diferentes fontes, abrangendo informações sobre os desafios de produtividade de soja brasileiros. Cada dump possui características específicas, como período de abrangência, volume de dados e estrutura de tabelas.

Ao longo dos anos, os dumps evoluíram em termos de complexidade e volume de dados, refletindo o crescimento do desafio e a adoção de novas tecnologias agrícolas, ocasionando mudanças significativas na estrutura dos dados. 

## Análise das Planilhas

As planilhas do CESB são arquivos Excel, desenvolvidos a partir de consultas realizadas nos dumps do CESB. Elas visam facilitar a análise e visualização dos dados, permitindo que os usuários explorem as informações nos 9 módulos principais:
1. Histórico da gleba
2. Correção do solo e gessagem
3. Implantação agrícola
4. Tratamento de sementes
5. Adubação
6. Agroquímicos
7. Tecnologia
8. Inscrição
9. Colheita

Para exemplificação, a planilha `08 - Tecnologias.xlsx` contém informações que foram obtidas utilizando várias tabelas dos dumps do período abrangido, como mostra o recorte abaixo:

| Colunas Planilha       | Tabelas Dump Relacionadas                                  |
|------------------------|------------------------------------------------------------|
| Data_Inscricao         | Inscricoes                                                 |
| Data_Ultima_Edicao     | Inscricoes, Usuarios                                       |
| Safra                  | Safras, Plantio, Colheita                                  |
| Categoria              | Categorias                                                 |
| Nacional               | Regioes, Estados, Municipios                               |
| Regional               | Regioes, Municipios, Estados                               |
| Estadual               | Estados, Municipios                                        |
| Municipal              | Municipios                                                 |
| Nome_Propriedade       | Proprietarios, Inscricoes                                  |
| Patrocinador           | Fornecedores                                               |
| Nome_Consultor         | Consultores                                                |
| Nome_Produtor          | Proprietarios                                              |
| TECNOLOGIA             | Tecnologia, Produtos, Pulverizador                         |



As planilhas são atualizadas para posteriormente ocorrer a geração de relatórios e dashboards, permitindo uma análise mais aprofundada dos dados coletados ao longo dos anos no desafio. Esses dados podem ser utilizados pelos participantes para otimizar suas práticas agrícolas, melhorar a produtividade e reduzir custos de seus cultivos.
