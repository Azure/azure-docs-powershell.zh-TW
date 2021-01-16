---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 266d553f70cb5c128df1d266f95ee93cb1eb013c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277587"
---
# <span data-ttu-id="2d873-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="2d873-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="2d873-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2d873-102">SYNOPSIS</span></span>
<span data-ttu-id="2d873-103">建立 WAF 原則建立的 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="2d873-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="2d873-104">句法</span><span class="sxs-lookup"><span data-stu-id="2d873-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d873-105">說明</span><span class="sxs-lookup"><span data-stu-id="2d873-105">DESCRIPTION</span></span>
<span data-ttu-id="2d873-106">建立 WAF 原則建立的 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="2d873-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="2d873-107">示例</span><span class="sxs-lookup"><span data-stu-id="2d873-107">EXAMPLES</span></span>

### <span data-ttu-id="2d873-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2d873-108">Example 1</span></span>
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

<span data-ttu-id="2d873-109">建立 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="2d873-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="2d873-110">參數</span><span class="sxs-lookup"><span data-stu-id="2d873-110">PARAMETERS</span></span>

### <span data-ttu-id="2d873-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d873-111">-DefaultProfile</span></span>
<span data-ttu-id="2d873-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d873-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d873-113">-排除</span><span class="sxs-lookup"><span data-stu-id="2d873-113">-Exclusion</span></span>
<span data-ttu-id="2d873-114">他</span><span class="sxs-lookup"><span data-stu-id="2d873-114">Exclusion</span></span>

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

### <span data-ttu-id="2d873-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="2d873-115">-RuleGroupOverride</span></span>
<span data-ttu-id="2d873-116">Azure managed 提供者覆蓋設定的清單</span><span class="sxs-lookup"><span data-stu-id="2d873-116">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="2d873-117">-類型</span><span class="sxs-lookup"><span data-stu-id="2d873-117">-Type</span></span>
<span data-ttu-id="2d873-118">規則集的類型</span><span class="sxs-lookup"><span data-stu-id="2d873-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="2d873-119">-版本</span><span class="sxs-lookup"><span data-stu-id="2d873-119">-Version</span></span>
<span data-ttu-id="2d873-120">版本的規則集</span><span class="sxs-lookup"><span data-stu-id="2d873-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="2d873-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d873-121">CommonParameters</span></span>
<span data-ttu-id="2d873-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2d873-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d873-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2d873-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d873-124">輸入</span><span class="sxs-lookup"><span data-stu-id="2d873-124">INPUTS</span></span>

### <span data-ttu-id="2d873-125">所有</span><span class="sxs-lookup"><span data-stu-id="2d873-125">None</span></span>

## <span data-ttu-id="2d873-126">輸出</span><span class="sxs-lookup"><span data-stu-id="2d873-126">OUTPUTS</span></span>

### <span data-ttu-id="2d873-127">PSAzureManagedRule 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="2d873-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="2d873-128">筆記</span><span class="sxs-lookup"><span data-stu-id="2d873-128">NOTES</span></span>

## <span data-ttu-id="2d873-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d873-129">RELATED LINKS</span></span>

<span data-ttu-id="2d873-130">[新-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[更新-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
[新-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="2d873-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
