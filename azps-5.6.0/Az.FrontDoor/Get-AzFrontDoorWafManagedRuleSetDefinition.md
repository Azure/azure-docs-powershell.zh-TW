---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoorwafmanagedrulesetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafManagedRuleSetDefinition.md
ms.openlocfilehash: 28c4278f86600b53b64d3a0ea2d0b4896f8227bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902597"
---
# <span data-ttu-id="f919e-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="f919e-101">Get-AzFrontDoorWafManagedRuleSetDefinition</span></span>

## <span data-ttu-id="f919e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f919e-102">SYNOPSIS</span></span>
<span data-ttu-id="f919e-103">取得 WAF 受管理的規則集定義</span><span class="sxs-lookup"><span data-stu-id="f919e-103">Get WAF managed rule set definitions</span></span>

## <span data-ttu-id="f919e-104">語法</span><span class="sxs-lookup"><span data-stu-id="f919e-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafManagedRuleSetDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f919e-105">描述</span><span class="sxs-lookup"><span data-stu-id="f919e-105">DESCRIPTION</span></span>
<span data-ttu-id="f919e-106">獲得 WAF 受管理規則集定義清單以做為參照</span><span class="sxs-lookup"><span data-stu-id="f919e-106">Gets the list of WAF managed rule set definitions to use as reference</span></span>

## <span data-ttu-id="f919e-107">例子</span><span class="sxs-lookup"><span data-stu-id="f919e-107">EXAMPLES</span></span>

### <span data-ttu-id="f919e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f919e-108">Example 1</span></span>
```powershell
PS C:> Get-AzFrontDoorWafManagedRuleSetDefinition

ProvisioningState RuleSetType                 RuleSetVersion RuleGroups
----------------- -----------                 -------------- ----------
Succeeded         DefaultRuleSet              1.0            {PROTOCOL-ATTACK, LFI, RFI, RCE...}
Succeeded         Microsoft_BotManagerRuleSet 1.0            {BadBots, GoodBots, UnknownBots}
Succeeded         DefaultRuleSet              preview-0.1    {LFI, RFI, RCE, PHP...}
Succeeded         BotProtection               preview-0.1    {KnownBadBots}
```

<span data-ttu-id="f919e-109">{{ 在這裡新增範例描述 }}</span><span class="sxs-lookup"><span data-stu-id="f919e-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="f919e-110">參數</span><span class="sxs-lookup"><span data-stu-id="f919e-110">PARAMETERS</span></span>

### <span data-ttu-id="f919e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f919e-111">-DefaultProfile</span></span>
<span data-ttu-id="f919e-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f919e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f919e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f919e-113">CommonParameters</span></span>
<span data-ttu-id="f919e-114">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f919e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f919e-115">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f919e-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f919e-116">輸入</span><span class="sxs-lookup"><span data-stu-id="f919e-116">INPUTS</span></span>

### <span data-ttu-id="f919e-117">沒有</span><span class="sxs-lookup"><span data-stu-id="f919e-117">None</span></span>

## <span data-ttu-id="f919e-118">輸出</span><span class="sxs-lookup"><span data-stu-id="f919e-118">OUTPUTS</span></span>

### <span data-ttu-id="f919e-119">Microsoft.Azure.Commands.FrontDoor.models.PSManagedRuleSetDefinition</span><span class="sxs-lookup"><span data-stu-id="f919e-119">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleSetDefinition</span></span>

## <span data-ttu-id="f919e-120">筆記</span><span class="sxs-lookup"><span data-stu-id="f919e-120">NOTES</span></span>

## <span data-ttu-id="f919e-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="f919e-121">RELATED LINKS</span></span>

<span data-ttu-id="f919e-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="f919e-122">[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
