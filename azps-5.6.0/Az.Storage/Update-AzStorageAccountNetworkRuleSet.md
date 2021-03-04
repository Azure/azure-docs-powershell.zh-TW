---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 03e6169a9e69b9f2faa3dfaccba934428f7db4e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907245"
---
# <span data-ttu-id="b6cd3-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6cd3-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="b6cd3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b6cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="b6cd3-103">更新儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="b6cd3-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="b6cd3-104">語法</span><span class="sxs-lookup"><span data-stu-id="b6cd3-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-ResourceAccessRule <PSResourceAccessRule[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6cd3-105">描述</span><span class="sxs-lookup"><span data-stu-id="b6cd3-105">DESCRIPTION</span></span>
<span data-ttu-id="b6cd3-106">**Update-AzStorageAccountNetworkRuleSet** Cmdlet 會更新儲存帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="b6cd3-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="b6cd3-107">例子</span><span class="sxs-lookup"><span data-stu-id="b6cd3-107">EXAMPLES</span></span>

### <span data-ttu-id="b6cd3-108">範例 1：更新 NetworkRule 的所有屬性，使用 JSON 輸入規則</span><span class="sxs-lookup"><span data-stu-id="b6cd3-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"}) -ResourceAccessRule (@{ResourceId=$ResourceId1;TenantId=$tenantId1},@{ResourceId=$ResourceId2;TenantId=$tenantId1})
```

<span data-ttu-id="b6cd3-109">此命令會更新 NetworkRule 的所有屬性，以及使用 JSON 輸入規則。</span><span class="sxs-lookup"><span data-stu-id="b6cd3-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="b6cd3-110">範例 2：NetworkRule 的更新旁路屬性</span><span class="sxs-lookup"><span data-stu-id="b6cd3-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="b6cd3-111">此命令更新 NetworkRule 的 Bypass 屬性 (不會變更其他屬性) 。</span><span class="sxs-lookup"><span data-stu-id="b6cd3-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="b6cd3-112">範例 3：清理儲存空間帳戶的 NetworkRule 規則</span><span class="sxs-lookup"><span data-stu-id="b6cd3-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @() -ResourceAccessRule @()
```

<span data-ttu-id="b6cd3-113">此命令會清除儲存空間帳戶的 NetworkRule 規則， (不會變更其他) 。</span><span class="sxs-lookup"><span data-stu-id="b6cd3-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="b6cd3-114">參數</span><span class="sxs-lookup"><span data-stu-id="b6cd3-114">PARAMETERS</span></span>

### <span data-ttu-id="b6cd3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6cd3-115">-AsJob</span></span>
<span data-ttu-id="b6cd3-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b6cd3-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cd3-117">-旁路</span><span class="sxs-lookup"><span data-stu-id="b6cd3-117">-Bypass</span></span>
<span data-ttu-id="b6cd3-118">要更新至儲存空間帳戶的 NetworkRule 屬性的 Bypass 值。</span><span class="sxs-lookup"><span data-stu-id="b6cd3-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="b6cd3-119">允許的值不是或任何組合：• Logging • 計量 • Azureservices</span><span class="sxs-lookup"><span data-stu-id="b6cd3-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, Logging, Metrics, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cd3-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="b6cd3-120">-DefaultAction</span></span>
<span data-ttu-id="b6cd3-121">要更新至儲存空間帳戶 NetworkRule 屬性的 DefaultAction 值。</span><span class="sxs-lookup"><span data-stu-id="b6cd3-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="b6cd3-122">允許的選項：• 允許 • 拒絕</span><span class="sxs-lookup"><span data-stu-id="b6cd3-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cd3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6cd3-123">-DefaultProfile</span></span>
<span data-ttu-id="b6cd3-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6cd3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6cd3-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="b6cd3-125">-IPRule</span></span>
<span data-ttu-id="b6cd3-126">要更新至儲存帳戶 NetworkRule 屬性的 IpRule 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="b6cd3-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cd3-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="b6cd3-127">-Name</span></span>
<span data-ttu-id="b6cd3-128">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6cd3-128">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cd3-129">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="b6cd3-129">-ResourceAccessRule</span></span>
<span data-ttu-id="b6cd3-130">儲存帳戶 NetworkRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="b6cd3-130">Storage Account NetworkRule ResourceAccessRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSResourceAccessRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cd3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6cd3-131">-ResourceGroupName</span></span>
<span data-ttu-id="b6cd3-132">指定包含儲存空間帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b6cd3-132">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cd3-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b6cd3-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="b6cd3-134">要更新為儲存帳戶 NetworkRule 屬性的 VirtualNetworkRule 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="b6cd3-134">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cd3-135">-確認</span><span class="sxs-lookup"><span data-stu-id="b6cd3-135">-Confirm</span></span>
<span data-ttu-id="b6cd3-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b6cd3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6cd3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6cd3-137">-WhatIf</span></span>
<span data-ttu-id="b6cd3-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b6cd3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6cd3-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6cd3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6cd3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6cd3-140">CommonParameters</span></span>
<span data-ttu-id="b6cd3-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b6cd3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6cd3-142">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b6cd3-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6cd3-143">輸入</span><span class="sxs-lookup"><span data-stu-id="b6cd3-143">INPUTS</span></span>

### <span data-ttu-id="b6cd3-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b6cd3-144">System.String</span></span>

### <span data-ttu-id="b6cd3-145">Microsoft.Azure.Commands.management.storage.models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="b6cd3-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="b6cd3-146">Microsoft.Azure.Commands.management.storage.models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="b6cd3-146">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="b6cd3-147">輸出</span><span class="sxs-lookup"><span data-stu-id="b6cd3-147">OUTPUTS</span></span>

### <span data-ttu-id="b6cd3-148">Microsoft.Azure.Commands.management.storage.models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6cd3-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="b6cd3-149">筆記</span><span class="sxs-lookup"><span data-stu-id="b6cd3-149">NOTES</span></span>

## <span data-ttu-id="b6cd3-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6cd3-150">RELATED LINKS</span></span>
