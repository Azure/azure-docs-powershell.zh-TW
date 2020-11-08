---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: d93431066acd3747d6c7dcbea2eae7cd259ee21b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140502"
---
# <span data-ttu-id="7f516-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="7f516-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="7f516-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f516-102">SYNOPSIS</span></span>
<span data-ttu-id="7f516-103">取得 WAF managed 規則集定義</span><span class="sxs-lookup"><span data-stu-id="7f516-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="7f516-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f516-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f516-105">說明</span><span class="sxs-lookup"><span data-stu-id="7f516-105">DESCRIPTION</span></span>
<span data-ttu-id="7f516-106">取得 WAF managed 規則集定義的清單，以供參考</span><span class="sxs-lookup"><span data-stu-id="7f516-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="7f516-107">示例</span><span class="sxs-lookup"><span data-stu-id="7f516-107">EXAMPLES</span></span>

### <span data-ttu-id="7f516-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7f516-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="7f516-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="7f516-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="7f516-110">參數</span><span class="sxs-lookup"><span data-stu-id="7f516-110">PARAMETERS</span></span>

### <span data-ttu-id="7f516-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f516-111">-DefaultProfile</span></span>
<span data-ttu-id="7f516-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f516-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f516-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f516-113">CommonParameters</span></span>
<span data-ttu-id="7f516-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f516-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f516-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7f516-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f516-116">輸入</span><span class="sxs-lookup"><span data-stu-id="7f516-116">INPUTS</span></span>

### <span data-ttu-id="7f516-117">所有</span><span class="sxs-lookup"><span data-stu-id="7f516-117">None</span></span>

## <span data-ttu-id="7f516-118">輸出</span><span class="sxs-lookup"><span data-stu-id="7f516-118">OUTPUTS</span></span>

### <span data-ttu-id="7f516-119">PSManagedRuleSetDefinition 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="7f516-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="7f516-120">筆記</span><span class="sxs-lookup"><span data-stu-id="7f516-120">NOTES</span></span>

## <span data-ttu-id="7f516-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f516-121">RELATED LINKS</span></span>

<span data-ttu-id="7f516-122">[新-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
[新-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
[新-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="7f516-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
