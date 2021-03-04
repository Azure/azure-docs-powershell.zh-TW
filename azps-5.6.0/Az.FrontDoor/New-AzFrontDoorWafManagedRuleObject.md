---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: f31b7c995c66e2b187038c45d9955a31f904764b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906641"
---
# <span data-ttu-id="24bf6-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="24bf6-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="24bf6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="24bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="24bf6-103">建立 ManagedRule 物件以建立 WAF 策略</span><span class="sxs-lookup"><span data-stu-id="24bf6-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="24bf6-104">語法</span><span class="sxs-lookup"><span data-stu-id="24bf6-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24bf6-105">描述</span><span class="sxs-lookup"><span data-stu-id="24bf6-105">DESCRIPTION</span></span>
<span data-ttu-id="24bf6-106">建立 ManagedRule 物件以建立 WAF 策略</span><span class="sxs-lookup"><span data-stu-id="24bf6-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="24bf6-107">例子</span><span class="sxs-lookup"><span data-stu-id="24bf6-107">EXAMPLES</span></span>

### <span data-ttu-id="24bf6-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="24bf6-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="24bf6-109">建立 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="24bf6-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="24bf6-110">參數</span><span class="sxs-lookup"><span data-stu-id="24bf6-110">PARAMETERS</span></span>

### <span data-ttu-id="24bf6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24bf6-111">-DefaultProfile</span></span>
<span data-ttu-id="24bf6-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="24bf6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24bf6-113">-排除</span><span class="sxs-lookup"><span data-stu-id="24bf6-113">-Exclusion</span></span>
<span data-ttu-id="24bf6-114">排除</span><span class="sxs-lookup"><span data-stu-id="24bf6-114">Exclusion</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf6-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="24bf6-115">-RuleGroupOverride</span></span>
<span data-ttu-id="24bf6-116">Azure 受管理提供者的重寫群組原則清單</span><span class="sxs-lookup"><span data-stu-id="24bf6-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf6-117">-類型</span><span class="sxs-lookup"><span data-stu-id="24bf6-117">-Type</span></span>
<span data-ttu-id="24bf6-118">規則集的類型</span><span class="sxs-lookup"><span data-stu-id="24bf6-118">Type of the ruleset</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf6-119">-版本</span><span class="sxs-lookup"><span data-stu-id="24bf6-119">-Version</span></span>
<span data-ttu-id="24bf6-120">規則集版本</span><span class="sxs-lookup"><span data-stu-id="24bf6-120">Version of the ruleset</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bf6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24bf6-121">CommonParameters</span></span>
<span data-ttu-id="24bf6-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="24bf6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24bf6-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24bf6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24bf6-124">輸入</span><span class="sxs-lookup"><span data-stu-id="24bf6-124">INPUTS</span></span>

### <span data-ttu-id="24bf6-125">沒有</span><span class="sxs-lookup"><span data-stu-id="24bf6-125">None</span></span>

## <span data-ttu-id="24bf6-126">輸出</span><span class="sxs-lookup"><span data-stu-id="24bf6-126">OUTPUTS</span></span>

### <span data-ttu-id="24bf6-127">Microsoft.Azure.Commands.FrontDoor.models.PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="24bf6-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="24bf6-128">筆記</span><span class="sxs-lookup"><span data-stu-id="24bf6-128">NOTES</span></span>

## <span data-ttu-id="24bf6-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="24bf6-129">RELATED LINKS</span></span>

<span data-ttu-id="24bf6-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="24bf6-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
