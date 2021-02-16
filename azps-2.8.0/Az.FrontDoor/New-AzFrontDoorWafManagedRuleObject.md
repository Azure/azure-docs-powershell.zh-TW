---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 44fe7da11f3a06d7938f084b0edf6a6a39bb30f5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412753"
---
# <span data-ttu-id="b0194-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="b0194-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="b0194-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b0194-102">SYNOPSIS</span></span>
<span data-ttu-id="b0194-103">建立 ManagedRule 物件以建立 WAF 策略</span><span class="sxs-lookup"><span data-stu-id="b0194-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="b0194-104">語法</span><span class="sxs-lookup"><span data-stu-id="b0194-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0194-105">描述</span><span class="sxs-lookup"><span data-stu-id="b0194-105">DESCRIPTION</span></span>
<span data-ttu-id="b0194-106">建立 ManagedRule 物件以建立 WAF 策略</span><span class="sxs-lookup"><span data-stu-id="b0194-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="b0194-107">例子</span><span class="sxs-lookup"><span data-stu-id="b0194-107">EXAMPLES</span></span>

### <span data-ttu-id="b0194-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="b0194-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="b0194-109">建立 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="b0194-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="b0194-110">參數</span><span class="sxs-lookup"><span data-stu-id="b0194-110">PARAMETERS</span></span>

### <span data-ttu-id="b0194-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0194-111">-DefaultProfile</span></span>
<span data-ttu-id="b0194-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0194-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0194-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="b0194-113">-RuleGroupOverride</span></span>
<span data-ttu-id="b0194-114">Azure 受管理提供者的重寫群組原則清單</span><span class="sxs-lookup"><span data-stu-id="b0194-114">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="b0194-115">-類型</span><span class="sxs-lookup"><span data-stu-id="b0194-115">-Type</span></span>
<span data-ttu-id="b0194-116">規則集的類型</span><span class="sxs-lookup"><span data-stu-id="b0194-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="b0194-117">-版本</span><span class="sxs-lookup"><span data-stu-id="b0194-117">-Version</span></span>
<span data-ttu-id="b0194-118">規則集版本</span><span class="sxs-lookup"><span data-stu-id="b0194-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="b0194-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0194-119">CommonParameters</span></span>
<span data-ttu-id="b0194-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b0194-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0194-121">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0194-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0194-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b0194-122">INPUTS</span></span>

### <span data-ttu-id="b0194-123">沒有</span><span class="sxs-lookup"><span data-stu-id="b0194-123">None</span></span>

## <span data-ttu-id="b0194-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b0194-124">OUTPUTS</span></span>

### <span data-ttu-id="b0194-125">Microsoft.Azure.Commands.FrontDoor.models.PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="b0194-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="b0194-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b0194-126">NOTES</span></span>

## <span data-ttu-id="b0194-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0194-127">RELATED LINKS</span></span>

<span data-ttu-id="b0194-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="b0194-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
