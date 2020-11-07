---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureshare
schema: 2.0.0
ms.openlocfilehash: e5fce1490b27bb569ce493a66a1c2646b73466a4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796449"
---
# <span data-ttu-id="4fde2-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="4fde2-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="4fde2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4fde2-102">SYNOPSIS</span></span>
<span data-ttu-id="4fde2-103">傳回要求的結構檔案共用。</span><span class="sxs-lookup"><span data-stu-id="4fde2-103">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="4fde2-104">句法</span><span class="sxs-lookup"><span data-stu-id="4fde2-104">SYNTAX</span></span>

### <span data-ttu-id="4fde2-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="4fde2-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="4fde2-106">獲取</span><span class="sxs-lookup"><span data-stu-id="4fde2-106">Get</span></span>
```
Get-AzsInfrastructureShare -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4fde2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4fde2-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureShare -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="4fde2-108">說明</span><span class="sxs-lookup"><span data-stu-id="4fde2-108">DESCRIPTION</span></span>
<span data-ttu-id="4fde2-109">傳回要求的結構檔案共用。</span><span class="sxs-lookup"><span data-stu-id="4fde2-109">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="4fde2-110">示例</span><span class="sxs-lookup"><span data-stu-id="4fde2-110">EXAMPLES</span></span>

### <span data-ttu-id="4fde2-111">範例1：</span><span class="sxs-lookup"><span data-stu-id="4fde2-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare
```

<span data-ttu-id="4fde2-112">傳回所有檔案共用的清單。</span><span class="sxs-lookup"><span data-stu-id="4fde2-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="4fde2-113">範例2：</span><span class="sxs-lookup"><span data-stu-id="4fde2-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare -Name SU1_ObjStore_1
```

<span data-ttu-id="4fde2-114">根據名稱返回檔案共用。</span><span class="sxs-lookup"><span data-stu-id="4fde2-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="4fde2-115">參數</span><span class="sxs-lookup"><span data-stu-id="4fde2-115">PARAMETERS</span></span>

### <span data-ttu-id="4fde2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fde2-116">-DefaultProfile</span></span>
<span data-ttu-id="4fde2-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fde2-118">-篩選</span><span class="sxs-lookup"><span data-stu-id="4fde2-118">-Filter</span></span>
<span data-ttu-id="4fde2-119">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="4fde2-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="4fde2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fde2-120">-InputObject</span></span>
<span data-ttu-id="4fde2-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4fde2-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4fde2-122">-位置</span><span class="sxs-lookup"><span data-stu-id="4fde2-122">-Location</span></span>
<span data-ttu-id="4fde2-123">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="4fde2-123">Location of the resource.</span></span>

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

### <span data-ttu-id="4fde2-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="4fde2-124">-Name</span></span>
<span data-ttu-id="4fde2-125">Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-125">Fabric file share name.</span></span>

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

### <span data-ttu-id="4fde2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fde2-126">-PassThru</span></span>
<span data-ttu-id="4fde2-127">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="4fde2-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4fde2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fde2-128">-ResourceGroupName</span></span>
<span data-ttu-id="4fde2-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="4fde2-130">-略過</span><span class="sxs-lookup"><span data-stu-id="4fde2-130">-Skip</span></span>
<span data-ttu-id="4fde2-131">OData 略過參數。</span><span class="sxs-lookup"><span data-stu-id="4fde2-131">OData skip parameter.</span></span>

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

### <span data-ttu-id="4fde2-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4fde2-132">-SubscriptionId</span></span>
<span data-ttu-id="4fde2-133">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4fde2-133">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4fde2-134">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="4fde2-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4fde2-135">-上方</span><span class="sxs-lookup"><span data-stu-id="4fde2-135">-Top</span></span>
<span data-ttu-id="4fde2-136">OData top 參數。</span><span class="sxs-lookup"><span data-stu-id="4fde2-136">OData top parameter.</span></span>

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

### <span data-ttu-id="4fde2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fde2-137">CommonParameters</span></span>
<span data-ttu-id="4fde2-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4fde2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fde2-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4fde2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fde2-140">輸入</span><span class="sxs-lookup"><span data-stu-id="4fde2-140">INPUTS</span></span>

### <span data-ttu-id="4fde2-141">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="4fde2-141">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="4fde2-142">輸出</span><span class="sxs-lookup"><span data-stu-id="4fde2-142">OUTPUTS</span></span>

### <span data-ttu-id="4fde2-143">IFileShare （FabricAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="4fde2-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFileShare</span></span>



## <span data-ttu-id="4fde2-144">筆記</span><span class="sxs-lookup"><span data-stu-id="4fde2-144">NOTES</span></span>

<span data-ttu-id="4fde2-145">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="4fde2-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4fde2-146">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4fde2-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4fde2-147">INPUTOBJECT <IFabricAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4fde2-147">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4fde2-148">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-148">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="4fde2-149">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-149">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="4fde2-150">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-150">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="4fde2-151">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="4fde2-151">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="4fde2-152">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-152">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="4fde2-153">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-153">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="4fde2-154">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="4fde2-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4fde2-155">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-155">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="4fde2-156">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-156">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="4fde2-157">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="4fde2-157">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="4fde2-158">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-158">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="4fde2-159">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-159">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="4fde2-160">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-160">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="4fde2-161">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="4fde2-161">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="4fde2-162">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-162">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="4fde2-163">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-163">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="4fde2-164">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-164">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="4fde2-165">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-165">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="4fde2-166">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-166">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="4fde2-167">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4fde2-167">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4fde2-168">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="4fde2-168">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4fde2-169">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fde2-169">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="4fde2-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="4fde2-170">RELATED LINKS</span></span>

