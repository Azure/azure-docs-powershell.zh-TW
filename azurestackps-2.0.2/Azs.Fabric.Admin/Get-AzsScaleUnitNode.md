---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d1534c7cfacbcc70c2fe822676d67142401f9ff9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968076"
---
# <span data-ttu-id="0e0f5-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="0e0f5-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="0e0f5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0e0f5-102">SYNOPSIS</span></span>


## <span data-ttu-id="0e0f5-103">句法</span><span class="sxs-lookup"><span data-stu-id="0e0f5-103">SYNTAX</span></span>

### <span data-ttu-id="0e0f5-104"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="0e0f5-104">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="0e0f5-105">獲取</span><span class="sxs-lookup"><span data-stu-id="0e0f5-105">Get</span></span>
```
Get-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="0e0f5-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0e0f5-106">GetViaIdentity</span></span>
```
Get-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="0e0f5-107">說明</span><span class="sxs-lookup"><span data-stu-id="0e0f5-107">DESCRIPTION</span></span>


## <span data-ttu-id="0e0f5-108">示例</span><span class="sxs-lookup"><span data-stu-id="0e0f5-108">EXAMPLES</span></span>

### <span data-ttu-id="0e0f5-109">範例1：</span><span class="sxs-lookup"><span data-stu-id="0e0f5-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsScaleUnitNode

A list of all scale unit nodes at a location.
```

<span data-ttu-id="0e0f5-110">取得某個位置的所有縮放單位節點。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-110">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="0e0f5-111">範例2：</span><span class="sxs-lookup"><span data-stu-id="0e0f5-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsScaleUnitNode -Name "HC1n25r2231"

A specific scale unit node at a location given a name.
```

<span data-ttu-id="0e0f5-112">在指定名稱的位置取得特定的縮放單位節點。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-112">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="0e0f5-113">參數</span><span class="sxs-lookup"><span data-stu-id="0e0f5-113">PARAMETERS</span></span>

### <span data-ttu-id="0e0f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e0f5-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="0e0f5-115">-篩選</span><span class="sxs-lookup"><span data-stu-id="0e0f5-115">-Filter</span></span>


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

### <span data-ttu-id="0e0f5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e0f5-116">-InputObject</span></span>
<span data-ttu-id="0e0f5-117">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0e0f5-118">-位置</span><span class="sxs-lookup"><span data-stu-id="0e0f5-118">-Location</span></span>


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

### <span data-ttu-id="0e0f5-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="0e0f5-119">-Name</span></span>


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

### <span data-ttu-id="0e0f5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e0f5-120">-PassThru</span></span>


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

### <span data-ttu-id="0e0f5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e0f5-121">-ResourceGroupName</span></span>


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

### <span data-ttu-id="0e0f5-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0e0f5-122">-SubscriptionId</span></span>


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

### <span data-ttu-id="0e0f5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e0f5-123">CommonParameters</span></span>
<span data-ttu-id="0e0f5-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e0f5-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e0f5-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0e0f5-126">INPUTS</span></span>

### <span data-ttu-id="0e0f5-127">IFabricAdminIdentity （FabricAdmin）的</span><span class="sxs-lookup"><span data-stu-id="0e0f5-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="0e0f5-128">輸出</span><span class="sxs-lookup"><span data-stu-id="0e0f5-128">OUTPUTS</span></span>

### <span data-ttu-id="0e0f5-129">IScaleUnitNode （FabricAdmin）。 Api20160501。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleUnitNode</span></span>



## <span data-ttu-id="0e0f5-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0e0f5-130">NOTES</span></span>

<span data-ttu-id="0e0f5-131">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0e0f5-132">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0e0f5-133">INPUTOBJECT <IFabricAdminIdentity> ：</span><span class="sxs-lookup"><span data-stu-id="0e0f5-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="0e0f5-134">`[Drive <String>]`：儲存空間磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="0e0f5-135">`[EdgeGateway <String>]`： Edge 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="0e0f5-136">`[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="0e0f5-137">`[FabricLocation <String>]`： Fabric 位置。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="0e0f5-138">`[FileShare <String>]`： Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="0e0f5-139">`[IPPool <String>]`： IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="0e0f5-140">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="0e0f5-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0e0f5-141">`[InfraRole <String>]`：結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="0e0f5-142">`[InfraRoleInstance <String>]`：結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="0e0f5-143">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="0e0f5-144">`[LogicalNetwork <String>]`：邏輯網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="0e0f5-145">`[LogicalSubnet <String>]`：邏輯子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="0e0f5-146">`[MacAddressPool <String>]`： MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="0e0f5-147">`[Operation <String>]`： [操作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="0e0f5-148">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="0e0f5-149">`[ScaleUnit <String>]`：縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="0e0f5-150">`[ScaleUnitNode <String>]`：縮放單位節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="0e0f5-151">`[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="0e0f5-152">`[StorageSubSystem <String>]`：存儲系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="0e0f5-153">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0e0f5-154">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0e0f5-155">`[Volume <String>]`：儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0f5-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="0e0f5-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e0f5-156">RELATED LINKS</span></span>

