---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 3f5adef6382038fdaf8c17620508b4a450ff74bc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968255"
---
# <span data-ttu-id="0ccc2-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="0ccc2-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="0ccc2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0ccc2-102">SYNOPSIS</span></span>
<span data-ttu-id="0ccc2-103">關閉刻度單位節點的電源。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="0ccc2-104">句法</span><span class="sxs-lookup"><span data-stu-id="0ccc2-104">SYNTAX</span></span>

### <span data-ttu-id="0ccc2-105">關機 (預設) </span><span class="sxs-lookup"><span data-stu-id="0ccc2-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0ccc2-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0ccc2-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0ccc2-107">立即</span><span class="sxs-lookup"><span data-stu-id="0ccc2-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0ccc2-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0ccc2-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0ccc2-109">說明</span><span class="sxs-lookup"><span data-stu-id="0ccc2-109">DESCRIPTION</span></span>
<span data-ttu-id="0ccc2-110">關閉刻度單位節點的電源。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="0ccc2-111">示例</span><span class="sxs-lookup"><span data-stu-id="0ccc2-111">EXAMPLES</span></span>

### <span data-ttu-id="0ccc2-112">範例1：</span><span class="sxs-lookup"><span data-stu-id="0ccc2-112">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="0ccc2-113">關閉比例單位節點的電源。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-113">Power down a scale unit node.</span></span>

### <span data-ttu-id="0ccc2-114">範例2：</span><span class="sxs-lookup"><span data-stu-id="0ccc2-114">Example 2:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="0ccc2-115">關閉比例單位節點的電源。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-115">Power down a scale unit node.</span></span> <span data-ttu-id="0ccc2-116">做為作業。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-116">As a job.</span></span>

## <span data-ttu-id="0ccc2-117">參數</span><span class="sxs-lookup"><span data-stu-id="0ccc2-117">PARAMETERS</span></span>

### <span data-ttu-id="0ccc2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ccc2-118">-AsJob</span></span>
<span data-ttu-id="0ccc2-119">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="0ccc2-119">Run the command as a job</span></span>

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

### <span data-ttu-id="0ccc2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ccc2-120">-DefaultProfile</span></span>
<span data-ttu-id="0ccc2-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ccc2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0ccc2-122">-Force</span></span>
<span data-ttu-id="0ccc2-123">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-123">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0ccc2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ccc2-124">-InputObject</span></span>
<span data-ttu-id="0ccc2-125">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0ccc2-126">-位置</span><span class="sxs-lookup"><span data-stu-id="0ccc2-126">-Location</span></span>
<span data-ttu-id="0ccc2-127">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-127">Location of the resource.</span></span>

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

### <span data-ttu-id="0ccc2-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="0ccc2-128">-Name</span></span>
<span data-ttu-id="0ccc2-129">結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-129">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="0ccc2-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0ccc2-130">-NoWait</span></span>
<span data-ttu-id="0ccc2-131">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="0ccc2-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0ccc2-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ccc2-132">-PassThru</span></span>
<span data-ttu-id="0ccc2-133">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="0ccc2-133">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0ccc2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ccc2-134">-ResourceGroupName</span></span>
<span data-ttu-id="0ccc2-135">[縮放單位] 節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-135">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="0ccc2-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ccc2-136">-SubscriptionId</span></span>
<span data-ttu-id="0ccc2-137">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0ccc2-138">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0ccc2-139">-確認</span><span class="sxs-lookup"><span data-stu-id="0ccc2-139">-Confirm</span></span>
<span data-ttu-id="0ccc2-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ccc2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ccc2-141">-WhatIf</span></span>
<span data-ttu-id="0ccc2-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ccc2-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ccc2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ccc2-144">CommonParameters</span></span>
<span data-ttu-id="0ccc2-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ccc2-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ccc2-147">輸入</span><span class="sxs-lookup"><span data-stu-id="0ccc2-147">INPUTS</span></span>

### <span data-ttu-id="0ccc2-148">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="0ccc2-148">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="0ccc2-149">輸出</span><span class="sxs-lookup"><span data-stu-id="0ccc2-149">OUTPUTS</span></span>

### <span data-ttu-id="0ccc2-150">System.object</span><span class="sxs-lookup"><span data-stu-id="0ccc2-150">System.Boolean</span></span>

## <span data-ttu-id="0ccc2-151">筆記</span><span class="sxs-lookup"><span data-stu-id="0ccc2-151">NOTES</span></span>

<span data-ttu-id="0ccc2-152">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ccc2-153">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0ccc2-154">INPUTOBJECT <IFabricAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="0ccc2-154">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0ccc2-155">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-155">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="0ccc2-156">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-156">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="0ccc2-157">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-157">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="0ccc2-158">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-158">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="0ccc2-159">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-159">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="0ccc2-160">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-160">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="0ccc2-161">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="0ccc2-161">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0ccc2-162">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-162">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="0ccc2-163">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-163">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="0ccc2-164">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-164">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="0ccc2-165">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-165">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="0ccc2-166">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-166">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="0ccc2-167">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-167">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="0ccc2-168">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-168">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="0ccc2-169">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-169">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="0ccc2-170">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-170">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="0ccc2-171">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-171">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="0ccc2-172">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-172">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="0ccc2-173">`[StoragePool <String>]`：儲存池名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-173">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="0ccc2-174">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-174">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="0ccc2-175">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-175">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0ccc2-176">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-176">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0ccc2-177">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ccc2-177">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="0ccc2-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ccc2-178">RELATED LINKS</span></span>
