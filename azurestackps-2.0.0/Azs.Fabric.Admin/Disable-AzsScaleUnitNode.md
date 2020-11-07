---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/disable-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 532ca56646ae2cfa25f6e3480f9f924d918cfedc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794928"
---
# <span data-ttu-id="9f54a-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="9f54a-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="9f54a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9f54a-102">SYNOPSIS</span></span>


## <span data-ttu-id="9f54a-103">句法</span><span class="sxs-lookup"><span data-stu-id="9f54a-103">SYNTAX</span></span>

### <span data-ttu-id="9f54a-104">停止 (預設) </span><span class="sxs-lookup"><span data-stu-id="9f54a-104">Stop (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9f54a-105">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9f54a-105">StopViaIdentity</span></span>
```
Disable-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9f54a-106">說明</span><span class="sxs-lookup"><span data-stu-id="9f54a-106">DESCRIPTION</span></span>


## <span data-ttu-id="9f54a-107">示例</span><span class="sxs-lookup"><span data-stu-id="9f54a-107">EXAMPLES</span></span>

### <span data-ttu-id="9f54a-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="9f54a-108">Example 1:</span></span>
```powershell
PS C:\> Disable-AzsScaleUnitNode -Name "HC1n25r2236"

Enable maintenance mode for a scale unit node.
```

<span data-ttu-id="9f54a-109">啟動 [縮放單位] 節點的 [維護模式]。</span><span class="sxs-lookup"><span data-stu-id="9f54a-109">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="9f54a-110">參數</span><span class="sxs-lookup"><span data-stu-id="9f54a-110">PARAMETERS</span></span>

### <span data-ttu-id="9f54a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f54a-111">-AsJob</span></span>


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

### <span data-ttu-id="9f54a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f54a-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="9f54a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9f54a-113">-Force</span></span>


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

### <span data-ttu-id="9f54a-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f54a-114">-InputObject</span></span>
<span data-ttu-id="9f54a-115">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9f54a-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9f54a-116">-位置</span><span class="sxs-lookup"><span data-stu-id="9f54a-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9f54a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="9f54a-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9f54a-118">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9f54a-118">-NoWait</span></span>


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

### <span data-ttu-id="9f54a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f54a-119">-PassThru</span></span>


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

### <span data-ttu-id="9f54a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f54a-120">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9f54a-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f54a-121">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9f54a-122">-確認</span><span class="sxs-lookup"><span data-stu-id="9f54a-122">-Confirm</span></span>
<span data-ttu-id="9f54a-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9f54a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f54a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f54a-124">-WhatIf</span></span>
<span data-ttu-id="9f54a-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9f54a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f54a-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9f54a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f54a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f54a-127">CommonParameters</span></span>
<span data-ttu-id="9f54a-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9f54a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f54a-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9f54a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f54a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="9f54a-130">INPUTS</span></span>

### <span data-ttu-id="9f54a-131">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="9f54a-131">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="9f54a-132">輸出</span><span class="sxs-lookup"><span data-stu-id="9f54a-132">OUTPUTS</span></span>

### <span data-ttu-id="9f54a-133">System.object</span><span class="sxs-lookup"><span data-stu-id="9f54a-133">System.Boolean</span></span>



## <span data-ttu-id="9f54a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="9f54a-134">NOTES</span></span>

<span data-ttu-id="9f54a-135">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="9f54a-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9f54a-136">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9f54a-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9f54a-137">INPUTOBJECT <IFabricAdminIdentity> ：</span><span class="sxs-lookup"><span data-stu-id="9f54a-137">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="9f54a-138">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f54a-138">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="9f54a-139">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f54a-139">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="9f54a-140">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f54a-140">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="9f54a-141">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="9f54a-141">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="9f54a-142">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="9f54a-142">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="9f54a-143">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="9f54a-143">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="9f54a-144">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="9f54a-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9f54a-145">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="9f54a-145">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="9f54a-146">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f54a-146">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="9f54a-147">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="9f54a-147">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="9f54a-148">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f54a-148">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="9f54a-149">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f54a-149">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="9f54a-150">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f54a-150">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="9f54a-151">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="9f54a-151">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="9f54a-152">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f54a-152">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="9f54a-153">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f54a-153">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="9f54a-154">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f54a-154">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="9f54a-155">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f54a-155">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="9f54a-156">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f54a-156">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="9f54a-157">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="9f54a-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9f54a-158">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="9f54a-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9f54a-159">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f54a-159">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="9f54a-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f54a-160">RELATED LINKS</span></span>

