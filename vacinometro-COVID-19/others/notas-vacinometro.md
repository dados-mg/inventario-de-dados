# Notas vacinometro

1. formato de relatório em vez de formato de base: para cada nova categoria incluída no cronograma vacinal, será necessária inclusão de novas colunas, o que torna muito mutável o esquema do dicionário de dados; tanto a indicação de qual grupo prioritário se refere cada linha, quanto a indicação da dose, poderiam estar numa coluna cada; 

2. outros dados: 

    2.1. já contidos no [painel do MS](https://viz.saude.gov.br/extensions/DEMAS_C19Vacina/DEMAS_C19Vacina.html):

	- laboratório fabricante da vacina, 
	 
	- sexo, 
	- faixa etária, 

	2.2. no [vacinômetro do ES](https://coronavirus.es.gov.br/painel-vacinacao): 

	- remessa de cada laboratório,
	- percentual de cobertura de cada dose e de cada grupo prioritário (mais proprícios para formato de )

* exemplo de dado em formato de base: 

	- São Paulo: [doses aplicadas](https://www.vacinaja.sp.gov.br/vacinometro/) e [doses distribuídas](https://www.vacinaja.sp.gov.br/vacinometro/)

* exemplo de dado em formato de relatório: 

	- Ceará: [distribuição de vacinas por grupo](https://www.saude.ce.gov.br/wp-content/uploads/sites/9/2020/02/distribuicao_vacinas_covid_por_grupo_20211801.pdf)

* possibilidade de uso da API do SI-PNI: 
https://servicos-datasus.saude.gov.br/detalhe/CddynnsgE2
https://mobileapps.saude.gov.br/portal-servicos/files/f3bd659c8c8ae3ee966e575fde27eb58/0b75c68d253b953a7374682347b28144_0svweqry0.pdf

## Alternativas:

a. reestruturar as informações necessárias em colunas perenes, para o formato de base:

|MUNICIPIO_RESIDENCIA|URS|MICRO|MACRO|CodigoIBGE|Data|Grupo                                            |Dose    |Total acumulado|
|--------------------|---|-----|-----|----------|----|-------------------------------------------------|--------|---------------|
|BH                  |   |     |     |          |    |Indigenas aldeados                               |primeira|               |
|BH                  |   |     |     |          |    |                                                 |segunda |               |
|BH                  |   |     |     |          |    |Idosos em ILPI                                   |primeira|               |
|BH                  |   |     |     |          |    |                                                 |segunda |               |
|BH                  |   |     |     |          |    |Pessoas com deficiencia em residencias inclusivas|primeira|               |
|BH                  |   |     |     |          |    |                                                 |segunda |               |
|BH                  |   |     |     |          |    |Profissionais de Saúde                           |primeira|               |
|BH                  |   |     |     |          |    |                                                 |segunda |               |


b. prever todas as categorias prioritárias no esquema = a depender da discussão da forma de aviso quando houver necessidade de inclusão ou mudança, e tb o modo de efetuar a inclusão manual = exemplo do [painel do Maranhão](https://painel-covid19.saude.ma.gov.br/vacinas/municipio/2107357)