---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/start-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: c8b1ed8ea0be65e92022cf1ac759024a07fc76c4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968144"
---
# <span data-ttu-id="cdb46-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="cdb46-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="cdb46-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cdb46-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb46-103">開啟 [縮放單元] 節點。</span><span class="sxs-lookup"><span data-stu-id="cdb46-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="cdb46-104">句法</span><span class="sxs-lookup"><span data-stu-id="cdb46-104">SYNTAX</span></span>

### <span data-ttu-id="cdb46-105">PowerOn (預設) </span><span class="sxs-lookup"><span data-stu-id="cdb46-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cdb46-106">PowerOnViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cdb46-106">PowerOnViaIdentity</span></span>
```
Start-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cdb46-107">說明</span><span class="sxs-lookup"><span data-stu-id="cdb46-107">DESCRIPTION</span></span>
<span data-ttu-id="cdb46-108">開啟 [縮放單元] 節點。</span><span class="sxs-lookup"><span data-stu-id="cdb46-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="cdb46-109">示例</span><span class="sxs-lookup"><span data-stu-id="cdb46-109">EXAMPLES</span></span>

### <span data-ttu-id="cdb46-110">範例1：</span><span class="sxs-lookup"><span data-stu-id="cdb46-110">Example 1:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="cdb46-111">開啟 [縮放單元] 節點。</span><span class="sxs-lookup"><span data-stu-id="cdb46-111">Power on a scale unit node.</span></span>

### <span data-ttu-id="cdb46-112">範例2：</span><span class="sxs-lookup"><span data-stu-id="cdb46-112">Example 2:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="cdb46-113">開啟 [縮放單元] 節點。</span><span class="sxs-lookup"><span data-stu-id="cdb46-113">Power on a scale unit node.</span></span> <span data-ttu-id="cdb46-114">做為作業。</span><span class="sxs-lookup"><span data-stu-id="cdb46-114">As a job.</span></span>

## <span data-ttu-id="cdb46-115">參數</span><span class="sxs-lookup"><span data-stu-id="cdb46-115">PARAMETERS</span></span>

### <span data-ttu-id="cdb46-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cdb46-116">-AsJob</span></span>
<span data-ttu-id="cdb46-117">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="cdb46-117">Run the command as a job</span></span>

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

### <span data-ttu-id="cdb46-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb46-118">-DefaultProfile</span></span>
<span data-ttu-id="cdb46-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdb46-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cdb46-120">-Force</span></span>
<span data-ttu-id="cdb46-121">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="cdb46-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cdb46-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdb46-122">-InputObject</span></span>
<span data-ttu-id="cdb46-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cdb46-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cdb46-124">-位置</span><span class="sxs-lookup"><span data-stu-id="cdb46-124">-Location</span></span>
<span data-ttu-id="cdb46-125">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="cdb46-125">Location of the resource.</span></span>

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

### <span data-ttu-id="cdb46-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="cdb46-126">-Name</span></span>
<span data-ttu-id="cdb46-127">[縮放單位] 節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-127">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="cdb46-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cdb46-128">-NoWait</span></span>
<span data-ttu-id="cdb46-129">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="cdb46-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cdb46-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdb46-130">-PassThru</span></span>
<span data-ttu-id="cdb46-131">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="cdb46-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cdb46-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdb46-132">-ResourceGroupName</span></span>
<span data-ttu-id="cdb46-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="cdb46-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cdb46-134">-SubscriptionId</span></span>
<span data-ttu-id="cdb46-135">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="cdb46-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cdb46-136">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="cdb46-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cdb46-137">-確認</span><span class="sxs-lookup"><span data-stu-id="cdb46-137">-Confirm</span></span>
<span data-ttu-id="cdb46-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cdb46-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdb46-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdb46-139">-WhatIf</span></span>
<span data-ttu-id="cdb46-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cdb46-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdb46-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cdb46-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdb46-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb46-142">CommonParameters</span></span>
<span data-ttu-id="cdb46-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cdb46-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb46-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cdb46-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb46-145">輸入</span><span class="sxs-lookup"><span data-stu-id="cdb46-145">INPUTS</span></span>

### <span data-ttu-id="cdb46-146">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="cdb46-146">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="cdb46-147">輸出</span><span class="sxs-lookup"><span data-stu-id="cdb46-147">OUTPUTS</span></span>

### <span data-ttu-id="cdb46-148">System.object</span><span class="sxs-lookup"><span data-stu-id="cdb46-148">System.Boolean</span></span>

## <span data-ttu-id="cdb46-149">筆記</span><span class="sxs-lookup"><span data-stu-id="cdb46-149">NOTES</span></span>

<span data-ttu-id="cdb46-150">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="cdb46-150">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cdb46-151">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="cdb46-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cdb46-152">INPUTOBJECT <IFabricAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="cdb46-152">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cdb46-153">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-153">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="cdb46-154">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-154">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="cdb46-155">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-155">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="cdb46-156">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="cdb46-156">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="cdb46-157">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-157">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="cdb46-158">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-158">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="cdb46-159">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="cdb46-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cdb46-160">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-160">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="cdb46-161">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-161">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="cdb46-162">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="cdb46-162">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="cdb46-163">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-163">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="cdb46-164">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-164">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="cdb46-165">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-165">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="cdb46-166">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="cdb46-166">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="cdb46-167">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-167">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="cdb46-168">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-168">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="cdb46-169">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-169">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="cdb46-170">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-170">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="cdb46-171">`[StoragePool <String>]`：儲存池名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-171">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="cdb46-172">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-172">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="cdb46-173">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="cdb46-173">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cdb46-174">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="cdb46-174">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cdb46-175">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb46-175">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="cdb46-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="cdb46-176">RELATED LINKS</span></span>
