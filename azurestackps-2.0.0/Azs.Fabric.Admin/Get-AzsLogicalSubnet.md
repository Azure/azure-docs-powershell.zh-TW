---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azslogicalsubnet
schema: 2.0.0
ms.openlocfilehash: eae4d8e861b6b229cfa3e5fe9b4e424a69c487c2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796445"
---
# <span data-ttu-id="e31e2-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="e31e2-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="e31e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e31e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e31e2-103">傳回要求的邏輯子網。</span><span class="sxs-lookup"><span data-stu-id="e31e2-103">Returns the requested logical subnet.</span></span>

## <span data-ttu-id="e31e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="e31e2-104">SYNTAX</span></span>

### <span data-ttu-id="e31e2-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="e31e2-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="e31e2-106">獲取</span><span class="sxs-lookup"><span data-stu-id="e31e2-106">Get</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="e31e2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e31e2-107">GetViaIdentity</span></span>
```
Get-AzsLogicalSubnet -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="e31e2-108">說明</span><span class="sxs-lookup"><span data-stu-id="e31e2-108">DESCRIPTION</span></span>
<span data-ttu-id="e31e2-109">傳回要求的邏輯子網。</span><span class="sxs-lookup"><span data-stu-id="e31e2-109">Returns the requested logical subnet.</span></span>

## <span data-ttu-id="e31e2-110">示例</span><span class="sxs-lookup"><span data-stu-id="e31e2-110">EXAMPLES</span></span>

### <span data-ttu-id="e31e2-111">範例1：</span><span class="sxs-lookup"><span data-stu-id="e31e2-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork

A list of all logical networks at a location.
```

<span data-ttu-id="e31e2-112">取得某個位置的所有邏輯網路。</span><span class="sxs-lookup"><span data-stu-id="e31e2-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="e31e2-113">範例2：</span><span class="sxs-lookup"><span data-stu-id="e31e2-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"

A a specific logical networks at a location based on a name.
```

<span data-ttu-id="e31e2-114">根據名稱在某個位置取得特定的邏輯網路。</span><span class="sxs-lookup"><span data-stu-id="e31e2-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="e31e2-115">參數</span><span class="sxs-lookup"><span data-stu-id="e31e2-115">PARAMETERS</span></span>

### <span data-ttu-id="e31e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e31e2-116">-DefaultProfile</span></span>
<span data-ttu-id="e31e2-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e31e2-118">-篩選</span><span class="sxs-lookup"><span data-stu-id="e31e2-118">-Filter</span></span>
<span data-ttu-id="e31e2-119">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="e31e2-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="e31e2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e31e2-120">-InputObject</span></span>
<span data-ttu-id="e31e2-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e31e2-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e31e2-122">-位置</span><span class="sxs-lookup"><span data-stu-id="e31e2-122">-Location</span></span>
<span data-ttu-id="e31e2-123">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="e31e2-123">Location of the resource.</span></span>

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

### <span data-ttu-id="e31e2-124">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="e31e2-124">-LogicalNetwork</span></span>
<span data-ttu-id="e31e2-125">邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-125">Name of the logical network.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e31e2-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="e31e2-126">-Name</span></span>
<span data-ttu-id="e31e2-127">邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-127">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="e31e2-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e31e2-128">-PassThru</span></span>
<span data-ttu-id="e31e2-129">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="e31e2-129">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e31e2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e31e2-130">-ResourceGroupName</span></span>
<span data-ttu-id="e31e2-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-131">Name of the resource group.</span></span>

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

### <span data-ttu-id="e31e2-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e31e2-132">-SubscriptionId</span></span>
<span data-ttu-id="e31e2-133">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e31e2-133">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e31e2-134">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="e31e2-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e31e2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e31e2-135">CommonParameters</span></span>
<span data-ttu-id="e31e2-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e31e2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e31e2-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e31e2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e31e2-138">輸入</span><span class="sxs-lookup"><span data-stu-id="e31e2-138">INPUTS</span></span>

### <span data-ttu-id="e31e2-139">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="e31e2-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="e31e2-140">輸出</span><span class="sxs-lookup"><span data-stu-id="e31e2-140">OUTPUTS</span></span>

### <span data-ttu-id="e31e2-141">ILogicalSubnet （FabricAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="e31e2-141">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.ILogicalSubnet</span></span>



## <span data-ttu-id="e31e2-142">筆記</span><span class="sxs-lookup"><span data-stu-id="e31e2-142">NOTES</span></span>

<span data-ttu-id="e31e2-143">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="e31e2-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e31e2-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e31e2-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e31e2-145">INPUTOBJECT <IFabricAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e31e2-145">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e31e2-146">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-146">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="e31e2-147">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-147">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="e31e2-148">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-148">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="e31e2-149">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="e31e2-149">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="e31e2-150">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-150">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="e31e2-151">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-151">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="e31e2-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="e31e2-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e31e2-153">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-153">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="e31e2-154">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-154">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="e31e2-155">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="e31e2-155">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="e31e2-156">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-156">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="e31e2-157">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-157">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="e31e2-158">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-158">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="e31e2-159">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="e31e2-159">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="e31e2-160">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-160">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="e31e2-161">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-161">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="e31e2-162">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-162">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="e31e2-163">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-163">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="e31e2-164">`[StoragePool <String>]`：儲存池名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-164">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="e31e2-165">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-165">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="e31e2-166">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e31e2-166">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e31e2-167">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="e31e2-167">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e31e2-168">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-168">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="e31e2-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="e31e2-169">RELATED LINKS</span></span>

