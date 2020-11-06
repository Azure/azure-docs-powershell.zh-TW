---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: bde2d2edd48edf83efaf7f548daf4f97d6cffbaa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612353"
---
# <span data-ttu-id="dba9a-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="dba9a-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="dba9a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dba9a-102">SYNOPSIS</span></span>
<span data-ttu-id="dba9a-103">建立 WAF 原則建立的 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="dba9a-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="dba9a-104">句法</span><span class="sxs-lookup"><span data-stu-id="dba9a-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dba9a-105">說明</span><span class="sxs-lookup"><span data-stu-id="dba9a-105">DESCRIPTION</span></span>
<span data-ttu-id="dba9a-106">建立 WAF 原則建立的 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="dba9a-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="dba9a-107">示例</span><span class="sxs-lookup"><span data-stu-id="dba9a-107">EXAMPLES</span></span>

### <span data-ttu-id="dba9a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="dba9a-108">Example 1</span></span>
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

<span data-ttu-id="dba9a-109">建立 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="dba9a-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="dba9a-110">參數</span><span class="sxs-lookup"><span data-stu-id="dba9a-110">PARAMETERS</span></span>

### <span data-ttu-id="dba9a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba9a-111">-DefaultProfile</span></span>
<span data-ttu-id="dba9a-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dba9a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dba9a-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="dba9a-113">-RuleGroupOverride</span></span>
<span data-ttu-id="dba9a-114">Azure managed 提供者覆蓋設定的清單</span><span class="sxs-lookup"><span data-stu-id="dba9a-114">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="dba9a-115">-類型</span><span class="sxs-lookup"><span data-stu-id="dba9a-115">-Type</span></span>
<span data-ttu-id="dba9a-116">規則集的類型</span><span class="sxs-lookup"><span data-stu-id="dba9a-116">Type of the ruleset</span></span>

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

### <span data-ttu-id="dba9a-117">-版本</span><span class="sxs-lookup"><span data-stu-id="dba9a-117">-Version</span></span>
<span data-ttu-id="dba9a-118">版本的規則集</span><span class="sxs-lookup"><span data-stu-id="dba9a-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="dba9a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba9a-119">CommonParameters</span></span>
<span data-ttu-id="dba9a-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dba9a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba9a-121">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dba9a-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba9a-122">輸入</span><span class="sxs-lookup"><span data-stu-id="dba9a-122">INPUTS</span></span>

### <span data-ttu-id="dba9a-123">所有</span><span class="sxs-lookup"><span data-stu-id="dba9a-123">None</span></span>

## <span data-ttu-id="dba9a-124">輸出</span><span class="sxs-lookup"><span data-stu-id="dba9a-124">OUTPUTS</span></span>

### <span data-ttu-id="dba9a-125">PSAzureManagedRule 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="dba9a-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="dba9a-126">筆記</span><span class="sxs-lookup"><span data-stu-id="dba9a-126">NOTES</span></span>

## <span data-ttu-id="dba9a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="dba9a-127">RELATED LINKS</span></span>

<span data-ttu-id="dba9a-128">[新-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md) 
[新-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="dba9a-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
