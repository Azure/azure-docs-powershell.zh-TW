---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdisk
schema: 2.0.0
ms.openlocfilehash: 9c3c87e7c62764cff0a7d6b9d65a3dfe3df31990
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968521"
---
# <span data-ttu-id="2f0a8-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="2f0a8-101">Get-AzsDisk</span></span>

## <span data-ttu-id="2f0a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f0a8-102">SYNOPSIS</span></span>
<span data-ttu-id="2f0a8-103">傳回磁片。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-103">Returns the disk.</span></span>

## <span data-ttu-id="2f0a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f0a8-104">SYNTAX</span></span>

### <span data-ttu-id="2f0a8-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="2f0a8-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-SubscriptionId <String[]>] [-Count <Int32>] [-ScaleUnit <String>]
 [-SharePath <String>] [-Start <Int32>] [-Status <String>] [-UserSubscriptionId <String>]
 [-VolumeLabel <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2f0a8-106">獲取</span><span class="sxs-lookup"><span data-stu-id="2f0a8-106">Get</span></span>
```
Get-AzsDisk -Name <String> [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f0a8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2f0a8-107">GetViaIdentity</span></span>
```
Get-AzsDisk -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2f0a8-108">說明</span><span class="sxs-lookup"><span data-stu-id="2f0a8-108">DESCRIPTION</span></span>
<span data-ttu-id="2f0a8-109">傳回磁片。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-109">Returns the disk.</span></span>

## <span data-ttu-id="2f0a8-110">示例</span><span class="sxs-lookup"><span data-stu-id="2f0a8-110">EXAMPLES</span></span>

### <span data-ttu-id="2f0a8-111">範例1：取得所有磁片</span><span class="sxs-lookup"><span data-stu-id="2f0a8-111">Example 1: Get All Disks</span></span> 
```powershell
PS C:\> Get-AzsDisk
```

<span data-ttu-id="2f0a8-112">如果沒有任何參數， `Get-AzsDisk` 將會列出所有磁片。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-112">Without any parameters, `Get-AzsDisk` will list all Disks.</span></span>

### <span data-ttu-id="2f0a8-113">範例2：依名稱取得磁片</span><span class="sxs-lookup"><span data-stu-id="2f0a8-113">Example 2: Get a Disk by Name</span></span>
```powershell
PS C:\> Get-AzsDisk -Name "426b8945-8a24-42ad-acdc-c26f16202489"

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="2f0a8-114">您可以指定磁片 `Name` 來取得磁片。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-114">Specify a disk by its `Name` to retrieve it.</span></span>

### <span data-ttu-id="2f0a8-115">範例3：取得指定的磁片數</span><span class="sxs-lookup"><span data-stu-id="2f0a8-115">Example 3: Get a Specified number of Disks</span></span>
```powershell
PS C:\>  Get-AzsDisk -Count 3

ActualSizeGb    : 24
DiskId          : 20f1619e-4210-47f6-81e6-b89e3028df06
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/20f1619e-4210-47f6-81e6-b89e3028df06
Location        : northwest
ManagedBy       :
Name            : northwest/20f1619e-4210-47f6-81e6-b89e3028df06
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/RG1/providers/Microsoft.Compute/Di
                  sks/TEST_OsDisk_1_20f1619e421047f681e6b89e3028df06

ActualSizeGb    : 24
DiskId          : 38a767e4-4ceb-49fb-a53c-48de9b08aaae
DiskSku         : Standard_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/38a767e4-4ceb-49fb-a53c-48de9b08aaae
Location        : northwest
ManagedBy       :
Name            : northwest/38a767e4-4ceb-49fb-a53c-48de9b08aaae
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/SCTE/providers/Microsoft.Compute/D
                  isks/SCTETest_OsDisk_1_38a767e44ceb49fba53c48de9b08aaae

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="2f0a8-116">使用 `Count` 參數來檢索特定的磁片數。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-116">Use the `Count` parameter to retrieve a specific number of disks.</span></span>

### <span data-ttu-id="2f0a8-117">範例4：取得特定位置中的所有磁片</span><span class="sxs-lookup"><span data-stu-id="2f0a8-117">Example 4: Get all disks in specific location</span></span>
```powershell
PS C:\> Get-AzsDisk -Status All -ScaleUnit s-cluster -VolumeLabel Objstore_4

ActualSizeGb    : 2
DiskId          : e4732f76-0753-40ec-80f5-8effdd0b437d
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/e4732f76-0753-40ec-80f5-8effdd0b437d
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/e4732f76-0753-40ec-80f5-8effdd0b437d
ProvisionSizeGb : 30
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/test1_OsDisk_1_e4732f76075340ec80f58effdd0b437d

ActualSizeGb    : 1
DiskId          : 0485cbc9-1efa-43bd-86c2-0e201d79c528
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/0485cbc9-1efa-43bd-86c2-0e201d79c528
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/0485cbc9-1efa-43bd-86c2-0e201d79c528
ProvisionSizeGb : 64
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/TESTRG1/providers/Microsoft.Compute/Disks/gpsdisk

ActualSizeGb    : 1
DiskId          : 137893db-e7ce-4907-a488-b35c5e928614
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/137893db-e7ce-4907-a488-b35c5e928614
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/137893db-e7ce-4907-a488-b35c5e928614
ProvisionSizeGb : 55
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/testdd
```

<span data-ttu-id="2f0a8-118">使用 `ScaleUnit` or `VolumeLabel` 參數列出特定位置中的所有磁片</span><span class="sxs-lookup"><span data-stu-id="2f0a8-118">Use the `ScaleUnit` or `VolumeLabel` parameter to list all disks in specific location</span></span>

## <span data-ttu-id="2f0a8-119">參數</span><span class="sxs-lookup"><span data-stu-id="2f0a8-119">PARAMETERS</span></span>

### <span data-ttu-id="2f0a8-120">-Count</span><span class="sxs-lookup"><span data-stu-id="2f0a8-120">-Count</span></span>
<span data-ttu-id="2f0a8-121">要傳回的磁片數量上限。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-121">The maximum number of disks to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f0a8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f0a8-122">-DefaultProfile</span></span>
<span data-ttu-id="2f0a8-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f0a8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f0a8-124">-InputObject</span></span>
<span data-ttu-id="2f0a8-125">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2f0a8-126">-位置</span><span class="sxs-lookup"><span data-stu-id="2f0a8-126">-Location</span></span>
<span data-ttu-id="2f0a8-127">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-127">Location of the resource.</span></span>

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

### <span data-ttu-id="2f0a8-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f0a8-128">-Name</span></span>
<span data-ttu-id="2f0a8-129">以身分識別的磁片 guid。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-129">The disk guid as identity.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f0a8-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="2f0a8-130">-ScaleUnit</span></span>
<span data-ttu-id="2f0a8-131">資源所屬的縮放單位。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-131">The scale unit which the resource belongs to.</span></span>

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

### <span data-ttu-id="2f0a8-132">-SharePath</span><span class="sxs-lookup"><span data-stu-id="2f0a8-132">-SharePath</span></span>
<span data-ttu-id="2f0a8-133">資源所屬的共用。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-133">The share which the resource belongs to.</span></span>

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

### <span data-ttu-id="2f0a8-134">-開始</span><span class="sxs-lookup"><span data-stu-id="2f0a8-134">-Start</span></span>
<span data-ttu-id="2f0a8-135">Query 中磁片的起始索引。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-135">The start index of disks in query.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f0a8-136">-狀態</span><span class="sxs-lookup"><span data-stu-id="2f0a8-136">-Status</span></span>
<span data-ttu-id="2f0a8-137">磁片狀態的參數。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-137">The parameters of disk state.</span></span>

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

### <span data-ttu-id="2f0a8-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f0a8-138">-SubscriptionId</span></span>
<span data-ttu-id="2f0a8-139">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2f0a8-140">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2f0a8-141">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f0a8-141">-UserSubscriptionId</span></span>
<span data-ttu-id="2f0a8-142">資源所屬的使用者訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-142">User Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="2f0a8-143">-VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="2f0a8-143">-VolumeLabel</span></span>
<span data-ttu-id="2f0a8-144">資源所屬卷的標籤。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-144">The volume label of the volume which the resource belongs to.</span></span>

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

### <span data-ttu-id="2f0a8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0a8-145">CommonParameters</span></span>
<span data-ttu-id="2f0a8-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0a8-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0a8-148">輸入</span><span class="sxs-lookup"><span data-stu-id="2f0a8-148">INPUTS</span></span>

### <span data-ttu-id="2f0a8-149">IComputeAdminIdentity （ComputeAdmin）的</span><span class="sxs-lookup"><span data-stu-id="2f0a8-149">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="2f0a8-150">輸出</span><span class="sxs-lookup"><span data-stu-id="2f0a8-150">OUTPUTS</span></span>

### <span data-ttu-id="2f0a8-151">IDisk （ComputeAdmin）。 Api20180730Preview。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk</span></span>



## <span data-ttu-id="2f0a8-152">筆記</span><span class="sxs-lookup"><span data-stu-id="2f0a8-152">NOTES</span></span>

<span data-ttu-id="2f0a8-153">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-153">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2f0a8-154">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2f0a8-155">INPUTOBJECT <IComputeAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="2f0a8-155">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2f0a8-156">`[DiskId <String>]`：磁片 guid 作為身分識別。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-156">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="2f0a8-157">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="2f0a8-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2f0a8-158">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="2f0a8-159">`[MigrationId <String>]`：遷移作業 guid 名稱。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-159">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="2f0a8-160">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-160">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="2f0a8-161">`[Publisher <String>]`：發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-161">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="2f0a8-162">`[QuotaName <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-162">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="2f0a8-163">`[Sku <String>]`： SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-163">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="2f0a8-164">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2f0a8-165">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2f0a8-166">`[Type <String>]`：延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-166">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="2f0a8-167">`[Version <String>]`：資源的版本。</span><span class="sxs-lookup"><span data-stu-id="2f0a8-167">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="2f0a8-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f0a8-168">RELATED LINKS</span></span>

