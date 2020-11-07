---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/repair-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: b9a285e650f0ed47dd0144a460b324ecdae49f7d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968593"
---
# <span data-ttu-id="cb557-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="cb557-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="cb557-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb557-102">SYNOPSIS</span></span>
<span data-ttu-id="cb557-103">修復叢集節點。</span><span class="sxs-lookup"><span data-stu-id="cb557-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="cb557-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb557-104">SYNTAX</span></span>

### <span data-ttu-id="cb557-105">RepairExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="cb557-105">RepairExpanded (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-BiosVersion <String>] [-BmciPv4Address <String>] [-ClusterName <String>]
 [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>] [-SerialNumber <String>]
 [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cb557-106">維修中心</span><span class="sxs-lookup"><span data-stu-id="cb557-106">Repair</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BareMetalNode <IBareMetalNodeDescription> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cb557-107">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cb557-107">RepairViaIdentity</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> -BareMetalNode <IBareMetalNodeDescription>
 [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cb557-108">RepairViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cb557-108">RepairViaIdentityExpanded</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-BiosVersion <String>] [-BmciPv4Address <String>]
 [-ClusterName <String>] [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>]
 [-SerialNumber <String>] [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cb557-109">說明</span><span class="sxs-lookup"><span data-stu-id="cb557-109">DESCRIPTION</span></span>
<span data-ttu-id="cb557-110">修復叢集節點。</span><span class="sxs-lookup"><span data-stu-id="cb557-110">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="cb557-111">示例</span><span class="sxs-lookup"><span data-stu-id="cb557-111">EXAMPLES</span></span>

### <span data-ttu-id="cb557-112">範例1：</span><span class="sxs-lookup"><span data-stu-id="cb557-112">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***

```

<span data-ttu-id="cb557-113">修復 [縮放單位] 節點。</span><span class="sxs-lookup"><span data-stu-id="cb557-113">Repair a scale unit node.</span></span>


## <span data-ttu-id="cb557-114">參數</span><span class="sxs-lookup"><span data-stu-id="cb557-114">PARAMETERS</span></span>

### <span data-ttu-id="cb557-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb557-115">-AsJob</span></span>
<span data-ttu-id="cb557-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="cb557-116">Run the command as a job</span></span>

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

### <span data-ttu-id="cb557-117">-BareMetalNode</span><span class="sxs-lookup"><span data-stu-id="cb557-117">-BareMetalNode</span></span>
<span data-ttu-id="cb557-118">在群集上用於 ScaleOut 操作的裸機節點描述。</span><span class="sxs-lookup"><span data-stu-id="cb557-118">Description of a bare metal node used for ScaleOut operation on a cluster.</span></span>
<span data-ttu-id="cb557-119">若要建立，請參閱 BAREMETALNODE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="cb557-119">To construct, see NOTES section for BAREMETALNODE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription
Parameter Sets: Repair, RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="cb557-120">-BiosVersion</span><span class="sxs-lookup"><span data-stu-id="cb557-120">-BiosVersion</span></span>
<span data-ttu-id="cb557-121">物理電腦的 Bios 版本。</span><span class="sxs-lookup"><span data-stu-id="cb557-121">Bios version of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cb557-122">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="cb557-122">-BmciPv4Address</span></span>
<span data-ttu-id="cb557-123">物理電腦的 BMC 位址。</span><span class="sxs-lookup"><span data-stu-id="cb557-123">BMC address of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cb557-124">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cb557-124">-ClusterName</span></span>
<span data-ttu-id="cb557-125">群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-125">Name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cb557-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="cb557-126">-ComputerName</span></span>
<span data-ttu-id="cb557-127">電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-127">Name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cb557-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb557-128">-DefaultProfile</span></span>
<span data-ttu-id="cb557-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb557-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb557-130">-Force</span><span class="sxs-lookup"><span data-stu-id="cb557-130">-Force</span></span>
<span data-ttu-id="cb557-131">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="cb557-131">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cb557-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb557-132">-InputObject</span></span>
<span data-ttu-id="cb557-133">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cb557-133">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RepairViaIdentity, RepairViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="cb557-134">-位置</span><span class="sxs-lookup"><span data-stu-id="cb557-134">-Location</span></span>
<span data-ttu-id="cb557-135">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="cb557-135">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cb557-136">-MacAddress</span><span class="sxs-lookup"><span data-stu-id="cb557-136">-MacAddress</span></span>
<span data-ttu-id="cb557-137">裸機節點之 MAC 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-137">Name of the MAC address of the bare metal node.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cb557-138">-模型</span><span class="sxs-lookup"><span data-stu-id="cb557-138">-Model</span></span>
<span data-ttu-id="cb557-139">物理電腦的模型。</span><span class="sxs-lookup"><span data-stu-id="cb557-139">Model of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cb557-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb557-140">-Name</span></span>
<span data-ttu-id="cb557-141">[縮放單位] 節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-141">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cb557-142">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cb557-142">-NoWait</span></span>
<span data-ttu-id="cb557-143">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="cb557-143">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cb557-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb557-144">-PassThru</span></span>
<span data-ttu-id="cb557-145">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="cb557-145">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cb557-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb557-146">-ResourceGroupName</span></span>
<span data-ttu-id="cb557-147">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-147">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cb557-148">-SerialNumber</span><span class="sxs-lookup"><span data-stu-id="cb557-148">-SerialNumber</span></span>
<span data-ttu-id="cb557-149">物理電腦的序列值。</span><span class="sxs-lookup"><span data-stu-id="cb557-149">Serial number of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cb557-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb557-150">-SubscriptionId</span></span>
<span data-ttu-id="cb557-151">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="cb557-151">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cb557-152">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="cb557-152">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cb557-153">-供應商</span><span class="sxs-lookup"><span data-stu-id="cb557-153">-Vendor</span></span>
<span data-ttu-id="cb557-154">物理電腦的供應商。</span><span class="sxs-lookup"><span data-stu-id="cb557-154">Vendor of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cb557-155">-確認</span><span class="sxs-lookup"><span data-stu-id="cb557-155">-Confirm</span></span>
<span data-ttu-id="cb557-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb557-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb557-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb557-157">-WhatIf</span></span>
<span data-ttu-id="cb557-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb557-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb557-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb557-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb557-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb557-160">CommonParameters</span></span>
<span data-ttu-id="cb557-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb557-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb557-162">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cb557-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb557-163">輸入</span><span class="sxs-lookup"><span data-stu-id="cb557-163">INPUTS</span></span>

### <span data-ttu-id="cb557-164">IBareMetalNodeDescription （FabricAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="cb557-164">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription</span></span>

### <span data-ttu-id="cb557-165">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="cb557-165">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="cb557-166">輸出</span><span class="sxs-lookup"><span data-stu-id="cb557-166">OUTPUTS</span></span>

### <span data-ttu-id="cb557-167">System.object</span><span class="sxs-lookup"><span data-stu-id="cb557-167">System.Boolean</span></span>



## <span data-ttu-id="cb557-168">筆記</span><span class="sxs-lookup"><span data-stu-id="cb557-168">NOTES</span></span>

<span data-ttu-id="cb557-169">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="cb557-169">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb557-170">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="cb557-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cb557-171">BAREMETALNODE <IBareMetalNodeDescription> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="cb557-171">BAREMETALNODE <IBareMetalNodeDescription>: Identity Parameter</span></span>
  - <span data-ttu-id="cb557-172">`[BiosVersion <String>]`： Bios 版本的物理電腦。</span><span class="sxs-lookup"><span data-stu-id="cb557-172">`[BiosVersion <String>]`: Bios version of the physical machine.</span></span>
  - <span data-ttu-id="cb557-173">`[BmciPv4Address <String>]`：物理電腦的 BMC 位址。</span><span class="sxs-lookup"><span data-stu-id="cb557-173">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="cb557-174">`[ClusterName <String>]`：群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-174">`[ClusterName <String>]`: Name of the cluster.</span></span>
  - <span data-ttu-id="cb557-175">`[ComputerName <String>]`：電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-175">`[ComputerName <String>]`: Name of the computer.</span></span>
  - <span data-ttu-id="cb557-176">`[MacAddress <String>]`：裸機節點之 MAC 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-176">`[MacAddress <String>]`: Name of the MAC address of the bare metal node.</span></span>
  - <span data-ttu-id="cb557-177">`[Model <String>]`：物理電腦的模型。</span><span class="sxs-lookup"><span data-stu-id="cb557-177">`[Model <String>]`: Model of the physical machine.</span></span>
  - <span data-ttu-id="cb557-178">`[SerialNumber <String>]`：物理電腦的序列值。</span><span class="sxs-lookup"><span data-stu-id="cb557-178">`[SerialNumber <String>]`: Serial number of the physical machine.</span></span>
  - <span data-ttu-id="cb557-179">`[Vendor <String>]`：物理電腦的廠商。</span><span class="sxs-lookup"><span data-stu-id="cb557-179">`[Vendor <String>]`: Vendor of the physical machine.</span></span>

<span data-ttu-id="cb557-180">INPUTOBJECT <IFabricAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="cb557-180">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cb557-181">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-181">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="cb557-182">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-182">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="cb557-183">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-183">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="cb557-184">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="cb557-184">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="cb557-185">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-185">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="cb557-186">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-186">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="cb557-187">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="cb557-187">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cb557-188">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-188">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="cb557-189">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-189">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="cb557-190">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="cb557-190">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="cb557-191">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-191">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="cb557-192">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-192">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="cb557-193">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-193">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="cb557-194">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="cb557-194">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="cb557-195">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-195">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="cb557-196">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-196">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="cb557-197">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-197">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="cb557-198">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-198">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="cb557-199">`[StoragePool <String>]`：儲存池名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-199">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="cb557-200">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-200">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="cb557-201">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="cb557-201">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cb557-202">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="cb557-202">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cb557-203">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb557-203">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="cb557-204">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb557-204">RELATED LINKS</span></span>

