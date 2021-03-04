---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: bc4aa72d202938b5727245386f3485fbc43a6ab5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906201"
---
# <span data-ttu-id="d9703-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="d9703-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="d9703-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d9703-102">SYNOPSIS</span></span>
<span data-ttu-id="d9703-103">更新 WAF 政策</span><span class="sxs-lookup"><span data-stu-id="d9703-103">Update WAF policy</span></span>

## <span data-ttu-id="d9703-104">語法</span><span class="sxs-lookup"><span data-stu-id="d9703-104">SYNTAX</span></span>

### <span data-ttu-id="d9703-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d9703-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9703-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9703-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9703-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9703-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9703-108">描述</span><span class="sxs-lookup"><span data-stu-id="d9703-108">DESCRIPTION</span></span>
<span data-ttu-id="d9703-109">**Update-AzFrontDoorWafPolicy** Cmdlet 會更新現有的 WAF 策略。</span><span class="sxs-lookup"><span data-stu-id="d9703-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="d9703-110">如果沒有提供輸入參數，將會使用來自現有 WAF 策略的舊參數。</span><span class="sxs-lookup"><span data-stu-id="d9703-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="d9703-111">例子</span><span class="sxs-lookup"><span data-stu-id="d9703-111">EXAMPLES</span></span>

### <span data-ttu-id="d9703-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="d9703-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="d9703-113">更新現有的 WAF 策略自訂狀態碼。</span><span class="sxs-lookup"><span data-stu-id="d9703-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="d9703-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="d9703-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="d9703-115">更新現有的 WAF 策略模式。</span><span class="sxs-lookup"><span data-stu-id="d9703-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="d9703-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="d9703-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="d9703-117">更新已啟用 WAF 策略的現有狀態和模式。</span><span class="sxs-lookup"><span data-stu-id="d9703-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="d9703-118">範例 4</span><span class="sxs-lookup"><span data-stu-id="d9703-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="d9703-119">更新所有 WAF $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9703-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="d9703-120">參數</span><span class="sxs-lookup"><span data-stu-id="d9703-120">PARAMETERS</span></span>

### <span data-ttu-id="d9703-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="d9703-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="d9703-122">自訂回應內體</span><span class="sxs-lookup"><span data-stu-id="d9703-122">Custom Response Body</span></span>

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

### <span data-ttu-id="d9703-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="d9703-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="d9703-124">自訂回應狀態碼</span><span class="sxs-lookup"><span data-stu-id="d9703-124">Custom Response Status Code</span></span>

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

### <span data-ttu-id="d9703-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="d9703-125">-Customrule</span></span>
<span data-ttu-id="d9703-126">原則內的自訂規則</span><span class="sxs-lookup"><span data-stu-id="d9703-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="d9703-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9703-127">-DefaultProfile</span></span>
<span data-ttu-id="d9703-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9703-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9703-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="d9703-129">-EnabledState</span></span>
<span data-ttu-id="d9703-130">該策略處於啟用狀態或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="d9703-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="d9703-131">可能的值包括：'已停用'、'Enabled'</span><span class="sxs-lookup"><span data-stu-id="d9703-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="d9703-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9703-132">-InputObject</span></span>
<span data-ttu-id="d9703-133">要更新的 FireWallPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="d9703-133">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="d9703-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="d9703-134">-ManagedRule</span></span>
<span data-ttu-id="d9703-135">原則內的受管理規則</span><span class="sxs-lookup"><span data-stu-id="d9703-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="d9703-136">-模式</span><span class="sxs-lookup"><span data-stu-id="d9703-136">-Mode</span></span>
<span data-ttu-id="d9703-137">說明它處於偵測模式或策略層級的防護模式。</span><span class="sxs-lookup"><span data-stu-id="d9703-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="d9703-138">可能的值包括：'Prevention'， 'Detection'</span><span class="sxs-lookup"><span data-stu-id="d9703-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="d9703-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="d9703-139">-Name</span></span>
<span data-ttu-id="d9703-140">要更新的 FireWallPolicy 名稱。</span><span class="sxs-lookup"><span data-stu-id="d9703-140">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="d9703-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="d9703-141">-RedirectUrl</span></span>
<span data-ttu-id="d9703-142">重新導向 URL</span><span class="sxs-lookup"><span data-stu-id="d9703-142">Redirect URL</span></span>

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

### <span data-ttu-id="d9703-143">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="d9703-143">-RequestBodyCheck</span></span>
<span data-ttu-id="d9703-144">定義是否由受管理規則檢查本體。</span><span class="sxs-lookup"><span data-stu-id="d9703-144">Defines if the body should be inspected by managed rules.</span></span> <span data-ttu-id="d9703-145">可能的值包括：'Enabled'， 'Disabled'</span><span class="sxs-lookup"><span data-stu-id="d9703-145">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="d9703-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9703-146">-ResourceGroupName</span></span>
<span data-ttu-id="d9703-147">FireWallPolicy 所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="d9703-147">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="d9703-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9703-148">-ResourceId</span></span>
<span data-ttu-id="d9703-149">要更新的 FireWallPolicy 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d9703-149">Resource Id of the FireWallPolicy to update</span></span>

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

### <span data-ttu-id="d9703-150">-確認</span><span class="sxs-lookup"><span data-stu-id="d9703-150">-Confirm</span></span>
<span data-ttu-id="d9703-151">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d9703-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9703-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9703-152">-WhatIf</span></span>
<span data-ttu-id="d9703-153">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d9703-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9703-154">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9703-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9703-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9703-155">CommonParameters</span></span>
<span data-ttu-id="d9703-156">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d9703-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9703-157">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9703-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9703-158">輸入</span><span class="sxs-lookup"><span data-stu-id="d9703-158">INPUTS</span></span>

### <span data-ttu-id="d9703-159">Microsoft.Azure.Commands.FrontDoor.models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d9703-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="d9703-160">System.String</span><span class="sxs-lookup"><span data-stu-id="d9703-160">System.String</span></span>

## <span data-ttu-id="d9703-161">輸出</span><span class="sxs-lookup"><span data-stu-id="d9703-161">OUTPUTS</span></span>

### <span data-ttu-id="d9703-162">Microsoft.Azure.Commands.FrontDoor.models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d9703-162">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="d9703-163">筆記</span><span class="sxs-lookup"><span data-stu-id="d9703-163">NOTES</span></span>

## <span data-ttu-id="d9703-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9703-164">RELATED LINKS</span></span>

<span data-ttu-id="d9703-165">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="d9703-165">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
