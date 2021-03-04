---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 295f79f48ffa966024561486745cdcf52ec8e38f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907254"
---
# <span data-ttu-id="d8744-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d8744-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="d8744-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d8744-102">SYNOPSIS</span></span>
<span data-ttu-id="d8744-103">從儲存帳戶的 NetWorkRule 屬性移除 IpRules 或 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="d8744-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="d8744-104">語法</span><span class="sxs-lookup"><span data-stu-id="d8744-104">SYNTAX</span></span>

### <span data-ttu-id="d8744-105">NetWorkRuleString (預設) </span><span class="sxs-lookup"><span data-stu-id="d8744-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8744-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="d8744-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8744-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="d8744-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8744-108">ResourceAccessRuleObject</span><span class="sxs-lookup"><span data-stu-id="d8744-108">ResourceAccessRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -ResourceAccessRule <PSResourceAccessRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8744-109">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="d8744-109">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8744-110">ResourceAccessRuleString</span><span class="sxs-lookup"><span data-stu-id="d8744-110">ResourceAccessRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -TenantId <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8744-111">描述</span><span class="sxs-lookup"><span data-stu-id="d8744-111">DESCRIPTION</span></span>
<span data-ttu-id="d8744-112">**Remove-AzStorageAccountNetworkRule** Cmdlet 會從儲存帳戶的 NetWorkRule 屬性移除 IpRules 或 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="d8744-112">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="d8744-113">例子</span><span class="sxs-lookup"><span data-stu-id="d8744-113">EXAMPLES</span></span>

### <span data-ttu-id="d8744-114">範例 1：使用 IPAddressOrRange 移除多個 IpRules</span><span class="sxs-lookup"><span data-stu-id="d8744-114">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="d8744-115">此命令會使用 IPAddressOrRange 移除多個 IpRules。</span><span class="sxs-lookup"><span data-stu-id="d8744-115">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="d8744-116">範例 2：使用 JSON 移除 VirtualNetworkRule 與 VirtualNetworkRule 物件輸入</span><span class="sxs-lookup"><span data-stu-id="d8744-116">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="d8744-117">此命令會移除 VirtualNetworkRule 與 VirtualNetworkRule 物件輸入 JSON。</span><span class="sxs-lookup"><span data-stu-id="d8744-117">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="d8744-118">範例 3：使用管線移除第一個 IpRule</span><span class="sxs-lookup"><span data-stu-id="d8744-118">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="d8744-119">此命令會移除第一個具有管線的 IpRule。</span><span class="sxs-lookup"><span data-stu-id="d8744-119">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="d8744-120">範例 4：使用 VirtualNetworkResourceID 移除多個 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="d8744-120">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="d8744-121">此命令會使用 VirtualNetworkResourceID 移除多個 VirtualNetworkRules。</span><span class="sxs-lookup"><span data-stu-id="d8744-121">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="d8744-122">範例 5：移除具有 TenantId 和 ResourceId 的資源存取規則。</span><span class="sxs-lookup"><span data-stu-id="d8744-122">Example 5: Remove a resource access rule with TenantId and ResourceId.</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount"  -TenantId $tenantId -ResourceId $ResourceId
```

<span data-ttu-id="d8744-123">此命令會移除具有 TenantId 和 ResourceId 的資源存取規則。</span><span class="sxs-lookup"><span data-stu-id="d8744-123">This command removes a resource access rule with TenantId and ResourceId.</span></span>

### <span data-ttu-id="d8744-124">範例 6：從儲存帳戶移除前 3 個資源存取規則</span><span class="sxs-lookup"><span data-stu-id="d8744-124">Example 6: Remove the first 3 resource access rules from a storage account</span></span>
```
PS C:\> (Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount").ResourceAccessRules | Select-Object -First 3 | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="d8744-125">此命令會從儲存帳戶移除前 3 個資源存取規則。</span><span class="sxs-lookup"><span data-stu-id="d8744-125">This command removes the first 3 resource access rules from a storage account.</span></span>

## <span data-ttu-id="d8744-126">參數</span><span class="sxs-lookup"><span data-stu-id="d8744-126">PARAMETERS</span></span>

### <span data-ttu-id="d8744-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8744-127">-AsJob</span></span>
<span data-ttu-id="d8744-128">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d8744-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8744-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8744-129">-DefaultProfile</span></span>
<span data-ttu-id="d8744-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8744-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8744-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d8744-131">-IPAddressOrRange</span></span>
<span data-ttu-id="d8744-132">IpAddressOrRange 陣列會從 NetWorkRule 屬性移除與相同 IpAddressOrRange 的 IpRule。</span><span class="sxs-lookup"><span data-stu-id="d8744-132">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8744-133">-IPRule</span><span class="sxs-lookup"><span data-stu-id="d8744-133">-IPRule</span></span>
<span data-ttu-id="d8744-134">要從 NetWorkRule 屬性移除的 IpRule 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="d8744-134">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8744-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8744-135">-Name</span></span>
<span data-ttu-id="d8744-136">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8744-136">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="d8744-137">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="d8744-137">-ResourceAccessRule</span></span>
<span data-ttu-id="d8744-138">儲存帳戶 NetworkRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="d8744-138">Storage Account NetworkRule ResourceAccessRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSResourceAccessRule[]
Parameter Sets: ResourceAccessRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8744-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8744-139">-ResourceGroupName</span></span>
<span data-ttu-id="d8744-140">指定包含儲存空間帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d8744-140">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="d8744-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8744-141">-ResourceId</span></span>
<span data-ttu-id="d8744-142">儲存帳戶 ResourceAccessRule ResourceId in string.</span><span class="sxs-lookup"><span data-stu-id="d8744-142">Storage Account ResourceAccessRule ResourceId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8744-143">-TenantId</span><span class="sxs-lookup"><span data-stu-id="d8744-143">-TenantId</span></span>
<span data-ttu-id="d8744-144">儲存帳戶 ResourceAccessRule TenantId in string.</span><span class="sxs-lookup"><span data-stu-id="d8744-144">Storage Account ResourceAccessRule TenantId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8744-145">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="d8744-145">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="d8744-146">VirtualNetworkResourceId 陣列會從 NetWorkRule 屬性移除與 VirtualNetworkResourceId 相同的 VirtualNetworkRule。</span><span class="sxs-lookup"><span data-stu-id="d8744-146">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8744-147">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d8744-147">-VirtualNetworkRule</span></span>
<span data-ttu-id="d8744-148">要從 NetWorkRule 屬性移除的 VirtualNetworkRule 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="d8744-148">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8744-149">-確認</span><span class="sxs-lookup"><span data-stu-id="d8744-149">-Confirm</span></span>
<span data-ttu-id="d8744-150">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d8744-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8744-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8744-151">-WhatIf</span></span>
<span data-ttu-id="d8744-152">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d8744-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8744-153">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d8744-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8744-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8744-154">CommonParameters</span></span>
<span data-ttu-id="d8744-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d8744-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8744-156">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d8744-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8744-157">輸入</span><span class="sxs-lookup"><span data-stu-id="d8744-157">INPUTS</span></span>

### <span data-ttu-id="d8744-158">System.String</span><span class="sxs-lookup"><span data-stu-id="d8744-158">System.String</span></span>

### <span data-ttu-id="d8744-159">Microsoft.Azure.Commands.management.storage.models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="d8744-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="d8744-160">Microsoft.Azure.Commands.management.storage.models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="d8744-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="d8744-161">輸出</span><span class="sxs-lookup"><span data-stu-id="d8744-161">OUTPUTS</span></span>

### <span data-ttu-id="d8744-162">Microsoft.Azure.Commands.management.storage.models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d8744-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="d8744-163">Microsoft.Azure.Commands.management.storage.models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="d8744-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="d8744-164">筆記</span><span class="sxs-lookup"><span data-stu-id="d8744-164">NOTES</span></span>

## <span data-ttu-id="d8744-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8744-165">RELATED LINKS</span></span>
