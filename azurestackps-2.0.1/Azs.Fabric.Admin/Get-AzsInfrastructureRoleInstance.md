---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: b5eb59c1f2ad631e8cbb9fdffbf65bee00425d43
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966673"
---
# <span data-ttu-id="97beb-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="97beb-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="97beb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97beb-102">SYNOPSIS</span></span>
<span data-ttu-id="97beb-103">傳回要求的基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="97beb-103">Return the requested infrastructure role instance.</span></span>

## <span data-ttu-id="97beb-104">句法</span><span class="sxs-lookup"><span data-stu-id="97beb-104">SYNTAX</span></span>

### <span data-ttu-id="97beb-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="97beb-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="97beb-106">獲取</span><span class="sxs-lookup"><span data-stu-id="97beb-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="97beb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="97beb-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="97beb-108">說明</span><span class="sxs-lookup"><span data-stu-id="97beb-108">DESCRIPTION</span></span>
<span data-ttu-id="97beb-109">傳回要求的基礎結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="97beb-109">Return the requested infrastructure role instance.</span></span>

## <span data-ttu-id="97beb-110">示例</span><span class="sxs-lookup"><span data-stu-id="97beb-110">EXAMPLES</span></span>

### <span data-ttu-id="97beb-111">範例1：</span><span class="sxs-lookup"><span data-stu-id="97beb-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureRoleInstance

A list of all infrastructure role instances.
```

<span data-ttu-id="97beb-112">傳回所有結構角色實例的清單。</span><span class="sxs-lookup"><span data-stu-id="97beb-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="97beb-113">範例2：</span><span class="sxs-lookup"><span data-stu-id="97beb-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

A single infrastructure role instance based on name.
```

<span data-ttu-id="97beb-114">根據名稱傳回單一的結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="97beb-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="97beb-115">參數</span><span class="sxs-lookup"><span data-stu-id="97beb-115">PARAMETERS</span></span>

### <span data-ttu-id="97beb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97beb-116">-DefaultProfile</span></span>
<span data-ttu-id="97beb-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97beb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97beb-118">-篩選</span><span class="sxs-lookup"><span data-stu-id="97beb-118">-Filter</span></span>
<span data-ttu-id="97beb-119">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="97beb-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="97beb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97beb-120">-InputObject</span></span>
<span data-ttu-id="97beb-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="97beb-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="97beb-122">-位置</span><span class="sxs-lookup"><span data-stu-id="97beb-122">-Location</span></span>
<span data-ttu-id="97beb-123">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="97beb-123">Location of the resource.</span></span>

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

### <span data-ttu-id="97beb-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="97beb-124">-Name</span></span>
<span data-ttu-id="97beb-125">結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-125">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="97beb-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97beb-126">-PassThru</span></span>
<span data-ttu-id="97beb-127">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="97beb-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="97beb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97beb-128">-ResourceGroupName</span></span>
<span data-ttu-id="97beb-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="97beb-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97beb-130">-SubscriptionId</span></span>
<span data-ttu-id="97beb-131">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="97beb-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="97beb-132">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="97beb-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="97beb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97beb-133">CommonParameters</span></span>
<span data-ttu-id="97beb-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97beb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97beb-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="97beb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97beb-136">輸入</span><span class="sxs-lookup"><span data-stu-id="97beb-136">INPUTS</span></span>

### <span data-ttu-id="97beb-137">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="97beb-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="97beb-138">輸出</span><span class="sxs-lookup"><span data-stu-id="97beb-138">OUTPUTS</span></span>

### <span data-ttu-id="97beb-139">IInfraRoleInstance （FabricAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="97beb-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IInfraRoleInstance</span></span>



## <span data-ttu-id="97beb-140">筆記</span><span class="sxs-lookup"><span data-stu-id="97beb-140">NOTES</span></span>

<span data-ttu-id="97beb-141">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="97beb-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97beb-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="97beb-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="97beb-143">INPUTOBJECT <IFabricAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="97beb-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="97beb-144">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="97beb-145">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="97beb-146">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="97beb-147">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="97beb-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="97beb-148">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="97beb-149">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="97beb-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="97beb-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="97beb-151">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="97beb-152">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="97beb-153">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="97beb-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="97beb-154">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="97beb-155">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="97beb-156">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="97beb-157">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="97beb-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="97beb-158">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="97beb-159">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="97beb-160">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="97beb-161">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="97beb-162">`[StoragePool <String>]`：儲存池名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="97beb-163">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="97beb-164">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="97beb-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="97beb-165">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="97beb-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="97beb-166">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="97beb-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="97beb-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="97beb-167">RELATED LINKS</span></span>

