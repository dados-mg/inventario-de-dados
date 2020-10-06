## Dado aberto

**pressupostos** - vide [art. 8 § 3º, da LAI](http://www.planalto.gov.br/ccivil_03/_ato2011-2014/2011/lei/l12527.htm#art8%C2%A73), que trata dos requisitos para transparência ativa nos sítios eletrônicos: 

> + formato aberto, estruturado e legível por máquina (III);

> + detalhes dos formatos da estruturação da informação (IV);

> + atualização das informações disponíveis para acesso (VI)


* Características e motivação da abertura e uso de dados: https://dados.gov.br/pagina/dados-abertos


**escala de 5 estrelas**: 

Tim Berners-Lee, o pai da web, criou um modelo para classificar dados abertos publicados. Esse modelo é conhecido como o modelo das 5 estrelas, no qual dados com 1 estrela estão na forma mais pobre e simples, e dados com 5 estrelas são mais ricos e complexos.

A classificação proposta pelo Berners-Lee é a seguinte:

★ : dados disponíveis na web (não importa o formato) sob uma licença aberta. Por exemplo, um PDF.

★ ★ : dados disponíveis de forma estruturada. Por exemplo, um arquivo Excel.

★ ★ ★ : dados disponíveis em formatos não-proprietários. Por exemplo, um CSV.

★ ★ ★ ★ : use URIs para denotar os dados, assim outras pessoas podem criar links para eles. Por exemplo, um RDF.

★ ★ ★ ★ ★ : link os seus dados a outros. Por exemplo, um RDF que tenha links para outros RDF.

_“Se os dados não estão disponíveis num formato aberto e legível por máquina, eles não podem ser reutilizados.” (David Eaves/Opendata Charter - principles)_


### Formatos de dados abertos: tabular, csv, json

**dado tabular**:

````
field     field
  |         |
  |         |
  V         V

 A     |    B    |    C    |    D      <--- Row (Header)
 ------------------------------------
 valA  |   valB  |  valC   |   valD    <--- Row
````
 
 **csv**:

 - definição, características e exemplos no [portal de Dados Abertos de Buenos Aires](https://datosgcba.github.io/guia-datos/guia-abiertos/#csv)
 
 - o que é, como editar, importar e exportar: https://rockcontent.com/br/blog/csv/

**json**:

````
[
  { "A": value, "B": value, ... },
  { "A": value, "B": value, ... },
  ...
]
````

* dado tabular X json: https://specs.frictionlessdata.io/table-schema/#concepts

* exemplo de descrição lógica, em formato json, da estrutura do arquivo csv:

````
{
  "dialect": {
    "csvddfVersion": 1.2,
    "delimiter": ";",
    "doubleQuote": true,
    "lineTerminator": "\r\n",
    "quoteChar": "\"",
    "skipInitialSpace": true,
    "header": true,
    "commentChar": "#"
  }
}

````


* editores de texto


## Documentação

* metadados

* dicionário de dados


### Decisões de arquitetura tomadas pela Diretoria de Transparência no processo de abertura e publicação dos dados: 

adoção do padrão Frictionless Data, controle de versão dos conjuntos de dados em repositórios abertos no GitHub e validação automático dos dados via goodtables (serviço oferecido pela comunidade como o datapackage creator da Frictionless Data)


## Padrão Frictionless Data:

conjunto de ferramentas para interoperabilidade de dados, por meio de padrões e critérios técnicos para otimizar o armazenamento e os usos de dados

* [Decreto Federal 8777/2016: art. 2º, IV](http://www.planalto.gov.br/ccivil_03/_ato2015-2018/2016/decreto/d8777.htm#art2): formato aberto implica que a especificação esteja documentada publicamente

* [especificações do datapackage](https://specs.frictionlessdata.io/) = arquivo em formato json que descreve:

a) o conjunto de dados e seus metadados (como título, descrição, formato de arquivo, palavras-chave, dentre outros),

b) as colunas de cada recurso (arquivo ou URL) que contém (~ schema),

* [datapackage creator](https://create.frictionlessdata.io/): ferramenta de auxílio à elaboração do arquivo datapackage.json que faz a descrição lógica do conjunto de dados, dos recursos e do dicionário de dados (variáveis) em formato json


## Controle de versão

* GitHub

* Validação automática contínua ([goodtables io](https://goodtables.io/)): checagem da exatidão da descrição lógica (datapackage.json) sobre o recurso físico (csv), a cada registro de alteração (commit) efetuado no reposiotório GitHub


## Dado aberto - correspondência das decisões de arquitetura do esquema de transformação e publicação dos dados aos pressupostos da LAI:

* formato aberto, estruturado e legível por máquina = acessível e editável via software não-proprietário, com formato predefinido dos arquivos de recurso (i.e. tabular = csv) e datapackage em formato json (compreensível por máquina) para cada conjunto de dados

* detalhes dos formatos da estruturação da informação = metadados descritos na especificação Data Frictionless (dataset/conjunto, recurso e dicionário de dados/variáveis)

* atualização das informações disponíveis para acesso = versionamento em repositório com controle e informação da periodicidade de atualização como propriedade de metadado no datapackage.json


## Referências:

* Toolkit do Gov.Br para dados abertos = https://github.com/dadosgovbr/kit

* Escalas de Dados Abertos = https://imasters.com.br/devsecops/5-estrelas-dos-dados-abertos#:~:text=Esse%20modelo%20%C3%A9%20conhecido%20como,Berners%2DLee%20%C3%A9%20a%20seguinte%3A&text=%3A%20dados%20dispon%C3%ADveis%20na%20web%20(n%C3%A3o,formato)%20sob%20uma%20licen%C3%A7a%20aberta.

* Formatos abertos de arquivos (em espanhol, do portal de Buenos Aires) = https://datosgcba.github.io/guia-datos/guia-abiertos/#formatos-abiertos-de-archivos
