---
title: Dispositivos gerenciados pela placa com o Intune-API do Microsoft Graph
description: Lista a API do Microsoft Graph para os pontos de extremidade do Intune (REST) usados para a integração (configuração e inicialização) de dispositivos para uma organização de locatário.
localization_priority: Normal
author: dougeby
ms.prod: intune
ms.openlocfilehash: 5788b1d7a13f0be84b0368dfa73e7932f4820d9d
ms.sourcegitcommit: eb536655ffd8d49ae258664f35c50a8263238400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49266547"
---
# <a name="enroll-devices-for-management-in-intune"></a>Registrar dispositivos para o gerenciamento no Intune

Namespace: microsoft.graph

> **Importante:** as APIs na versão /beta no Microsoft Graph estão em visualização e sujeitas a alterações. Não há suporte para o uso dessas APIs em aplicativos de produção.

> **Observação:** A API do Microsoft Graph para Intune requer uma [licença ativa do Intune](https://go.microsoft.com/fwlink/?linkid=839381) para o locatário.

É possível registrar dispositivos, incluindo computadores Windows, para habilitar o gerenciamento de dispositivo móvel (MDM) com o Microsoft Intune. Este tópico descreve as diferentes maneiras de registrar dispositivos móveis no gerenciamento do Intune. A maneira de registrar dispositivos depende do tipo de dispositivo, da propriedade e do nível de gerenciamento necessário. O registro "Traga seu próprio dispositivo" (BYOD) permite aos usuários registrar seus telefones, computador e tablets pessoais. O registro de dispositivo de propriedade corporativa (COD) permite cenários de gerenciamento como apagamento remoto, dispositivos compartilhados ou afinidade de usuários em um dispositivo.

Os seguintes recursos do Graph estão disponíveis para gerenciar registros no Intune:

- [Configuração de conector de certificado](intune-onboarding-certificateconnectorsetting.md)
- [Parceiro de gerenciamento de conformidade](intune-onboarding-compliancemanagementpartner.md)
- [Atribuição de parceiro de gerenciamento de conformidade](intune-onboarding-compliancemanagementpartnerassignment.md)
- [Dados de gerenciamento de aplicativo e dispositivo](intune-onboarding-deviceandappmanagementdata.md)
- [Configuração de autoridade de cogerenciamento de dispositivos](intune-onboarding-devicecomanagementauthorityconfiguration.md)
- [Configuração de limite do registro do dispositivo](intune-onboarding-deviceenrollmentlimitconfiguration.md)
- [Restrição da plataforma de registro do dispositivo](intune-onboarding-deviceenrollmentplatformrestriction.md)
- [Configuração das restrições da plataforma de registro do dispositivo](intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md)
- [Configuração do Windows Hello para empresas do registro do dispositivo](intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md)
- [Nível de acesso do Exchange de gerenciamento de dispositivo](intune-onboarding-devicemanagementexchangeaccesslevel.md)
- [Regra de acesso do Exchange de gerenciamento de dispositivo](intune-onboarding-devicemanagementexchangeaccessrule.md)
- [Tipo de regra de acesso do Exchange de gerenciamento de dispositivo](intune-onboarding-devicemanagementexchangeaccessruletype.md)
- [Conector do Exchange de gerenciamento de dispositivo](intune-onboarding-devicemanagementexchangeconnector.md)
- [Status do conector do Exchange de gerenciamento de dispositivo](intune-onboarding-devicemanagementexchangeconnectorstatus.md)
- [Tipo de sincronização do conector do Exchange de gerenciamento de dispositivo](intune-onboarding-devicemanagementexchangeconnectorsynctype.md)
- [Tipo de conector do Exchange de gerenciamento de dispositivo](intune-onboarding-devicemanagementexchangeconnectortype.md)
- [Classe de dispositivo do exchange de gerenciamento de dispositivo](intune-onboarding-devicemanagementexchangedeviceclass.md)
- [Política local do exchange para gerenciamento de dispositivo](intune-onboarding-devicemanagementexchangeonpremisespolicy.md)
- [Parceiro de gerenciamento do dispositivo](intune-onboarding-devicemanagementpartner.md)
- [Tipo de aplicativo de parceiro de gerenciamento do dispositivo](intune-onboarding-devicemanagementpartnerapptype.md)
- [Atribuição de parceiro de gerenciamento de dispositivos](intune-onboarding-devicemanagementpartnerassignment.md)
- [Estado de locatário de parceiro de gerenciamento do dispositivo](intune-onboarding-devicemanagementpartnertenantstate.md)
- [Atribuição de configuração do registro](intune-onboarding-enrollmentconfigurationassignment.md)
- [Marca Intune](intune-onboarding-intunebrand.md)
- [Autoridade MDM](intune-onboarding-mdmauthority.md)
- [Opções de seleção do portal da Microsoft Store para Empresas](intune-onboarding-microsoftstoreforbusinessportalselectionoptions.md)
- [Conector de defesa contra ameaças móveis](intune-onboarding-mobilethreatdefenseconnector.md)
- [Estado de locatário do parceiro de ameaças móveis](intune-onboarding-mobilethreatpartnertenantstate.md)
- [Configuração de acesso condicional local](intune-onboarding-onpremisesconditionalaccesssettings.md)
- [Organização](intune-onboarding-organization.md)
- [Chave de sideload](intune-onboarding-sideloadingkey.md)
- [Token VPP](intune-onboarding-vpptoken.md)
- [resultado de ação de token VPP](intune-onboarding-vpptokenactionresult.md)
- [Resumo da licença de token VPP](intune-onboarding-vpptokenlicensesummary.md)
- [Resultado da ação de revogar licenças de token VPP](intune-onboarding-vpptokenrevokelicensesactionresult.md)
- [Estado do token VPP](intune-onboarding-vpptokenstate.md)
- [Status de sincronização do token VPP](intune-onboarding-vpptokensyncstatus.md)
- [Configuração da página de conclusão do registro do Windows 10](intune-onboarding-windows10enrollmentcompletionpageconfiguration.md)
- [Uso do PIN do Windows Hello para empresas](intune-onboarding-windowshelloforbusinesspinusage.md)