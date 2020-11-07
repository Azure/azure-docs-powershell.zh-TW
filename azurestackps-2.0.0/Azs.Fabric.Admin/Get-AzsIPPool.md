---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsippool
schema: 2.0.0
ms.openlocfilehash: 532dcd2a91591b639b93b5b67851a4118457068b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794909"
---
# <span data-ttu-id="e4c50-101">Get-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="e4c50-101">Get-AzsIPPool</span></span>

## <span data-ttu-id="e4c50-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4c50-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c50-103">傳回要求的 IP 池。</span><span class="sxs-lookup"><span data-stu-id="e4c50-103">Return the requested IP pool.</span></span>

## <span data-ttu-id="e4c50-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4c50-104">SYNTAX</span></span>

### <span data-ttu-id="e4c50-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="e4c50-105">List (Default)</span></span>
```
Get-AzsIPPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="e4c50-106">獲取</span><span class="sxs-lookup"><span data-stu-id="e4c50-106">Get</span></span>
```
Get-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="e4c50-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e4c50-107">GetViaIdentity</span></span>
```
Get-AzsIPPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="e4c50-108">說明</span><span class="sxs-lookup"><span data-stu-id="e4c50-108">DESCRIPTION</span></span>
<span data-ttu-id="e4c50-109">傳回要求的 IP 池。</span><span class="sxs-lookup"><span data-stu-id="e4c50-109">Return the requested IP pool.</span></span>

## <span data-ttu-id="e4c50-110">示例</span><span class="sxs-lookup"><span data-stu-id="e4c50-110">EXAMPLES</span></span>

### <span data-ttu-id="e4c50-111">範例1：</span><span class="sxs-lookup"><span data-stu-id="e4c50-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsIpPool

Return an all infrastructure ip pools.
```

<span data-ttu-id="e4c50-112">取得所有基礎結構 ip 池。</span><span class="sxs-lookup"><span data-stu-id="e4c50-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="e4c50-113">範例2：</span><span class="sxs-lookup"><span data-stu-id="e4c50-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"

Get an infrastructure ip pool based on name.
```

<span data-ttu-id="e4c50-114">根據名稱取得基礎結構 ip 池。</span><span class="sxs-lookup"><span data-stu-id="e4c50-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="e4c50-115">參數</span><span class="sxs-lookup"><span data-stu-id="e4c50-115">PARAMETERS</span></span>

### <span data-ttu-id="e4c50-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4c50-116">-DefaultProfile</span></span>


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

### <span data-ttu-id="e4c50-117">-篩選</span><span class="sxs-lookup"><span data-stu-id="e4c50-117">-Filter</span></span>
<span data-ttu-id="e4c50-118">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="e4c50-118">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e4c50-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4c50-119">-InputObject</span></span>
<span data-ttu-id="e4c50-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e4c50-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e4c50-121">-位置</span><span class="sxs-lookup"><span data-stu-id="e4c50-121">-Location</span></span>
<span data-ttu-id="e4c50-122">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="e4c50-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e4c50-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="e4c50-123">-Name</span></span>
<span data-ttu-id="e4c50-124">IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-124">IP pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e4c50-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4c50-125">-PassThru</span></span>
<span data-ttu-id="e4c50-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="e4c50-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e4c50-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4c50-127">-ResourceGroupName</span></span>
<span data-ttu-id="e4c50-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e4c50-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4c50-129">-SubscriptionId</span></span>
<span data-ttu-id="e4c50-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e4c50-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e4c50-131">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="e4c50-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e4c50-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c50-132">CommonParameters</span></span>
<span data-ttu-id="e4c50-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4c50-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c50-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e4c50-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c50-135">輸入</span><span class="sxs-lookup"><span data-stu-id="e4c50-135">INPUTS</span></span>

### <span data-ttu-id="e4c50-136">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="e4c50-136">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="e4c50-137">輸出</span><span class="sxs-lookup"><span data-stu-id="e4c50-137">OUTPUTS</span></span>

### <span data-ttu-id="e4c50-138">IIPPool （FabricAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="e4c50-138">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="e4c50-139">筆記</span><span class="sxs-lookup"><span data-stu-id="e4c50-139">NOTES</span></span>

<span data-ttu-id="e4c50-140">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="e4c50-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4c50-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e4c50-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e4c50-142">INPUTOBJECT <IFabricAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e4c50-142">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e4c50-143">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-143">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="e4c50-144">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-144">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="e4c50-145">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-145">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="e4c50-146">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="e4c50-146">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="e4c50-147">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-147">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="e4c50-148">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-148">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="e4c50-149">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="e4c50-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e4c50-150">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-150">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="e4c50-151">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-151">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="e4c50-152">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="e4c50-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="e4c50-153">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-153">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="e4c50-154">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-154">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="e4c50-155">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-155">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="e4c50-156">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="e4c50-156">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="e4c50-157">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-157">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="e4c50-158">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-158">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="e4c50-159">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-159">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="e4c50-160">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-160">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="e4c50-161">`[StoragePool <String>]`：儲存池名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-161">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="e4c50-162">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-162">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="e4c50-163">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e4c50-163">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e4c50-164">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="e4c50-164">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e4c50-165">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4c50-165">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="e4c50-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4c50-166">RELATED LINKS</span></span>

