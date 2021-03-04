---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 5d8e872ea2ca47169c727a29c1847a83b5a6542b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917742"
---
# <span data-ttu-id="bf726-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="bf726-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="bf726-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bf726-102">SYNOPSIS</span></span>
<span data-ttu-id="bf726-103">建立 RuleGroupOverride 物件以建立 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="bf726-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="bf726-104">語法</span><span class="sxs-lookup"><span data-stu-id="bf726-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf726-105">描述</span><span class="sxs-lookup"><span data-stu-id="bf726-105">DESCRIPTION</span></span>
<span data-ttu-id="bf726-106">建立 RuleGroupOverride 物件以建立 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="bf726-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="bf726-107">例子</span><span class="sxs-lookup"><span data-stu-id="bf726-107">EXAMPLES</span></span>

### <span data-ttu-id="bf726-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="bf726-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="bf726-109">建立 RuleGroupOverride 物件</span><span class="sxs-lookup"><span data-stu-id="bf726-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="bf726-110">參數</span><span class="sxs-lookup"><span data-stu-id="bf726-110">PARAMETERS</span></span>

### <span data-ttu-id="bf726-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf726-111">-DefaultProfile</span></span>
<span data-ttu-id="bf726-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf726-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf726-113">-排除</span><span class="sxs-lookup"><span data-stu-id="bf726-113">-Exclusion</span></span>
<span data-ttu-id="bf726-114">排除</span><span class="sxs-lookup"><span data-stu-id="bf726-114">Exclusion</span></span>

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

### <span data-ttu-id="bf726-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="bf726-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="bf726-116">規則重寫清單</span><span class="sxs-lookup"><span data-stu-id="bf726-116">Rule override list</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf726-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="bf726-117">-RuleGroupName</span></span>
<span data-ttu-id="bf726-118">適用于這些替代的規則組名</span><span class="sxs-lookup"><span data-stu-id="bf726-118">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="bf726-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf726-119">CommonParameters</span></span>
<span data-ttu-id="bf726-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bf726-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf726-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf726-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf726-122">輸入</span><span class="sxs-lookup"><span data-stu-id="bf726-122">INPUTS</span></span>

### <span data-ttu-id="bf726-123">沒有</span><span class="sxs-lookup"><span data-stu-id="bf726-123">None</span></span>

## <span data-ttu-id="bf726-124">輸出</span><span class="sxs-lookup"><span data-stu-id="bf726-124">OUTPUTS</span></span>

### <span data-ttu-id="bf726-125">Microsoft.Azure.Commands.FrontDoor.models.PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="bf726-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="bf726-126">筆記</span><span class="sxs-lookup"><span data-stu-id="bf726-126">NOTES</span></span>

## <span data-ttu-id="bf726-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf726-127">RELATED LINKS</span></span>

[<span data-ttu-id="bf726-128">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="bf726-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
