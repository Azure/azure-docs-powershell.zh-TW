---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 67caf6c97c493ad1d19b95ef00c896cb96a47582
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787817"
---
# <span data-ttu-id="1f4ca-101">New-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="1f4ca-101">New-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="1f4ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f4ca-102">SYNOPSIS</span></span>
<span data-ttu-id="1f4ca-103">建立 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="1f4ca-103">Create WAF policy</span></span>

## <span data-ttu-id="1f4ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f4ca-104">SYNTAX</span></span>

```
New-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f4ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="1f4ca-105">DESCRIPTION</span></span>
<span data-ttu-id="1f4ca-106">**AzFrontDoorFireWallPolicy** Cmdlet 會在指定的資源群組中，在 [目前訂閱] 底下建立新的 Azure WAF 原則</span><span class="sxs-lookup"><span data-stu-id="1f4ca-106">The **New-AzFrontDoorFireWallPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="1f4ca-107">示例</span><span class="sxs-lookup"><span data-stu-id="1f4ca-107">EXAMPLES</span></span>

### <span data-ttu-id="1f4ca-108">範例1：建立 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="1f4ca-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="1f4ca-109">建立 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="1f4ca-109">Create WAF policy</span></span>

## <span data-ttu-id="1f4ca-110">參數</span><span class="sxs-lookup"><span data-stu-id="1f4ca-110">PARAMETERS</span></span>

### <span data-ttu-id="1f4ca-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="1f4ca-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="1f4ca-112">自訂回應主體</span><span class="sxs-lookup"><span data-stu-id="1f4ca-112">Custom Response Body</span></span>

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

### <span data-ttu-id="1f4ca-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="1f4ca-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="1f4ca-114">自訂回應狀態碼</span><span class="sxs-lookup"><span data-stu-id="1f4ca-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="1f4ca-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="1f4ca-115">-Customrule</span></span>
<span data-ttu-id="1f4ca-116">原則內的自訂規則</span><span class="sxs-lookup"><span data-stu-id="1f4ca-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="1f4ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f4ca-117">-DefaultProfile</span></span>
<span data-ttu-id="1f4ca-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f4ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f4ca-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="1f4ca-119">-EnabledState</span></span>
<span data-ttu-id="1f4ca-120">原則處於 [啟用] 狀態或 [已停用] 狀態。</span><span class="sxs-lookup"><span data-stu-id="1f4ca-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="1f4ca-121">可能的值包括：「已停用」、「已啟用」</span><span class="sxs-lookup"><span data-stu-id="1f4ca-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="1f4ca-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="1f4ca-122">-ManagedRule</span></span>
<span data-ttu-id="1f4ca-123">原則中的受管理規則</span><span class="sxs-lookup"><span data-stu-id="1f4ca-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="1f4ca-124">模式</span><span class="sxs-lookup"><span data-stu-id="1f4ca-124">-Mode</span></span>
<span data-ttu-id="1f4ca-125">描述它是否在策略層級的偵測模式或預防模式中。</span><span class="sxs-lookup"><span data-stu-id="1f4ca-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="1f4ca-126">可能的值包括：「預防」、「偵測」</span><span class="sxs-lookup"><span data-stu-id="1f4ca-126">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMode
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f4ca-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f4ca-127">-Name</span></span>
<span data-ttu-id="1f4ca-128">WebApplicationFireWallPolicy [名稱]。</span><span class="sxs-lookup"><span data-stu-id="1f4ca-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="1f4ca-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="1f4ca-129">-RedirectUrl</span></span>
<span data-ttu-id="1f4ca-130">重新導向 URL</span><span class="sxs-lookup"><span data-stu-id="1f4ca-130">Redirect URL</span></span>

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

### <span data-ttu-id="1f4ca-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f4ca-131">-ResourceGroupName</span></span>
<span data-ttu-id="1f4ca-132">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="1f4ca-132">The resource group name</span></span>

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

### <span data-ttu-id="1f4ca-133">-確認</span><span class="sxs-lookup"><span data-stu-id="1f4ca-133">-Confirm</span></span>
<span data-ttu-id="1f4ca-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1f4ca-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f4ca-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f4ca-135">-WhatIf</span></span>
<span data-ttu-id="1f4ca-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f4ca-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f4ca-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f4ca-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f4ca-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f4ca-138">CommonParameters</span></span>
<span data-ttu-id="1f4ca-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f4ca-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f4ca-140">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1f4ca-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f4ca-141">輸入</span><span class="sxs-lookup"><span data-stu-id="1f4ca-141">INPUTS</span></span>

### <span data-ttu-id="1f4ca-142">所有</span><span class="sxs-lookup"><span data-stu-id="1f4ca-142">None</span></span>

## <span data-ttu-id="1f4ca-143">輸出</span><span class="sxs-lookup"><span data-stu-id="1f4ca-143">OUTPUTS</span></span>

### <span data-ttu-id="1f4ca-144">PSPolicy 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="1f4ca-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="1f4ca-145">筆記</span><span class="sxs-lookup"><span data-stu-id="1f4ca-145">NOTES</span></span>

## <span data-ttu-id="1f4ca-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f4ca-146">RELATED LINKS</span></span>

<span data-ttu-id="1f4ca-147">[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md) 
[AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md) 
[移除-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md) 
[新-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md) 
[新-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="1f4ca-147">[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)
[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md)
[New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span></span>
