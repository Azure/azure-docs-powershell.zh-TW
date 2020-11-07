---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: 127cbe1efb710fff04420590985e97ee72a196a9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794923"
---
# <span data-ttu-id="12e16-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="12e16-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="12e16-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12e16-102">SYNOPSIS</span></span>
<span data-ttu-id="12e16-103">使用指定的發行者、優惠、sku 及版本建立新的平臺影像。</span><span class="sxs-lookup"><span data-stu-id="12e16-103">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="12e16-104">句法</span><span class="sxs-lookup"><span data-stu-id="12e16-104">SYNTAX</span></span>

### <span data-ttu-id="12e16-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="12e16-105">CreateExpanded (Default)</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-BillingPartNumber <String>] [-DataDisks <IDataDisk[]>] [-OsType <OSType>]
 [-OsUri <String>] [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12e16-106">建立</span><span class="sxs-lookup"><span data-stu-id="12e16-106">Create</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 -NewImage <IPlatformImageParameters> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12e16-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="12e16-107">CreateViaIdentity</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> -NewImage <IPlatformImageParameters>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12e16-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="12e16-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-BillingPartNumber <String>]
 [-DataDisks <IDataDisk[]>] [-OsType <OSType>] [-OsUri <String>] [-ProvisioningState <ProvisioningState>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="12e16-109">說明</span><span class="sxs-lookup"><span data-stu-id="12e16-109">DESCRIPTION</span></span>
<span data-ttu-id="12e16-110">使用指定的發行者、優惠、sku 及版本建立新的平臺影像。</span><span class="sxs-lookup"><span data-stu-id="12e16-110">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="12e16-111">示例</span><span class="sxs-lookup"><span data-stu-id="12e16-111">EXAMPLES</span></span>

### <span data-ttu-id="12e16-112">範例1： Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="12e16-112">Example 1: Add-AzsPlatformImage</span></span>
```powershell
PS C:\> Add-AzsPlatformImage -Offer "asdf" -Publisher "asdf" -Sku "asdf" -Version "1.0.0" -OsType Windows -OsUri "https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https&sig=CKkE2r9MJc%2FK40PjRB5Tfz6DArxNd0akD90IvKJX95g%3D"

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
#Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="12e16-113">從 Blob 儲存體新增平臺影像。</span><span class="sxs-lookup"><span data-stu-id="12e16-113">Add a Platform Image from Blob Storage.</span></span> <span data-ttu-id="12e16-114">使用 a SasUri 指定 PlatformImage 的位置，或使用公開存取的 URL。</span><span class="sxs-lookup"><span data-stu-id="12e16-114">Use the a SasUri to specify the location of the PlatformImage, or use a publicly accessible URL.</span></span>

## <span data-ttu-id="12e16-115">參數</span><span class="sxs-lookup"><span data-stu-id="12e16-115">PARAMETERS</span></span>

### <span data-ttu-id="12e16-116">例外狀況。訊息</span><span class="sxs-lookup"><span data-stu-id="12e16-116">Exception.Message</span></span>
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

### <span data-ttu-id="12e16-117">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="12e16-117">-BillingPartNumber</span></span>
<span data-ttu-id="12e16-118">組件編號是用來帳單軟體成本。</span><span class="sxs-lookup"><span data-stu-id="12e16-118">The part number is used to bill for software costs.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12e16-119">-DataDisks</span><span class="sxs-lookup"><span data-stu-id="12e16-119">-DataDisks</span></span>
<span data-ttu-id="12e16-120">平臺影像所使用的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="12e16-120">Data disks used by the platform image.</span></span>
<span data-ttu-id="12e16-121">若要建立，請參閱 DATADISKS 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="12e16-121">To construct, see NOTES section for DATADISKS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IDataDisk[]
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12e16-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e16-122">-DefaultProfile</span></span>
<span data-ttu-id="12e16-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12e16-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12e16-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12e16-124">-InputObject</span></span>
<span data-ttu-id="12e16-125">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="12e16-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="12e16-126">-位置</span><span class="sxs-lookup"><span data-stu-id="12e16-126">-Location</span></span>
<span data-ttu-id="12e16-127">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="12e16-127">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12e16-128">-NewImage</span><span class="sxs-lookup"><span data-stu-id="12e16-128">-NewImage</span></span>
<span data-ttu-id="12e16-129">用來建立新平臺影像的參數。</span><span class="sxs-lookup"><span data-stu-id="12e16-129">Parameters used to create a new platform image.</span></span>
<span data-ttu-id="12e16-130">若要建立，請參閱 NEWIMAGE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="12e16-130">To construct, see NOTES section for NEWIMAGE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="12e16-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="12e16-131">-NoWait</span></span>
<span data-ttu-id="12e16-132">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="12e16-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="12e16-133">-優惠</span><span class="sxs-lookup"><span data-stu-id="12e16-133">-Offer</span></span>
<span data-ttu-id="12e16-134">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e16-134">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12e16-135">-OsType</span><span class="sxs-lookup"><span data-stu-id="12e16-135">-OsType</span></span>
<span data-ttu-id="12e16-136">作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="12e16-136">Operating system type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.OSType
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12e16-137">-OsUri</span><span class="sxs-lookup"><span data-stu-id="12e16-137">-OsUri</span></span>
<span data-ttu-id="12e16-138">磁片的位置。</span><span class="sxs-lookup"><span data-stu-id="12e16-138">Location of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12e16-139">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="12e16-139">-ProvisioningState</span></span>
<span data-ttu-id="12e16-140">平臺影像的提供狀態。</span><span class="sxs-lookup"><span data-stu-id="12e16-140">Provisioning status of the platform image.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12e16-141">-Publisher</span><span class="sxs-lookup"><span data-stu-id="12e16-141">-Publisher</span></span>
<span data-ttu-id="12e16-142">發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e16-142">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12e16-143">-Sku</span><span class="sxs-lookup"><span data-stu-id="12e16-143">-Sku</span></span>
<span data-ttu-id="12e16-144">SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e16-144">Name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12e16-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12e16-145">-SubscriptionId</span></span>
<span data-ttu-id="12e16-146">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="12e16-146">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="12e16-147">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="12e16-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12e16-148">-版本</span><span class="sxs-lookup"><span data-stu-id="12e16-148">-Version</span></span>
<span data-ttu-id="12e16-149">資源的版本。</span><span class="sxs-lookup"><span data-stu-id="12e16-149">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12e16-150">-確認</span><span class="sxs-lookup"><span data-stu-id="12e16-150">-Confirm</span></span>
<span data-ttu-id="12e16-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="12e16-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12e16-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12e16-152">-WhatIf</span></span>
<span data-ttu-id="12e16-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12e16-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12e16-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12e16-154">The cmdlet is not run.</span></span>

### <span data-ttu-id="12e16-155">例外狀況。訊息</span><span class="sxs-lookup"><span data-stu-id="12e16-155">Exception.Message</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12e16-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e16-156">CommonParameters</span></span>
<span data-ttu-id="12e16-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12e16-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e16-158">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="12e16-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e16-159">輸入</span><span class="sxs-lookup"><span data-stu-id="12e16-159">INPUTS</span></span>

### <span data-ttu-id="12e16-160">IPlatformImageParameters （ComputeAdmin）。 Api20151201Preview。</span><span class="sxs-lookup"><span data-stu-id="12e16-160">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters</span></span>

### <span data-ttu-id="12e16-161">IComputeAdminIdentity （ComputeAdmin）的</span><span class="sxs-lookup"><span data-stu-id="12e16-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="12e16-162">輸出</span><span class="sxs-lookup"><span data-stu-id="12e16-162">OUTPUTS</span></span>

### <span data-ttu-id="12e16-163">IPlatformImage （ComputeAdmin）。 Api20151201Preview。</span><span class="sxs-lookup"><span data-stu-id="12e16-163">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="12e16-164">筆記</span><span class="sxs-lookup"><span data-stu-id="12e16-164">NOTES</span></span>

<span data-ttu-id="12e16-165">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="12e16-165">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12e16-166">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="12e16-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="12e16-167">DATADISKS <IDataDisk [] >：平臺影像所使用的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="12e16-167">DATADISKS <IDataDisk[]>: Data disks used by the platform image.</span></span>
  - <span data-ttu-id="12e16-168">`[Lun <Int32?>]`：邏輯單元號碼。</span><span class="sxs-lookup"><span data-stu-id="12e16-168">`[Lun <Int32?>]`: Logical unit number.</span></span>
  - <span data-ttu-id="12e16-169">`[Uri <String>]`：磁片模版的位置。</span><span class="sxs-lookup"><span data-stu-id="12e16-169">`[Uri <String>]`: Location of the disk template.</span></span>

<span data-ttu-id="12e16-170">INPUTOBJECT <IComputeAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="12e16-170">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="12e16-171">`[DiskId <String>]`：磁片 guid 作為身分識別。</span><span class="sxs-lookup"><span data-stu-id="12e16-171">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="12e16-172">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="12e16-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="12e16-173">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="12e16-173">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="12e16-174">`[MigrationId <String>]`：遷移作業 guid 名稱。</span><span class="sxs-lookup"><span data-stu-id="12e16-174">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="12e16-175">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e16-175">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="12e16-176">`[Publisher <String>]`：發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e16-176">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="12e16-177">`[QuotaName <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e16-177">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="12e16-178">`[Sku <String>]`： SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e16-178">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="12e16-179">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="12e16-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="12e16-180">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="12e16-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="12e16-181">`[Type <String>]`：延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="12e16-181">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="12e16-182">`[Version <String>]`：資源的版本。</span><span class="sxs-lookup"><span data-stu-id="12e16-182">`[Version <String>]`: The version of the resource.</span></span>

<span data-ttu-id="12e16-183">NEWIMAGE <IPlatformImageParameters> ：用來建立新平臺影像的參數。</span><span class="sxs-lookup"><span data-stu-id="12e16-183">NEWIMAGE <IPlatformImageParameters>: Parameters used to create a new platform image.</span></span>
  - <span data-ttu-id="12e16-184">`[DataDisk <IDataDisk[]>]`：平臺影像所使用的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="12e16-184">`[DataDisk <IDataDisk[]>]`: Data disks used by the platform image.</span></span>
    - <span data-ttu-id="12e16-185">`[Lun <Int32?>]`：邏輯單元號碼。</span><span class="sxs-lookup"><span data-stu-id="12e16-185">`[Lun <Int32?>]`: Logical unit number.</span></span>
    - <span data-ttu-id="12e16-186">`[Uri <String>]`：磁片模版的位置。</span><span class="sxs-lookup"><span data-stu-id="12e16-186">`[Uri <String>]`: Location of the disk template.</span></span>
  - <span data-ttu-id="12e16-187">`[DetailBillingPartNumber <String>]`： [部件編號] 用來帳單軟體成本。</span><span class="sxs-lookup"><span data-stu-id="12e16-187">`[DetailBillingPartNumber <String>]`: The part number is used to bill for software costs.</span></span>
  - <span data-ttu-id="12e16-188">`[OSDiskOstype <OSType?>]`：作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="12e16-188">`[OSDiskOstype <OSType?>]`: Operating system type.</span></span>
  - <span data-ttu-id="12e16-189">`[OSDiskUri <String>]`：磁片位置。</span><span class="sxs-lookup"><span data-stu-id="12e16-189">`[OSDiskUri <String>]`: Location of the disk.</span></span>
  - <span data-ttu-id="12e16-190">`[ProvisioningState <ProvisioningState?>]`：配置平臺影像的狀態。</span><span class="sxs-lookup"><span data-stu-id="12e16-190">`[ProvisioningState <ProvisioningState?>]`: Provisioning status of the platform image.</span></span>

## <span data-ttu-id="12e16-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="12e16-191">RELATED LINKS</span></span>

