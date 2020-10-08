## Dado aberto: normas, características, princípios

**pressupostos normativos** 

vide [art. 8 § 3º, da LAI](http://www.planalto.gov.br/ccivil_03/_ato2011-2014/2011/lei/l12527.htm#art8%C2%A73), que trata dos requisitos para transparência ativa nos sítios eletrônicos: 

> diversos formatos eletrônicos, inclusive abertos e não proprietários, tais como planilhas e texto, de modo a facilitar a análise das informações (II);

> formato aberto, estruturado e legível por máquina (III);

> detalhes dos formatos da estruturação da informação (IV);

> atualização das informações disponíveis para acesso (VI)


**[3 leis dos dados abertos](https://eaves.ca/2009/09/30/three-law-of-open-government-data/)**:

_1. Se os dados não podem ser encontrados ou indexados na Web, eles não existem._

_2. Se os dados não estão disponíveis em um formato aberto e legível por máquina, eles
 não podem ser reutilizados._
 
_3. Se dispositivos legais não permitem que os dados sejam partilhados, eles não são úteis_


**[princípios](https://public.resource.org/8_principles.html)**:

1. Completitude: disponibilização de todos os dados públicos, sem limitações de privacidade, segurança ou controle de acesso;

2. Primariedade: publicação da forma coletada na fonte, sem transformação ou agregação;

3. Atualização: numa velocidade que preserve seu valor;

4. Acessibilidade: para o público mais amplo e para propósitos mais variados possíveis; 

5. Processáveis por máquina: estruturados para serem processados automaticamente;

6. Acesso não-discriminatório: sem necessidde de identificação ou registro para acessar os dados;

7. Formatos não-proprietários: nenhum ente pode ter controle exclusivo do formato no qual o dado é disponibilizado;

8. Licenças livres: não há restrição de marca, patente, segredo industrial ou direito autoral.


* destaca-se, ainda, como princípios da [Carta Internacional de Dados Abertos](https://opendatacharter.net/principles/):

Oportunos e compreensíveis

Acessíveis e utilizáveis

Comparáveis e interoperáveis


**escala de 5 estrelas**: 

Tim Berners-Lee, o pai da web, criou um modelo para classificar dados abertos publicados. Esse modelo é conhecido como o modelo das 5 estrelas, no qual dados com 1 estrela estão na forma mais pobre e simples, e dados com 5 estrelas são mais ricos e complexos.

A classificação proposta pelo Berners-Lee é a seguinte:

★ : dados disponíveis na web (não importa o formato) sob uma licença aberta. Por exemplo, um PDF.

★ ★ : dados disponíveis de forma estruturada. Por exemplo, um arquivo Excel.

★ ★ ★ : dados disponíveis em formatos não-proprietários. Por exemplo, um CSV.

★ ★ ★ ★ : use URIs para denotar os dados, assim outras pessoas podem criar links para eles. Por exemplo, um RDF.

★ ★ ★ ★ ★ : link os seus dados a outros. Por exemplo, um RDF que tenha links para outros RDF.


## Formatos de dados abertos: tabular, csv, json

Os formatos legíveis por máquina mais comuns são: CSV, XML, JSON, GeoJSON, XLS.

**dado tabular**:

````
campo     campo
  |         |
  |         |
  V         V

 A     |    B    |    C    |    D      <--- linha (cabeçalho)
 ------------------------------------
 valA  |   valB  |  valC   |   valD    <--- linha
````
 
 **csv**:

 - definição, características e exemplos no [portal de Dados Abertos de Buenos Aires](https://datosgcba.github.io/guia-datos/guia-abiertos/#csv)
 
 - o que é, como editar, importar e exportar: https://rockcontent.com/br/blog/csv/

**json**:

````
[
  { "A": valor, "B": valor, ... },
  { "A": valor, "B": valor, ... },
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

**metadados**

É essencial fornecer informações que auxiliem pessoas e aplicações de computadores a compreenderem os dados, assim como outros aspectos importantes que descrevam o conjunto de dados ou a distribuição. Os metadados apresentam a estrutura dos dados (chaves, índices, colunas), as informações sobre o conjunto de dados (título, autor,assuntos, palavras-chave) e as informações de proveniência (editor, histórico de revisões,mudanças, fonte dos dados). Ampliam os recursos de busca e permitem a interoperabilidade entre diferentes sistemas.

Fornecer informações descritivas de conjuntos de dados de forma explícita possibilita que agentes de software descubram automaticamente conjuntos de dados disponíveis na Web, e isto permite que pessoas compreendam a natureza do conjunto de dados e suas distribuições. [Os metadados descritivos podem incluir as seguintes características genéricas de um conjunto de dados](https://w3c.br/traducoes/DWBP-pt-br/#metadata):

O **título e a descrição** do conjunto de dados.

As **palavras-chave** que descrevem o conjunto de dados.

A **data de publicação** do conjunto de dados.

A **entidade responsável** (publicadora de dados) por disponibilizar o conjunto de dados.

O **ponto de contato** para o conjunto de dados.

A **cobertura espacial** do conjunto de dados.

O **período temporal** coberto pelo conjunto de dados.

A **data da última modificação** do conjunto de dados.

Os **temas/categorias cobertos** por um conjunto de dados.

* dicionário de dados

* [Decreto Federal 8777/2016: art. 2º, IV](http://www.planalto.gov.br/ccivil_03/_ato2015-2018/2016/decreto/d8777.htm#art2): formato aberto implica que a especificação esteja documentada publicamente


## Decisões de arquitetura tomadas pela Diretoria de Transparência no processo de abertura e publicação dos dados: 

Adoção do **padrão Frictionless Data**, **controle de versão dos conjuntos de dados** em repositórios abertos no GitHub e **validação automática dos dados** via goodtables (serviço oferecido pela comunidade, como o datapackage creator da Frictionless Data).

Frictionless Data é um conjunto de ferramentas e estratégias focado em facilitar a interoperabilidade de dados por meio da definição de padrões e critérios técnicos e com o objetivo de otimizar o armazenamento e os usos de dados. Facilita, portanto, a gestão de metadados, a limpeza, a organização, a extração, o compartilhamento, entre outros recursos. 


### Padrão Frictionless Data:

* Introdução ao datapackage: [workshop da Frictionless data](https://www.youtube.com/watch?v=EFQmudQP4io&feature=youtu.be&t=616)

* [especificações do datapackage](https://specs.frictionlessdata.io/) = arquivo em formato json que descreve:

a) o conjunto de dados e seus metadados (como título, descrição, formato de arquivo, palavras-chave, dentre outros),

b) as colunas de cada recurso (arquivo ou URL) que contém (~ schema),


* [datapackage creator](https://create.frictionlessdata.io/): ferramenta de auxílio à elaboração do arquivo datapackage.json que faz a descrição lógica do conjunto de dados, dos recursos e do dicionário de dados (variáveis) em formato json

* como usar o datapackage: [guia rápido](https://www.youtube.com/watch?v=VrdPj28-L9g) e [workshop](https://www.youtube.com/watch?v=EFQmudQP4io&feature=youtu.be&t=998)

* exemplo de datapackage utilizado no novo Portal de Dados Abertos: [no CKAN](http://dados.mg.gov.br/dataset/doacoes-comodatos-amigo-estado-mg/resource/ec8b233a-c89f-4927-be0e-e114d7d094c0); [no repositório específico do GitHub](https://github.com/dados-mg/doacoes-comodatos-amigo-estado-mg/blob/master/datapackage.json)

  

### Controle de versão

**GitHub**

* [Curso da software carpentry](http://swcarpentry.github.io/git-novice/)

* exemplo de registros de alterações em datapackage no respectivo repositório do GitHub: https://github.com/dados-mg/doacoes-comodatos-amigo-estado-mg/commits/master


**Validação automática contínua** ([goodtables io](https://goodtables.io/)): checagem da exatidão da descrição lógica (datapackage.json) sobre o recurso físico (csv), a cada registro de alteração (commit) efetuado no reposiotório GitHub

* exemplo de histórico de validações: https://goodtables.io/github/dados-mg/doacoes-comodatos-amigo-estado-mg


## Dado aberto - correspondência das decisões de arquitetura do esquema de transformação e publicação dos dados aos pricípios e pressupostos normativos de dados abertos:

| princípio                              | referência legal                              | decisão da Diretoria de Transparência (DCTA)                                                                                                                                                                                                                  |
|----------------------------------------|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| oportuno, atual                        | Lei 12527, art. 8 § 3º, VI             | frequência de atualização equivalente à das consultas do Portal da   Transparência; versionamento em repositório com controle e informação da   periodicidade de atualização como propriedade de metadado no datapackage.json |
| compreensível                          | Lei 12527, art. 8 § 3º, IV             | adoção de dicionário de dados com padrão predefinido                                                                                                                                                                          |
| acessível                              | Lei 12527, art. 8 § 3º, III            | disponibilização dos datasets na plataforma CKAN, com possibilidade de   requisições via API                                                                                                                                  |
| utilizável, processável por máquina                             | Lei 12527, art. 8 § 3º, II             | formatos abertos e estruturados dos arquivos de recursos dos datasets   (csv, json)                                                                                                                                           |
| comparável                             | Decreto Federal 8777/2016: art. 2º, IV | especificação documentada publicamente através dos datapackage.json                                                                                                                                                           |
| interoperável | Lei 12527, art. 8 § 3º, III            | adoção do padrão Frictionless Data                                                                                                                                                                                            |




## Referências:

* Características e motivação da abertura e uso de dados: https://dados.gov.br/pagina/dados-abertos

* Toolkit do Gov.Br para dados abertos = https://github.com/dadosgovbr/kit

* [Modelo de Referência para Publicação de Dados Abertos](https://www.gov.br/cgu/pt-br/governo-aberto/a-ogp/planos-de-acao/4o-plano-de-acao-brasileiro/compromisso-2-docs/modelo-de-referencia-de-abertura-de-dados_versao-final-2.pdf)

* Escalas de Dados Abertos = https://imasters.com.br/devsecops/5-estrelas-dos-dados-abertos#:~:text=Esse%20modelo%20%C3%A9%20conhecido%20como,Berners%2DLee%20%C3%A9%20a%20seguinte%3A&text=%3A%20dados%20dispon%C3%ADveis%20na%20web%20(n%C3%A3o,formato)%20sob%20uma%20licen%C3%A7a%20aberta.

* Formatos abertos de arquivos (em espanhol, do portal de Buenos Aires) = https://datosgcba.github.io/guia-datos/guia-abiertos/#formatos-abiertos-de-archivos
