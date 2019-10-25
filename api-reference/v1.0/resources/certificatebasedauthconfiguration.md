---
title: tipo de recurso certificateBasedAuthConfiguration
description: Representa uma coleção de autoridades de certificação.
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: resourcePageType
ms.openlocfilehash: d0b5b57a7594dfaf4fde88615c6a21314618c0eb
ms.sourcegitcommit: 0dcabe677927c259c2ddcefd0d5e2a2aef065e8b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2019
ms.locfileid: "37539285"
---
# <a name="certificatebasedauthconfiguration-resource-type"></a><span data-ttu-id="82d6a-103">tipo de recurso certificateBasedAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d6a-103">certificateBasedAuthConfiguration resource type</span></span>

<span data-ttu-id="82d6a-104">A autenticação baseada em certificado permite que você seja autenticado pelo Azure Active Directory com um certificado de cliente em um dispositivo Windows, Android ou iOS ao conectar sua conta do Exchange Online a:</span><span class="sxs-lookup"><span data-stu-id="82d6a-104">Certificate-based authentication enables you to be authenticated by Azure Active Directory with a client certificate on a Windows, Android, or iOS device when connecting your Exchange Online account to:</span></span>

- <span data-ttu-id="82d6a-105">Aplicativos móveis da Microsoft, como Outlook e Word</span><span class="sxs-lookup"><span data-stu-id="82d6a-105">Microsoft mobile applications such as Outlook and Word</span></span>
- <span data-ttu-id="82d6a-106">Clientes do Exchange ActiveSync (EAS)</span><span class="sxs-lookup"><span data-stu-id="82d6a-106">Exchange ActiveSync (EAS) clients</span></span>

<span data-ttu-id="82d6a-107">A configuração desse recurso elimina a necessidade de inserir uma combinação de nome de usuário e senha em determinados emails e aplicativos do Microsoft Office em seu dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="82d6a-107">Configuring this feature eliminates the need to enter a username and password combination into certain mail and Microsoft Office applications on your mobile device.</span></span>

<span data-ttu-id="82d6a-108">A configuração de autenticação baseada em certificado é fornecida por meio de uma coleção de autoridades de certificação.</span><span class="sxs-lookup"><span data-stu-id="82d6a-108">Certificate-based authentication configuration is provided through a collection of certificate authorities.</span></span> <span data-ttu-id="82d6a-109">As autoridades de certificação são usadas para estabelecer uma cadeia de certificados confiáveis que permite que os clientes sejam autenticados pelo Azure Active Directory com um certificado de cliente.</span><span class="sxs-lookup"><span data-stu-id="82d6a-109">The certificate authorities are used to establish a trusted certificate chain which enables clients to be authenticated by Azure Active Directory with a client certificate.</span></span>

<span data-ttu-id="82d6a-110">Saiba mais sobre [a autenticação baseada em certificado no Azure Active Directory](https://docs.microsoft.com/azure/active-directory/authentication/active-directory-certificate-based-authentication-get-started).</span><span class="sxs-lookup"><span data-stu-id="82d6a-110">Learn more about [certificate-based authentication in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/authentication/active-directory-certificate-based-authentication-get-started).</span></span>

## <a name="methods"></a><span data-ttu-id="82d6a-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="82d6a-111">Methods</span></span>

| <span data-ttu-id="82d6a-112">Método</span><span class="sxs-lookup"><span data-stu-id="82d6a-112">Method</span></span>       | <span data-ttu-id="82d6a-113">Tipo de retorno</span><span class="sxs-lookup"><span data-stu-id="82d6a-113">Return Type</span></span> | <span data-ttu-id="82d6a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="82d6a-114">Description</span></span> |
|:-------------|:------------|:------------|
| [<span data-ttu-id="82d6a-115">Listar certificateBasedAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d6a-115">List certificateBasedAuthConfiguration</span></span>](../api/certificatebasedauthconfiguration-list.md) | [<span data-ttu-id="82d6a-116">certificateBasedAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d6a-116">certificateBasedAuthConfiguration</span></span>](certificatebasedauthconfiguration.md) | <span data-ttu-id="82d6a-117">Lista as propriedades da coleção **certificateBasedAuthConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="82d6a-117">List the properties of the **certificateBasedAuthConfiguration** collection.</span></span> |
| [<span data-ttu-id="82d6a-118">Criar certificateBasedAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d6a-118">Create certificateBasedAuthConfiguration</span></span>](../api/certificatebasedauthconfiguration-post-certificatebasedauthconfiguration.md) | [<span data-ttu-id="82d6a-119">certificateBasedAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d6a-119">certificateBasedAuthConfiguration</span></span>](certificatebasedauthconfiguration.md) | <span data-ttu-id="82d6a-120">Criar um novo objeto **certificateBasedAuthConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="82d6a-120">Create a new **certificateBasedAuthConfiguration** object.</span></span> |
| [<span data-ttu-id="82d6a-121">Obter certificateBasedAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d6a-121">Get certificateBasedAuthConfiguration</span></span>](../api/certificatebasedauthconfiguration-get.md) | [<span data-ttu-id="82d6a-122">certificateBasedAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d6a-122">certificateBasedAuthConfiguration</span></span>](certificatebasedauthconfiguration.md) | <span data-ttu-id="82d6a-123">Ler as propriedades de um objeto **certificateBasedAuthConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="82d6a-123">Read the properties of a **certificateBasedAuthConfiguration** object.</span></span> |
| [<span data-ttu-id="82d6a-124">Excluir certificateBasedAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="82d6a-124">Delete certificateBasedAuthConfiguration</span></span>](../api/certificatebasedauthconfiguration-delete.md) | <span data-ttu-id="82d6a-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="82d6a-125">None</span></span> | <span data-ttu-id="82d6a-126">Excluir um objeto **certificateBasedAuthConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="82d6a-126">Delete a **certificateBasedAuthConfiguration** object.</span></span> |

>[!NOTE]
><span data-ttu-id="82d6a-127">Não há suporte para a atualização de **cerficateBasedAuthConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="82d6a-127">Updating **cerficateBasedAuthConfiguration** is not supported.</span></span> <span data-ttu-id="82d6a-128">Para alterar um **cerficateBasedAuthConfiguration**, primeiro exclua e crie um novo **cerficateBasedAuthConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="82d6a-128">To change a **cerficateBasedAuthConfiguration**, first delete and then create a new **cerficateBasedAuthConfiguration**.</span></span>

## <a name="properties"></a><span data-ttu-id="82d6a-129">Propriedades</span><span class="sxs-lookup"><span data-stu-id="82d6a-129">Properties</span></span>

| <span data-ttu-id="82d6a-130">Propriedade</span><span class="sxs-lookup"><span data-stu-id="82d6a-130">Property</span></span>     | <span data-ttu-id="82d6a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="82d6a-131">Type</span></span>        | <span data-ttu-id="82d6a-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="82d6a-132">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="82d6a-133">certificateAuthorities</span><span class="sxs-lookup"><span data-stu-id="82d6a-133">certificateAuthorities</span></span>|<span data-ttu-id="82d6a-134">coleção [certificateAuthority](certificateauthority.md)</span><span class="sxs-lookup"><span data-stu-id="82d6a-134">[certificateAuthority](certificateauthority.md) collection</span></span>|<span data-ttu-id="82d6a-135">Coleção de autoridades de certificação que cria uma cadeia de certificado confiável.</span><span class="sxs-lookup"><span data-stu-id="82d6a-135">Collection of certificate authorities which creates a trusted certificate chain.</span></span>|
|<span data-ttu-id="82d6a-136">id</span><span class="sxs-lookup"><span data-stu-id="82d6a-136">id</span></span>|<span data-ttu-id="82d6a-137">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="82d6a-137">String</span></span>|<span data-ttu-id="82d6a-138">O identificador exclusivo da configuração de autenticação baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="82d6a-138">The unique identifier of the certificate based auth configuration.</span></span> <span data-ttu-id="82d6a-139">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="82d6a-139">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="82d6a-140">Relações</span><span class="sxs-lookup"><span data-stu-id="82d6a-140">Relationships</span></span>

<span data-ttu-id="82d6a-141">Nenhum</span><span class="sxs-lookup"><span data-stu-id="82d6a-141">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="82d6a-142">Representação JSON</span><span class="sxs-lookup"><span data-stu-id="82d6a-142">JSON representation</span></span>

<span data-ttu-id="82d6a-143">Veja a seguir uma representação JSON do recurso.</span><span class="sxs-lookup"><span data-stu-id="82d6a-143">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.certificateBasedAuthConfiguration",
  "baseType": "",
  "keyProperty": "id"
}-->

```json
{
  "certificateAuthorities": {"@odata.type": "collection(microsoft.graph.certificateAuthority)"},
  "id": "String (identifier)"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "certificateBasedAuthConfiguration resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->