---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: 96c14cd8d8d48b6212ed0e4c7b0d5934754912a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796582"
---
# <span data-ttu-id="dc3e3-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="dc3e3-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="dc3e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc3e3-102">SYNOPSIS</span></span>
<span data-ttu-id="dc3e3-103">傳回要求的磁片遷移作業。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-103">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="dc3e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc3e3-104">SYNTAX</span></span>

### <span data-ttu-id="dc3e3-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="dc3e3-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] [-SubscriptionId <String[]>] [-Status <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc3e3-106">獲取</span><span class="sxs-lookup"><span data-stu-id="dc3e3-106">Get</span></span>
```
Get-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc3e3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dc3e3-107">GetViaIdentity</span></span>
```
Get-AzsDiskMigrationJob -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dc3e3-108">說明</span><span class="sxs-lookup"><span data-stu-id="dc3e3-108">DESCRIPTION</span></span>
<span data-ttu-id="dc3e3-109">傳回要求的磁片遷移作業。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-109">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="dc3e3-110">示例</span><span class="sxs-lookup"><span data-stu-id="dc3e3-110">EXAMPLES</span></span>

### <span data-ttu-id="dc3e3-111">範例1：</span><span class="sxs-lookup"><span data-stu-id="dc3e3-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob
```

<span data-ttu-id="dc3e3-112">傳回本機位置的受管理磁片遷移作業清單。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-112">Returns a list of managed disk migration jobs at the location local.</span></span>

### <span data-ttu-id="dc3e3-113">範例2：</span><span class="sxs-lookup"><span data-stu-id="dc3e3-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob -Name TestNewDiskMigrationJob

CreationTime : 2/26/2020 10:45:41 AM
EndTime      : 2/26/2020 10:46:32 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestNewDiskMigrationJob
Location     : redmond
MigrationId  : TestNewDiskMigrationJob
Name         : redmond/TestNewDiskMigrationJob
StartTime    : 2/26/2020 10:45:41 AM
Status       : Succeeded
Subtask      : {edacd0f6-760a-43f9-a188-8833751f89ce, f1ee38a4-5c27-4728-a12b-36976c565042}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_1
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="dc3e3-114">取得特定的受管理磁片遷移作業。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-114">Get a specific managed disk migration job.</span></span>

## <span data-ttu-id="dc3e3-115">參數</span><span class="sxs-lookup"><span data-stu-id="dc3e3-115">PARAMETERS</span></span>

### <span data-ttu-id="dc3e3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc3e3-116">-DefaultProfile</span></span>
<span data-ttu-id="dc3e3-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc3e3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc3e3-118">-InputObject</span></span>
<span data-ttu-id="dc3e3-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dc3e3-120">-位置</span><span class="sxs-lookup"><span data-stu-id="dc3e3-120">-Location</span></span>
<span data-ttu-id="dc3e3-121">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-121">Location of the resource.</span></span>

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

### <span data-ttu-id="dc3e3-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc3e3-122">-Name</span></span>
<span data-ttu-id="dc3e3-123">[遷移作業 guid] 名稱。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-123">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dc3e3-124">-狀態</span><span class="sxs-lookup"><span data-stu-id="dc3e3-124">-Status</span></span>
<span data-ttu-id="dc3e3-125">磁片遷移作業狀態的參數。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-125">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="dc3e3-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc3e3-126">-SubscriptionId</span></span>
<span data-ttu-id="dc3e3-127">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-127">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dc3e3-128">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dc3e3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc3e3-129">CommonParameters</span></span>
<span data-ttu-id="dc3e3-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc3e3-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc3e3-132">輸入</span><span class="sxs-lookup"><span data-stu-id="dc3e3-132">INPUTS</span></span>

### <span data-ttu-id="dc3e3-133">IComputeAdminIdentity （ComputeAdmin）的</span><span class="sxs-lookup"><span data-stu-id="dc3e3-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="dc3e3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="dc3e3-134">OUTPUTS</span></span>

### <span data-ttu-id="dc3e3-135">IDiskMigrationJob （ComputeAdmin）。 Api20180730Preview。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="dc3e3-136">筆記</span><span class="sxs-lookup"><span data-stu-id="dc3e3-136">NOTES</span></span>

<span data-ttu-id="dc3e3-137">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc3e3-138">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="dc3e3-139">INPUTOBJECT <IComputeAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="dc3e3-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dc3e3-140">`[DiskId <String>]`：磁片 guid 作為身分識別。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="dc3e3-141">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="dc3e3-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dc3e3-142">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="dc3e3-143">`[MigrationId <String>]`：遷移作業 guid 名稱。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="dc3e3-144">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="dc3e3-145">`[Publisher <String>]`：發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="dc3e3-146">`[QuotaName <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="dc3e3-147">`[Sku <String>]`： SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="dc3e3-148">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dc3e3-149">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="dc3e3-150">`[Type <String>]`：延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="dc3e3-151">`[Version <String>]`：資源的版本。</span><span class="sxs-lookup"><span data-stu-id="dc3e3-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="dc3e3-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc3e3-152">RELATED LINKS</span></span>

