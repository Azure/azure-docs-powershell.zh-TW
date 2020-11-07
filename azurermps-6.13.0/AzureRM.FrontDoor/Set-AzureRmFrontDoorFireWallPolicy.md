---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: a02510cc72b9e674f9d4fded1355ae5b2cadc807
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623414"
---
# <span data-ttu-id="abe4c-101">Set-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="abe4c-101">Set-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="abe4c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="abe4c-102">SYNOPSIS</span></span>
<span data-ttu-id="abe4c-103">更新 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="abe4c-103">update WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abe4c-104">句法</span><span class="sxs-lookup"><span data-stu-id="abe4c-104">SYNTAX</span></span>

### <span data-ttu-id="abe4c-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="abe4c-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abe4c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="abe4c-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abe4c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="abe4c-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abe4c-108">說明</span><span class="sxs-lookup"><span data-stu-id="abe4c-108">DESCRIPTION</span></span>
<span data-ttu-id="abe4c-109">**AzureRmFrontDoor** Cmdlet 會更新現有的 WAF 原則。</span><span class="sxs-lookup"><span data-stu-id="abe4c-109">The **Set-AzureRmFrontDoor** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="abe4c-110">如果未提供輸入參數，則會使用來自現有 WAF 原則的舊參數。</span><span class="sxs-lookup"><span data-stu-id="abe4c-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="abe4c-111">示例</span><span class="sxs-lookup"><span data-stu-id="abe4c-111">EXAMPLES</span></span>

### <span data-ttu-id="abe4c-112">範例1：更新現有的 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="abe4c-112">Example 1: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $node

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="abe4c-113">更新現有的 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="abe4c-113">update an existing WAF policy</span></span>

### <span data-ttu-id="abe4c-114">範例2：更新現有的 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="abe4c-114">Example 2: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -InputObject $policy1 -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="abe4c-115">更新現有的 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="abe4c-115">update an existing WAF policy</span></span>

### <span data-ttu-id="abe4c-116">範例3：更新現有的 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="abe4c-116">Example 3: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -ResourceId $resourcdId -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="abe4c-117">更新現有的 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="abe4c-117">update an existing WAF policy</span></span>

### <span data-ttu-id="abe4c-118">範例4：更新 $resourceGroup 中的所有 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="abe4c-118">Example 4: update all WAF policies in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Set-AzureRmFrontDoorFireWallPolicy -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode
```

<span data-ttu-id="abe4c-119">更新 $resourceGroup 中的所有 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="abe4c-119">update all WAF policies in $resourceGroup</span></span>

## <span data-ttu-id="abe4c-120">參數</span><span class="sxs-lookup"><span data-stu-id="abe4c-120">PARAMETERS</span></span>

### <span data-ttu-id="abe4c-121">-Customrule</span><span class="sxs-lookup"><span data-stu-id="abe4c-121">-Customrule</span></span>
<span data-ttu-id="abe4c-122">原則內的自訂規則</span><span class="sxs-lookup"><span data-stu-id="abe4c-122">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="abe4c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abe4c-123">-DefaultProfile</span></span>
<span data-ttu-id="abe4c-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="abe4c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abe4c-125">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="abe4c-125">-EnabledState</span></span>
<span data-ttu-id="abe4c-126">原則處於 [啟用] 狀態或 [已停用] 狀態。</span><span class="sxs-lookup"><span data-stu-id="abe4c-126">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="abe4c-127">可能的值包括：「已停用」、「已啟用」</span><span class="sxs-lookup"><span data-stu-id="abe4c-127">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="abe4c-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abe4c-128">-InputObject</span></span>
<span data-ttu-id="abe4c-129">要更新的 FireWallPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="abe4c-129">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="abe4c-130">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="abe4c-130">-ManagedRule</span></span>
<span data-ttu-id="abe4c-131">原則中的受管理規則</span><span class="sxs-lookup"><span data-stu-id="abe4c-131">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="abe4c-132">模式</span><span class="sxs-lookup"><span data-stu-id="abe4c-132">-Mode</span></span>
<span data-ttu-id="abe4c-133">描述它是否在策略層級的偵測模式或預防模式中。</span><span class="sxs-lookup"><span data-stu-id="abe4c-133">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="abe4c-134">可能的值包括：「預防」、「偵測」</span><span class="sxs-lookup"><span data-stu-id="abe4c-134">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="abe4c-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="abe4c-135">-Name</span></span>
<span data-ttu-id="abe4c-136">要更新之 FireWallPolicy 的名稱。</span><span class="sxs-lookup"><span data-stu-id="abe4c-136">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="abe4c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abe4c-137">-ResourceGroupName</span></span>
<span data-ttu-id="abe4c-138">FireWallPolicy 所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="abe4c-138">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="abe4c-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abe4c-139">-ResourceId</span></span>
<span data-ttu-id="abe4c-140">要更新之 FireWallPolicy 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="abe4c-140">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abe4c-141">-確認</span><span class="sxs-lookup"><span data-stu-id="abe4c-141">-Confirm</span></span>
<span data-ttu-id="abe4c-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="abe4c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abe4c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abe4c-143">-WhatIf</span></span>
<span data-ttu-id="abe4c-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="abe4c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abe4c-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="abe4c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abe4c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abe4c-146">CommonParameters</span></span>
<span data-ttu-id="abe4c-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="abe4c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abe4c-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="abe4c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abe4c-149">輸入</span><span class="sxs-lookup"><span data-stu-id="abe4c-149">INPUTS</span></span>

### <span data-ttu-id="abe4c-150">PSPolicy 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="abe4c-150">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="abe4c-151">System.object</span><span class="sxs-lookup"><span data-stu-id="abe4c-151">System.String</span></span>

## <span data-ttu-id="abe4c-152">輸出</span><span class="sxs-lookup"><span data-stu-id="abe4c-152">OUTPUTS</span></span>

### <span data-ttu-id="abe4c-153">PSPolicy 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="abe4c-153">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="abe4c-154">筆記</span><span class="sxs-lookup"><span data-stu-id="abe4c-154">NOTES</span></span>

## <span data-ttu-id="abe4c-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="abe4c-155">RELATED LINKS</span></span>

<span data-ttu-id="abe4c-156">[新-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
[AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
[新-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
[新-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="abe4c-156">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>
