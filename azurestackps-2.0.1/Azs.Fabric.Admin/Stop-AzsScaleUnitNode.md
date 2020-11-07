---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d413d7da00fe18de804306d0cfaa1ccade0e2650
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966655"
---
# <span data-ttu-id="25657-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="25657-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="25657-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25657-102">SYNOPSIS</span></span>
<span data-ttu-id="25657-103">關閉刻度單位節點的電源。</span><span class="sxs-lookup"><span data-stu-id="25657-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="25657-104">句法</span><span class="sxs-lookup"><span data-stu-id="25657-104">SYNTAX</span></span>

### <span data-ttu-id="25657-105">關機 (預設) </span><span class="sxs-lookup"><span data-stu-id="25657-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="25657-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="25657-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="25657-107">立即</span><span class="sxs-lookup"><span data-stu-id="25657-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="25657-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="25657-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="25657-109">說明</span><span class="sxs-lookup"><span data-stu-id="25657-109">DESCRIPTION</span></span>
<span data-ttu-id="25657-110">關閉刻度單位節點的電源。</span><span class="sxs-lookup"><span data-stu-id="25657-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="25657-111">示例</span><span class="sxs-lookup"><span data-stu-id="25657-111">EXAMPLES</span></span>

### <span data-ttu-id="25657-112">範例1： {{在此加入標題}}</span><span class="sxs-lookup"><span data-stu-id="25657-112">Example 1: {{ Add title here }}</span></span>
```powershell
PS C:\> Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"

```

<span data-ttu-id="25657-113">關閉基礎結構角色實例的電源。</span><span class="sxs-lookup"><span data-stu-id="25657-113">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="25657-114">參數</span><span class="sxs-lookup"><span data-stu-id="25657-114">PARAMETERS</span></span>

### <span data-ttu-id="25657-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25657-115">-AsJob</span></span>
<span data-ttu-id="25657-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="25657-116">Run the command as a job</span></span>

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

### <span data-ttu-id="25657-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25657-117">-DefaultProfile</span></span>
<span data-ttu-id="25657-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="25657-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25657-119">-Force</span><span class="sxs-lookup"><span data-stu-id="25657-119">-Force</span></span>
<span data-ttu-id="25657-120">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="25657-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="25657-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25657-121">-InputObject</span></span>
<span data-ttu-id="25657-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="25657-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOffViaIdentity, ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="25657-123">-位置</span><span class="sxs-lookup"><span data-stu-id="25657-123">-Location</span></span>
<span data-ttu-id="25657-124">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="25657-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="25657-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="25657-125">-Name</span></span>
<span data-ttu-id="25657-126">結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-126">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="25657-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="25657-127">-NoWait</span></span>
<span data-ttu-id="25657-128">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="25657-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="25657-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25657-129">-PassThru</span></span>
<span data-ttu-id="25657-130">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="25657-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="25657-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25657-131">-ResourceGroupName</span></span>
<span data-ttu-id="25657-132">[縮放單位] 節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-132">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="25657-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25657-133">-SubscriptionId</span></span>
<span data-ttu-id="25657-134">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="25657-134">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="25657-135">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="25657-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="25657-136">-確認</span><span class="sxs-lookup"><span data-stu-id="25657-136">-Confirm</span></span>
<span data-ttu-id="25657-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="25657-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25657-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25657-138">-WhatIf</span></span>
<span data-ttu-id="25657-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="25657-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25657-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25657-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25657-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25657-141">CommonParameters</span></span>
<span data-ttu-id="25657-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25657-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25657-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="25657-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25657-144">輸入</span><span class="sxs-lookup"><span data-stu-id="25657-144">INPUTS</span></span>

### <span data-ttu-id="25657-145">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="25657-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="25657-146">輸出</span><span class="sxs-lookup"><span data-stu-id="25657-146">OUTPUTS</span></span>

### <span data-ttu-id="25657-147">System.object</span><span class="sxs-lookup"><span data-stu-id="25657-147">System.Boolean</span></span>



## <span data-ttu-id="25657-148">筆記</span><span class="sxs-lookup"><span data-stu-id="25657-148">NOTES</span></span>

<span data-ttu-id="25657-149">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="25657-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="25657-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="25657-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="25657-151">INPUTOBJECT <IFabricAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="25657-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="25657-152">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="25657-153">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="25657-154">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="25657-155">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="25657-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="25657-156">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="25657-157">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="25657-158">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="25657-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="25657-159">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="25657-160">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="25657-161">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="25657-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="25657-162">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="25657-163">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="25657-164">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="25657-165">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="25657-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="25657-166">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="25657-167">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="25657-168">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="25657-169">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="25657-170">`[StoragePool <String>]`：儲存池名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-170">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="25657-171">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-171">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="25657-172">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="25657-172">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="25657-173">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="25657-173">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="25657-174">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="25657-174">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="25657-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="25657-175">RELATED LINKS</span></span>

