---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 5c39a86b29ce27ea57d51e7e3bfb048560ef1ee6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906630"
---
# <span data-ttu-id="ab0ca-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="ab0ca-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="ab0ca-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ab0ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ab0ca-103">建立 WAF 政策</span><span class="sxs-lookup"><span data-stu-id="ab0ca-103">Create WAF policy</span></span>

## <span data-ttu-id="ab0ca-104">語法</span><span class="sxs-lookup"><span data-stu-id="ab0ca-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab0ca-105">描述</span><span class="sxs-lookup"><span data-stu-id="ab0ca-105">DESCRIPTION</span></span>
<span data-ttu-id="ab0ca-106">**New-AzFrontDoorWafPolicy** Cmdlet 會在目前訂閱下的指定資源群組中建立新的 Azure WAF 策略</span><span class="sxs-lookup"><span data-stu-id="ab0ca-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="ab0ca-107">例子</span><span class="sxs-lookup"><span data-stu-id="ab0ca-107">EXAMPLES</span></span>

### <span data-ttu-id="ab0ca-108">範例 1：建立 WAF 策略</span><span class="sxs-lookup"><span data-stu-id="ab0ca-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="ab0ca-109">建立 WAF 政策</span><span class="sxs-lookup"><span data-stu-id="ab0ca-109">Create WAF policy</span></span>

## <span data-ttu-id="ab0ca-110">參數</span><span class="sxs-lookup"><span data-stu-id="ab0ca-110">PARAMETERS</span></span>

### <span data-ttu-id="ab0ca-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="ab0ca-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="ab0ca-112">自訂回應內體</span><span class="sxs-lookup"><span data-stu-id="ab0ca-112">Custom Response Body</span></span>

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

### <span data-ttu-id="ab0ca-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="ab0ca-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="ab0ca-114">自訂回應狀態碼</span><span class="sxs-lookup"><span data-stu-id="ab0ca-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="ab0ca-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="ab0ca-115">-Customrule</span></span>
<span data-ttu-id="ab0ca-116">原則內的自訂規則</span><span class="sxs-lookup"><span data-stu-id="ab0ca-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="ab0ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab0ca-117">-DefaultProfile</span></span>
<span data-ttu-id="ab0ca-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab0ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab0ca-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="ab0ca-119">-EnabledState</span></span>
<span data-ttu-id="ab0ca-120">該策略處於啟用狀態或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="ab0ca-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="ab0ca-121">可能的值包括：'已停用'、'Enabled'</span><span class="sxs-lookup"><span data-stu-id="ab0ca-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="ab0ca-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="ab0ca-122">-ManagedRule</span></span>
<span data-ttu-id="ab0ca-123">原則內的受管理規則</span><span class="sxs-lookup"><span data-stu-id="ab0ca-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="ab0ca-124">-模式</span><span class="sxs-lookup"><span data-stu-id="ab0ca-124">-Mode</span></span>
<span data-ttu-id="ab0ca-125">說明它處於偵測模式或策略層級的防護模式。</span><span class="sxs-lookup"><span data-stu-id="ab0ca-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="ab0ca-126">可能的值包括：'Prevention'， 'Detection'</span><span class="sxs-lookup"><span data-stu-id="ab0ca-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="ab0ca-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab0ca-127">-Name</span></span>
<span data-ttu-id="ab0ca-128">WebApplicationFireWallPolicy 名稱。</span><span class="sxs-lookup"><span data-stu-id="ab0ca-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="ab0ca-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="ab0ca-129">-RedirectUrl</span></span>
<span data-ttu-id="ab0ca-130">重新導向 URL</span><span class="sxs-lookup"><span data-stu-id="ab0ca-130">Redirect URL</span></span>

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

### <span data-ttu-id="ab0ca-131">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="ab0ca-131">-RequestBodyCheck</span></span>
<span data-ttu-id="ab0ca-132">定義是否由受管理規則檢查本體。</span><span class="sxs-lookup"><span data-stu-id="ab0ca-132">Defines if the body should be inspected by managed rules.</span></span> <span data-ttu-id="ab0ca-133">可能的值包括：'Enabled'， 'Disabled'</span><span class="sxs-lookup"><span data-stu-id="ab0ca-133">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="ab0ca-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab0ca-134">-ResourceGroupName</span></span>
<span data-ttu-id="ab0ca-135">資源組名</span><span class="sxs-lookup"><span data-stu-id="ab0ca-135">The resource group name</span></span>

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

### <span data-ttu-id="ab0ca-136">-確認</span><span class="sxs-lookup"><span data-stu-id="ab0ca-136">-Confirm</span></span>
<span data-ttu-id="ab0ca-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ab0ca-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab0ca-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab0ca-138">-WhatIf</span></span>
<span data-ttu-id="ab0ca-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ab0ca-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab0ca-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab0ca-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab0ca-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab0ca-141">CommonParameters</span></span>
<span data-ttu-id="ab0ca-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ab0ca-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab0ca-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab0ca-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab0ca-144">輸入</span><span class="sxs-lookup"><span data-stu-id="ab0ca-144">INPUTS</span></span>

### <span data-ttu-id="ab0ca-145">沒有</span><span class="sxs-lookup"><span data-stu-id="ab0ca-145">None</span></span>

## <span data-ttu-id="ab0ca-146">輸出</span><span class="sxs-lookup"><span data-stu-id="ab0ca-146">OUTPUTS</span></span>

### <span data-ttu-id="ab0ca-147">Microsoft.Azure.Commands.FrontDoor.models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="ab0ca-147">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="ab0ca-148">筆記</span><span class="sxs-lookup"><span data-stu-id="ab0ca-148">NOTES</span></span>

## <span data-ttu-id="ab0ca-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab0ca-149">RELATED LINKS</span></span>

<span data-ttu-id="ab0ca-150">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="ab0ca-150">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
