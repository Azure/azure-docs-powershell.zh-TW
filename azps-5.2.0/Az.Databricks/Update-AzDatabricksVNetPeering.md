---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: d53b45b67aa0843ddbdd8c5b063ff9295661a495
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282092"
---
# <span data-ttu-id="cbae6-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="cbae6-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="cbae6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cbae6-102">SYNOPSIS</span></span>
<span data-ttu-id="cbae6-103">針對工作區更新 vNet 對等。</span><span class="sxs-lookup"><span data-stu-id="cbae6-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="cbae6-104">句法</span><span class="sxs-lookup"><span data-stu-id="cbae6-104">SYNTAX</span></span>

### <span data-ttu-id="cbae6-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="cbae6-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cbae6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cbae6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cbae6-107">說明</span><span class="sxs-lookup"><span data-stu-id="cbae6-107">DESCRIPTION</span></span>
<span data-ttu-id="cbae6-108">針對工作區更新 vNet 對等。</span><span class="sxs-lookup"><span data-stu-id="cbae6-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="cbae6-109">示例</span><span class="sxs-lookup"><span data-stu-id="cbae6-109">EXAMPLES</span></span>

### <span data-ttu-id="cbae6-110">範例1：更新對 vnet 對等的 AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="cbae6-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="cbae6-111">這個命令會更新 vnet 對等的 AllowForwardedTraffic。</span><span class="sxs-lookup"><span data-stu-id="cbae6-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="cbae6-112">範例2：更新依物件的 vnet 對等 AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="cbae6-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="cbae6-113">這個命令會透過物件更新 vnet 對等的 AllowForwardedTraffic。</span><span class="sxs-lookup"><span data-stu-id="cbae6-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="cbae6-114">參數</span><span class="sxs-lookup"><span data-stu-id="cbae6-114">PARAMETERS</span></span>

### <span data-ttu-id="cbae6-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="cbae6-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="cbae6-116">[SwitchParameter] 在遠端虛擬網路中，是否允許或不允許從本機虛擬網路中的 Vm 轉寄流量。</span><span class="sxs-lookup"><span data-stu-id="cbae6-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbae6-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="cbae6-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="cbae6-118">[SwitchParameter] 如果您可以在遠端虛擬網路中使用閘道連結來連結到這個虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="cbae6-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbae6-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="cbae6-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="cbae6-120">[SwitchParameter] 您的本地虛擬網路空間中的 Vm 是否能夠存取遠端虛擬網路空間中的 Vm。</span><span class="sxs-lookup"><span data-stu-id="cbae6-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbae6-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbae6-121">-AsJob</span></span>
<span data-ttu-id="cbae6-122">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="cbae6-122">Run the command as a job</span></span>

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

### <span data-ttu-id="cbae6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbae6-123">-DefaultProfile</span></span>
<span data-ttu-id="cbae6-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cbae6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbae6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbae6-125">-InputObject</span></span>
<span data-ttu-id="cbae6-126">身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="cbae6-126">Identity parameter.</span></span>
<span data-ttu-id="cbae6-127">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cbae6-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbae6-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="cbae6-128">-Name</span></span>
<span data-ttu-id="cbae6-129">VNetPeering 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbae6-129">The name of the VNetPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PeeringName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbae6-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cbae6-130">-NoWait</span></span>
<span data-ttu-id="cbae6-131">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="cbae6-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cbae6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbae6-132">-ResourceGroupName</span></span>
<span data-ttu-id="cbae6-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbae6-133">The name of the resource group.</span></span>
<span data-ttu-id="cbae6-134">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="cbae6-134">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbae6-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cbae6-135">-SubscriptionId</span></span>
<span data-ttu-id="cbae6-136">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="cbae6-136">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbae6-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="cbae6-137">-UseRemoteGateway</span></span>
<span data-ttu-id="cbae6-138">[SwitchParameter] 如果遠端閘道可在這個虛擬網路上使用，則為 [系統管理]。</span><span class="sxs-lookup"><span data-stu-id="cbae6-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="cbae6-139">如果旗標設定為 true，且 allowGatewayTransit 在遠端對等也為 true，則虛擬網路將會使用遠端虛擬網路的閘道進行傳輸。</span><span class="sxs-lookup"><span data-stu-id="cbae6-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="cbae6-140">只有一個對等可以將此標誌設定為 true。</span><span class="sxs-lookup"><span data-stu-id="cbae6-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="cbae6-141">如果虛擬網路已有閘道，則無法設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="cbae6-141">This flag cannot be set if virtual network already has a gateway.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbae6-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cbae6-142">-WorkspaceName</span></span>
<span data-ttu-id="cbae6-143">工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbae6-143">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbae6-144">-確認</span><span class="sxs-lookup"><span data-stu-id="cbae6-144">-Confirm</span></span>
<span data-ttu-id="cbae6-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cbae6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbae6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbae6-146">-WhatIf</span></span>
<span data-ttu-id="cbae6-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cbae6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbae6-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbae6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbae6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbae6-149">CommonParameters</span></span>
<span data-ttu-id="cbae6-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cbae6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbae6-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cbae6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbae6-152">輸入</span><span class="sxs-lookup"><span data-stu-id="cbae6-152">INPUTS</span></span>

### <span data-ttu-id="cbae6-153">IDatabricksIdentity （Databricks）的</span><span class="sxs-lookup"><span data-stu-id="cbae6-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="cbae6-154">輸出</span><span class="sxs-lookup"><span data-stu-id="cbae6-154">OUTPUTS</span></span>

### <span data-ttu-id="cbae6-155">IVirtualNetworkPeering （Databricks）。 Api20180401。</span><span class="sxs-lookup"><span data-stu-id="cbae6-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="cbae6-156">筆記</span><span class="sxs-lookup"><span data-stu-id="cbae6-156">NOTES</span></span>

<span data-ttu-id="cbae6-157">別名</span><span class="sxs-lookup"><span data-stu-id="cbae6-157">ALIASES</span></span>

<span data-ttu-id="cbae6-158">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="cbae6-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cbae6-159">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="cbae6-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cbae6-160">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="cbae6-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cbae6-161">INPUTOBJECT <IDatabricksIdentity> ：身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="cbae6-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="cbae6-162">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="cbae6-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cbae6-163">`[PeeringName <String>]`： Workspace vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbae6-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="cbae6-164">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbae6-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cbae6-165">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="cbae6-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="cbae6-166">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbae6-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cbae6-167">`[WorkspaceName <String>]`：工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbae6-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="cbae6-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="cbae6-168">RELATED LINKS</span></span>

