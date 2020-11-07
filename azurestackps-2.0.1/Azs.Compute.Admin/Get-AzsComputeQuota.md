---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 81a7a64f1880e2ed9acb2fedd3f90df614f1619d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966819"
---
# <span data-ttu-id="5b6b5-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="5b6b5-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="5b6b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b6b5-102">SYNOPSIS</span></span>
<span data-ttu-id="5b6b5-103">取得現有的計算配額。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-103">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="5b6b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b6b5-104">SYNTAX</span></span>

### <span data-ttu-id="5b6b5-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="5b6b5-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b6b5-106">獲取</span><span class="sxs-lookup"><span data-stu-id="5b6b5-106">Get</span></span>
```
Get-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5b6b5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5b6b5-107">GetViaIdentity</span></span>
```
Get-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5b6b5-108">說明</span><span class="sxs-lookup"><span data-stu-id="5b6b5-108">DESCRIPTION</span></span>
<span data-ttu-id="5b6b5-109">取得現有的計算配額。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-109">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="5b6b5-110">示例</span><span class="sxs-lookup"><span data-stu-id="5b6b5-110">EXAMPLES</span></span>

### <span data-ttu-id="5b6b5-111">範例1：取得所有計算配額</span><span class="sxs-lookup"><span data-stu-id="5b6b5-111">Example 1: Get All Compute Quotas</span></span>
```powershell
PS C:\> Get-AzsComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ascancompquota433
Location                           : local
Name                               : ascancompquota433
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 100
VirtualMachineCount                : 100
```

<span data-ttu-id="5b6b5-112">`Get-AzsComputeQuota`不使用參數執行，即可取得所有計算配額的清單。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-112">Run `Get-AzsComputeQuota` with no parameters to get a list of all Compute Quotas.</span></span>

### <span data-ttu-id="5b6b5-113">範例2：依名稱取得計算配額</span><span class="sxs-lookup"><span data-stu-id="5b6b5-113">Example 2: Get Compute Quota by Name</span></span>
```powershell
PS C:\> Get-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ExampleComputeQuotaWithDefaultParameters
Location                           : local
Name                               : ExampleComputeQuotaWithDefaultParameters
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="5b6b5-114">在命令列上指定配額的名稱，即可檢索特定的配額。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-114">Specify the Quota's name on the command line to retrieve a specific quota.</span></span>

## <span data-ttu-id="5b6b5-115">參數</span><span class="sxs-lookup"><span data-stu-id="5b6b5-115">PARAMETERS</span></span>

### <span data-ttu-id="5b6b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b6b5-116">-DefaultProfile</span></span>
<span data-ttu-id="5b6b5-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b6b5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b6b5-118">-InputObject</span></span>
<span data-ttu-id="5b6b5-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5b6b5-120">-位置</span><span class="sxs-lookup"><span data-stu-id="5b6b5-120">-Location</span></span>
<span data-ttu-id="5b6b5-121">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-121">Location of the resource.</span></span>

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

### <span data-ttu-id="5b6b5-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="5b6b5-122">-Name</span></span>
<span data-ttu-id="5b6b5-123">配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-123">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5b6b5-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b6b5-124">-SubscriptionId</span></span>
<span data-ttu-id="5b6b5-125">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5b6b5-126">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5b6b5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b6b5-127">CommonParameters</span></span>
<span data-ttu-id="5b6b5-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b6b5-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b6b5-130">輸入</span><span class="sxs-lookup"><span data-stu-id="5b6b5-130">INPUTS</span></span>

### <span data-ttu-id="5b6b5-131">IComputeAdminIdentity （ComputeAdmin）的</span><span class="sxs-lookup"><span data-stu-id="5b6b5-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="5b6b5-132">輸出</span><span class="sxs-lookup"><span data-stu-id="5b6b5-132">OUTPUTS</span></span>

### <span data-ttu-id="5b6b5-133">IQuota （ComputeAdmin）。 Api20180209。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="5b6b5-134">筆記</span><span class="sxs-lookup"><span data-stu-id="5b6b5-134">NOTES</span></span>

<span data-ttu-id="5b6b5-135">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5b6b5-136">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5b6b5-137">INPUTOBJECT <IComputeAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5b6b5-137">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5b6b5-138">`[DiskId <String>]`：磁片 guid 作為身分識別。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-138">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="5b6b5-139">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="5b6b5-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5b6b5-140">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-140">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="5b6b5-141">`[MigrationId <String>]`：遷移作業 guid 名稱。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-141">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="5b6b5-142">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-142">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="5b6b5-143">`[Publisher <String>]`：發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-143">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="5b6b5-144">`[QuotaName <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-144">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="5b6b5-145">`[Sku <String>]`： SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-145">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="5b6b5-146">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5b6b5-147">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5b6b5-148">`[Type <String>]`：延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-148">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="5b6b5-149">`[Version <String>]`：資源的版本。</span><span class="sxs-lookup"><span data-stu-id="5b6b5-149">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="5b6b5-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b6b5-150">RELATED LINKS</span></span>

