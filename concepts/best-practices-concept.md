---
title: Práticas recomendadas para trabalhar com o Microsoft Graph
description: Este artigo descreve as práticas recomendadas que você pode aplicar para ajudar seus aplicativos a tirar o máximo proveito do Microsoft Graph, caso isso envolva saber mais sobre o Microsoft Graph, melhorar o desempenho do aplicativo ou tornar seu aplicativo mais confiável para os usuários finais.
localization_priority: Priority
ms.custom: graphiamtop20
ms.openlocfilehash: adfb7a1989ddd7667f5afc230f349295ac1c642e
ms.sourcegitcommit: 3fbc2249b307e8d3a9de18f22ef6911094ca272c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48288046"
---
# <a name="best-practices-for-working-with-microsoft-graph"></a>Práticas recomendadas para trabalhar com o Microsoft Graph

Este artigo descreve as práticas recomendadas que você pode aplicar para ajudar seus aplicativos a tirar o máximo proveito do Microsoft Graph, caso isso envolva saber mais sobre o Microsoft Graph, melhorar o desempenho do aplicativo ou tornar seu aplicativo mais confiável para os usuários finais.

## <a name="use-graph-explorer-to-get-to-know-the-api"></a>Usar o Graph Explorer para saber mais sobre a API

A melhor maneira de começar a explorar os dados disponíveis pelo Microsoft Graph é usando o [Graph Explorer](https://aka.ms/ge). O Graph Explorer permite criar solicitações REST (com suporte completo para CRUD), adaptar os cabeçalhos de solicitação HTTP e ver as respostas dos dados. Para ajudar você a começar, o Graph Explorer também oferece um conjunto de consultas de exemplo.

Experimente novas APIs antes de integrá-las em seu aplicativo.

## <a name="authentication"></a>Autenticação

Para acessar os dados no Microsoft Graph, seu aplicativo precisará adquirir um token de acesso do OAuth 2.0 e apresentá-lo ao Microsoft Graph em um dos itens a seguir:

- O cabeçalho de solicitação HTTP *Authorization*, como um token de *Portador*
- O construtor do cliente gráfico ao usar uma biblioteca de cliente do Microsoft Graph

Use a API da Biblioteca de Autenticação Microsoft, [MSAL](/azure/active-directory/develop/active-directory-v2-libraries), para adquirir o token de acesso para o Microsoft Graph.

## <a name="consent-and-authorization"></a>Consentimento e autorização

Aplique as seguintes práticas recomendadas de consentimento e autorização ao aplicativo:

- **Use privilégios mínimos**. Apenas solicite permissões absolutamente necessárias e somente quando você precisar delas. Para as APIs que o aplicativo chama, verifique a seção de permissões nos tópicos do método (por exemplo, confira [como criar um usuário](/graph/api/user-post-users?view=graph-rest-1.0) e escolha as permissões com menos privilégios. Uma ver uma lista completa de permissões, confira [referência de permissões](permissions-reference.md).

- **Use o tipo de permissão correto com base nos cenários**. Se você estiver criando um aplicativo interativo no qual um usuário conectado está presente, seu aplicativo deverá usar permissões *delegadas* nas quais o aplicativo recebe permissão de atuar como um usuário conectado ao fazer chamadas para o Microsoft Graph. Se, no entanto, seu aplicativo for executado sem um usuário conectado, como um serviço em segundo plano ou um daemon, seu aplicativo deverá usar permissões de aplicativo.

    >**Observação:** o uso de permissões de aplicativo para cenários interativos pode colocar a conformidade e a segurança de seu aplicativo em risco. Isso pode elevar inadvertidamente os privilégios de um usuário para acessar dados, contornando as políticas configuradas por um administrador.
<!-- LG: Use a more clear lead-in here, like "Consider the end user and admin experience"? -->
- **Esteja atento ao configurar seu aplicativo**. Isso afetará diretamente as experiências do usuário final e do administrador, além da adoção e segurança do aplicativo. Por exemplo:

  - A declaração de privacidade, os termos de uso, o nome, o logotipo e o domínio do seu aplicativo serão exibidos com consentimento e outras experiências. Portanto, verifique se foram configurados com cuidado para que sejam compreendidos pelos usuários finais.
  - Leve em consideração quem consentirá com seu aplicativo, seja o usuário final ou administrador, e configure seu aplicativo para [solicitar permissões de forma adequada](/azure/active-directory/develop/active-directory-v2-scopes).
  - Verifique se você entende a diferença entre [consentimento estático, dinâmico e incremental](/azure/active-directory/develop/active-directory-v2-compare#incremental-and-dynamic-consent).

- **Considere usar aplicativos multilocatários**. Tenha em mente que os clientes podem ter vários controles de aplicativo e consentimentos em diferentes estados. Por exemplo:

  - os administradores de locatários podem desabilitar a capacidade dos usuários finais permitirem os aplicativos. Nesse caso, um administrador precisaria consentir em nome de seus usuários.
  - Os administradores de locatários podem definir políticas de autorização personalizadas, como impedir que os usuários leiam perfis de outros usuários ou limitar a criação de grupos de autoatendimento a um conjunto limitado de usuários. Nesse caso, seu aplicativo deve esperar que a resposta de erro 403 seja tratada ao atuar em nome de um usuário.

## <a name="handle-responses-effectively"></a>Controlar as respostas com eficiência

Dependendo das solicitações feitas ao Microsoft Graph, seus aplicativos devem estar preparados para lidar com diferentes tipos de respostas. Veja a seguir algumas das práticas mais importantes a seguir para garantir que seu aplicativo se comporte de maneira confiável e previsível para seus usuários finais.

### <a name="pagination"></a>Paginação

Ao consultar um conjunto de recursos, você deve esperar que o Microsoft Graph retorne o conjunto de resultados em várias páginas devido aos limites de tamanho de página do lado do servidor. Quando um conjunto de resultados se estende por várias páginas, o Microsoft Graph retorna uma propriedade `@odata.nextLink` na resposta que contém uma URL para a próxima página de resultados.

Por exemplo, listar as mensagens de usuários conectados:

```http
GET https://graph.microsoft.com/v1.0/me/messages
```

retornaria uma resposta contendo uma propriedade `@odata.nextLink`, se o conjunto de resultados exceder o limite de tamanho de página do lado do servidor.

```json
"@odata.nextLink": "https://graph.microsoft.com/v1.0/me/messages?$skip=23"
```

>**Observação:** seu aplicativo deve **sempre** lidar com a possibilidade das respostas serem paginadas sem processamento e usar a propriedade `@odata.nextLink` para obter o próximo conjunto paginado de resultados, até que todas as páginas do conjunto de resultados sejam lidas. A página final não conterá uma propriedade `@odata.nextLink`. Você deve incluir a URL inteira na propriedade `@odata:nextLink` na solicitação da próxima página de resultados, tratando toda a URL como uma cadeia de caracteres opaca.

Para saber mais, confira [paginação](paging.md).

### <a name="handling-expected-errors"></a>Como tratar erros esperados

Como seu aplicativo tem que lidar com todas as respostas de erro (nos intervalos 400 e 500), dê especial atenção a determinados erros e respostas esperados que estão listados na tabela a seguir.

| Tópico   | Código de erro HTTP    | Prática recomendada|
|:-----------|:--------|:----------|
| O usuário não tem acesso | 403 | Se seu aplicativo estiver em execução, ele poderá encontrar esse erro, mesmo que tenha recebido as permissões necessárias por meio de uma experiência de consentimento.  Nesse caso, é mais provável que o usuário conectado não tenha privilégios para acessar o recurso solicitado. Seu aplicativo deve fornecer um erro genérico de "Acesso negado" para o usuário conectado. |
|Não encontrado| 404 | Em certos casos, um recurso solicitado pode não ser encontrado. Por exemplo, um recurso pode não existir porque ainda não foi provisionado (como a foto de um usuário) ou porque foi excluído. Alguns recursos excluídos *podem* ser totalmente restaurados em até 30 dias após a exclusão, como recursos de usuários, grupos e aplicativos, portanto, o aplicativo também deve levar isso em consideração.|
|Limitação|429|As APIs podem limitar a qualquer momento por diversos motivos, portanto, seu aplicativo deve **sempre** estar preparado para manipular 429 respostas. Essa resposta de erro inclui o campo *Retry-After* no cabeçalho de resposta HTTP. Desativar solicitações usando o atraso *Retry-After* é a forma mais rápida de se recuperar da limitação. Para saber mais, confira [limitação](throttling.md).|
|Serviço indisponível| 503 | O motivo mais provável é que os serviços estejam ocupados. Você deve empregar uma estratégia de retirada similar à 429. Além disso, você deve **sempre** fazer novas solicitações de novas tentativas em uma nova conexão HTTP.|

### <a name="evolvable-enums"></a>Enums que evoluem

Os aplicativos cliente podem ser desfeitos com a adição de membros a um enum existente. Para alguns dos enums mais recentes do Microsoft Graph, um mecanismo está disponível para permitir a adição de novos membros sem implicar em uma alteração significativa. Nesses enums mais recentes, você verá um membro *sentinela* comum chamado `unknownFutureValue` que demarca membros enum conhecidos e desconhecidos. Os membros conhecidos terão um número menor que o membro sentinela, enquanto os membros desconhecidos terão um valor maior.
Por padrão, o Microsoft Graph não retorna membros desconhecidos. Se, no entanto, seu aplicativo tiver sido gravado para manipular a aparência de membros desconhecidos, ele poderá optar por receber membros enum desconhecidos usando um cabeçalho de solicitação HTTP *Prefer*.

>**Observação:** se o aplicativo estiver preparado para lidar com membros enum desconhecidos, ele deverá aceitar a condição usando um cabeçalho solicitação HTTP *prefer*: `Prefer: include-unknown-enum-members`.


## <a name="storing-data-locally"></a>Armazenamento de dados no local

Idealmente, seu aplicativo deveria fazer chamadas para o Microsoft Graph para recuperar dados em tempo real conforme necessário. Você só deve armazenar em cache ou armazenar dados localmente se um cenário específico assim o exigir e, se esse caso de uso for abrangido pelos seus termos de uso e pela política de privacidade e não violar os [termos de uso das APIs da Microsoft](/legal/microsoft-apis/terms-of-use?context=/graph/context). O aplicativo também deve implementar políticas adequadas de retenção e de exclusão.

## <a name="optimizations"></a>Otimizações

Em geral, por motivos de desempenho e até mesmo segurança ou privacidade, você só deve obter os dados que seu aplicativo realmente precisar e nada mais.

### <a name="use-projections"></a>Usar projeções

Escolha apenas as propriedades que seu aplicativo realmente precisa e nada mais já que isso evitará tráfego de rede e processamento de dados desnecessários em seu aplicativo (e no serviço).

>**Observação:** use o parâmetro de consulta `$select` para limitar as propriedades retornadas por uma consulta àquelas exigidas pelo aplicativo.

Por exemplo, ao recuperar as mensagens do usuário conectado, você pode especificar que somente as propriedades **from** e **subject** sejam retornadas:

```http
GET https://graph.microsoft.com/v1.0/me/messages?$select=from,subject
```

### <a name="getting-minimal-responses"></a>Como obter respostas mínimas

Para algumas operações, como PUT e PATCH (e, em alguns casos, POST), se seu aplicativo não precisa usar uma carga de resposta, solicite à API que retorne dados mínimos. Observe que alguns serviços já retornam uma resposta 204 No Content para operações PUT e PATCH.

>**Observação:** solicite respostas de representação mínima usando um cabeçalho de solicitação HTTP onde for apropriado: *Prefer: return=minimal*. Observe que, em operações de criação, isso pode não ser adequado já que o aplicativo pode estar esperando receber o serviço gerado `id` para o objeto recém-criado na resposta.

### <a name="track-changes-delta-query-and-webhook-notifications"></a>Controlar alterações: consulta delta e notificações de webhook

Se for preciso que o aplicativo saiba quais alterações foram feitas nos dados, você provavelmente receberá uma notificação de webhook sempre que dados de seu interesse forem alterados. Isso é mais eficiente do que simplesmente fazer pesquisas regularmente.

Use [notificações de webhook](/graph/api/resources/webhooks?view=graph-rest-1.0) para receber notificações por push quando os dados forem alterados.

Use a consulta delta se seu aplicativo tiver que armazenar em cache ou armazenar dados do Microsoft Graph localmente, e mantê-los atualizados, ou tiver que controlar alterações nos dados por qualquer outro motivo. Isso evitará a computação excessiva do aplicativo para recuperar dados que ele já possui, minimizar o tráfego de rede e reduzir a probabilidade de atingir um limite de limitação.

Use a [consulta delta](delta-query-overview.md) para manter os dados atualizados com eficiência.

### <a name="using-webhooks-and-delta-query-together"></a>Usar consultas delta e webhooks em conjunto

Os webhooks e a consulta delta geralmente funcionam melhor quando são usados em conjunto já que, se você usar a consulta delta sozinha, precisará calcular o intervalo de sondagem correto. Se esse intervalo for muito curto poderá levar a respostas vazias que desperdiçam recursos, mas, se for muito longo, você poderá acabar ficando com dados obsoletos. Você terá o melhor de dois mundos se usar as notificações de webhook como o gatilho para fazer chamadas de consulta delta.

Use as [notificações de webhook](/graph/api/resources/webhooks?view=graph-rest-1.0) como o gatilho para fazer chamadas de consulta delta. Você também deve garantir que seu aplicativo tenha um limite de pesquisa de backstop, caso nenhuma notificação seja acionada.

### <a name="batching"></a>Envio em lote

Os lotes JSON permitem otimizar seu aplicativo combinando várias solicitações em um único objeto JSON. Combinar essas solicitações individuais em uma única solicitação em lote pode economizar latência de rede significativa para o aplicativo e conservar recursos de conexão.

Use o [envio em lote](json-batching.md) onde uma latência de rede significativa pode ter um grande impacto no desempenho.

## <a name="reliability-and-support"></a>Confiabilidade e suporte
Para garantir a segurança e facilitar o suporte do aplicativo:

- Respeite o TTL DNS e defina a conexão TTL para correspondê-lo. Isso garantirá a disponibilidade em caso de failovers.
- Abra conexões para todas as respostas de DNS anunciadas.
- Gerar um GUID exclusivo e o enviar em cada solicitação REST do Microsoft Graph. Isso ajudará a Microsoft a investigar os erros com maior facilidade, caso seja necessário relatar um problema com o Microsoft Graph.
  - Em todas as solicitações do Microsoft Graph, gere um GUID exclusivo, envie-o no cabeçalho de solicitação HTTP do `client-request-id` e também registre-o nos logs dos aplicativos.
  - Registre sempre o `request-id`, o `timestamp` e o `x-ms-ags-diagnostic` dos cabeçalhos de resposta HTTP. Estes, juntamente com o `client-request-id`, são necessários para relatar os problemas no [Stack Overflow](https://stackoverflow.com/questions/tagged/microsoft-graph) ou no Suporte da Microsoft.