---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 2d3811b5605b6f4923abd58c64d8d870ede8d334
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403845"
---
# <span data-ttu-id="0a07c-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="0a07c-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="0a07c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0a07c-102">SYNOPSIS</span></span>
<span data-ttu-id="0a07c-103">建立 WAF 政策</span><span class="sxs-lookup"><span data-stu-id="0a07c-103">Create WAF policy</span></span>

## <span data-ttu-id="0a07c-104">語法</span><span class="sxs-lookup"><span data-stu-id="0a07c-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a07c-105">描述</span><span class="sxs-lookup"><span data-stu-id="0a07c-105">DESCRIPTION</span></span>
<span data-ttu-id="0a07c-106">**New-AzFrontDoorWafPolicy** Cmdlet 會在目前訂閱下的指定資源群組中建立新的 Azure WAF 策略</span><span class="sxs-lookup"><span data-stu-id="0a07c-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="0a07c-107">例子</span><span class="sxs-lookup"><span data-stu-id="0a07c-107">EXAMPLES</span></span>

### <span data-ttu-id="0a07c-108">範例 1：建立 WAF 策略</span><span class="sxs-lookup"><span data-stu-id="0a07c-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="0a07c-109">建立 WAF 政策</span><span class="sxs-lookup"><span data-stu-id="0a07c-109">Create WAF policy</span></span>

## <span data-ttu-id="0a07c-110">參數</span><span class="sxs-lookup"><span data-stu-id="0a07c-110">PARAMETERS</span></span>

### <span data-ttu-id="0a07c-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="0a07c-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="0a07c-112">自訂回應內體</span><span class="sxs-lookup"><span data-stu-id="0a07c-112">Custom Response Body</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a07c-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="0a07c-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="0a07c-114">自訂回應狀態碼</span><span class="sxs-lookup"><span data-stu-id="0a07c-114">Custom Response Status Code</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a07c-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="0a07c-115">-Customrule</span></span>
<span data-ttu-id="0a07c-116">原則內的自訂規則</span><span class="sxs-lookup"><span data-stu-id="0a07c-116">Custom rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a07c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a07c-117">-DefaultProfile</span></span>
<span data-ttu-id="0a07c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a07c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a07c-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="0a07c-119">-EnabledState</span></span>
<span data-ttu-id="0a07c-120">該策略處於啟用狀態或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="0a07c-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="0a07c-121">可能的值包括：'Disabled'， 'Enabled'</span><span class="sxs-lookup"><span data-stu-id="0a07c-121">Possible values include: 'Disabled', 'Enabled'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a07c-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="0a07c-122">-ManagedRule</span></span>
<span data-ttu-id="0a07c-123">原則內的受管理規則</span><span class="sxs-lookup"><span data-stu-id="0a07c-123">Managed rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a07c-124">-模式</span><span class="sxs-lookup"><span data-stu-id="0a07c-124">-Mode</span></span>
<span data-ttu-id="0a07c-125">說明它處於偵測模式或策略層級的防護模式。</span><span class="sxs-lookup"><span data-stu-id="0a07c-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="0a07c-126">可能的值包括：'Prevention'， 'Detection'</span><span class="sxs-lookup"><span data-stu-id="0a07c-126">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a07c-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a07c-127">-Name</span></span>
<span data-ttu-id="0a07c-128">WebApplicationFireWallPolicy 名稱。</span><span class="sxs-lookup"><span data-stu-id="0a07c-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="0a07c-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="0a07c-129">-RedirectUrl</span></span>
<span data-ttu-id="0a07c-130">重新導向 URL</span><span class="sxs-lookup"><span data-stu-id="0a07c-130">Redirect URL</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a07c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a07c-131">-ResourceGroupName</span></span>
<span data-ttu-id="0a07c-132">資源組名</span><span class="sxs-lookup"><span data-stu-id="0a07c-132">The resource group name</span></span>

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

### <span data-ttu-id="0a07c-133">-確認</span><span class="sxs-lookup"><span data-stu-id="0a07c-133">-Confirm</span></span>
<span data-ttu-id="0a07c-134">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0a07c-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a07c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a07c-135">-WhatIf</span></span>
<span data-ttu-id="0a07c-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a07c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a07c-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a07c-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a07c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a07c-138">CommonParameters</span></span>
<span data-ttu-id="0a07c-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0a07c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a07c-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a07c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a07c-141">輸入</span><span class="sxs-lookup"><span data-stu-id="0a07c-141">INPUTS</span></span>

### <span data-ttu-id="0a07c-142">沒有</span><span class="sxs-lookup"><span data-stu-id="0a07c-142">None</span></span>

## <span data-ttu-id="0a07c-143">輸出</span><span class="sxs-lookup"><span data-stu-id="0a07c-143">OUTPUTS</span></span>

### <span data-ttu-id="0a07c-144">Microsoft.Azure.Commands.FrontDoor.models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="0a07c-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="0a07c-145">筆記</span><span class="sxs-lookup"><span data-stu-id="0a07c-145">NOTES</span></span>

## <span data-ttu-id="0a07c-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a07c-146">RELATED LINKS</span></span>

<span data-ttu-id="0a07c-147">[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="0a07c-147">[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
