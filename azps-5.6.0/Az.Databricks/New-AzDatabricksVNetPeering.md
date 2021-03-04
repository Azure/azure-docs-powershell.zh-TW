---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: a569f605c139d5cd34c42ee1567989acebabbe61
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904485"
---
# <span data-ttu-id="1c881-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="1c881-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="1c881-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1c881-102">SYNOPSIS</span></span>
<span data-ttu-id="1c881-103">建立工作區的 vNet 對等。</span><span class="sxs-lookup"><span data-stu-id="1c881-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="1c881-104">語法</span><span class="sxs-lookup"><span data-stu-id="1c881-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1c881-105">描述</span><span class="sxs-lookup"><span data-stu-id="1c881-105">DESCRIPTION</span></span>
<span data-ttu-id="1c881-106">建立工作區的 vNet 對等。</span><span class="sxs-lookup"><span data-stu-id="1c881-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="1c881-107">例子</span><span class="sxs-lookup"><span data-stu-id="1c881-107">EXAMPLES</span></span>

### <span data-ttu-id="1c881-108">範例 1：建立 datab一s 的 vnet 對等</span><span class="sxs-lookup"><span data-stu-id="1c881-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="1c881-109">此命令會為 datab本體建立 vnet 對等。</span><span class="sxs-lookup"><span data-stu-id="1c881-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="1c881-110">參數</span><span class="sxs-lookup"><span data-stu-id="1c881-110">PARAMETERS</span></span>

### <span data-ttu-id="1c881-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="1c881-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="1c881-112">是否允許/禁止從遠端虛擬網路中從本地虛擬網路中從虛擬機器轉轉的流量。</span><span class="sxs-lookup"><span data-stu-id="1c881-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="1c881-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="1c881-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="1c881-114">如果閘道連結可用於遠端虛擬網路，可連結至此虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="1c881-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="1c881-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="1c881-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="1c881-116">本地虛擬網路空間中的虛擬機器是否能存取遠端虛擬網路空間中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1c881-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="1c881-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c881-117">-AsJob</span></span>
<span data-ttu-id="1c881-118">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="1c881-118">Run the command as a job</span></span>

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

### <span data-ttu-id="1c881-119">-DatabaxsAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="1c881-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="1c881-120">CIDR 標記法中為此虛擬網路保留的位址區塊清單。</span><span class="sxs-lookup"><span data-stu-id="1c881-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c881-121">-DatabworksVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="1c881-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="1c881-122">Datab一s 虛擬網路的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c881-122">The Id of the databricks virtual network.</span></span>

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

### <span data-ttu-id="1c881-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c881-123">-DefaultProfile</span></span>
<span data-ttu-id="1c881-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c881-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c881-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="1c881-125">-Name</span></span>
<span data-ttu-id="1c881-126">工作區 vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c881-126">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="1c881-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1c881-127">-NoWait</span></span>
<span data-ttu-id="1c881-128">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="1c881-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1c881-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="1c881-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="1c881-130">CIDR 標記法中為此虛擬網路保留的位址區塊清單。</span><span class="sxs-lookup"><span data-stu-id="1c881-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c881-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="1c881-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="1c881-132">遠端虛擬網路的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c881-132">The Id of the remote virtual network.</span></span>

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

### <span data-ttu-id="1c881-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c881-133">-ResourceGroupName</span></span>
<span data-ttu-id="1c881-134">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c881-134">The name of the resource group.</span></span>
<span data-ttu-id="1c881-135">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="1c881-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1c881-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c881-136">-SubscriptionId</span></span>
<span data-ttu-id="1c881-137">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c881-137">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c881-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="1c881-138">-UseRemoteGateway</span></span>
<span data-ttu-id="1c881-139">如果遠端閘道可以在這個虛擬網路上使用。</span><span class="sxs-lookup"><span data-stu-id="1c881-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="1c881-140">如果旗標設定為 True，且遠端對等上的 allowGatewayTransit 也為 True，則虛擬網路會使用遠端虛擬網路的閘道進行傳輸。</span><span class="sxs-lookup"><span data-stu-id="1c881-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="1c881-141">只有一個對等可以設定此旗標為 True。</span><span class="sxs-lookup"><span data-stu-id="1c881-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="1c881-142">如果虛擬網路已經有閘道，就無法設定此標號。</span><span class="sxs-lookup"><span data-stu-id="1c881-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="1c881-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1c881-143">-WorkspaceName</span></span>
<span data-ttu-id="1c881-144">工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c881-144">The name of the workspace.</span></span>

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

### <span data-ttu-id="1c881-145">-確認</span><span class="sxs-lookup"><span data-stu-id="1c881-145">-Confirm</span></span>
<span data-ttu-id="1c881-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1c881-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c881-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c881-147">-WhatIf</span></span>
<span data-ttu-id="1c881-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1c881-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c881-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1c881-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c881-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c881-150">CommonParameters</span></span>
<span data-ttu-id="1c881-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1c881-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c881-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c881-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c881-153">輸入</span><span class="sxs-lookup"><span data-stu-id="1c881-153">INPUTS</span></span>

## <span data-ttu-id="1c881-154">輸出</span><span class="sxs-lookup"><span data-stu-id="1c881-154">OUTPUTS</span></span>

### <span data-ttu-id="1c881-155">Microsoft.Azure.PowerShell.Cmdlets.Databworks.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1c881-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="1c881-156">筆記</span><span class="sxs-lookup"><span data-stu-id="1c881-156">NOTES</span></span>

<span data-ttu-id="1c881-157">別名</span><span class="sxs-lookup"><span data-stu-id="1c881-157">ALIASES</span></span>

## <span data-ttu-id="1c881-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c881-158">RELATED LINKS</span></span>

