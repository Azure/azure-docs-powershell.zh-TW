---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructurelocation
schema: 2.0.0
ms.openlocfilehash: 0d0f2856503943d19653dd09a8cb1c125fec9517
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966731"
---
# <span data-ttu-id="c4cee-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="c4cee-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="c4cee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4cee-102">SYNOPSIS</span></span>
<span data-ttu-id="c4cee-103">傳回要求的結構位置。</span><span class="sxs-lookup"><span data-stu-id="c4cee-103">Returns the requested fabric location.</span></span>

## <span data-ttu-id="c4cee-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4cee-104">SYNTAX</span></span>

### <span data-ttu-id="c4cee-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="c4cee-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c4cee-106">獲取</span><span class="sxs-lookup"><span data-stu-id="c4cee-106">Get</span></span>
```
Get-AzsInfrastructureLocation -FabricLocation <String> [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="c4cee-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c4cee-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureLocation -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="c4cee-108">說明</span><span class="sxs-lookup"><span data-stu-id="c4cee-108">DESCRIPTION</span></span>
<span data-ttu-id="c4cee-109">傳回要求的結構位置。</span><span class="sxs-lookup"><span data-stu-id="c4cee-109">Returns the requested fabric location.</span></span>

## <span data-ttu-id="c4cee-110">示例</span><span class="sxs-lookup"><span data-stu-id="c4cee-110">EXAMPLES</span></span>

### <span data-ttu-id="c4cee-111">範例1：</span><span class="sxs-lookup"><span data-stu-id="c4cee-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation

Return a list of all fabric locations.
```

<span data-ttu-id="c4cee-112">取得所有 fabric 位置的清單。</span><span class="sxs-lookup"><span data-stu-id="c4cee-112">Get a list of all fabric locations.</span></span>

### <span data-ttu-id="c4cee-113">範例2：</span><span class="sxs-lookup"><span data-stu-id="c4cee-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation -Location "local"

Return a location based on the name.
```

<span data-ttu-id="c4cee-114">根據名稱取得位置。</span><span class="sxs-lookup"><span data-stu-id="c4cee-114">Get a location based on the name.</span></span>

## <span data-ttu-id="c4cee-115">參數</span><span class="sxs-lookup"><span data-stu-id="c4cee-115">PARAMETERS</span></span>

### <span data-ttu-id="c4cee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4cee-116">-DefaultProfile</span></span>
<span data-ttu-id="c4cee-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4cee-118">-FabricLocation</span><span class="sxs-lookup"><span data-stu-id="c4cee-118">-FabricLocation</span></span>
<span data-ttu-id="c4cee-119">Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="c4cee-119">Fabric location.</span></span>

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

### <span data-ttu-id="c4cee-120">-篩選</span><span class="sxs-lookup"><span data-stu-id="c4cee-120">-Filter</span></span>
<span data-ttu-id="c4cee-121">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="c4cee-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="c4cee-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4cee-122">-InputObject</span></span>
<span data-ttu-id="c4cee-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c4cee-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c4cee-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4cee-124">-PassThru</span></span>
<span data-ttu-id="c4cee-125">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="c4cee-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c4cee-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4cee-126">-ResourceGroupName</span></span>
<span data-ttu-id="c4cee-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="c4cee-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4cee-128">-SubscriptionId</span></span>
<span data-ttu-id="c4cee-129">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="c4cee-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c4cee-130">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="c4cee-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c4cee-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4cee-131">CommonParameters</span></span>
<span data-ttu-id="c4cee-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4cee-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4cee-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c4cee-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4cee-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c4cee-134">INPUTS</span></span>

### <span data-ttu-id="c4cee-135">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="c4cee-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="c4cee-136">輸出</span><span class="sxs-lookup"><span data-stu-id="c4cee-136">OUTPUTS</span></span>

### <span data-ttu-id="c4cee-137">IFabricLocation （FabricAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="c4cee-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFabricLocation</span></span>



## <span data-ttu-id="c4cee-138">筆記</span><span class="sxs-lookup"><span data-stu-id="c4cee-138">NOTES</span></span>

<span data-ttu-id="c4cee-139">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c4cee-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4cee-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c4cee-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c4cee-141">INPUTOBJECT <IFabricAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="c4cee-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4cee-142">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="c4cee-143">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="c4cee-144">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="c4cee-145">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="c4cee-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="c4cee-146">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="c4cee-147">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="c4cee-148">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="c4cee-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4cee-149">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="c4cee-150">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="c4cee-151">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="c4cee-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="c4cee-152">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="c4cee-153">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="c4cee-154">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="c4cee-155">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="c4cee-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="c4cee-156">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="c4cee-157">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="c4cee-158">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="c4cee-159">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="c4cee-160">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-160">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="c4cee-161">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="c4cee-161">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c4cee-162">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="c4cee-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c4cee-163">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4cee-163">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="c4cee-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4cee-164">RELATED LINKS</span></span>

