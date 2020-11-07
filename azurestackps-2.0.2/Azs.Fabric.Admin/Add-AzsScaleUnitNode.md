---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: fe7726c25ee9dd83ca940b4ac6e47b3cc26a6457
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968159"
---
# <span data-ttu-id="5d5d2-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="5d5d2-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="5d5d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5d5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="5d5d2-103">擴大比例單位。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="5d5d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="5d5d2-104">SYNTAX</span></span>

### <span data-ttu-id="5d5d2-105">ScaleExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="5d5d2-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-BmciPv4Address <String>] [-ComputerName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5d5d2-106">調整</span><span class="sxs-lookup"><span data-stu-id="5d5d2-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5d5d2-107">ScaleViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5d5d2-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5d5d2-108">ScaleViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5d5d2-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-BmciPv4Address <String>] [-ComputerName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5d5d2-109">說明</span><span class="sxs-lookup"><span data-stu-id="5d5d2-109">DESCRIPTION</span></span>
<span data-ttu-id="5d5d2-110">擴大比例單位。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="5d5d2-111">示例</span><span class="sxs-lookup"><span data-stu-id="5d5d2-111">EXAMPLES</span></span>

### <span data-ttu-id="5d5d2-112">範例1： Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="5d5d2-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -BmciPv4Address $BmciPv4Address -ComputerName $ComputerName -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="5d5d2-113">將新的縮放比例單位節點新增至縮放比例單位分類。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="5d5d2-114">參數</span><span class="sxs-lookup"><span data-stu-id="5d5d2-114">PARAMETERS</span></span>

### <span data-ttu-id="5d5d2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d5d2-115">-AsJob</span></span>
<span data-ttu-id="5d5d2-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="5d5d2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5d5d2-117">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="5d5d2-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="5d5d2-118">[旗標] 表示該作業是否應該等到儲存之後，才能返回。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="5d5d2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d5d2-119">-DefaultProfile</span></span>
<span data-ttu-id="5d5d2-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d5d2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d5d2-121">-InputObject</span></span>
<span data-ttu-id="5d5d2-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5d5d2-123">-位置</span><span class="sxs-lookup"><span data-stu-id="5d5d2-123">-Location</span></span>
<span data-ttu-id="5d5d2-124">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-124">Location of the resource.</span></span>

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

### <span data-ttu-id="5d5d2-125">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="5d5d2-125">-BmciPv4Address</span></span> 
<span data-ttu-id="5d5d2-126">物理電腦的 BMC 位址。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-126">BMC address of the physical machine.</span></span>

### <span data-ttu-id="5d5d2-127">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="5d5d2-127">-ComputerName</span></span> 
<span data-ttu-id="5d5d2-128">物理電腦的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-128">Computer name of the physical machine.</span></span>

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

### <span data-ttu-id="5d5d2-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5d5d2-129">-NoWait</span></span>
<span data-ttu-id="5d5d2-130">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="5d5d2-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5d5d2-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d5d2-131">-PassThru</span></span>
<span data-ttu-id="5d5d2-132">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="5d5d2-132">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5d5d2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d5d2-133">-ResourceGroupName</span></span>
<span data-ttu-id="5d5d2-134">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-134">Name of the resource group.</span></span>

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

### <span data-ttu-id="5d5d2-135">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="5d5d2-135">-ScaleUnit</span></span>
<span data-ttu-id="5d5d2-136">縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-136">Name of the scale units.</span></span>

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

### <span data-ttu-id="5d5d2-137">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="5d5d2-137">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="5d5d2-138">可讓您新增一組比例單位節點的輸入資料清單。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-138">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="5d5d2-139">若要建立，請參閱 SCALEUNITNODEPARAMETER 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-139">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="5d5d2-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d5d2-140">-SubscriptionId</span></span>
<span data-ttu-id="5d5d2-141">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-141">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5d5d2-142">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-142">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5d5d2-143">-確認</span><span class="sxs-lookup"><span data-stu-id="5d5d2-143">-Confirm</span></span>
<span data-ttu-id="5d5d2-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d5d2-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d5d2-145">-WhatIf</span></span>
<span data-ttu-id="5d5d2-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d5d2-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d5d2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d5d2-148">CommonParameters</span></span>
<span data-ttu-id="5d5d2-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d5d2-150">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d5d2-151">輸入</span><span class="sxs-lookup"><span data-stu-id="5d5d2-151">INPUTS</span></span>

### <span data-ttu-id="5d5d2-152">IScaleOutScaleUnitParametersList （FabricAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="5d5d2-153">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="5d5d2-153">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="5d5d2-154">輸出</span><span class="sxs-lookup"><span data-stu-id="5d5d2-154">OUTPUTS</span></span>

### <span data-ttu-id="5d5d2-155">System.object</span><span class="sxs-lookup"><span data-stu-id="5d5d2-155">System.Boolean</span></span>

## <span data-ttu-id="5d5d2-156">筆記</span><span class="sxs-lookup"><span data-stu-id="5d5d2-156">NOTES</span></span>

<span data-ttu-id="5d5d2-157">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-157">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5d5d2-158">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5d5d2-159">INPUTOBJECT <IFabricAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5d5d2-159">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5d5d2-160">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-160">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="5d5d2-161">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-161">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="5d5d2-162">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-162">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="5d5d2-163">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-163">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="5d5d2-164">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-164">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="5d5d2-165">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-165">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="5d5d2-166">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="5d5d2-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5d5d2-167">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-167">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="5d5d2-168">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-168">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="5d5d2-169">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-169">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="5d5d2-170">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-170">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="5d5d2-171">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-171">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="5d5d2-172">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-172">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="5d5d2-173">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-173">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="5d5d2-174">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-174">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="5d5d2-175">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-175">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="5d5d2-176">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-176">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="5d5d2-177">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-177">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="5d5d2-178">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-178">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="5d5d2-179">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5d5d2-180">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5d5d2-181">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-181">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="5d5d2-182">NODELIST <IScaleOutScaleUnitParameters [] >：比例單位中的節點清單。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-182">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="5d5d2-183">`[BmciPv4Address <String>]`：物理電腦的 BMC 位址。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-183">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="5d5d2-184">`[ComputerName <String>]`：物理電腦的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-184">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="5d5d2-185">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> ：可讓您新增一組比例單位節點的輸入資料清單。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-185">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="5d5d2-186">`[AwaitStorageConvergence <Boolean?>]`： [旗標] 表示該作業是否應該等到儲存之後才能返回。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-186">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="5d5d2-187">`[NodeList <IScaleOutScaleUnitParameters[]>]`：比例單位中的節點清單。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-187">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="5d5d2-188">`[BmciPv4Address <String>]`：物理電腦的 BMC 位址。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-188">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="5d5d2-189">`[ComputerName <String>]`：物理電腦的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="5d5d2-189">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="5d5d2-190">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d5d2-190">RELATED LINKS</span></span>
