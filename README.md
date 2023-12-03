
# Api REST e RESTFul
---
API REST, também chamada de API RESTful, é uma interface de programação de aplicações (API ou API web) em conformidade com as restrições do estilo de arquitetura REST, permitindo a interação com serviços web RESTful. REST é a sigla em inglês para "Representational State Transfer", que em português significa tansferência de estado representacional. Essa arquitetura foi criada pelo cientista da computação Roy Fielding.
## Diferenças entre REST e RESTFul
---
REST é um conceito mais amplo, um estilo arquitetural, enquanto RESTful é a aplicação prática desses princípios em serviços web específicos. RESTful adere a padrões e convenções para garantir uma abordagem consistente, simplificando a interoperabilidade entre sistemas distribuídos. Em resumo, REST é o conceito, enquanto RESTful é a implementação coesa e prática desse conceito.
## HTTP verbs
---
O protocolo HTTP define um conjunto de métodos de requisição responsáveis por indicar a ação a ser executada para um dado recurso. Embora esses métodos possam ser descritos como substantivos, eles também são comumente referenciados como HTTP Verbs (Verbos HTTP). Cada um deles implementa uma semântica diferente, mas alguns recursos são compartilhados por um grupo deles, como por exemplo, qualquer método de requisição pode ser do tipo safe, idempotent ou cacheable (en-US).

**-[GET](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Methods/GET)**: O método GET solicita a representação de um recurso específico. Requisições utilizando o método GET devem retornar apenas dados.

**-[HEAD](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Methods/HEAD)**: O método HEAD solicita uma resposta de forma idêntica ao método GET, porém sem conter o corpo da resposta.

**-[POST](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Methods/POST)**: O método POST é utilizado para submeter uma entidade a um recurso específico, frequentemente causando uma mudança no estado do recurso ou efeitos colaterais no servidor.

**-[PUT](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Methods/PUT)**: O método PUT substitui todas as atuais representações do recurso de destino pela carga de dados da requisição.

**-[DELETE](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Methods/DELETE)**: O método DELETE remove um recurso específico.

**-[CONNECT](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Methods/CONNECT)**: O método CONNECT estabelece um túnel para o servidor identificado pelo recurso de destino.

**-[OPTIONS](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Methods/OPTIONS)**: O método OPTIONS é usado para descrever as opções de comunicação com o recurso de destino.

**-[TRACE](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Methods/TRACE)**: O método TRACE executa um teste de chamada loop-back junto com o caminho para o recurso de destino

**-[PATCH](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Methods/PATCH)**: O método PATCH é utilizado para aplicar modificações parciais em um recurso.

## HTTP Status Code
---
Os códigos de status são retornados como parte da resposta de uma solicitação feita a um servidor. Podem indicar falha ou sucesso de uma solicitação. Eles são agrupados em 5 categorias:

### 1xx (Informational)
Significa que a solicitação foi recebida e o processo continua.

- 100 Continue: Apenas uma parte da solicitação foi recebida pelo servidor, mas enquanto não for rejeitada, o cliente deverá continuar com a solicitação.
- 101 Switching Protocols: O servidor muda de protocolo.

### 2xx (Success)
Significa que a solicitação foi recebida, compreendida e aceita com sucesso.

- 200 OK: O pedido está OK.
- 201 Created: A solicitação é concluída e um novo recurso é criado.
- 202 Accepted: A solicitação é aceita para processamento, mas o processamento não é concluído.
- 203 Non-authoritative Information: As informações no cabeçalho da entidade são de uma cópia local ou de terceiros, e não do servidor original.
- 204 No Content: Um código de status e um cabeçalho são fornecidos na resposta, mas não há corpo de entidade na resposta.
- 205 Reset Content: O navegador deve limpar o formulário usado para esta transação para entrada adicional.
- 206 Partial Content: O servidor está retornando dados parciais do tamanho solicitado. Usado em resposta a uma solicitação especificando um cabeçalho Range. O servidor deve especificar o intervalo incluído na resposta com o cabeçalho Content-Range.

### 3xx (Redirection)
Significa que mais ações são necessárias para completar a solicitação

- 300 Multiple Choices: Uma lista de links. O usuário pode selecionar um link e ir para esse local. Máximo de cinco endereços.
- 301 Moved Permanently: A página solicitada foi movida para um novo URL.
- 302 Found: A página solicitada foi movida temporariamente para um novo URL.
- 303 See Other: A página solicitada pode ser encontrada em um URL diferente.
- 304 Not Modified: Este é o código de resposta para um cabeçalho If-Modified-Since ou If-None-Match, onde o URL não foi modificado desde a data especificada.
- 305 Use Proxy: A URL solicitada deve ser acessada através do proxy mencionado no cabeçalho Location.
- 306 Unused: Este código foi usado em uma versão anterior. Não é mais usado, mas o código está reservado.
- 307 Temporary Redirect: A página solicitada foi movida temporariamente para um novo URL.

### 4xx (Client Error)
Significa que a solicitação contém sintaxe incorreta ou não pode ser cumprida.

- 400 Bad Request: O servidor não entendeu a solicitação.
- 401 Unauthorized: A página solicitada precisa de um nome de usuário e uma senha.
- 402 Payment Required: Você não pode usar este código ainda.
- 403 Forbidden: É proibido o acesso à página solicitada.
- 404 Not Found: O servidor não consegue encontrar a página solicitada.
- 405 Method Not Allowed: O método especificado na solicitação não é permitido.
- 406 Not Acceptable: O servidor só pode gerar uma resposta que não seja aceita pelo cliente.
- 407 Proxy Authentication Required: Você deve se autenticar com um servidor proxy antes que essa solicitação possa ser atendida.
- 408 Request Timeout: A solicitação demorou mais do que o servidor estava preparado para esperar.
- 409 Conflict: A solicitação não pôde ser concluída devido a um conflito.
- 410 Gone: A página solicitada não está mais disponível.
- 411 Length Required: O "Content-Length" não está definido. O servidor não aceitará a solicitação sem ele
- 412 Precondition Failed: A pré-condição fornecida na solicitação avaliada como falsa pelo servidor.
- 413 Request Entity Too Large: O servidor não aceitará a solicitação porque a entidade solicitada é muito grande.
- 414 Request-url Too Long: O servidor não aceitará a solicitação porque a URL é muito longa. Ocorre quando você converte uma solicitação "post" em uma solicitação "get" com informações de consulta longas.
- 415 Unsupported Media Type: O servidor não aceitará a solicitação porque o tipo de mídia não é compatível.
- 416 Requested Range Not Satisfiable: O intervalo de bytes solicitado não está disponível e está fora dos limites.
- 417 Expectation Failed: A expectativa fornecida em um campo de cabeçalho de solicitação Expect não pôde ser atendida por este servidor.

### 5xx (Server Error)
Significa que o servidor falhou em cumprir uma solicitação aparentemente válida.

- 500 Internal Server Error: A solicitação não foi concluída. O servidor atendeu a uma condição inesperada.
- 501 Not Implemented: A solicitação não foi concluída. O servidor não suportava a funcionalidade necessária.
- 502 Bad Gateway: A solicitação não foi concluída. O servidor recebeu uma resposta inválida do servidor upstream.
- 503 Service Unavailable: A solicitação não foi concluída. O servidor está temporariamente sobrecarregado ou inativo.
- 504 Gateway Timeout: O gateway expirou.
- 505 HTTP Version Not Supported: O servidor não suporta a versão "protocolo http".


---
**Autor do resumo:** Caio Nemésio de Araújo e Sousa - 01564870

