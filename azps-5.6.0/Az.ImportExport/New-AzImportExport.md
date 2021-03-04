---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: e38402359a3bccebc33d92211ed10d8032a0dd4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908197"
---
# <span data-ttu-id="e8469-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="e8469-101">New-AzImportExport</span></span>

## <span data-ttu-id="e8469-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e8469-102">SYNOPSIS</span></span>
<span data-ttu-id="e8469-103">建立新工作或更新指定訂閱中的現有工作。</span><span class="sxs-lookup"><span data-stu-id="e8469-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="e8469-104">語法</span><span class="sxs-lookup"><span data-stu-id="e8469-104">SYNTAX</span></span>

```
New-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-ClientTenantId <String>] [-BackupDriveManifest] [-BlobListBlobPath <String[]>]
 [-BlobListBlobPathPrefix <String[]>] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DiagnosticsPath <String>] [-DriveList <IDriveStatus[]>]
 [-ExportBlobListblobPath <String>] [-IncompleteBlobListUri <String>] [-JobType <String>] [-Location <String>]
 [-LogLevel <String>] [-PercentComplete <Int32>] [-ProvisioningState <String>] [-ReturnAddressCity <String>]
 [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>]
 [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnPackageCarrierName <String>]
 [-ReturnPackageDriveCount <Int32>] [-ReturnPackageShipDate <String>] [-ReturnPackageTrackingNumber <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>]
 [-ShippingInformationCity <String>] [-ShippingInformationCountryOrRegion <String>]
 [-ShippingInformationPhone <String>] [-ShippingInformationPostalCode <String>]
 [-ShippingInformationRecipientName <String>] [-ShippingInformationStateOrProvince <String>]
 [-ShippingInformationStreetAddress1 <String>] [-ShippingInformationStreetAddress2 <String>] [-State <String>]
 [-StorageAccountId <String>] [-Tag <IPutJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e8469-105">描述</span><span class="sxs-lookup"><span data-stu-id="e8469-105">DESCRIPTION</span></span>
<span data-ttu-id="e8469-106">建立新工作或更新指定訂閱中的現有工作。</span><span class="sxs-lookup"><span data-stu-id="e8469-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="e8469-107">例子</span><span class="sxs-lookup"><span data-stu-id="e8469-107">EXAMPLES</span></span>

### <span data-ttu-id="e8469-108">範例 1：建立新的 ImportExport 工作</span><span class="sxs-lookup"><span data-stu-id="e8469-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="e8469-109">這些 Cmdlet 會建立新的 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="e8469-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="e8469-110">參數</span><span class="sxs-lookup"><span data-stu-id="e8469-110">PARAMETERS</span></span>

### <span data-ttu-id="e8469-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="e8469-111">-AcceptLanguage</span></span>
<span data-ttu-id="e8469-112">指定回應的偏好語言。</span><span class="sxs-lookup"><span data-stu-id="e8469-112">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="e8469-113">-BackupDriveManifest</span></span>
<span data-ttu-id="e8469-114">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="e8469-114">Default value is false.</span></span>
<span data-ttu-id="e8469-115">指出是否應該複製磁片磁碟機上的清單檔案以封鎖 Blob。</span><span class="sxs-lookup"><span data-stu-id="e8469-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="e8469-116">-BlobListBlobPath</span><span class="sxs-lookup"><span data-stu-id="e8469-116">-BlobListBlobPath</span></span>
<span data-ttu-id="e8469-117">Blob 路徑字串的集合。</span><span class="sxs-lookup"><span data-stu-id="e8469-117">A collection of blob-path strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-118">-BlobListBlobPathPrefix</span><span class="sxs-lookup"><span data-stu-id="e8469-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="e8469-119">Blob 首碼字串的集合。</span><span class="sxs-lookup"><span data-stu-id="e8469-119">A collection of blob-prefix strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-120">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="e8469-120">-CancelRequested</span></span>
<span data-ttu-id="e8469-121">表示是否已提交取消工作的要求。</span><span class="sxs-lookup"><span data-stu-id="e8469-121">Indicates whether a request has been submitted to cancel the job.</span></span>

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

### <span data-ttu-id="e8469-122">-ClientTenantId</span><span class="sxs-lookup"><span data-stu-id="e8469-122">-ClientTenantId</span></span>
<span data-ttu-id="e8469-123">提出要求之用戶端的租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8469-123">The tenant ID of the client making the request.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8469-124">-DefaultProfile</span></span>
<span data-ttu-id="e8469-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8469-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8469-126">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="e8469-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="e8469-127">用來出貨匯進或匯出磁片磁碟機的電信業者名稱。</span><span class="sxs-lookup"><span data-stu-id="e8469-127">The name of the carrier that is used to ship the import or export drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-128">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="e8469-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="e8469-129">套件中包含的磁片磁碟機數量。</span><span class="sxs-lookup"><span data-stu-id="e8469-129">The number of drives included in the package.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-130">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="e8469-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="e8469-131">包裹出貨日期。</span><span class="sxs-lookup"><span data-stu-id="e8469-131">The date when the package is shipped.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-132">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="e8469-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="e8469-133">包裹的追蹤編號。</span><span class="sxs-lookup"><span data-stu-id="e8469-133">The tracking number of the package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-134">-DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="e8469-134">-DiagnosticsPath</span></span>
<span data-ttu-id="e8469-135">虛擬 Blob 目錄，其中會儲存磁片磁碟機清單檔案的複製記錄 (如果已啟用) 備份。</span><span class="sxs-lookup"><span data-stu-id="e8469-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="e8469-136">-DriveList</span></span>
<span data-ttu-id="e8469-137">包含工作最多十個磁片磁碟機的清單。</span><span class="sxs-lookup"><span data-stu-id="e8469-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="e8469-138">硬碟清單是一項匯出工作所需的元素;未指定匯出工作。</span><span class="sxs-lookup"><span data-stu-id="e8469-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="e8469-139">若要建構，請參閱 DRIVELIST 屬性的附注區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e8469-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-140">-ExportBlobListblobPath</span><span class="sxs-lookup"><span data-stu-id="e8469-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="e8469-141">包含如上述定義之 Blob 路徑清單或 Blob 路徑首碼清單的區塊 Blob 的相對 URI，從容器名稱開始。</span><span class="sxs-lookup"><span data-stu-id="e8469-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="e8469-142">如果 blob 位於根容器中，URI 必須以 $root。</span><span class="sxs-lookup"><span data-stu-id="e8469-142">If the blob is in root container, the URI must begin with $root.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-143">-未完成BlobListUri</span><span class="sxs-lookup"><span data-stu-id="e8469-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="e8469-144">指向包含 Blob 名稱清單的 Blob 路徑，該 Blob 路徑因磁碟機空間不足而未匯出。</span><span class="sxs-lookup"><span data-stu-id="e8469-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="e8469-145">如果已成功匯出所有 Blob，則此元素不會包含在回應中。</span><span class="sxs-lookup"><span data-stu-id="e8469-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-146">-JobType</span><span class="sxs-lookup"><span data-stu-id="e8469-146">-JobType</span></span>
<span data-ttu-id="e8469-147">工作類型</span><span class="sxs-lookup"><span data-stu-id="e8469-147">The type of job</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-148">-位置</span><span class="sxs-lookup"><span data-stu-id="e8469-148">-Location</span></span>
<span data-ttu-id="e8469-149">指定應建立工作的受支援 Azure 位置</span><span class="sxs-lookup"><span data-stu-id="e8469-149">Specifies the supported Azure location where the job should be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="e8469-150">-LogLevel</span></span>
<span data-ttu-id="e8469-151">預設值為錯誤。</span><span class="sxs-lookup"><span data-stu-id="e8469-151">Default value is Error.</span></span>
<span data-ttu-id="e8469-152">指出是否會啟用錯誤記錄或詳細記錄。</span><span class="sxs-lookup"><span data-stu-id="e8469-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-153">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8469-153">-Name</span></span>
<span data-ttu-id="e8469-154">匯進/匯出工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8469-154">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-155">-完成百分比</span><span class="sxs-lookup"><span data-stu-id="e8469-155">-PercentComplete</span></span>
<span data-ttu-id="e8469-156">已完成該工作的整體百分比。</span><span class="sxs-lookup"><span data-stu-id="e8469-156">Overall percentage completed for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="e8469-157">-ProvisioningState</span></span>
<span data-ttu-id="e8469-158">指定工作的撥備狀態。</span><span class="sxs-lookup"><span data-stu-id="e8469-158">Specifies the provisioning state of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8469-159">-ResourceGroupName</span></span>
<span data-ttu-id="e8469-160">資源組名可唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e8469-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="e8469-161">-ReturnAddressCity</span></span>
<span data-ttu-id="e8469-162">要用於退回磁片磁碟機的城市名稱。</span><span class="sxs-lookup"><span data-stu-id="e8469-162">The city name to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="e8469-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="e8469-164">退回磁片磁碟機時要使用的國家/地區或地區。</span><span class="sxs-lookup"><span data-stu-id="e8469-164">The country or region to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="e8469-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="e8469-166">所退回磁片磁碟機收件者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="e8469-166">Email address of the recipient of the returned drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="e8469-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="e8469-168">所退回磁片磁碟機收件者的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="e8469-168">Phone number of the recipient of the returned drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-169">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="e8469-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="e8469-170">退回磁片磁碟機時使用的郵遞區號。</span><span class="sxs-lookup"><span data-stu-id="e8469-170">The postal code to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="e8469-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="e8469-172">收到硬碟的收件者名稱。</span><span class="sxs-lookup"><span data-stu-id="e8469-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-173">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="e8469-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="e8469-174">退回磁片磁碟機時所使用之省/市。</span><span class="sxs-lookup"><span data-stu-id="e8469-174">The state or province to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-175">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="e8469-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="e8469-176">退回磁片磁碟機時，所使用街地道號的第一行。</span><span class="sxs-lookup"><span data-stu-id="e8469-176">The first line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-177">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="e8469-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="e8469-178">退回磁片磁碟機時，所使用之街地道道的第二行。</span><span class="sxs-lookup"><span data-stu-id="e8469-178">The second line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-179">-ReturnPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="e8469-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="e8469-180">用來出貨匯進或匯出磁片磁碟機的電信業者名稱。</span><span class="sxs-lookup"><span data-stu-id="e8469-180">The name of the carrier that is used to ship the import or export drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="e8469-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="e8469-182">套件中包含的磁片磁碟機數量。</span><span class="sxs-lookup"><span data-stu-id="e8469-182">The number of drives included in the package.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="e8469-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="e8469-184">包裹出貨日期。</span><span class="sxs-lookup"><span data-stu-id="e8469-184">The date when the package is shipped.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-185">-ReturnPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="e8469-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="e8469-186">包裹的追蹤編號。</span><span class="sxs-lookup"><span data-stu-id="e8469-186">The tracking number of the package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="e8469-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="e8469-188">客戶與電信公司的帳戶號碼。</span><span class="sxs-lookup"><span data-stu-id="e8469-188">The customer's account number with the carrier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="e8469-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="e8469-190">電信公司的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8469-190">The carrier's name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-191">-ShippingInformationCity</span><span class="sxs-lookup"><span data-stu-id="e8469-191">-ShippingInformationCity</span></span>
<span data-ttu-id="e8469-192">要用於退回磁片磁碟機的城市名稱。</span><span class="sxs-lookup"><span data-stu-id="e8469-192">The city name to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-193">-ShippingInformationCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="e8469-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="e8469-194">退回磁片磁碟機時要使用的國家/地區或地區。</span><span class="sxs-lookup"><span data-stu-id="e8469-194">The country or region to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-195">-ShippingInformationPhone</span><span class="sxs-lookup"><span data-stu-id="e8469-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="e8469-196">所退回磁片磁碟機收件者的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="e8469-196">Phone number of the recipient of the returned drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-197">-ShippingInformationPostalCode</span><span class="sxs-lookup"><span data-stu-id="e8469-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="e8469-198">退回磁片磁碟機時使用的郵遞區號。</span><span class="sxs-lookup"><span data-stu-id="e8469-198">The postal code to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-199">-ShippingInformationRecipientName</span><span class="sxs-lookup"><span data-stu-id="e8469-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="e8469-200">收到硬碟的收件者名稱。</span><span class="sxs-lookup"><span data-stu-id="e8469-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-201">-ShippingInformationStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="e8469-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="e8469-202">退回磁片磁碟機時所使用之省/市。</span><span class="sxs-lookup"><span data-stu-id="e8469-202">The state or province to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-203">-ShippingInformationStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="e8469-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="e8469-204">退回磁片磁碟機時，所使用街地道號的第一行。</span><span class="sxs-lookup"><span data-stu-id="e8469-204">The first line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-205">-ShippingInformationStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="e8469-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="e8469-206">退回磁片磁碟機時，所使用之街地道道的第二行。</span><span class="sxs-lookup"><span data-stu-id="e8469-206">The second line of the street address to use when returning the drives.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-207">-State</span><span class="sxs-lookup"><span data-stu-id="e8469-207">-State</span></span>
<span data-ttu-id="e8469-208">工作的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="e8469-208">Current state of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-209">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e8469-209">-StorageAccountId</span></span>
<span data-ttu-id="e8469-210">要匯進或匯出資料的儲存空間帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8469-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-211">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8469-211">-SubscriptionId</span></span>
<span data-ttu-id="e8469-212">Azure 使用者的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8469-212">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-213">-標記</span><span class="sxs-lookup"><span data-stu-id="e8469-213">-Tag</span></span>
<span data-ttu-id="e8469-214">指定要指派給工作的標記。</span><span class="sxs-lookup"><span data-stu-id="e8469-214">Specifies the tags that will be assigned to the job.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IPutJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8469-215">-確認</span><span class="sxs-lookup"><span data-stu-id="e8469-215">-Confirm</span></span>
<span data-ttu-id="e8469-216">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e8469-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8469-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8469-217">-WhatIf</span></span>
<span data-ttu-id="e8469-218">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8469-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8469-219">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8469-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8469-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8469-220">CommonParameters</span></span>
<span data-ttu-id="e8469-221">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e8469-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8469-222">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8469-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8469-223">輸入</span><span class="sxs-lookup"><span data-stu-id="e8469-223">INPUTS</span></span>

## <span data-ttu-id="e8469-224">輸出</span><span class="sxs-lookup"><span data-stu-id="e8469-224">OUTPUTS</span></span>

### <span data-ttu-id="e8469-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="e8469-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="e8469-226">筆記</span><span class="sxs-lookup"><span data-stu-id="e8469-226">NOTES</span></span>

<span data-ttu-id="e8469-227">別名</span><span class="sxs-lookup"><span data-stu-id="e8469-227">ALIASES</span></span>

<span data-ttu-id="e8469-228">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e8469-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e8469-229">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e8469-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e8469-230">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e8469-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e8469-231">DRIVELIST <IDriveStatus[]>：最多十個組成工作的磁片磁碟機清單。</span><span class="sxs-lookup"><span data-stu-id="e8469-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="e8469-232">硬碟清單是一項匯出工作所需的元素;未指定匯出工作。</span><span class="sxs-lookup"><span data-stu-id="e8469-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="e8469-233">`[BitLockerKey <String>]`：用來加密硬碟的 BitLocker 金鑰。</span><span class="sxs-lookup"><span data-stu-id="e8469-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="e8469-234">`[BytesSucceeded <Int64?>]`：已成功傳輸硬碟的位元組。</span><span class="sxs-lookup"><span data-stu-id="e8469-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="e8469-235">`[CopyStatus <String>]`：資料傳輸程式的詳細狀態。</span><span class="sxs-lookup"><span data-stu-id="e8469-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="e8469-236">在磁碟機位於傳輸狀態之前，此欄位不會在回應中返回。</span><span class="sxs-lookup"><span data-stu-id="e8469-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="e8469-237">`[DriveHeaderHash <String>]`：磁碟機頭雜湊值。</span><span class="sxs-lookup"><span data-stu-id="e8469-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="e8469-238">`[DriveId <String>]`：不含空格的硬碟硬體序號。</span><span class="sxs-lookup"><span data-stu-id="e8469-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="e8469-239">`[ErrorLogUri <String>]`：指向包含資料傳輸作業錯誤記錄之 Blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="e8469-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="e8469-240">`[ManifestFile <String>]`：磁碟機上之清單檔案的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="e8469-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="e8469-241">`[ManifestHash <String>]`：雲端硬碟上清單檔案的 Base16 編碼 MD5 雜湊。</span><span class="sxs-lookup"><span data-stu-id="e8469-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="e8469-242">`[ManifestUri <String>]`：指向包含磁碟機清單檔案之 Blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="e8469-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="e8469-243">`[PercentComplete <Int32?>]`：完成磁碟機的百分比。</span><span class="sxs-lookup"><span data-stu-id="e8469-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="e8469-244">`[State <DriveState?>]`：磁碟機的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="e8469-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="e8469-245">`[VerboseLogUri <String>]`：指向包含資料傳輸作業詳細記錄之 Blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="e8469-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="e8469-246">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8469-246">RELATED LINKS</span></span>

