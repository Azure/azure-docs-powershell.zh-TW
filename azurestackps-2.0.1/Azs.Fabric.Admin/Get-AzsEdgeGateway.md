---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegateway
schema: 2.0.0
ms.openlocfilehash: a9c883fab422252aad167d92da3adf55edd9a78b
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966802"
---
# <span data-ttu-id="a36fb-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="a36fb-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="a36fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a36fb-102">SYNOPSIS</span></span>
<span data-ttu-id="a36fb-103">傳回要求的 edge 閘道。</span><span class="sxs-lookup"><span data-stu-id="a36fb-103">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="a36fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="a36fb-104">SYNTAX</span></span>

### <span data-ttu-id="a36fb-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="a36fb-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="a36fb-106">獲取</span><span class="sxs-lookup"><span data-stu-id="a36fb-106">Get</span></span>
```
Get-AzsEdgeGateway -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="a36fb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a36fb-107">GetViaIdentity</span></span>
```
Get-AzsEdgeGateway -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="a36fb-108">說明</span><span class="sxs-lookup"><span data-stu-id="a36fb-108">DESCRIPTION</span></span>
<span data-ttu-id="a36fb-109">傳回要求的 edge 閘道。</span><span class="sxs-lookup"><span data-stu-id="a36fb-109">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="a36fb-110">示例</span><span class="sxs-lookup"><span data-stu-id="a36fb-110">EXAMPLES</span></span>

### <span data-ttu-id="a36fb-111">範例1：</span><span class="sxs-lookup"><span data-stu-id="a36fb-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsEdgeGateway

Get a list of all edge gateways.
```

<span data-ttu-id="a36fb-112">傳回特定位置上所有 edge 閘道的清單。</span><span class="sxs-lookup"><span data-stu-id="a36fb-112">Returns the list of all edge gateways at a certain location.</span></span>


## <span data-ttu-id="a36fb-113">參數</span><span class="sxs-lookup"><span data-stu-id="a36fb-113">PARAMETERS</span></span>

### <span data-ttu-id="a36fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a36fb-114">-DefaultProfile</span></span>
<span data-ttu-id="a36fb-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a36fb-116">-篩選</span><span class="sxs-lookup"><span data-stu-id="a36fb-116">-Filter</span></span>
<span data-ttu-id="a36fb-117">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="a36fb-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="a36fb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a36fb-118">-InputObject</span></span>
<span data-ttu-id="a36fb-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a36fb-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a36fb-120">-位置</span><span class="sxs-lookup"><span data-stu-id="a36fb-120">-Location</span></span>
<span data-ttu-id="a36fb-121">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="a36fb-121">Location of the resource.</span></span>

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

### <span data-ttu-id="a36fb-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a36fb-122">-Name</span></span>
<span data-ttu-id="a36fb-123">Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-123">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="a36fb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a36fb-124">-PassThru</span></span>
<span data-ttu-id="a36fb-125">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="a36fb-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a36fb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a36fb-126">-ResourceGroupName</span></span>
<span data-ttu-id="a36fb-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="a36fb-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a36fb-128">-SubscriptionId</span></span>
<span data-ttu-id="a36fb-129">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a36fb-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a36fb-130">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="a36fb-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a36fb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a36fb-131">CommonParameters</span></span>
<span data-ttu-id="a36fb-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a36fb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a36fb-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a36fb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a36fb-134">輸入</span><span class="sxs-lookup"><span data-stu-id="a36fb-134">INPUTS</span></span>

### <span data-ttu-id="a36fb-135">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="a36fb-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="a36fb-136">輸出</span><span class="sxs-lookup"><span data-stu-id="a36fb-136">OUTPUTS</span></span>

### <span data-ttu-id="a36fb-137">IEdgeGateway （FabricAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="a36fb-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGateway</span></span>



## <span data-ttu-id="a36fb-138">筆記</span><span class="sxs-lookup"><span data-stu-id="a36fb-138">NOTES</span></span>

<span data-ttu-id="a36fb-139">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="a36fb-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a36fb-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a36fb-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a36fb-141">INPUTOBJECT <IFabricAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a36fb-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a36fb-142">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="a36fb-143">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="a36fb-144">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="a36fb-145">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="a36fb-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="a36fb-146">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="a36fb-147">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="a36fb-148">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="a36fb-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a36fb-149">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="a36fb-150">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="a36fb-151">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="a36fb-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="a36fb-152">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="a36fb-153">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="a36fb-154">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="a36fb-155">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="a36fb-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="a36fb-156">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="a36fb-157">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="a36fb-158">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="a36fb-159">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="a36fb-160">`[StoragePool <String>]`：儲存池名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-160">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="a36fb-161">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-161">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="a36fb-162">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="a36fb-162">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a36fb-163">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="a36fb-163">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a36fb-164">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36fb-164">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="a36fb-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="a36fb-165">RELATED LINKS</span></span>

