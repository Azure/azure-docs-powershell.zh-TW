---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsdrive
schema: 2.0.0
ms.openlocfilehash: ec2216a9234086702e8a9331888c04034d13a99f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796453"
---
# <span data-ttu-id="99357-101">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="99357-101">Get-AzsDrive</span></span>

## <span data-ttu-id="99357-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99357-102">SYNOPSIS</span></span>
<span data-ttu-id="99357-103">傳回要求的儲存空間磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="99357-103">Return the requested a storage drive.</span></span>

## <span data-ttu-id="99357-104">句法</span><span class="sxs-lookup"><span data-stu-id="99357-104">SYNTAX</span></span>

### <span data-ttu-id="99357-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="99357-105">List (Default)</span></span>
```
Get-AzsDrive -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="99357-106">獲取</span><span class="sxs-lookup"><span data-stu-id="99357-106">Get</span></span>
```
Get-AzsDrive -Name <String> -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="99357-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="99357-107">GetViaIdentity</span></span>
```
Get-AzsDrive -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="99357-108">說明</span><span class="sxs-lookup"><span data-stu-id="99357-108">DESCRIPTION</span></span>
<span data-ttu-id="99357-109">傳回要求的儲存空間磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="99357-109">Return the requested a storage drive.</span></span>

## <span data-ttu-id="99357-110">示例</span><span class="sxs-lookup"><span data-stu-id="99357-110">EXAMPLES</span></span>

### <span data-ttu-id="99357-111">範例1：</span><span class="sxs-lookup"><span data-stu-id="99357-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name
```

<span data-ttu-id="99357-112">取得指定群集所有儲存空間的清單。</span><span class="sxs-lookup"><span data-stu-id="99357-112">Get a list of all storage drives for a given cluster.</span></span>

### <span data-ttu-id="99357-113">範例2：</span><span class="sxs-lookup"><span data-stu-id="99357-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name -Name '{a185d466-4d21-4c1f-9489-7c9c66b6b172}:PD:{fd389cf7-2115-2144-5afe-27910562d6b3}'
```

<span data-ttu-id="99357-114">使用特定群集的名稱取得儲存空間磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="99357-114">Get a storage drive by name for a given cluster.</span></span>

## <span data-ttu-id="99357-115">參數</span><span class="sxs-lookup"><span data-stu-id="99357-115">PARAMETERS</span></span>

### <span data-ttu-id="99357-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99357-116">-DefaultProfile</span></span>
<span data-ttu-id="99357-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="99357-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99357-118">-篩選</span><span class="sxs-lookup"><span data-stu-id="99357-118">-Filter</span></span>
<span data-ttu-id="99357-119">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="99357-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="99357-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99357-120">-InputObject</span></span>
<span data-ttu-id="99357-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="99357-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="99357-122">-位置</span><span class="sxs-lookup"><span data-stu-id="99357-122">-Location</span></span>
<span data-ttu-id="99357-123">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="99357-123">Location of the resource.</span></span>

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

### <span data-ttu-id="99357-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="99357-124">-Name</span></span>
<span data-ttu-id="99357-125">儲存空間磁片磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-125">Name of the storage drive.</span></span>

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

### <span data-ttu-id="99357-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99357-126">-PassThru</span></span>
<span data-ttu-id="99357-127">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="99357-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="99357-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99357-128">-ResourceGroupName</span></span>
<span data-ttu-id="99357-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="99357-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="99357-130">-ScaleUnit</span></span>
<span data-ttu-id="99357-131">縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="99357-132">-略過</span><span class="sxs-lookup"><span data-stu-id="99357-132">-Skip</span></span>
<span data-ttu-id="99357-133">OData 略過參數。</span><span class="sxs-lookup"><span data-stu-id="99357-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="99357-134">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="99357-134">-StorageSubSystem</span></span>
<span data-ttu-id="99357-135">儲存空間系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-135">Name of the storage system.</span></span>

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

### <span data-ttu-id="99357-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99357-136">-SubscriptionId</span></span>
<span data-ttu-id="99357-137">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="99357-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="99357-138">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="99357-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="99357-139">-上方</span><span class="sxs-lookup"><span data-stu-id="99357-139">-Top</span></span>
<span data-ttu-id="99357-140">OData top 參數。</span><span class="sxs-lookup"><span data-stu-id="99357-140">OData top parameter.</span></span>

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

### <span data-ttu-id="99357-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99357-141">CommonParameters</span></span>
<span data-ttu-id="99357-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99357-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99357-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="99357-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99357-144">輸入</span><span class="sxs-lookup"><span data-stu-id="99357-144">INPUTS</span></span>

### <span data-ttu-id="99357-145">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="99357-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="99357-146">輸出</span><span class="sxs-lookup"><span data-stu-id="99357-146">OUTPUTS</span></span>

### <span data-ttu-id="99357-147">IDrive （FabricAdmin）。 Api20190501。</span><span class="sxs-lookup"><span data-stu-id="99357-147">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20190501.IDrive</span></span>



## <span data-ttu-id="99357-148">筆記</span><span class="sxs-lookup"><span data-stu-id="99357-148">NOTES</span></span>

<span data-ttu-id="99357-149">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="99357-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="99357-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="99357-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="99357-151">INPUTOBJECT <IFabricAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="99357-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="99357-152">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="99357-153">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="99357-154">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="99357-155">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="99357-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="99357-156">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="99357-157">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="99357-158">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="99357-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="99357-159">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="99357-160">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="99357-161">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="99357-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="99357-162">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="99357-163">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="99357-164">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="99357-165">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="99357-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="99357-166">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="99357-167">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="99357-168">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="99357-169">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="99357-170">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-170">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="99357-171">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="99357-171">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="99357-172">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="99357-172">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="99357-173">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="99357-173">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="99357-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="99357-174">RELATED LINKS</span></span>

