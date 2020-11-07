---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/restart-azsinfrastructurerole
schema: 2.0.0
ms.openlocfilehash: 6e8b5f2dbfde62613a521fd7a49fba27c54ab498
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966746"
---
# <span data-ttu-id="92bcc-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="92bcc-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="92bcc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="92bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="92bcc-103">重新開機要求的基礎結構角色。</span><span class="sxs-lookup"><span data-stu-id="92bcc-103">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="92bcc-104">句法</span><span class="sxs-lookup"><span data-stu-id="92bcc-104">SYNTAX</span></span>

### <span data-ttu-id="92bcc-105">重新開機 (預設) </span><span class="sxs-lookup"><span data-stu-id="92bcc-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="92bcc-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="92bcc-106">RestartViaIdentity</span></span>
```
Restart-AzsInfrastructureRole -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="92bcc-107">說明</span><span class="sxs-lookup"><span data-stu-id="92bcc-107">DESCRIPTION</span></span>
<span data-ttu-id="92bcc-108">重新開機要求的基礎結構角色。</span><span class="sxs-lookup"><span data-stu-id="92bcc-108">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="92bcc-109">示例</span><span class="sxs-lookup"><span data-stu-id="92bcc-109">EXAMPLES</span></span>

### <span data-ttu-id="92bcc-110">範例1：</span><span class="sxs-lookup"><span data-stu-id="92bcc-110">Example 1:</span></span>
```powershell
PS C:\> Restart-AzsInfrastructureRole -Name "Compute Controller"

```

<span data-ttu-id="92bcc-111">重新開機已損壞的基礎結構角色。</span><span class="sxs-lookup"><span data-stu-id="92bcc-111">Restart an infrastructure role which has crashed.</span></span>



## <span data-ttu-id="92bcc-112">參數</span><span class="sxs-lookup"><span data-stu-id="92bcc-112">PARAMETERS</span></span>

### <span data-ttu-id="92bcc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92bcc-113">-AsJob</span></span>
<span data-ttu-id="92bcc-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="92bcc-114">Run the command as a job</span></span>

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

### <span data-ttu-id="92bcc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92bcc-115">-DefaultProfile</span></span>
<span data-ttu-id="92bcc-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92bcc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="92bcc-117">-Force</span></span>
<span data-ttu-id="92bcc-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="92bcc-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="92bcc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92bcc-119">-InputObject</span></span>
<span data-ttu-id="92bcc-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="92bcc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="92bcc-121">-位置</span><span class="sxs-lookup"><span data-stu-id="92bcc-121">-Location</span></span>
<span data-ttu-id="92bcc-122">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="92bcc-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92bcc-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="92bcc-123">-Name</span></span>
<span data-ttu-id="92bcc-124">結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-124">Infrastructure role name.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92bcc-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="92bcc-125">-NoWait</span></span>
<span data-ttu-id="92bcc-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="92bcc-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="92bcc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92bcc-127">-PassThru</span></span>
<span data-ttu-id="92bcc-128">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="92bcc-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="92bcc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92bcc-129">-ResourceGroupName</span></span>
<span data-ttu-id="92bcc-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92bcc-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92bcc-131">-SubscriptionId</span></span>
<span data-ttu-id="92bcc-132">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="92bcc-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="92bcc-133">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="92bcc-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="92bcc-134">-確認</span><span class="sxs-lookup"><span data-stu-id="92bcc-134">-Confirm</span></span>
<span data-ttu-id="92bcc-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="92bcc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92bcc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92bcc-136">-WhatIf</span></span>
<span data-ttu-id="92bcc-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="92bcc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92bcc-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92bcc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92bcc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92bcc-139">CommonParameters</span></span>
<span data-ttu-id="92bcc-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="92bcc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92bcc-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="92bcc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92bcc-142">輸入</span><span class="sxs-lookup"><span data-stu-id="92bcc-142">INPUTS</span></span>

### <span data-ttu-id="92bcc-143">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="92bcc-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="92bcc-144">輸出</span><span class="sxs-lookup"><span data-stu-id="92bcc-144">OUTPUTS</span></span>

### <span data-ttu-id="92bcc-145">System.object</span><span class="sxs-lookup"><span data-stu-id="92bcc-145">System.Boolean</span></span>



## <span data-ttu-id="92bcc-146">筆記</span><span class="sxs-lookup"><span data-stu-id="92bcc-146">NOTES</span></span>

<span data-ttu-id="92bcc-147">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="92bcc-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="92bcc-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="92bcc-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="92bcc-149">INPUTOBJECT <IFabricAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="92bcc-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="92bcc-150">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="92bcc-151">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="92bcc-152">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="92bcc-153">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="92bcc-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="92bcc-154">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="92bcc-155">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="92bcc-156">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="92bcc-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="92bcc-157">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="92bcc-158">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="92bcc-159">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="92bcc-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="92bcc-160">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="92bcc-161">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="92bcc-162">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="92bcc-163">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="92bcc-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="92bcc-164">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="92bcc-165">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="92bcc-166">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="92bcc-167">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="92bcc-168">`[StoragePool <String>]`：儲存池名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-168">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="92bcc-169">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-169">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="92bcc-170">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="92bcc-170">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="92bcc-171">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="92bcc-171">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="92bcc-172">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="92bcc-172">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="92bcc-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="92bcc-173">RELATED LINKS</span></span>

