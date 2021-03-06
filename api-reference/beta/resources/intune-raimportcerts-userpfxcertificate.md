---
title: tipo de recurso userPFXCertificate
description: Entidade que encapsula todas as informações necessárias para os certificados PFX de um usuário.
author: dougeby
localization_priority: Normal
ms.prod: intune
doc_type: resourcePageType
ms.openlocfilehash: 7d893d27a46036b2eb7bc9aa59960b8182aef478
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49300952"
---
# <a name="userpfxcertificate-resource-type"></a>tipo de recurso userPFXCertificate

Namespace: microsoft.graph

> **Importante:** As APIs do Microsoft Graph na versão/beta estão sujeitas a alterações; Não há suporte para o uso de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Entidade que encapsula todas as informações necessárias para os certificados PFX de um usuário.

## <a name="methods"></a>Métodos
|Método|Tipo de retorno|Descrição|
|:---|:---|:---|
|[Listar userPFXCertificates](../api/intune-raimportcerts-userpfxcertificate-list.md)|coleção [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md)|Listar Propriedades e relações dos objetos [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) .|
|[Obter userPFXCertificate](../api/intune-raimportcerts-userpfxcertificate-get.md)|[userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md)|Leia as propriedades e as relações do objeto [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) .|
|[Criar userPFXCertificate](../api/intune-raimportcerts-userpfxcertificate-create.md)|[userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md)|Criar um novo objeto [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) .|
|[Excluir userPFXCertificate](../api/intune-raimportcerts-userpfxcertificate-delete.md)|Nenhum|Exclui [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md).|
|[Atualizar userPFXCertificate](../api/intune-raimportcerts-userpfxcertificate-update.md)|[userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md)|Atualiza as propriedades de um objeto [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) .|

## <a name="properties"></a>Propriedades
|Propriedade|Tipo|Descrição|
|:---|:---|:---|
|id|String|Identificador exclusivo do certificado PFX.|
|identificação|String|Impressão digital SHA-1 do certificado PFX.|
|Da intendedpurpose|[userPfxIntendedPurpose](../resources/intune-raimportcerts-userpfxintendedpurpose.md)|Finalidade do certificado do ponto de vista da implantação. Os valores possíveis são: `unassigned`, `smimeEncryption`, `smimeSigning`, `vpn`, `wifi`.|
|userPrincipalName|String|Nome principal de usuário do certificado PFX.|
|startDateTime|DateTimeOffset|Data/hora de início da validade do certificado.|
|expirationDateTime|DateTimeOffset|Data/hora de validade do certificado.|
|providerName|String|Provedor de criptografia usado para criptografar este BLOB.|
|keyName|String|Nome da chave (dentro do provedor) usada para criptografar o blob.|
|paddingScheme|[userPfxPaddingScheme](../resources/intune-raimportcerts-userpfxpaddingscheme.md)|Esquema de preenchimento usado pelo provedor durante a criptografia/descriptografia. Os possíveis valores são: `none`, `pkcs1`, `oaepSha1`, `oaepSha256`, `oaepSha384`, `oaepSha512`.|
|encryptedPfxBlob|Binária|Blob PFX criptografado.|
|encryptedPfxPassword|String|Senha PFX criptografada.|
|createdDateTime|DateTimeOffset|Data/hora em que este certificado PFX foi importado.|
|lastModifiedDateTime|DateTimeOffset|Data/hora em que este certificado PFX foi modificado pela última vez.|

## <a name="relationships"></a>Relações
Nenhum

## <a name="json-representation"></a>Representação JSON
Veja a seguir uma representação JSON do recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.userPFXCertificate"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.userPFXCertificate",
  "id": "String (identifier)",
  "thumbprint": "String",
  "intendedPurpose": "String",
  "userPrincipalName": "String",
  "startDateTime": "String (timestamp)",
  "expirationDateTime": "String (timestamp)",
  "providerName": "String",
  "keyName": "String",
  "paddingScheme": "String",
  "encryptedPfxBlob": "binary",
  "encryptedPfxPassword": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)"
}
```




