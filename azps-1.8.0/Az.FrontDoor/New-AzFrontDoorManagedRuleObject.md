---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
ms.openlocfilehash: b6035e991b585ba296a9fdc591ccbdb44dd1b089
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787794"
---
# <span data-ttu-id="1d68f-101">New-AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="1d68f-101">New-AzFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="1d68f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d68f-102">SYNOPSIS</span></span>
<span data-ttu-id="1d68f-103">建立 WAF 原則建立的 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="1d68f-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="1d68f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d68f-104">SYNTAX</span></span>

```
New-AzFrontDoorManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d68f-105">說明</span><span class="sxs-lookup"><span data-stu-id="1d68f-105">DESCRIPTION</span></span>
<span data-ttu-id="1d68f-106">建立 WAF 原則建立的 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="1d68f-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="1d68f-107">示例</span><span class="sxs-lookup"><span data-stu-id="1d68f-107">EXAMPLES</span></span>

### <span data-ttu-id="1d68f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1d68f-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="1d68f-109">建立 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="1d68f-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="1d68f-110">參數</span><span class="sxs-lookup"><span data-stu-id="1d68f-110">PARAMETERS</span></span>

### <span data-ttu-id="1d68f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d68f-111">-DefaultProfile</span></span>
<span data-ttu-id="1d68f-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1d68f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d68f-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="1d68f-113">-RuleGroupOverride</span></span>
<span data-ttu-id="1d68f-114">Azure managed 提供者覆蓋設定的清單</span><span class="sxs-lookup"><span data-stu-id="1d68f-114">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="1d68f-115">-類型</span><span class="sxs-lookup"><span data-stu-id="1d68f-115">-Type</span></span>
<span data-ttu-id="1d68f-116">規則集的類型</span><span class="sxs-lookup"><span data-stu-id="1d68f-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="1d68f-117">-版本</span><span class="sxs-lookup"><span data-stu-id="1d68f-117">-Version</span></span>
<span data-ttu-id="1d68f-118">版本的規則集</span><span class="sxs-lookup"><span data-stu-id="1d68f-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="1d68f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d68f-119">CommonParameters</span></span>
<span data-ttu-id="1d68f-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1d68f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d68f-121">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1d68f-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d68f-122">輸入</span><span class="sxs-lookup"><span data-stu-id="1d68f-122">INPUTS</span></span>

### <span data-ttu-id="1d68f-123">所有</span><span class="sxs-lookup"><span data-stu-id="1d68f-123">None</span></span>

## <span data-ttu-id="1d68f-124">輸出</span><span class="sxs-lookup"><span data-stu-id="1d68f-124">OUTPUTS</span></span>

### <span data-ttu-id="1d68f-125">PSAzureManagedRule 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="1d68f-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="1d68f-126">筆記</span><span class="sxs-lookup"><span data-stu-id="1d68f-126">NOTES</span></span>

## <span data-ttu-id="1d68f-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d68f-127">RELATED LINKS</span></span>

<span data-ttu-id="1d68f-128">[新-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md) 
[新-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="1d68f-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span></span>
