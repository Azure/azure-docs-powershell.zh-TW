---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 9d05502b518dcd10a22c9583546a2d010b424902
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956650"
---
# <span data-ttu-id="a6b36-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="a6b36-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="a6b36-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6b36-102">SYNOPSIS</span></span>
<span data-ttu-id="a6b36-103">建立 WAF 原則建立的 RuleGroupOverride 物件</span><span class="sxs-lookup"><span data-stu-id="a6b36-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="a6b36-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6b36-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6b36-105">說明</span><span class="sxs-lookup"><span data-stu-id="a6b36-105">DESCRIPTION</span></span>
<span data-ttu-id="a6b36-106">建立 WAF 原則建立的 RuleGroupOverride 物件</span><span class="sxs-lookup"><span data-stu-id="a6b36-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="a6b36-107">示例</span><span class="sxs-lookup"><span data-stu-id="a6b36-107">EXAMPLES</span></span>

### <span data-ttu-id="a6b36-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a6b36-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="a6b36-109">建立 RuleGroupOverride 物件</span><span class="sxs-lookup"><span data-stu-id="a6b36-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="a6b36-110">參數</span><span class="sxs-lookup"><span data-stu-id="a6b36-110">PARAMETERS</span></span>

### <span data-ttu-id="a6b36-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6b36-111">-DefaultProfile</span></span>
<span data-ttu-id="a6b36-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6b36-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6b36-113">-排除</span><span class="sxs-lookup"><span data-stu-id="a6b36-113">-Exclusion</span></span>
<span data-ttu-id="a6b36-114">他</span><span class="sxs-lookup"><span data-stu-id="a6b36-114">Exclusion</span></span>

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

### <span data-ttu-id="a6b36-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="a6b36-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="a6b36-116">規則覆寫清單</span><span class="sxs-lookup"><span data-stu-id="a6b36-116">Rule override list</span></span>

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

### <span data-ttu-id="a6b36-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="a6b36-117">-RuleGroupName</span></span>
<span data-ttu-id="a6b36-118">這些覆蓋適用的規則組名</span><span class="sxs-lookup"><span data-stu-id="a6b36-118">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="a6b36-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6b36-119">CommonParameters</span></span>
<span data-ttu-id="a6b36-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6b36-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6b36-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a6b36-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6b36-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a6b36-122">INPUTS</span></span>

### <span data-ttu-id="a6b36-123">所有</span><span class="sxs-lookup"><span data-stu-id="a6b36-123">None</span></span>

## <span data-ttu-id="a6b36-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a6b36-124">OUTPUTS</span></span>

### <span data-ttu-id="a6b36-125">PSAzureRuleGroupOverride 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="a6b36-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="a6b36-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a6b36-126">NOTES</span></span>

## <span data-ttu-id="a6b36-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6b36-127">RELATED LINKS</span></span>

[<span data-ttu-id="a6b36-128">新-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="a6b36-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
