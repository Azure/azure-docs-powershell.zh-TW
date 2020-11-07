---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4546be57a2a2bd7f3f450290be2e0bf144e09817
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966825"
---
# <span data-ttu-id="a099b-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="a099b-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="a099b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a099b-102">SYNOPSIS</span></span>
<span data-ttu-id="a099b-103">擴大比例單位。</span><span class="sxs-lookup"><span data-stu-id="a099b-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="a099b-104">句法</span><span class="sxs-lookup"><span data-stu-id="a099b-104">SYNTAX</span></span>

### <span data-ttu-id="a099b-105">ScaleExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="a099b-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-NodeList <IScaleOutScaleUnitParameters[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a099b-106">調整</span><span class="sxs-lookup"><span data-stu-id="a099b-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a099b-107">ScaleViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a099b-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a099b-108">ScaleViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a099b-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-NodeList <IScaleOutScaleUnitParameters[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a099b-109">說明</span><span class="sxs-lookup"><span data-stu-id="a099b-109">DESCRIPTION</span></span>
<span data-ttu-id="a099b-110">擴大比例單位。</span><span class="sxs-lookup"><span data-stu-id="a099b-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="a099b-111">示例</span><span class="sxs-lookup"><span data-stu-id="a099b-111">EXAMPLES</span></span>

### <span data-ttu-id="a099b-112">範例1： Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="a099b-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="a099b-113">將新的縮放比例單位節點新增至縮放比例單位分類。</span><span class="sxs-lookup"><span data-stu-id="a099b-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="a099b-114">參數</span><span class="sxs-lookup"><span data-stu-id="a099b-114">PARAMETERS</span></span>

### <span data-ttu-id="a099b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a099b-115">-AsJob</span></span>
<span data-ttu-id="a099b-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="a099b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a099b-117">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="a099b-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="a099b-118">[旗標] 表示該作業是否應該等到儲存之後，才能返回。</span><span class="sxs-lookup"><span data-stu-id="a099b-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a099b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a099b-119">-DefaultProfile</span></span>
<span data-ttu-id="a099b-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a099b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a099b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a099b-121">-InputObject</span></span>
<span data-ttu-id="a099b-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a099b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ScaleViaIdentity, ScaleViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a099b-123">-位置</span><span class="sxs-lookup"><span data-stu-id="a099b-123">-Location</span></span>
<span data-ttu-id="a099b-124">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="a099b-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a099b-125">-NodeList</span><span class="sxs-lookup"><span data-stu-id="a099b-125">-NodeList</span></span>
<span data-ttu-id="a099b-126">刻度單位中的節點清單。</span><span class="sxs-lookup"><span data-stu-id="a099b-126">List of nodes in the scale unit.</span></span>
<span data-ttu-id="a099b-127">若要建立，請參閱 NODELIST 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="a099b-127">To construct, see NOTES section for NODELIST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParameters[]
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a099b-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a099b-128">-NoWait</span></span>
<span data-ttu-id="a099b-129">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="a099b-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a099b-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a099b-130">-PassThru</span></span>
<span data-ttu-id="a099b-131">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="a099b-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a099b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a099b-132">-ResourceGroupName</span></span>
<span data-ttu-id="a099b-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a099b-134">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="a099b-134">-ScaleUnit</span></span>
<span data-ttu-id="a099b-135">縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-135">Name of the scale units.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a099b-136">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="a099b-136">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="a099b-137">可讓您新增一組比例單位節點的輸入資料清單。</span><span class="sxs-lookup"><span data-stu-id="a099b-137">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="a099b-138">若要建立，請參閱 SCALEUNITNODEPARAMETER 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="a099b-138">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList
Parameter Sets: Scale, ScaleViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a099b-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a099b-139">-SubscriptionId</span></span>
<span data-ttu-id="a099b-140">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a099b-140">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a099b-141">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="a099b-141">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a099b-142">-確認</span><span class="sxs-lookup"><span data-stu-id="a099b-142">-Confirm</span></span>
<span data-ttu-id="a099b-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a099b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a099b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a099b-144">-WhatIf</span></span>
<span data-ttu-id="a099b-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a099b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a099b-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a099b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a099b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a099b-147">CommonParameters</span></span>
<span data-ttu-id="a099b-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a099b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a099b-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a099b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a099b-150">輸入</span><span class="sxs-lookup"><span data-stu-id="a099b-150">INPUTS</span></span>

### <span data-ttu-id="a099b-151">IScaleOutScaleUnitParametersList （FabricAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="a099b-151">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="a099b-152">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="a099b-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="a099b-153">輸出</span><span class="sxs-lookup"><span data-stu-id="a099b-153">OUTPUTS</span></span>

### <span data-ttu-id="a099b-154">System.object</span><span class="sxs-lookup"><span data-stu-id="a099b-154">System.Boolean</span></span>



## <span data-ttu-id="a099b-155">筆記</span><span class="sxs-lookup"><span data-stu-id="a099b-155">NOTES</span></span>

<span data-ttu-id="a099b-156">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="a099b-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a099b-157">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a099b-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a099b-158">INPUTOBJECT <IFabricAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a099b-158">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a099b-159">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-159">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="a099b-160">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-160">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="a099b-161">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-161">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="a099b-162">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="a099b-162">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="a099b-163">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-163">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="a099b-164">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-164">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="a099b-165">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="a099b-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a099b-166">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-166">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="a099b-167">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-167">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="a099b-168">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="a099b-168">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="a099b-169">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-169">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="a099b-170">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-170">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="a099b-171">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-171">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="a099b-172">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="a099b-172">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="a099b-173">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-173">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="a099b-174">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-174">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="a099b-175">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-175">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="a099b-176">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-176">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="a099b-177">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-177">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="a099b-178">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a099b-178">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a099b-179">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="a099b-179">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a099b-180">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-180">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="a099b-181">NODELIST <IScaleOutScaleUnitParameters [] >：比例單位中的節點清單。</span><span class="sxs-lookup"><span data-stu-id="a099b-181">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="a099b-182">`[BmciPv4Address <String>]`：物理電腦的 BMC 位址。</span><span class="sxs-lookup"><span data-stu-id="a099b-182">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="a099b-183">`[ComputerName <String>]`：物理電腦的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-183">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="a099b-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> ：可讓您新增一組比例單位節點的輸入資料清單。</span><span class="sxs-lookup"><span data-stu-id="a099b-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="a099b-185">`[AwaitStorageConvergence <Boolean?>]`： [旗標] 表示該作業是否應該等到儲存之後才能返回。</span><span class="sxs-lookup"><span data-stu-id="a099b-185">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="a099b-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`：比例單位中的節點清單。</span><span class="sxs-lookup"><span data-stu-id="a099b-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="a099b-187">`[BmciPv4Address <String>]`：物理電腦的 BMC 位址。</span><span class="sxs-lookup"><span data-stu-id="a099b-187">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="a099b-188">`[ComputerName <String>]`：物理電腦的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="a099b-188">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="a099b-189">相關連結</span><span class="sxs-lookup"><span data-stu-id="a099b-189">RELATED LINKS</span></span>

