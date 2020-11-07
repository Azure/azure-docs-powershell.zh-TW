---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsstoragesubsystem
schema: 2.0.0
ms.openlocfilehash: 75349838437ad34743b67510f3a284ff2736b30c
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966751"
---
# <span data-ttu-id="df26e-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="df26e-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="df26e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df26e-102">SYNOPSIS</span></span>
<span data-ttu-id="df26e-103">傳回要求的儲存子系統。</span><span class="sxs-lookup"><span data-stu-id="df26e-103">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="df26e-104">句法</span><span class="sxs-lookup"><span data-stu-id="df26e-104">SYNTAX</span></span>

### <span data-ttu-id="df26e-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="df26e-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="df26e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="df26e-106">Get</span></span>
```
Get-AzsStorageSubSystem -Name <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="df26e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="df26e-107">GetViaIdentity</span></span>
```
Get-AzsStorageSubSystem -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="df26e-108">說明</span><span class="sxs-lookup"><span data-stu-id="df26e-108">DESCRIPTION</span></span>
<span data-ttu-id="df26e-109">傳回要求的儲存子系統。</span><span class="sxs-lookup"><span data-stu-id="df26e-109">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="df26e-110">示例</span><span class="sxs-lookup"><span data-stu-id="df26e-110">EXAMPLES</span></span>

### <span data-ttu-id="df26e-111">範例1：</span><span class="sxs-lookup"><span data-stu-id="df26e-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
```

<span data-ttu-id="df26e-112">從比例單位取得所有儲存子系統。</span><span class="sxs-lookup"><span data-stu-id="df26e-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="df26e-113">範例2：</span><span class="sxs-lookup"><span data-stu-id="df26e-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name -Name s-cluster.DomainFQDN
```

<span data-ttu-id="df26e-114">取得具有縮放比例單位和名稱的儲存子系統。</span><span class="sxs-lookup"><span data-stu-id="df26e-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="df26e-115">參數</span><span class="sxs-lookup"><span data-stu-id="df26e-115">PARAMETERS</span></span>

### <span data-ttu-id="df26e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df26e-116">-DefaultProfile</span></span>
<span data-ttu-id="df26e-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="df26e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df26e-118">-篩選</span><span class="sxs-lookup"><span data-stu-id="df26e-118">-Filter</span></span>
<span data-ttu-id="df26e-119">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="df26e-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="df26e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df26e-120">-InputObject</span></span>
<span data-ttu-id="df26e-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="df26e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="df26e-122">-位置</span><span class="sxs-lookup"><span data-stu-id="df26e-122">-Location</span></span>
<span data-ttu-id="df26e-123">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="df26e-123">Location of the resource.</span></span>

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

### <span data-ttu-id="df26e-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="df26e-124">-Name</span></span>
<span data-ttu-id="df26e-125">儲存空間系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-125">Name of the storage system.</span></span>

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

### <span data-ttu-id="df26e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df26e-126">-PassThru</span></span>
<span data-ttu-id="df26e-127">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="df26e-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="df26e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df26e-128">-ResourceGroupName</span></span>
<span data-ttu-id="df26e-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="df26e-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="df26e-130">-ScaleUnit</span></span>
<span data-ttu-id="df26e-131">縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="df26e-132">-略過</span><span class="sxs-lookup"><span data-stu-id="df26e-132">-Skip</span></span>
<span data-ttu-id="df26e-133">OData 略過參數。</span><span class="sxs-lookup"><span data-stu-id="df26e-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="df26e-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df26e-134">-SubscriptionId</span></span>
<span data-ttu-id="df26e-135">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="df26e-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="df26e-136">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="df26e-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="df26e-137">-上方</span><span class="sxs-lookup"><span data-stu-id="df26e-137">-Top</span></span>
<span data-ttu-id="df26e-138">OData top 參數。</span><span class="sxs-lookup"><span data-stu-id="df26e-138">OData top parameter.</span></span>

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

### <span data-ttu-id="df26e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df26e-139">CommonParameters</span></span>
<span data-ttu-id="df26e-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df26e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df26e-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="df26e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df26e-142">輸入</span><span class="sxs-lookup"><span data-stu-id="df26e-142">INPUTS</span></span>

### <span data-ttu-id="df26e-143">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="df26e-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="df26e-144">輸出</span><span class="sxs-lookup"><span data-stu-id="df26e-144">OUTPUTS</span></span>

### <span data-ttu-id="df26e-145">IStorageSubSystem （FabricAdmin）。 Api20181001。</span><span class="sxs-lookup"><span data-stu-id="df26e-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20181001.IStorageSubSystem</span></span>



## <span data-ttu-id="df26e-146">筆記</span><span class="sxs-lookup"><span data-stu-id="df26e-146">NOTES</span></span>

<span data-ttu-id="df26e-147">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="df26e-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="df26e-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="df26e-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="df26e-149">INPUTOBJECT <IFabricAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="df26e-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="df26e-150">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="df26e-151">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="df26e-152">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="df26e-153">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="df26e-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="df26e-154">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="df26e-155">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="df26e-156">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="df26e-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="df26e-157">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="df26e-158">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="df26e-159">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="df26e-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="df26e-160">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="df26e-161">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="df26e-162">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="df26e-163">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="df26e-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="df26e-164">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="df26e-165">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="df26e-166">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="df26e-167">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="df26e-168">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="df26e-169">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="df26e-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="df26e-170">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="df26e-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="df26e-171">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="df26e-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="df26e-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="df26e-172">RELATED LINKS</span></span>

