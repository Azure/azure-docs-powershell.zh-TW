---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/start-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: 922aea432548557857b627696e156c75a8e46157
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796490"
---
# <span data-ttu-id="fb524-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="fb524-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="fb524-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb524-102">SYNOPSIS</span></span>
<span data-ttu-id="fb524-103">開啟基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="fb524-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="fb524-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb524-104">SYNTAX</span></span>

### <span data-ttu-id="fb524-105">PowerOn (預設) </span><span class="sxs-lookup"><span data-stu-id="fb524-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fb524-106">PowerOnViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fb524-106">PowerOnViaIdentity</span></span>
```
Start-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fb524-107">說明</span><span class="sxs-lookup"><span data-stu-id="fb524-107">DESCRIPTION</span></span>
<span data-ttu-id="fb524-108">開啟基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="fb524-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="fb524-109">示例</span><span class="sxs-lookup"><span data-stu-id="fb524-109">EXAMPLES</span></span>

### <span data-ttu-id="fb524-110">範例1：</span><span class="sxs-lookup"><span data-stu-id="fb524-110">Example 1:</span></span>
```powershell
PS C:\> Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

```

<span data-ttu-id="fb524-111">開啟基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="fb524-111">Power on an infrastructure role instance.</span></span>


## <span data-ttu-id="fb524-112">參數</span><span class="sxs-lookup"><span data-stu-id="fb524-112">PARAMETERS</span></span>

### <span data-ttu-id="fb524-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb524-113">-AsJob</span></span>
<span data-ttu-id="fb524-114">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="fb524-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="fb524-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb524-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="fb524-116">-Force</span><span class="sxs-lookup"><span data-stu-id="fb524-116">-Force</span></span>
<span data-ttu-id="fb524-117">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="fb524-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="fb524-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb524-118">-InputObject</span></span>
<span data-ttu-id="fb524-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="fb524-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOnViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="fb524-120">-位置</span><span class="sxs-lookup"><span data-stu-id="fb524-120">-Location</span></span>
<span data-ttu-id="fb524-121">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="fb524-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fb524-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb524-122">-Name</span></span>
<span data-ttu-id="fb524-123">結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-123">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fb524-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fb524-124">-NoWait</span></span>
<span data-ttu-id="fb524-125">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="fb524-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fb524-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb524-126">-PassThru</span></span>
<span data-ttu-id="fb524-127">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="fb524-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fb524-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb524-128">-ResourceGroupName</span></span>
<span data-ttu-id="fb524-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-129">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fb524-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fb524-130">-SubscriptionId</span></span>
<span data-ttu-id="fb524-131">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="fb524-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fb524-132">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="fb524-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fb524-133">-確認</span><span class="sxs-lookup"><span data-stu-id="fb524-133">-Confirm</span></span>
<span data-ttu-id="fb524-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fb524-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb524-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb524-135">-WhatIf</span></span>
<span data-ttu-id="fb524-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fb524-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb524-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb524-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb524-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb524-138">CommonParameters</span></span>
<span data-ttu-id="fb524-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb524-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb524-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fb524-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb524-141">輸入</span><span class="sxs-lookup"><span data-stu-id="fb524-141">INPUTS</span></span>

### <span data-ttu-id="fb524-142">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="fb524-142">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="fb524-143">輸出</span><span class="sxs-lookup"><span data-stu-id="fb524-143">OUTPUTS</span></span>

### <span data-ttu-id="fb524-144">System.object</span><span class="sxs-lookup"><span data-stu-id="fb524-144">System.Boolean</span></span>



## <span data-ttu-id="fb524-145">筆記</span><span class="sxs-lookup"><span data-stu-id="fb524-145">NOTES</span></span>

<span data-ttu-id="fb524-146">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="fb524-146">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fb524-147">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="fb524-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="fb524-148">INPUTOBJECT <IFabricAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="fb524-148">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fb524-149">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-149">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="fb524-150">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-150">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="fb524-151">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-151">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="fb524-152">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="fb524-152">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="fb524-153">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-153">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="fb524-154">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-154">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="fb524-155">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="fb524-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fb524-156">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-156">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="fb524-157">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-157">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="fb524-158">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="fb524-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="fb524-159">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-159">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="fb524-160">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-160">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="fb524-161">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-161">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="fb524-162">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="fb524-162">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="fb524-163">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-163">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="fb524-164">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-164">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="fb524-165">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-165">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="fb524-166">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-166">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="fb524-167">`[StoragePool <String>]`：儲存池名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-167">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="fb524-168">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="fb524-169">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="fb524-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fb524-170">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="fb524-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="fb524-171">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb524-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="fb524-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb524-172">RELATED LINKS</span></span>

