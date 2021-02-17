---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorManagedRuleObject.md
ms.openlocfilehash: c72573f467377a4ea16fd487a8cee5f0055a5cee
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401448"
---
# <span data-ttu-id="d5f32-101">New-AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="d5f32-101">New-AzFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="d5f32-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d5f32-102">SYNOPSIS</span></span>
<span data-ttu-id="d5f32-103">建立 ManagedRule 物件以建立 WAF 策略</span><span class="sxs-lookup"><span data-stu-id="d5f32-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="d5f32-104">語法</span><span class="sxs-lookup"><span data-stu-id="d5f32-104">SYNTAX</span></span>

```
New-AzFrontDoorManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5f32-105">描述</span><span class="sxs-lookup"><span data-stu-id="d5f32-105">DESCRIPTION</span></span>
<span data-ttu-id="d5f32-106">建立 ManagedRule 物件以建立 WAF 策略</span><span class="sxs-lookup"><span data-stu-id="d5f32-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="d5f32-107">例子</span><span class="sxs-lookup"><span data-stu-id="d5f32-107">EXAMPLES</span></span>

### <span data-ttu-id="d5f32-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="d5f32-108">Example 1</span></span>
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

<span data-ttu-id="d5f32-109">建立 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="d5f32-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="d5f32-110">參數</span><span class="sxs-lookup"><span data-stu-id="d5f32-110">PARAMETERS</span></span>

### <span data-ttu-id="d5f32-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5f32-111">-DefaultProfile</span></span>
<span data-ttu-id="d5f32-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d5f32-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5f32-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="d5f32-113">-RuleGroupOverride</span></span>
<span data-ttu-id="d5f32-114">Azure 受管理提供者的重寫群組原則清單</span><span class="sxs-lookup"><span data-stu-id="d5f32-114">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="d5f32-115">-類型</span><span class="sxs-lookup"><span data-stu-id="d5f32-115">-Type</span></span>
<span data-ttu-id="d5f32-116">規則集的類型</span><span class="sxs-lookup"><span data-stu-id="d5f32-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="d5f32-117">-版本</span><span class="sxs-lookup"><span data-stu-id="d5f32-117">-Version</span></span>
<span data-ttu-id="d5f32-118">規則集版本</span><span class="sxs-lookup"><span data-stu-id="d5f32-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="d5f32-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5f32-119">CommonParameters</span></span>
<span data-ttu-id="d5f32-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d5f32-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5f32-121">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5f32-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5f32-122">輸入</span><span class="sxs-lookup"><span data-stu-id="d5f32-122">INPUTS</span></span>

### <span data-ttu-id="d5f32-123">沒有</span><span class="sxs-lookup"><span data-stu-id="d5f32-123">None</span></span>

## <span data-ttu-id="d5f32-124">輸出</span><span class="sxs-lookup"><span data-stu-id="d5f32-124">OUTPUTS</span></span>

### <span data-ttu-id="d5f32-125">Microsoft.Azure.Commands.FrontDoor.models.PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="d5f32-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="d5f32-126">筆記</span><span class="sxs-lookup"><span data-stu-id="d5f32-126">NOTES</span></span>

## <span data-ttu-id="d5f32-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5f32-127">RELATED LINKS</span></span>

<span data-ttu-id="d5f32-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md) 
[New-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="d5f32-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorRuleGroupOverrideObject](./New-AzFrontDoorRuleGroupOverrideObject.md)</span></span>
