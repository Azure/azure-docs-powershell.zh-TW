---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 5724448a3d10c1e72e38ff5ab83c82a68edfef33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614521"
---
# <span data-ttu-id="ce212-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce212-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="ce212-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce212-102">SYNOPSIS</span></span>
<span data-ttu-id="ce212-103">從存儲帳戶的 NetWorkRule 屬性移除 IpRules 或 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="ce212-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="ce212-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce212-104">SYNTAX</span></span>

### <span data-ttu-id="ce212-105">NetWorkRuleString (預設) </span><span class="sxs-lookup"><span data-stu-id="ce212-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce212-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="ce212-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce212-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="ce212-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce212-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="ce212-108">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce212-109">說明</span><span class="sxs-lookup"><span data-stu-id="ce212-109">DESCRIPTION</span></span>
<span data-ttu-id="ce212-110">**AzStorageAccountNetworkRule** Cmdlet 會從儲存空間帳戶的 NetWorkRule 屬性中移除 IpRules 或 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="ce212-110">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="ce212-111">示例</span><span class="sxs-lookup"><span data-stu-id="ce212-111">EXAMPLES</span></span>

### <span data-ttu-id="ce212-112">範例1：使用 IPAddressOrRange 移除數個 IpRules</span><span class="sxs-lookup"><span data-stu-id="ce212-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="ce212-113">這個命令會以 IPAddressOrRange 移除數個 IpRules。</span><span class="sxs-lookup"><span data-stu-id="ce212-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="ce212-114">範例2：使用 JSON VirtualNetworkRule 物件輸入來移除 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce212-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="ce212-115">這個命令會移除具有 VirtualNetworkRule 物件輸入的 VirtualNetworkRule，並使用 JSON。</span><span class="sxs-lookup"><span data-stu-id="ce212-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="ce212-116">範例3：移除使用管線的第一個 IpRule</span><span class="sxs-lookup"><span data-stu-id="ce212-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="ce212-117">這個命令會將第一個 IpRule 移除為管線。</span><span class="sxs-lookup"><span data-stu-id="ce212-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="ce212-118">範例4：使用 VirtualNetworkResourceID 移除多個 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="ce212-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="ce212-119">這個命令會以 VirtualNetworkResourceID 移除數個 VirtualNetworkRules。</span><span class="sxs-lookup"><span data-stu-id="ce212-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="ce212-120">參數</span><span class="sxs-lookup"><span data-stu-id="ce212-120">PARAMETERS</span></span>

### <span data-ttu-id="ce212-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce212-121">-AsJob</span></span>
<span data-ttu-id="ce212-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce212-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce212-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce212-123">-DefaultProfile</span></span>
<span data-ttu-id="ce212-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce212-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce212-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ce212-125">-IPAddressOrRange</span></span>
<span data-ttu-id="ce212-126">IpAddressOrRange 陣列會從 NetWorkRule 屬性移除具有相同 IpAddressOrRange 的 IpRule。</span><span class="sxs-lookup"><span data-stu-id="ce212-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="ce212-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="ce212-127">-IPRule</span></span>
<span data-ttu-id="ce212-128">要從 NetWorkRule 屬性移除的 IpRule 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="ce212-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="ce212-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce212-129">-Name</span></span>
<span data-ttu-id="ce212-130">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce212-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="ce212-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce212-131">-ResourceGroupName</span></span>
<span data-ttu-id="ce212-132">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce212-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="ce212-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="ce212-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="ce212-134">VirtualNetworkResourceId 陣列會從 NetWorkRule 屬性移除具有相同 VirtualNetworkResourceId 的 VirtualNetworkRule。</span><span class="sxs-lookup"><span data-stu-id="ce212-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="ce212-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce212-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="ce212-136">要從 NetWorkRule 屬性移除的 VirtualNetworkRule 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="ce212-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="ce212-137">-確認</span><span class="sxs-lookup"><span data-stu-id="ce212-137">-Confirm</span></span>
<span data-ttu-id="ce212-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce212-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce212-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce212-139">-WhatIf</span></span>
<span data-ttu-id="ce212-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce212-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce212-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce212-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce212-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce212-142">CommonParameters</span></span>
<span data-ttu-id="ce212-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce212-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce212-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce212-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce212-145">輸入</span><span class="sxs-lookup"><span data-stu-id="ce212-145">INPUTS</span></span>

### <span data-ttu-id="ce212-146">System.object</span><span class="sxs-lookup"><span data-stu-id="ce212-146">System.String</span></span>

### <span data-ttu-id="ce212-147">PSIpRule [] 的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ce212-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="ce212-148">PSVirtualNetworkRule [] 的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ce212-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="ce212-149">輸出</span><span class="sxs-lookup"><span data-stu-id="ce212-149">OUTPUTS</span></span>

### <span data-ttu-id="ce212-150">PSVirtualNetworkRule 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ce212-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="ce212-151">PSIpRule 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ce212-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="ce212-152">筆記</span><span class="sxs-lookup"><span data-stu-id="ce212-152">NOTES</span></span>

## <span data-ttu-id="ce212-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce212-153">RELATED LINKS</span></span>
