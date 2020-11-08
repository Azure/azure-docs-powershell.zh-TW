---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: f1af71bd2c05f2b1219a3ad7f1f09eb2f9560ad4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969258"
---
# <span data-ttu-id="2228d-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="2228d-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="2228d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2228d-102">SYNOPSIS</span></span>
<span data-ttu-id="2228d-103">針對工作區建立 vNet 對等。</span><span class="sxs-lookup"><span data-stu-id="2228d-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="2228d-104">句法</span><span class="sxs-lookup"><span data-stu-id="2228d-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2228d-105">說明</span><span class="sxs-lookup"><span data-stu-id="2228d-105">DESCRIPTION</span></span>
<span data-ttu-id="2228d-106">針對工作區建立 vNet 對等。</span><span class="sxs-lookup"><span data-stu-id="2228d-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="2228d-107">示例</span><span class="sxs-lookup"><span data-stu-id="2228d-107">EXAMPLES</span></span>

### <span data-ttu-id="2228d-108">範例1：為 databricks 建立 vnet 對等</span><span class="sxs-lookup"><span data-stu-id="2228d-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="2228d-109">這個命令會為 databricks 建立 vnet 對等。</span><span class="sxs-lookup"><span data-stu-id="2228d-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="2228d-110">參數</span><span class="sxs-lookup"><span data-stu-id="2228d-110">PARAMETERS</span></span>

### <span data-ttu-id="2228d-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="2228d-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="2228d-112">在遠端虛擬網路中，是否允許或不允許將來自本機虛擬網路中之 Vm 的轉寄流量傳送。</span><span class="sxs-lookup"><span data-stu-id="2228d-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="2228d-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="2228d-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="2228d-114">如果您可以在遠端虛擬網路中使用閘道連結來連結到這個虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="2228d-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="2228d-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="2228d-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="2228d-116">本機虛擬網路空間中的 Vm 是否能夠存取遠端虛擬網路空間中的 Vm。</span><span class="sxs-lookup"><span data-stu-id="2228d-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="2228d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2228d-117">-AsJob</span></span>
<span data-ttu-id="2228d-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="2228d-118">Run the command as a job</span></span>

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

### <span data-ttu-id="2228d-119">-DatabricksAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="2228d-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="2228d-120">以 CIDR 標記法為此虛擬網路保留的位址區塊清單。</span><span class="sxs-lookup"><span data-stu-id="2228d-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="2228d-121">-DatabricksVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2228d-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="2228d-122">Databricks 虛擬網路的 Id。</span><span class="sxs-lookup"><span data-stu-id="2228d-122">The Id of the databricks virtual network.</span></span>

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

### <span data-ttu-id="2228d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2228d-123">-DefaultProfile</span></span>
<span data-ttu-id="2228d-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2228d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2228d-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="2228d-125">-Name</span></span>
<span data-ttu-id="2228d-126">工作區 vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="2228d-126">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="2228d-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2228d-127">-NoWait</span></span>
<span data-ttu-id="2228d-128">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="2228d-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2228d-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="2228d-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="2228d-130">以 CIDR 標記法為此虛擬網路保留的位址區塊清單。</span><span class="sxs-lookup"><span data-stu-id="2228d-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="2228d-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2228d-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="2228d-132">遠端虛擬網路的 Id。</span><span class="sxs-lookup"><span data-stu-id="2228d-132">The Id of the remote virtual network.</span></span>

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

### <span data-ttu-id="2228d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2228d-133">-ResourceGroupName</span></span>
<span data-ttu-id="2228d-134">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2228d-134">The name of the resource group.</span></span>
<span data-ttu-id="2228d-135">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2228d-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2228d-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2228d-136">-SubscriptionId</span></span>
<span data-ttu-id="2228d-137">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="2228d-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2228d-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="2228d-138">-UseRemoteGateway</span></span>
<span data-ttu-id="2228d-139">如果您可以在此虛擬網路上使用遠端閘道。</span><span class="sxs-lookup"><span data-stu-id="2228d-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="2228d-140">如果旗標設定為 true，且 allowGatewayTransit 在遠端對等也為 true，則虛擬網路將會使用遠端虛擬網路的閘道進行傳輸。</span><span class="sxs-lookup"><span data-stu-id="2228d-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="2228d-141">只有一個對等可以將此標誌設定為 true。</span><span class="sxs-lookup"><span data-stu-id="2228d-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="2228d-142">如果虛擬網路已有閘道，則無法設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="2228d-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="2228d-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2228d-143">-WorkspaceName</span></span>
<span data-ttu-id="2228d-144">工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="2228d-144">The name of the workspace.</span></span>

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

### <span data-ttu-id="2228d-145">-確認</span><span class="sxs-lookup"><span data-stu-id="2228d-145">-Confirm</span></span>
<span data-ttu-id="2228d-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2228d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2228d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2228d-147">-WhatIf</span></span>
<span data-ttu-id="2228d-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2228d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2228d-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2228d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2228d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2228d-150">CommonParameters</span></span>
<span data-ttu-id="2228d-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2228d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2228d-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2228d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2228d-153">輸入</span><span class="sxs-lookup"><span data-stu-id="2228d-153">INPUTS</span></span>

## <span data-ttu-id="2228d-154">輸出</span><span class="sxs-lookup"><span data-stu-id="2228d-154">OUTPUTS</span></span>

### <span data-ttu-id="2228d-155">IVirtualNetworkPeering （Databricks）。 Api20180401。</span><span class="sxs-lookup"><span data-stu-id="2228d-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="2228d-156">筆記</span><span class="sxs-lookup"><span data-stu-id="2228d-156">NOTES</span></span>

<span data-ttu-id="2228d-157">別名</span><span class="sxs-lookup"><span data-stu-id="2228d-157">ALIASES</span></span>

## <span data-ttu-id="2228d-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="2228d-158">RELATED LINKS</span></span>

