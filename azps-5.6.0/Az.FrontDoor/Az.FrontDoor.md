---
Module Name: Az.FrontDoor
Module Guid: 91832aaa-dc11-4583-8239-adb7df531604
Download Help Link: https://docs.microsoft.com/powershell/module/az.frontdoor
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Az.FrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Az.FrontDoor.md
ms.openlocfilehash: 3f91574362a996b1f406cf1b9cb36886078f77d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905409"
---
# Az.FrontDoor 模組
## 描述
本節主題將說明 Azure Resource Manager 中 Azure Front Door Service 的 Azure PowerShell Cmdlet (ARM) 架構。 Cmdlet 存在於 Microsoft.Azure.Commands.FrontDoor 命名空間中。

## Az.FrontDoor Cmdlets
### [Disable-AzFrontDoorCustomDomainHttps](Disable-AzFrontDoorCustomDomainHttps.md)
停用自訂網域的 HTTPS

### [Enable-AzFrontDoorCustomDomainHttps](Enable-AzFrontDoorCustomDomainHttps.md)
使用 Front Door 受管理的憑證，或是使用 Azure 金鑰庫的憑證，為自訂網域啟用 HTTPS。

### [Get-AzFrontDoor](Get-AzFrontDoor.md)
取得前門負載平衡器

### [Get-AzFrontDoorFrontendEndpoint](Get-AzFrontDoorFrontendEndpoint.md)
取得前門前方端點。

### [Get-AzFrontDoorRulesEngine](Get-AzFrontDoorRulesEngine.md)
取得規則引擎組配置。

### [Get-AzFrontDoorWafManagedRuleSetDefinition](Get-AzFrontDoorWafManagedRuleSetDefinition.md)
取得 WAF 受管理的規則集定義

### [Get-AzFrontDoorWafPolicy](Get-AzFrontDoorWafPolicy.md)
取得 WAF 政策

### [New-AzFrontDoor](New-AzFrontDoor.md)
建立新的 Azure 前門負載平衡器

### [New-AzFrontDoorBackendObject](New-AzFrontDoorBackendObject.md)
建立 PSBackend 物件

### [New-AzFrontDoorBackendPoolObject](New-AzFrontDoorBackendPoolObject.md)
建立 PSBackendPool 物件以建立前端門

### [New-AzFrontDoorBackendPoolsSettingObject](New-AzFrontDoorBackendPoolsSettingObject.md)
建立 PSBackendPoolsSetting 物件以用於建立前門。

### [New-AzFrontDoorFrontendPointObject](New-AzFrontDoorFrontendEndpointObject.md)
建立 PSFrontendEndpoint 物件以用於建立前門

### [New-AzFrontDoorHeaderActionObject](New-AzFrontDoorHeaderActionObject.md)
建立 PSHeaderAction 物件。

### [New-AzFrontDoorHealthProbeSettingObject](New-AzFrontDoorHealthProbeSettingObject.md)
建立 PSHealthProbeSetting 物件以用於建立前門

### [New-AzFrontDoorLoadBalsettingSettingObject](New-AzFrontDoorLoadBalancingSettingObject.md)
建立 PSLoadBalsettingSetting 物件以建立前端門

### [New-AzFrontDoorRoutingRuleObject](New-AzFrontDoorRoutingRuleObject.md)
建立 PSRoutingRuleObject 以建立門道

### [New-AzFrontDoorRulesEngine](New-AzFrontDoorRulesEngine.md)
為指定的前門建立新規則引擎組。 

### [New-AzFrontDoorRulesEngineActionObject](New-AzFrontDoorRulesEngineActionObject.md)
建立 PSRulesEngineAction 物件以建立規則引擎規則。

### [New-AzFrontDoorRulesEngineMatchConditionObject](New-AzFrontDoorRulesEngineMatchConditionObject.md)
建立 PSRulesEngineMatchCondition 物件以建立規則引擎規則。

### [New-AzFrontDoorRulesEngineRuleObject](New-AzFrontDoorRulesEngineRuleObject.md)
建立 PSRulesEngineRule 物件以建立規則引擎。

### [New-AzFrontDoorWafCustomRuleObject](New-AzFrontDoorWafCustomRuleObject.md)
建立自訂規則物件以建立 WAF 策略

### [New-AzFrontDoorWafManagedRuleExclusionObject](New-AzFrontDoorWafManagedRuleExclusionObject.md)
建立 WAF 受管理規則集、群組或規則的受管理規則排除物件。

### [New-AzFrontDoorWafManagedRuleObject](New-AzFrontDoorWafManagedRuleObject.md)
建立 ManagedRule 物件以建立 WAF 策略

### [New-AzFrontDoorWafManagedRuleOverrideObject](New-AzFrontDoorWafManagedRuleOverrideObject.md)
建立受管理規則重寫物件

### [New-AzFrontDoorWafMatchConditionObject](New-AzFrontDoorWafMatchConditionObject.md)
建立 MatchCondition 物件以建立 WAF 策略

### [New-AzFrontDoorWafPolicy](New-AzFrontDoorWafPolicy.md)
建立 WAF 政策

### [New-AzFrontDoorWafRuleGroupOverrideObject](New-AzFrontDoorWafRuleGroupOverrideObject.md)
建立 RuleGroupOverride 物件以建立 WAF 原則

### [Remove-AzFrontDoor](Remove-AzFrontDoor.md)
移除前門負載平衡器

### [Remove-AzFrontDoorContent](Remove-AzFrontDoorContent.md)
移除前方門中的內容

### [Remove-AzFrontDoorRulesEngine](Remove-AzFrontDoorRulesEngine.md)
從前門移除規則引擎

### [Remove-AzFrontDoorWafPolicy](Remove-AzFrontDoorWafPolicy.md)
移除 WAF 政策

### [Set-AzFrontDoor](Set-AzFrontDoor.md)
更新前門負載平衡器

### [Set-AzFrontDoorRulesEngine](Set-AzFrontDoorRulesEngine.md)
更新規則引擎。

### [Update-AzFrontDoorWafPolicy](Update-AzFrontDoorWafPolicy.md)
更新 WAF 政策

