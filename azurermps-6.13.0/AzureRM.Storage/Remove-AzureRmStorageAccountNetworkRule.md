---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: 73f096c516bb285b89e45d90107ff6a3ad406dbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626034"
---
# <span data-ttu-id="3fdf7-101">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3fdf7-101">Remove-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="3fdf7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3fdf7-102">SYNOPSIS</span></span>
<span data-ttu-id="3fdf7-103">從存儲帳戶的 NetWorkRule 屬性移除 IpRules 或 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="3fdf7-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fdf7-104">句法</span><span class="sxs-lookup"><span data-stu-id="3fdf7-104">SYNTAX</span></span>

### <span data-ttu-id="3fdf7-105">NetWorkRuleString (預設) </span><span class="sxs-lookup"><span data-stu-id="3fdf7-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3fdf7-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="3fdf7-106">IpRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fdf7-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="3fdf7-107">NetworkRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fdf7-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="3fdf7-108">IpRuleString</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3fdf7-109">說明</span><span class="sxs-lookup"><span data-stu-id="3fdf7-109">DESCRIPTION</span></span>
<span data-ttu-id="3fdf7-110">**AzureRmStorageAccountNetworkRule** Cmdlet 會從儲存空間帳戶的 NetWorkRule 屬性中移除 IpRules 或 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="3fdf7-110">The **Remove-AzureRmStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="3fdf7-111">示例</span><span class="sxs-lookup"><span data-stu-id="3fdf7-111">EXAMPLES</span></span>

### <span data-ttu-id="3fdf7-112">範例1：使用 IPAddressOrRange 移除數個 IpRules</span><span class="sxs-lookup"><span data-stu-id="3fdf7-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="3fdf7-113">這個命令會以 IPAddressOrRange 移除數個 IpRules。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="3fdf7-114">範例2：使用 JSON VirtualNetworkRule 物件輸入來移除 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3fdf7-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="3fdf7-115">這個命令會移除具有 VirtualNetworkRule 物件輸入的 VirtualNetworkRule，並使用 JSON。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="3fdf7-116">範例3：移除使用管線的第一個 IpRule</span><span class="sxs-lookup"><span data-stu-id="3fdf7-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="3fdf7-117">這個命令會將第一個 IpRule 移除為管線。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="3fdf7-118">範例4：使用 VirtualNetworkResourceID 移除多個 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="3fdf7-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="3fdf7-119">這個命令會以 VirtualNetworkResourceID 移除數個 VirtualNetworkRules。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="3fdf7-120">參數</span><span class="sxs-lookup"><span data-stu-id="3fdf7-120">PARAMETERS</span></span>

### <span data-ttu-id="3fdf7-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fdf7-121">-AsJob</span></span>
<span data-ttu-id="3fdf7-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3fdf7-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fdf7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fdf7-123">-DefaultProfile</span></span>
<span data-ttu-id="3fdf7-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fdf7-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3fdf7-125">-IPAddressOrRange</span></span>
<span data-ttu-id="3fdf7-126">IpAddressOrRange 陣列會從 NetWorkRule 屬性移除具有相同 IpAddressOrRange 的 IpRule。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="3fdf7-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="3fdf7-127">-IPRule</span></span>
<span data-ttu-id="3fdf7-128">要從 NetWorkRule 屬性移除的 IpRule 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="3fdf7-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="3fdf7-129">-Name</span></span>
<span data-ttu-id="3fdf7-130">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="3fdf7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fdf7-131">-ResourceGroupName</span></span>
<span data-ttu-id="3fdf7-132">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="3fdf7-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3fdf7-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="3fdf7-134">VirtualNetworkResourceId 陣列會從 NetWorkRule 屬性移除具有相同 VirtualNetworkResourceId 的 VirtualNetworkRule。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="3fdf7-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3fdf7-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="3fdf7-136">要從 NetWorkRule 屬性移除的 VirtualNetworkRule 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="3fdf7-137">-確認</span><span class="sxs-lookup"><span data-stu-id="3fdf7-137">-Confirm</span></span>
<span data-ttu-id="3fdf7-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fdf7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fdf7-139">-WhatIf</span></span>
<span data-ttu-id="3fdf7-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fdf7-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fdf7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fdf7-142">CommonParameters</span></span>
<span data-ttu-id="3fdf7-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fdf7-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fdf7-145">輸入</span><span class="sxs-lookup"><span data-stu-id="3fdf7-145">INPUTS</span></span>

### <span data-ttu-id="3fdf7-146">System.object</span><span class="sxs-lookup"><span data-stu-id="3fdf7-146">System.String</span></span>

### <span data-ttu-id="3fdf7-147">PSIpRule [] 的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="3fdf7-148">參數： IPRule (ByValue) </span><span class="sxs-lookup"><span data-stu-id="3fdf7-148">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="3fdf7-149">PSVirtualNetworkRule [] 的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="3fdf7-150">參數： VirtualNetworkRule (ByValue) </span><span class="sxs-lookup"><span data-stu-id="3fdf7-150">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="3fdf7-151">輸出</span><span class="sxs-lookup"><span data-stu-id="3fdf7-151">OUTPUTS</span></span>

### <span data-ttu-id="3fdf7-152">PSVirtualNetworkRule 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-152">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="3fdf7-153">PSIpRule 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="3fdf7-153">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="3fdf7-154">筆記</span><span class="sxs-lookup"><span data-stu-id="3fdf7-154">NOTES</span></span>

## <span data-ttu-id="3fdf7-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="3fdf7-155">RELATED LINKS</span></span>
