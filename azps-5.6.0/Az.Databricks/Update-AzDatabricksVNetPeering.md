---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: 60d679cf8540e39d1be293a46f9e4e441e397627
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904474"
---
# <span data-ttu-id="2ef47-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="2ef47-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="2ef47-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2ef47-102">SYNOPSIS</span></span>
<span data-ttu-id="2ef47-103">更新工作區的 vNet 對等。</span><span class="sxs-lookup"><span data-stu-id="2ef47-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="2ef47-104">語法</span><span class="sxs-lookup"><span data-stu-id="2ef47-104">SYNTAX</span></span>

### <span data-ttu-id="2ef47-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="2ef47-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2ef47-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2ef47-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2ef47-107">描述</span><span class="sxs-lookup"><span data-stu-id="2ef47-107">DESCRIPTION</span></span>
<span data-ttu-id="2ef47-108">更新工作區的 vNet 對等。</span><span class="sxs-lookup"><span data-stu-id="2ef47-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="2ef47-109">例子</span><span class="sxs-lookup"><span data-stu-id="2ef47-109">EXAMPLES</span></span>

### <span data-ttu-id="2ef47-110">範例 1：更新 vnet 對等的 AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="2ef47-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="2ef47-111">此命令會更新 vnet 對等的 AllowForwardedTraffic。</span><span class="sxs-lookup"><span data-stu-id="2ef47-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="2ef47-112">範例 2：根據物件更新 vnet 對等的 AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="2ef47-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="2ef47-113">此命令會更新物件對等的 AllowForwardedTraffic。</span><span class="sxs-lookup"><span data-stu-id="2ef47-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="2ef47-114">參數</span><span class="sxs-lookup"><span data-stu-id="2ef47-114">PARAMETERS</span></span>

### <span data-ttu-id="2ef47-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="2ef47-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="2ef47-116">[System.Management.Automation.SwitchParameter] 遠端虛擬網路中是否允許/不允許來自本地虛擬網路中之虛擬機器的轉轉流量。</span><span class="sxs-lookup"><span data-stu-id="2ef47-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="2ef47-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="2ef47-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="2ef47-118">[System.Management.Automation.SwitchParameter] 如果閘道連結可用於遠端虛擬網路以連結至此虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="2ef47-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="2ef47-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="2ef47-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="2ef47-120">[System.Management.Automation.SwitchParameter] 本地虛擬網路空間的虛擬機器是否能存取遠端虛擬網路空間的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2ef47-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="2ef47-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ef47-121">-AsJob</span></span>
<span data-ttu-id="2ef47-122">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="2ef47-122">Run the command as a job</span></span>

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

### <span data-ttu-id="2ef47-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ef47-123">-DefaultProfile</span></span>
<span data-ttu-id="2ef47-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ef47-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ef47-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ef47-125">-InputObject</span></span>
<span data-ttu-id="2ef47-126">身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="2ef47-126">Identity parameter.</span></span>
<span data-ttu-id="2ef47-127">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2ef47-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2ef47-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ef47-128">-Name</span></span>
<span data-ttu-id="2ef47-129">VNetPeering 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ef47-129">The name of the VNetPeering.</span></span>

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

### <span data-ttu-id="2ef47-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2ef47-130">-NoWait</span></span>
<span data-ttu-id="2ef47-131">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="2ef47-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2ef47-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ef47-132">-ResourceGroupName</span></span>
<span data-ttu-id="2ef47-133">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ef47-133">The name of the resource group.</span></span>
<span data-ttu-id="2ef47-134">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2ef47-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2ef47-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ef47-135">-SubscriptionId</span></span>
<span data-ttu-id="2ef47-136">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2ef47-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2ef47-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="2ef47-137">-UseRemoteGateway</span></span>
<span data-ttu-id="2ef47-138">[System.Management.Automation.SwitchParameter] 如果遠端閘道可以在此虛擬網路上使用。</span><span class="sxs-lookup"><span data-stu-id="2ef47-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="2ef47-139">如果旗標設定為 True，且遠端對等上的 allowGatewayTransit 也為 True，則虛擬網路會使用遠端虛擬網路的閘道進行傳輸。</span><span class="sxs-lookup"><span data-stu-id="2ef47-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="2ef47-140">只有一個對等可以設定此旗標為 True。</span><span class="sxs-lookup"><span data-stu-id="2ef47-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="2ef47-141">如果虛擬網路已經有閘道，就無法設定此標號。</span><span class="sxs-lookup"><span data-stu-id="2ef47-141">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="2ef47-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2ef47-142">-WorkspaceName</span></span>
<span data-ttu-id="2ef47-143">工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ef47-143">The name of the workspace.</span></span>

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

### <span data-ttu-id="2ef47-144">-確認</span><span class="sxs-lookup"><span data-stu-id="2ef47-144">-Confirm</span></span>
<span data-ttu-id="2ef47-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2ef47-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ef47-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ef47-146">-WhatIf</span></span>
<span data-ttu-id="2ef47-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2ef47-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ef47-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ef47-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ef47-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ef47-149">CommonParameters</span></span>
<span data-ttu-id="2ef47-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2ef47-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ef47-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ef47-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ef47-152">輸入</span><span class="sxs-lookup"><span data-stu-id="2ef47-152">INPUTS</span></span>

### <span data-ttu-id="2ef47-153">Microsoft.Azure.PowerShell.Cmdlets.Databuvs.models.IDatab一sIdentity</span><span class="sxs-lookup"><span data-stu-id="2ef47-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="2ef47-154">輸出</span><span class="sxs-lookup"><span data-stu-id="2ef47-154">OUTPUTS</span></span>

### <span data-ttu-id="2ef47-155">Microsoft.Azure.PowerShell.Cmdlets.Databworks.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2ef47-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="2ef47-156">筆記</span><span class="sxs-lookup"><span data-stu-id="2ef47-156">NOTES</span></span>

<span data-ttu-id="2ef47-157">別名</span><span class="sxs-lookup"><span data-stu-id="2ef47-157">ALIASES</span></span>

<span data-ttu-id="2ef47-158">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2ef47-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2ef47-159">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2ef47-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2ef47-160">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2ef47-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2ef47-161">INPUTOBJECT： <IDatabricksIdentity> 身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="2ef47-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="2ef47-162">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="2ef47-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2ef47-163">`[PeeringName <String>]`：工作區 vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ef47-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="2ef47-164">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ef47-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2ef47-165">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2ef47-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="2ef47-166">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2ef47-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2ef47-167">`[WorkspaceName <String>]`：工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ef47-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="2ef47-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ef47-168">RELATED LINKS</span></span>

