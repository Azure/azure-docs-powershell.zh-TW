---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: cafb705ec5f2882eb239931b22ccfba610721100
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957103"
---
# <span data-ttu-id="34efa-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="34efa-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="34efa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="34efa-102">SYNOPSIS</span></span>
<span data-ttu-id="34efa-103">更新 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="34efa-103">Update WAF policy</span></span>

## <span data-ttu-id="34efa-104">句法</span><span class="sxs-lookup"><span data-stu-id="34efa-104">SYNTAX</span></span>

### <span data-ttu-id="34efa-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="34efa-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34efa-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34efa-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34efa-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34efa-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34efa-108">說明</span><span class="sxs-lookup"><span data-stu-id="34efa-108">DESCRIPTION</span></span>
<span data-ttu-id="34efa-109">**AzFrontDoorWafPolicy** Cmdlet 會更新現有的 WAF 原則。</span><span class="sxs-lookup"><span data-stu-id="34efa-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="34efa-110">如果未提供輸入參數，則會使用來自現有 WAF 原則的舊參數。</span><span class="sxs-lookup"><span data-stu-id="34efa-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="34efa-111">示例</span><span class="sxs-lookup"><span data-stu-id="34efa-111">EXAMPLES</span></span>

### <span data-ttu-id="34efa-112">範例1</span><span class="sxs-lookup"><span data-stu-id="34efa-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="34efa-113">更新現有的 WAF 原則自訂狀態碼。</span><span class="sxs-lookup"><span data-stu-id="34efa-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="34efa-114">範例2</span><span class="sxs-lookup"><span data-stu-id="34efa-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="34efa-115">更新現有的 WAF 原則模式。</span><span class="sxs-lookup"><span data-stu-id="34efa-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="34efa-116">範例3</span><span class="sxs-lookup"><span data-stu-id="34efa-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="34efa-117">更新現有的 WAF 原則啟用狀態和模式。</span><span class="sxs-lookup"><span data-stu-id="34efa-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="34efa-118">範例4</span><span class="sxs-lookup"><span data-stu-id="34efa-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="34efa-119">更新 $resourceGroupName 中的所有 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="34efa-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="34efa-120">參數</span><span class="sxs-lookup"><span data-stu-id="34efa-120">PARAMETERS</span></span>

### <span data-ttu-id="34efa-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="34efa-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="34efa-122">自訂回應主體</span><span class="sxs-lookup"><span data-stu-id="34efa-122">Custom Response Body</span></span>

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

### <span data-ttu-id="34efa-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="34efa-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="34efa-124">自訂回應狀態碼</span><span class="sxs-lookup"><span data-stu-id="34efa-124">Custom Response Status Code</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34efa-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="34efa-125">-Customrule</span></span>
<span data-ttu-id="34efa-126">原則內的自訂規則</span><span class="sxs-lookup"><span data-stu-id="34efa-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="34efa-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34efa-127">-DefaultProfile</span></span>
<span data-ttu-id="34efa-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="34efa-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34efa-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="34efa-129">-EnabledState</span></span>
<span data-ttu-id="34efa-130">原則處於 [啟用] 狀態或 [已停用] 狀態。</span><span class="sxs-lookup"><span data-stu-id="34efa-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="34efa-131">可能的值包括：「已停用」、「已啟用」</span><span class="sxs-lookup"><span data-stu-id="34efa-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="34efa-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34efa-132">-InputObject</span></span>
<span data-ttu-id="34efa-133">要更新的 FireWallPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="34efa-133">The FireWallPolicy object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34efa-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="34efa-134">-ManagedRule</span></span>
<span data-ttu-id="34efa-135">原則中的受管理規則</span><span class="sxs-lookup"><span data-stu-id="34efa-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="34efa-136">模式</span><span class="sxs-lookup"><span data-stu-id="34efa-136">-Mode</span></span>
<span data-ttu-id="34efa-137">描述它是否在策略層級的偵測模式或預防模式中。</span><span class="sxs-lookup"><span data-stu-id="34efa-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="34efa-138">可能的值包括：「預防」、「偵測」</span><span class="sxs-lookup"><span data-stu-id="34efa-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="34efa-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="34efa-139">-Name</span></span>
<span data-ttu-id="34efa-140">要更新之 FireWallPolicy 的名稱。</span><span class="sxs-lookup"><span data-stu-id="34efa-140">The name of the FireWallPolicy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34efa-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="34efa-141">-RedirectUrl</span></span>
<span data-ttu-id="34efa-142">重新導向 URL</span><span class="sxs-lookup"><span data-stu-id="34efa-142">Redirect URL</span></span>

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

### <span data-ttu-id="34efa-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34efa-143">-ResourceGroupName</span></span>
<span data-ttu-id="34efa-144">FireWallPolicy 所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="34efa-144">The resource group to which the FireWallPolicy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34efa-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34efa-145">-ResourceId</span></span>
<span data-ttu-id="34efa-146">要更新之 FireWallPolicy 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="34efa-146">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34efa-147">-確認</span><span class="sxs-lookup"><span data-stu-id="34efa-147">-Confirm</span></span>
<span data-ttu-id="34efa-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="34efa-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34efa-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34efa-149">-WhatIf</span></span>
<span data-ttu-id="34efa-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="34efa-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34efa-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="34efa-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34efa-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34efa-152">CommonParameters</span></span>
<span data-ttu-id="34efa-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="34efa-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34efa-154">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="34efa-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34efa-155">輸入</span><span class="sxs-lookup"><span data-stu-id="34efa-155">INPUTS</span></span>

### <span data-ttu-id="34efa-156">PSPolicy 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="34efa-156">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="34efa-157">System.object</span><span class="sxs-lookup"><span data-stu-id="34efa-157">System.String</span></span>

## <span data-ttu-id="34efa-158">輸出</span><span class="sxs-lookup"><span data-stu-id="34efa-158">OUTPUTS</span></span>

### <span data-ttu-id="34efa-159">PSPolicy 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="34efa-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="34efa-160">筆記</span><span class="sxs-lookup"><span data-stu-id="34efa-160">NOTES</span></span>

## <span data-ttu-id="34efa-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="34efa-161">RELATED LINKS</span></span>

<span data-ttu-id="34efa-162">[新-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
[新-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
[新-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="34efa-162">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
