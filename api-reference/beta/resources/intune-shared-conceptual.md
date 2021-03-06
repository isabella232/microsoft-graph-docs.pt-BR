---
title: Recursos compartilhados no Microsoft Intune-API do Microsoft Graph
description: Lista a API do Microsoft Graph para os pontos de extremidade do Intune (REST) que dão suporte a vários fluxos de trabalho para uma organização de locatário.
localization_priority: Normal
author: dougeby
ms.prod: intune
ms.openlocfilehash: 80528f0ad7ab587e6945543e03225d112d958604
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49271930"
---
# <a name="shared-resources-in-microsoft-intune"></a>Recursos compartilhados no Microsoft Intune

Namespace: microsoft.graph

> **Importante:** as APIs na versão /beta no Microsoft Graph estão em visualização e sujeitas a alterações. Não há suporte para o uso dessas APIs em aplicativos de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

Esses pontos de extremidade são usados em vários fluxos de trabalho do Microsoft Graph API para o Intune.  A intenção, finalidade e permissões necessárias para usar um determinado recurso varia de acordo com o fluxo de trabalho específico e o contexto da chamada subjacente.  Além disso, determinados métodos, propriedades e ações têm suporte apenas para fluxos de trabalho específicos.

Os seguintes recursos de gráfico são compartilhados entre fluxos de trabalho do Intune:

- [Estado da ação](intune-shared-actionstate.md)
- [Destino de atribuição de todos os dispositivos](intune-shared-alldevicesassignmenttarget.md)
- [Destino de atribuição de todos os usuários licenciados](intune-shared-alllicensedusersassignmenttarget.md)
- [Proteção de aplicativo gerenciado Android](intune-shared-androidmanagedappprotection.md)
- [Configurações de atribuição de aplicativo repositório gerenciado do Android](intune-shared-androidmanagedstoreappassignmentsettings.md)
- [Armazenamento de destino de certificados](intune-shared-certificatedestinationstore.md)
- [Repositório de certificados](intune-shared-certificatestore.md)
- [Escala de período de validade do certificado](intune-shared-certificatevalidityperiodscale.md)
- [Ação do portal da empresa](intune-shared-companyportalaction.md)
- [Ação bloqueada do portal da empresa](intune-shared-companyportalblockedaction.md)
- [Status de conformidade](intune-shared-compliancestatus.md)
- [Tipo de filtro de atribuição de gerenciamento de dispositivos e aplicativos](intune-shared-deviceandappmanagementassignmentfiltertype.md)
- [Origem da atribuição de gerenciamento de dispositivos e aplicativos](intune-shared-deviceandappmanagementassignmentsource.md)
- [Destino de atribuição de gerenciamento de aplicativo e dispositivo](intune-shared-deviceandappmanagementassignmenttarget.md)
- [Gerenciamento de aplicativos de dispositivo](intune-shared-deviceappmanagement.md)
- [Categoria do dispositivo](intune-shared-devicecategory.md)
- [Política de conformidade do dispositivo](intune-shared-devicecompliancepolicy.md)
- [Configuração do dispositivo](intune-shared-deviceconfiguration.md)
- [Configuração de registro do dispositivo](intune-shared-deviceenrollmentconfiguration.md)
- [Tipo de registro de dispositivo](intune-shared-deviceenrollmenttype.md)
- [Gerenciamento de dispositivos](intune-shared-devicemanagement.md)
- [Configurações de credenciais derivadas de gerenciamento de dispositivos](intune-shared-devicemanagementderivedcredentialsettings.md)
- [Relatórios de gerenciamento de dispositivos](intune-shared-devicemanagementreports.md)
- [Script de gerenciamento de dispositivo](intune-shared-devicemanagementscript.md)
- [Tipo de plataforma do dispositivo](intune-shared-deviceplatformtype.md)
- [Tipo de dispositivo](intune-shared-devicetype.md)
- [Habilitação](intune-shared-enablement.md)
- [Opções de disponibilidade do registro](intune-shared-enrollmentavailabilityoptions.md)
- [Estado de registro](intune-shared-enrollmentstate.md)
- [Destino de atribuição de grupos de exclusão](intune-shared-exclusiongroupassignmenttarget.md)
- [Uso estendido de chave](intune-shared-extendedkeyusage.md)
- [Destino de atribuição de grupo](intune-shared-groupassignmenttarget.md)
- [Algoritmos hash](intune-shared-hashalgorithms.md)
- [Intenção de instalação](intune-shared-installintent.md)
- [Configurações de atribuição do aplicativo LOB do iOS](intune-shared-ioslobappassignmentsettings.md)
- [Configuração de provisionamento do aplicativo LOB do iOS](intune-shared-ioslobappprovisioningconfiguration.md)
- [Proteção de aplicativo gerenciado iOS](intune-shared-iosmanagedappprotection.md)
- [Configurações de atribuição de aplicativo da loja iOS](intune-shared-iosstoreappassignmentsettings.md)
- [Configurações de atribuição do aplicativo VPP do iOS](intune-shared-iosvppappassignmentsettings.md)
- [Intervalo de IP](intune-shared-iprange.md)
- [Intervalo de IPv4](intune-shared-ipv4range.md)
- [Intervalo de IPv6](intune-shared-ipv6range.md)
- [Tamanho da chave](intune-shared-keysize.md)
- [Opção de provedor de armazenamento de chaves](intune-shared-keystorageprovideroption.md)
- [Usos de chave](intune-shared-keyusages.md)
- [Par chave/valor](intune-shared-keyvaluepair.md)
- [Configurações de atribuição do aplicativo VPP do macOS](intune-shared-macosvppappassignmentsettings.md)
- [Tipo de proprietário do dispositivo gerenciado](intune-shared-manageddeviceownertype.md)
- [Tipo de agente de gerenciamento](intune-shared-managementagenttype.md)
- [Política de proteção de informações do Windows MDM](intune-shared-mdmwindowsinformationprotectionpolicy.md)
- [Configurações de atribuição do aplicativo da Microsoft Store para Empresas](intune-shared-microsoftstoreforbusinessappassignmentsettings.md)
- [Conteúdo MIME](intune-shared-mimecontent.md)
- [Aplicativo móvel](intune-shared-mobileapp.md)
- [Configurações de atribuição de aplicativo móvel](intune-shared-mobileappassignmentsettings.md)
- [Configurações de tempo de instalação do aplicativo móvel](intune-shared-mobileappinstalltimesettings.md)
- [Evento de solução de problemas de aplicativo móvel](intune-shared-mobileapptroubleshootingevent.md)
- [Tipo de proprietário](intune-shared-ownertype.md)
- [Tipo de plataforma da política](intune-shared-policyplatformtype.md)
- [Domínio com proxy](intune-shared-proxieddomain.md)
- [Report](intune-shared-report.md)
- [Raiz de relatório](intune-shared-reportroot.md)
- [Estado do aplicativo resultante](intune-shared-resultantappstate.md)
- [Cores RGB](intune-shared-rgbcolor.md)
- [Executar como tipo de conta](intune-shared-runasaccounttype.md)
- [Estado da execução](intune-shared-runstate.md)
- [Opções de geração do estado da interface do usuário salvas](intune-shared-saveduistategenerationoptions.md)
- [Tipo de fonte de configuração](intune-shared-settingsourcetype.md)
- [Tipo de nome alternativo da entidade](intune-shared-subjectalternativenametype.md)
- [Configuração direcionada de aplicativo gerenciado](intune-shared-targetedmanagedappconfiguration.md)
- [URI](intune-shared-uri.md)
- [Usuário](intune-shared-user.md)
- [Tipo de conta do token VPP](intune-shared-vpptokenaccounttype.md)
- [Causa da falha da ação do token VPP](intune-shared-vpptokenactionfailurereason.md)
- [Configurações de atribuição do aplicativo LOB do Win32](intune-shared-win32lobappassignmentsettings.md)
- [Prioridade de otimização de entrega do aplicativo LOB Win32](intune-shared-win32lobappdeliveryoptimizationpriority.md)
- [Notificação de aplicativo LOB do Win32](intune-shared-win32lobappnotification.md)
- [Configurações de reinicialização de aplicativos LOB do Win32](intune-shared-win32lobapprestartsettings.md)
- [Configurações de atribuição do aplicativo Windows AppX](intune-shared-windowsappxappassignmentsettings.md)
- [Perfil de implantação do Windows Autopilot](intune-shared-windowsautopilotdeploymentprofile.md)
- [Configuração de ingresso no domínio do Windows](intune-shared-windowsdomainjoinconfiguration.md)
- [Configurações de atribuição do aplicativo Windows universal AppX](intune-shared-windowsuniversalappxappassignmentsettings.md)
- [Estado do Windows Update](intune-shared-windowsupdatestate.md)