# SimpleText@CLEF-2022 Início

[Início](./) | [Chamada para papéis](./CFP) | [Datas importantes](./dates) | [Tarefas](./tasks)  | [Ferramentas](./tools) 
[Programa](./program) | [Publicações](./publications) | [Organisadores](./organisers) | [Portefólio](./portefolio) | [<img src="https://github.com/simpletext-madics/2021/blob/main/clef/FR.png?raw=true" width="30">](../fr/contacts)


---

<img align="left" src="https://github.com/simpletext-madics/2021/blob/main/clef/simpletext-logo-blue.png?raw=true" width="100"/>  

## SimpleText: Simplificação automática de textos científicos

* SimpleText é um novo laboratório organizado como parte da [conferência CLEF-2022](https://clef2022.clef-initiative.eu/index.php), initiated by [CLEF initiative](http://www.clef-initiative.eu/).*

### Tópico e objetivos do laboratório

SimpleText aborda desafios técnicos e desafios de avaliação, fornecendo dados apropriados e referências para simplificação de texto.
<br/> Propomos as seguintes tarefas:
* [TAREFA 1 O que está dentro (ou fora)?] (./Task1)
Selecione passagens para incluir em um resumo simplificado, dada uma consulta
* [TAREFA 2 O que não está claro?] (./Task2)
Dada uma passagem e uma consulta, classifique os termos / conceitos que devem ser explicados para a compreensão desta passagem (definições, contexto, aplicações, ..)
* [TAREFA 3 Reescreva isso!] (./Task3)
Dada uma consulta, simplifique as passagens de resumos científicos
* [TAREFA NÃO ESCARADA] (./task4)
Agradecemos qualquer envio que use nossos dados! 


Para enfrentar esses desafios, SimpleText visa responder às seguintes questões de pesquisa:
<br/> RQ1 --Que expressão textual portadora de informação deve ser simplificada (documento e trecho a serem incluídos no resumo simplificado)?
<br/> RQ2 --Que tipo de informação de fundo deve ser fornecida (quais termos devem ser contextualizados dando uma definição e / ou aplicação)? Que informação é a mais relevante ou útil?
<br/> RQ3 --Como melhorar a legibilidade de um determinado texto curto (por exemplo, reduzindo o vocabulário e a complexidade sintática) com uma taxa aceitável de distorção da informação?

### Significância para o campo e relevância para CLEF

Os sistemas de acesso à informação fornecem aos usuários informações importantes de fontes confiáveis, como literatura científica; no entanto, os não especialistas podem tender a evitar essas fontes devido à sua linguagem complexa ou à falta de conhecimento prévio. Isso permitirá que as pessoas leiam mais rápido, o que tornará eles estão mais conscientes dos resultados científicos. Isso é especialmente importante com uma explosão. Os textos simplificados são mais acessíveis para falantes não nativos, jovens leitores e pessoas com deficiência de leitura. Além disso, a simplificação de texto permite o aprimoramento de aplicativos de processamento de linguagem natural (PNL), incluindo resultados de tradução automática. A simplificação automática de texto pode ser útil para vários domínios, como comunicação científica, s A simplificação de texto pode ser usada na tradução (tradução auxiliada por computador e localização de sites, pré-edição) e redação técnica.

Embora poucos estudos tenham sido realizados no campo da simplificação automática de texto [1], [2], ainda permanece uma tarefa desafiadora. Até onde sabemos, nenhum conjunto de dados de RI multilíngue existe onde um resumo é escrito em um idioma diferente. Poucos trabalhos foram realizados para dados franceses [3] - [7] e eles não consideram as tarefas de seleção de informação nem fornecem conhecimento de fundo. Em contrapartida, a busca por conhecimento de fundo está próxima do INEX / CLEF Tweet de projetos anteriores, o SimpleText visa fornecer conhecimento de base insuficiente, mas mantendo o texto o mais curto possível, a fim de ajudar um usuário a entender um texto complexo que não pode ser mais simplificado sem distorção severa da informação. Trilha de contextualização 2011-2014 [27] e Microblog cultural CLEF Contextualização de 2016, Workshop de 2017 [34], mas SimpleText difere deles por fazer um foco em uma seleção de noções a serem ex explicado e a utilidade das informações fornecidas, em vez de sua relevância.

### Cenários

O objetivo é criar um resumo simplificado de vários documentos científicos com base em uma determinada consulta que forneça ao usuário um resumo simplificado instantâneo sobre um tópico específico de seu interesse ou para gerar um resumo diário, por exemplo, para ArXiv.

### Configuração de avaliação, métricas e tarefas

Conjunto de dados em inglês: Usamos o conjunto de dados Citation Network: DBLP + Citation, ACM Citation network (https://www.aminer.org/citation). Um índice de pesquisa elástico é fornecido aos participantes acessíveis por meio de uma API GUI. Este índice é adequado para ::
<br/> -aplicar métodos básicos de recuperação de passagens com base em modelos IR de vetor ou linguagem
<br/> -gerar modelos de alocação de Dirichlet latente,
<br/> -train Graph Neural Networks para recomendação de citação realizada em https://stellargraph.readthedocs.io/ por exemplo,
<br/> - aplique transformadores bidirecionais profundos para expansão de consulta ...
Consultas em inglês: Para esta edição as consultas são uma seleção de títulos de imprensa recentes do The Guardian enriquecidos com palavras-chave extraídas manualmente do conteúdo dos artigos. Foi verificado que cada palavra-chave permite extrair pelo menos 5 resumos relevantes. O uso dessas palavras-chave .é opcional.
<br/> Formato de entrada para todas as tarefas:
<br/> ● Os tópicos estão no formato MD
<br/> ● Artigos em texto completo do The Guardian (link, pasta com textos completos no formato MD)
<br/> ● Índice ElasticSearch no servidor de dados
<br/> ● DBLP full dump no formato JSON.GZ
<br/> ● resumos DBLP extraídos para cada tópico no seguinte formato MD (doc_id, ano, resumo) 

---

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [<img src="https://github.com/simpletext-madics/2021/blob/main/clef/logo-clef-2021.png?raw=true" width="150">](http://www.clef-initiative.eu/) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [<img src="https://github.com/simpletext-madics/2021/blob/main/clef/logo-clef-initiative.png?raw=true" width="200">](http://clef2021.clef-initiative.eu/) 
