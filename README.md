###  README para `messaging-service-api`

```markdown
# NailDesigner - API de Mensageria (Contrato)

Este projeto define o contrato da API (principalmente Data Transfer Objects - DTOs) para o `naildesigner-messaging-service`. Ele serve como uma biblioteca compartilhada para garantir que o serviço de mensageria e seus consumidores "falem a mesma língua".

## Conteúdo Principal

Este artefato contém:

* **DTOs (Data Transfer Objects):** Localizadas no pacote `br.com.naildesigner.messaging.api.dto`
    * `EmailDto.java`: Dados para a solicitação de envio de um e-mail (destinatários, assunto, corpo).

## Como Usar

Para que outro serviço utilize este contrato de API, adicione a seguinte dependência ao `pom.xml` do serviço consumidor:

```xml
<dependency>
    <groupId>br.com.naildesigner</groupId>
    <artifactId>messaging-service-api</artifactId>
    <version>0.0.1-SNAPSHOT</version> </dependency>
Opcionalmente, você pode adicionar uma interface de Cliente Feign aqui também, se desejar.

Como Construir (Build)
Para compilar esta biblioteca e instalá-la no seu repositório Maven local (para que outros projetos locais possam usá-la), navegue até a pasta raiz deste projeto e execute:

Bash

mvn clean install
Isso garantirá que as DTOs estejam disponíveis para os serviços que dependem desta API.
