# Proposta de Sumário para Manual de Catalogação de Dados no Portal de Dados Abertos


## 1. Panorama e conceitos preliminares

Alinhada com a diretriz estratégica govenrnamental de transparência para o governo do Estado de Minas Gerais, o planejamento estratégico da CGE prevê a expansão do número de conjunto de dados publicado no Portal de Dados Abertos. 

Mais do que meramente publicar mais dados, nossa proposta é fomentar a transparência e o controle social a partir da amplificação das possibilidades de uso dos dados, prezando pela sua acessibilidade e qualidade. Assim, baseamo-nos em padrões e referências reconhecidos nacional e internacionalmente, bem como na expertise de setores internos e de outros órgãoes e poderes com experiências exitosas.

Este é, portanto, o documento que irá nortear os procedimentos e padrões de publicação de dados para o gestor do poder executivo estadual de Minas Gerais.


## 2. Finalidade e Escopo

Definir procedimentos e regras para que os gestores dos órgãos e entidades da administração pública estadual possam catalogar e publicar seus dados no Portal de Dados Abertos.

Somente os dados que são geradas pelo órgão demandante poderão ser objeto de catalogação e publicação. 


## 3. Responsabilidades das partes envolvidas

* Setor demandante

* Ponto focal do órgão demandante

* ASCOM órgão demandante

* DTI órgão demandante

* Diretoria de Transparência Ativa da CGE

* ASCOM da CGE

* DTI da CGE 


## 4. Macroetapas

O gestor deverá se atentar para algumas normas a serem seguidas para publicar seus dados. A equipe da DTA orientará para o preenchimento dos documentos: mapeamento do fluxo dos dados; documentação descritiva dos dados


#### 4.1. Mapeamento do fluxo dos dados

Compreende criação, obtenção, transformação, consolidação, tratamento e publicação dos dados. Deve evidenciar as ações e responsabilidades de todos os agentes e respectivos setores que tratam cada conjunto de dados abertos a ser publicado.

[^] Possibilidade de aproveitamento das iniciativas do mapeamento para adequação dos órgãos à LGPD

[^] [Mapa de informações](http://mapadainformacao.com.br/) como exemplo de representação visual de encadeamento entre instâncias/fases da coleta e uso dos dados

#### 4.2. Documentação descritiva dos dados


Tal documentação deve conter os atributos de cada dataset (conjunto de dados) e recurso (arquivo), e sua elaboração deverá compreender:

* Dicionário de dados

(exemplo do Portal atual de MG - descritores das colunas/variáveis de todos os datasets, ainda que desatualizado: http://www.transparencia.dadosabertos.mg.gov.br/dataset/dicionario-de-dados-portal-da-transparencia/resource/fa2d3b71-3bd6-4bd2-81a9-3b1e7773c2d1)

(exemplo de São Paulo - dicionário como catálogo de metadados: http://dados.prefeitura.sp.gov.br/dataset/cmbd-catalogo-municipal-de-bases-de-dados/resource/e384fad5-c44e-489e-86dd-fde6328771a1)


* Metadados

Nota: cada órgão poderá ter seu catálogo individual, que poderá ser agrupado com outros ógrãos de temática adjacente para consolidar catálogos setoriais que agreguem conjuntos de órgãos para formar 'grupos' dde dados no CKAN. Por exemplo, estados de [Alagoas](http://dados.al.gov.br/) e [Rio Grande do Sul](https://dados.rs.gov.br/), embora este último esteja desatualizado


#### 4.3. Publicação, monitoramento e revisões

### 5.Convenções

Espaço não pode ser utilizado nos nomes dos arquivos e diretórios

Ano não é informação para constar no nome do dataset

Partículas (artigos, preposições) e VERBOS são dispensáveis nos nomes dos datasets e recursos

* Vide [html id](https://pandoc.org/MANUAL.html#extension-auto_identifiers) e [slug](https://slugify.online/)

Fazer analogias para padronizar com as nomenclaturas utilizadas nos títulos das seções do [Guia do Menu Transparência](https://transparencia-mg.github.io/guia-transparencia-ativa/v0/)

Nome legível por máquina (name) = gerado a partir do nome legível humanamente (title), substituindo espaços por hífens e eliminando acentos e cedilha

#### 5.1. [Especificação do csv](https://specs.frictionlessdata.io/csv-dialect/#example)

[The CSV dialect descriptor](https://specs.frictionlessdata.io/schemas/csv-dialect.json)


#### 5.2. Especificação dos metadados a partir do arquivo datapackage.json

https://raw.githubusercontent.com/dados-mg/inventario-de-dados/draft/depara-metadados-0.1.json

    




### . Apêndice 1: Glossário


Conceitos básicos de Dados Abertos e Governo Digital para nivelamento


* Arquivo (ou recurso) em formato aberto: um conjunto de dados pode ser composto por mais de um arquivo de dados. O critério básico para separar vários recursos em mais de um conjunto de dados é a constatação de que eles divergem em vários metadados.

* CKAN

* Conjunto de dados (ou dataset) 

* CSV

* Dado aberto

* Dicionário de Dados

* Fluxo ETL

* JSON

* Metadado

* Recurso

OBS.: referência de glossário do portal federal: https://kit.dados.gov.br/Gloss%C3%A1rio/


### . Apêndice 2: Modelo de Ficha de Mapeamento de Fluxo do Conjunto de Dados Abertos a ser Publicado


### . Anexo: Referências


Coletânea sumária de documentos e experiências conceituais e de experiências de outras instituições nacionais e internacionais

* Boas práticas de dados, W3C

* [Catálogo de Dados da Prefeitura de São Paulo](http://transparencia.prefeitura.sp.gov.br/administracao/Paginas/cmbd.aspx)

* Escala de maturidade de dados, Sunlight Foundation

* [Kit para Dados Abertos do Governo Federal](https://kit.dados.gov.br/))

