---
title: Atualizar organizationalBrandingProperties
description: Atualiza as propriedades de um objeto organizationalBrandingProperties.
localization_priority: Normal
author: kexia
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 7655caa6e5c8eb1187bcc159f7f6d8c78641abc9
ms.sourcegitcommit: 40b0e58312819b69567f35ab894ee0d2989837ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/13/2020
ms.locfileid: "49031895"
---
# <a name="update-organizationalbrandingproperties"></a>Atualizar organizationalBrandingProperties

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Atualiza as propriedades de um objeto [organizationalBrandingProperties](../resources/organizationalbrandingproperties.md) .

## <a name="permissions"></a>Permissões

Uma das seguintes permissões é obrigatória para chamar esta API. Para saber mais, incluindo como escolher permissões, confira [Permissões](/graph/permissions-reference).

| Tipo de permissão                        | Permissões (da com menos para a com mais privilégios) |
|:---------------------------------------|:--------------------------------------------|
| Delegado (conta corporativa ou de estudante)     | Organization.ReadWrite.All |
| Delegado (conta pessoal da Microsoft) | Sem suporte. |
| Aplicativo                            | Sem suporte. |

## <a name="http-request"></a>Solicitação HTTP

<!-- { "blockType": "ignored" } -->

```http
PATCH /organization/{id}/branding/{property name}
PUT /organization/{id}/branding/{property name}
```

## <a name="request-headers"></a>Cabeçalhos de solicitação

| Nome       | Descrição|
|:-----------|:-----------|
| Autorização | {token} de portador. Obrigatório. |
| Content-Type  | application/json. Obrigatório.  |
| Conteúdo-idioma  | LCID. Opcional.  |

## <a name="request-body"></a>Corpo da solicitação

No corpo da solicitação, forneça os valores para os campos relevantes que devem ser atualizados. Propriedades existentes que não estão incluídas no corpo da solicitação terão seus valores anteriores mantidos ou serão recalculadas com base nas alterações a outros valores de propriedade. Para alcançar o melhor desempenho, não inclua valores existentes que não foram alterados.

| Propriedade     | Tipo        | Descrição |
|:-------------|:------------|:------------|
|CorDoFundo|String|Cor que aparecerá no lugar da imagem de plano de fundo em conexões de baixa largura de banda. É recomendável usar a cor principal do logotipo de faixa ou a cor da sua organização aqui. Especifique isso em hexadecimal (por exemplo, branco é #FFFFFF).|
|backgroundImage|Fluxo|Imagem que aparece como plano de fundo da página de entrada. . png ou. jpg não é maior do que 1920 x 1080 e menor do que 300kb. Uma imagem menor reduzirá os requisitos de largura de banda e fará com que as cargas de página mais tenham mais desempenho.|
|bannerLogo|Fluxo|Uma versão de banner do logotipo da empresa que aparece aparece na página de entrada. . png ou. jpg não maior do que 36x245px. Recomendamos usar uma imagem transparente sem preenchimento em torno do logotipo.|
|signInPageText|String|Texto que aparece na parte inferior da caixa de entrada. Você pode usá-lo para comunicar informações adicionais, como o número de telefone para o suporte técnico ou uma instrução legal. Este texto deve ser Unicode e não exceder 1024 caracteres.|
|squareLogo|Fluxo|Versão quadrada do logotipo da sua empresa. Isso aparece nas experiências de uso (OOBE) do Windows 10 e quando o Windows AutoPilot está habilitado para implantação. . png ou. jpg não maior do que 240x240px e não mais do que 10 KB em tamanho. Recomendamos usar uma imagem transparente sem preenchimento em torno do logotipo.|
|usernameHintText|String|Cadeia de caracteres que mostra como a dica na caixa de texto username na tela de entrada. Este texto deve ser Unicode, sem links ou código, e não pode exceder 64 caracteres.|

A propriedade **ID** é ignorada quando passada.

## <a name="response"></a>Resposta

Se tiver êxito, este método retornará um código de resposta `204 OK`.

## <a name="examples"></a>Exemplos
### <a name="example-1-update-default-branding"></a>Exemplo 1: atualizar a identidade visual padrão
Se a identidade visual já existir, o PATCH substituirá apenas as propriedades especificadas, deixando inalteradas as propriedades não especificadas. 
#### <a name="request"></a>Solicitação

Este é um exemplo de solicitação.
<!-- {
  "blockType": "request",
  "name": "update_organizationalbrandingproperties"
}-->

```http
PATCH https://graph.microsoft.com/beta/organization/d69179bf-f4a4-41a9-a9de-249c0f2efb1d/branding
Content-Type: application/json

{
    "signInPageText":"Default",
    "usernameHintText":"DefaultHint"
}
```

#### <a name="response"></a>Resposta
Este é um exemplo de resposta.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.organizationalBrandingProperties"
} -->

```http
HTTP/1.1 204 OK
```

Nesse caso, os valores do/branding padrão são atualizados, mas nenhum valor é alterado em qualquer localização.

### <a name="example-2-update-bannerlogo-for-default-branding"></a>Exemplo 2: atualizar bannerLogo para identidade visual padrão
A solicitação a seguir atualiza o logotipo da faixa para a identidade visual padrão.
#### <a name="request"></a>Solicitação

Este é um exemplo de solicitação.
<!-- {
  "blockType": "request",
  "name": "update_organizationalbrandingproperties"
}-->

```http
PATCH https://graph.microsoft.com/beta/organization/d69179bf-f4a4-41a9-a9de-249c0f2efb1d/branding/bannerLogo
Content-Type: image/jpeg

<Image>
```

#### <a name="response"></a>Resposta
Este é um exemplo de resposta.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.organizationalBrandingProperties"
} -->

```http
HTTP/1.1 204 No Content
```

### <a name="example-3-update-localized-branding"></a>Exemplo 3: atualizar a identidade visual localizada
Se o cabeçalho de idioma de conteúdo for especificado, a localização associada ao conteúdo será criada, se ainda não existir, e atualizada com os valores especificados. A identidade visual padrão não é alterada.
#### <a name="request"></a>Solicitação

Este é um exemplo de solicitação.
<!-- {
  "blockType": "request",
  "name": "update_organizationalbrandingproperties"
}-->

```http
PATCH https://graph.microsoft.com/beta/organization/d69179bf-f4a4-41a9-a9de-249c0f2efb1d/branding
Content-Type: application/json
Content-Language: fr

{
    "backgroundColor":"#FFFF33"
}
```

#### <a name="response"></a>Resposta
Este é um exemplo de resposta.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.organizationalBrandingProperties"
} -->

```http
HTTP/1.1 204 No Content
```

Após essa solicitação, a localização fr é atualizada com o novo valor de backgroundColor, mas nenhuma alteração é feita no padrão/branding.

### <a name="example-4-replace-default-branding-and-all-localizations"></a>Exemplo 4: substituir a identidade visual padrão e todas as localizações
Se a identidade visual já existir, PUT substituirá a identidade visual padrão e todas as localizações.
#### <a name="request"></a>Solicitação

Este é um exemplo de solicitação.
<!-- {
  "blockType": "request",
  "name": "update_organizationalbrandingproperties"
}-->

```http
PUT https://graph.microsoft.com/beta/organization/d69179bf-f4a4-41a9-a9de-249c0f2efb1d/branding
Content-Type: application/json
Content-Language: fr

{
    "backgroundColor":"#FFFF33"
}
```

#### <a name="response"></a>Resposta
Este é um exemplo de resposta.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.organizationalBrandingProperties"
} -->

```http
HTTP/1.1 204 No Content
```

Após essa solicitação, a identidade visual padrão tem apenas o backgroundColor especificado e tem exatamente uma localização com a ID fr, também com o conjunto backgroundColor.
<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update organizationalbrandingproperties",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
