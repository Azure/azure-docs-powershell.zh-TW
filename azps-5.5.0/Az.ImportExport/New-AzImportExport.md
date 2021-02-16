---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: 9b0cf40b090111a6bd32bc87b6e72bc542eae5ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133175"
---
# <span data-ttu-id="d4a8e-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="d4a8e-101">New-AzImportExport</span></span>

## <span data-ttu-id="d4a8e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a8e-103">在指定的訂閱中建立新作業或更新現有作業。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="d4a8e-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4a8e-104">SYNTAX</span></span>

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

## <span data-ttu-id="d4a8e-105">說明</span><span class="sxs-lookup"><span data-stu-id="d4a8e-105">DESCRIPTION</span></span>
<span data-ttu-id="d4a8e-106">在指定的訂閱中建立新作業或更新現有作業。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="d4a8e-107">示例</span><span class="sxs-lookup"><span data-stu-id="d4a8e-107">EXAMPLES</span></span>

### <span data-ttu-id="d4a8e-108">範例1：建立新的 ImportExport 工作</span><span class="sxs-lookup"><span data-stu-id="d4a8e-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="d4a8e-109">這些 Cmdlet 會建立新的 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="d4a8e-110">參數</span><span class="sxs-lookup"><span data-stu-id="d4a8e-110">PARAMETERS</span></span>

### <span data-ttu-id="d4a8e-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="d4a8e-111">-AcceptLanguage</span></span>
<span data-ttu-id="d4a8e-112">指定回應的喜好語言。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="d4a8e-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="d4a8e-113">-BackupDriveManifest</span></span>
<span data-ttu-id="d4a8e-114">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-114">Default value is false.</span></span>
<span data-ttu-id="d4a8e-115">指出是否應該將磁片上的資訊清單檔案複製到封鎖 blob。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="d4a8e-116">-BlobListBlobPath</span><span class="sxs-lookup"><span data-stu-id="d4a8e-116">-BlobListBlobPath</span></span>
<span data-ttu-id="d4a8e-117">Blob 路徑字串的集合。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-117">A collection of blob-path strings.</span></span>

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

### <span data-ttu-id="d4a8e-118">-BlobListBlobPathPrefix</span><span class="sxs-lookup"><span data-stu-id="d4a8e-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="d4a8e-119">Blob 前置詞字串的集合。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-119">A collection of blob-prefix strings.</span></span>

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

### <span data-ttu-id="d4a8e-120">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="d4a8e-120">-CancelRequested</span></span>
<span data-ttu-id="d4a8e-121">指出是否已提交要求以取消作業。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-121">Indicates whether a request has been submitted to cancel the job.</span></span>

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

### <span data-ttu-id="d4a8e-122">-ClientTenantId</span><span class="sxs-lookup"><span data-stu-id="d4a8e-122">-ClientTenantId</span></span>
<span data-ttu-id="d4a8e-123">發出要求之用戶端的租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-123">The tenant ID of the client making the request.</span></span>

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

### <span data-ttu-id="d4a8e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a8e-124">-DefaultProfile</span></span>
<span data-ttu-id="d4a8e-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4a8e-126">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="d4a8e-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="d4a8e-127">用來傳送匯入或匯出磁碟機的載波名稱。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-127">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="d4a8e-128">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="d4a8e-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="d4a8e-129">套件中包含的磁片磁碟機數。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-129">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="d4a8e-130">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="d4a8e-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="d4a8e-131">傳送套件的日期。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-131">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="d4a8e-132">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="d4a8e-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="d4a8e-133">套件的追蹤號碼。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-133">The tracking number of the package.</span></span>

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

### <span data-ttu-id="d4a8e-134">-DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="d4a8e-134">-DiagnosticsPath</span></span>
<span data-ttu-id="d4a8e-135">在已啟用) 的情況下，將會儲存檔案記錄及磁片磁碟機資訊清單檔案 (的虛擬 blob 目錄。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

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

### <span data-ttu-id="d4a8e-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="d4a8e-136">-DriveList</span></span>
<span data-ttu-id="d4a8e-137">組成作業的最多十個磁片磁碟機清單。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="d4a8e-138">[磁碟機清單] 是匯入作業所需的元素;未指定匯出作業。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="d4a8e-139">若要建立，請參閱 DRIVELIST 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="d4a8e-140">-ExportBlobListblobPath</span><span class="sxs-lookup"><span data-stu-id="d4a8e-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="d4a8e-141">區塊 blob 的相對 URI，包含上述所定義的 blob 路徑或 blob 路徑首碼清單（從容器名稱開始）。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="d4a8e-142">如果 blob 位於根容器中，URI 必須以 $root 開頭。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-142">If the blob is in root container, the URI must begin with $root.</span></span>

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

### <span data-ttu-id="d4a8e-143">-IncompleteBlobListUri</span><span class="sxs-lookup"><span data-stu-id="d4a8e-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="d4a8e-144">指向區塊 blob 的 blob 路徑，其中包含由於磁碟空間不足而無法匯出的 blob 名稱清單。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="d4a8e-145">如果所有 blob 都已順利匯出，則回應中不會包含此元素。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

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

### <span data-ttu-id="d4a8e-146">-JobType</span><span class="sxs-lookup"><span data-stu-id="d4a8e-146">-JobType</span></span>
<span data-ttu-id="d4a8e-147">作業類型</span><span class="sxs-lookup"><span data-stu-id="d4a8e-147">The type of job</span></span>

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

### <span data-ttu-id="d4a8e-148">-位置</span><span class="sxs-lookup"><span data-stu-id="d4a8e-148">-Location</span></span>
<span data-ttu-id="d4a8e-149">指定應建立作業的受支援 Azure 位置</span><span class="sxs-lookup"><span data-stu-id="d4a8e-149">Specifies the supported Azure location where the job should be created</span></span>

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

### <span data-ttu-id="d4a8e-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="d4a8e-150">-LogLevel</span></span>
<span data-ttu-id="d4a8e-151">預設值為錯誤。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-151">Default value is Error.</span></span>
<span data-ttu-id="d4a8e-152">指出是否將啟用錯誤記錄或詳細記錄。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

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

### <span data-ttu-id="d4a8e-153">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4a8e-153">-Name</span></span>
<span data-ttu-id="d4a8e-154">匯入/匯出作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-154">The name of the import/export job.</span></span>

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

### <span data-ttu-id="d4a8e-155">-百分比</span><span class="sxs-lookup"><span data-stu-id="d4a8e-155">-PercentComplete</span></span>
<span data-ttu-id="d4a8e-156">作業的整體完成百分比。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-156">Overall percentage completed for the job.</span></span>

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

### <span data-ttu-id="d4a8e-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="d4a8e-157">-ProvisioningState</span></span>
<span data-ttu-id="d4a8e-158">指定作業的 [提供狀態]。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-158">Specifies the provisioning state of the job.</span></span>

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

### <span data-ttu-id="d4a8e-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4a8e-159">-ResourceGroupName</span></span>
<span data-ttu-id="d4a8e-160">資源群組名稱會唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="d4a8e-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="d4a8e-161">-ReturnAddressCity</span></span>
<span data-ttu-id="d4a8e-162">返回磁碟機時要使用的城市名稱。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-162">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="d4a8e-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="d4a8e-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="d4a8e-164">返回磁碟機時所要使用的國家或地區。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-164">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="d4a8e-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="d4a8e-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="d4a8e-166">傳回的磁碟機收件者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-166">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="d4a8e-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="d4a8e-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="d4a8e-168">傳回的磁碟機收件者的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-168">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="d4a8e-169">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="d4a8e-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="d4a8e-170">返回磁碟機時要使用的郵遞區號。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-170">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="d4a8e-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="d4a8e-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="d4a8e-172">要在傳回硬碟時接收硬碟的收件者名稱。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="d4a8e-173">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="d4a8e-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="d4a8e-174">返回磁片磁碟機時所要使用的省或直轄市。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-174">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="d4a8e-175">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="d4a8e-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="d4a8e-176">在傳回磁片磁碟機時要使用之街道位址的第一行。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-176">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="d4a8e-177">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="d4a8e-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="d4a8e-178">在傳回磁片磁碟機時要使用之街道位址的第二行。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-178">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="d4a8e-179">-ReturnPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="d4a8e-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="d4a8e-180">用來傳送匯入或匯出磁碟機的載波名稱。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-180">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="d4a8e-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="d4a8e-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="d4a8e-182">套件中包含的磁片磁碟機數。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-182">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="d4a8e-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="d4a8e-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="d4a8e-184">傳送套件的日期。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-184">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="d4a8e-185">-ReturnPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="d4a8e-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="d4a8e-186">套件的追蹤號碼。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-186">The tracking number of the package.</span></span>

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

### <span data-ttu-id="d4a8e-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="d4a8e-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="d4a8e-188">含承運人的客戶帳戶號碼。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-188">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="d4a8e-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="d4a8e-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="d4a8e-190">承運人名稱。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-190">The carrier's name.</span></span>

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

### <span data-ttu-id="d4a8e-191">-ShippingInformationCity</span><span class="sxs-lookup"><span data-stu-id="d4a8e-191">-ShippingInformationCity</span></span>
<span data-ttu-id="d4a8e-192">返回磁碟機時要使用的城市名稱。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-192">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="d4a8e-193">-ShippingInformationCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="d4a8e-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="d4a8e-194">返回磁碟機時所要使用的國家或地區。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-194">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="d4a8e-195">-ShippingInformationPhone</span><span class="sxs-lookup"><span data-stu-id="d4a8e-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="d4a8e-196">傳回的磁碟機收件者的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-196">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="d4a8e-197">-ShippingInformationPostalCode</span><span class="sxs-lookup"><span data-stu-id="d4a8e-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="d4a8e-198">返回磁碟機時要使用的郵遞區號。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-198">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="d4a8e-199">-ShippingInformationRecipientName</span><span class="sxs-lookup"><span data-stu-id="d4a8e-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="d4a8e-200">要在傳回硬碟時接收硬碟的收件者名稱。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="d4a8e-201">-ShippingInformationStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="d4a8e-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="d4a8e-202">返回磁片磁碟機時所要使用的省或直轄市。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-202">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="d4a8e-203">-ShippingInformationStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="d4a8e-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="d4a8e-204">在傳回磁片磁碟機時要使用之街道位址的第一行。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-204">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="d4a8e-205">-ShippingInformationStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="d4a8e-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="d4a8e-206">在傳回磁片磁碟機時要使用之街道位址的第二行。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-206">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="d4a8e-207">-State</span><span class="sxs-lookup"><span data-stu-id="d4a8e-207">-State</span></span>
<span data-ttu-id="d4a8e-208">工作的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-208">Current state of the job.</span></span>

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

### <span data-ttu-id="d4a8e-209">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d4a8e-209">-StorageAccountId</span></span>
<span data-ttu-id="d4a8e-210">要匯入或匯出資料之儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

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

### <span data-ttu-id="d4a8e-211">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4a8e-211">-SubscriptionId</span></span>
<span data-ttu-id="d4a8e-212">Azure 使用者的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-212">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="d4a8e-213">-Tag</span><span class="sxs-lookup"><span data-stu-id="d4a8e-213">-Tag</span></span>
<span data-ttu-id="d4a8e-214">指定將指派給作業的標記。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-214">Specifies the tags that will be assigned to the job.</span></span>

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

### <span data-ttu-id="d4a8e-215">-確認</span><span class="sxs-lookup"><span data-stu-id="d4a8e-215">-Confirm</span></span>
<span data-ttu-id="d4a8e-216">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4a8e-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4a8e-217">-WhatIf</span></span>
<span data-ttu-id="d4a8e-218">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4a8e-219">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4a8e-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a8e-220">CommonParameters</span></span>
<span data-ttu-id="d4a8e-221">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a8e-222">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a8e-223">輸入</span><span class="sxs-lookup"><span data-stu-id="d4a8e-223">INPUTS</span></span>

## <span data-ttu-id="d4a8e-224">輸出</span><span class="sxs-lookup"><span data-stu-id="d4a8e-224">OUTPUTS</span></span>

### <span data-ttu-id="d4a8e-225">IJobResponse （ImportExport）。 Api20161101。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="d4a8e-226">筆記</span><span class="sxs-lookup"><span data-stu-id="d4a8e-226">NOTES</span></span>

<span data-ttu-id="d4a8e-227">別名</span><span class="sxs-lookup"><span data-stu-id="d4a8e-227">ALIASES</span></span>

<span data-ttu-id="d4a8e-228">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="d4a8e-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d4a8e-229">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4a8e-230">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d4a8e-231">DRIVELIST <IDriveStatus [] >：組成作業的最多十個磁片磁碟機清單。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="d4a8e-232">[磁碟機清單] 是匯入作業所需的元素;未指定匯出作業。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="d4a8e-233">`[BitLockerKey <String>]`：用來加密磁片磁碟機的 BitLocker 金鑰。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="d4a8e-234">`[BytesSucceeded <Int64?>]`：已成功地傳送磁片磁碟機的位元組數。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="d4a8e-235">`[CopyStatus <String>]`：資料傳輸處理常式的詳細狀態。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="d4a8e-236">除非磁碟機處於轉移狀態，否則不會在回應中傳回此欄位。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="d4a8e-237">`[DriveHeaderHash <String>]`：磁碟機標頭雜湊值。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="d4a8e-238">`[DriveId <String>]`：磁片磁碟機的硬體序列值（不含空格）。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="d4a8e-239">`[ErrorLogUri <String>]`：指向內含資料傳輸作業錯誤記錄的 blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="d4a8e-240">`[ManifestFile <String>]`：磁碟機上資訊清單檔案的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="d4a8e-241">`[ManifestHash <String>]`：磁碟機上的資訊清單檔案的 Base16 編碼 MD5 雜湊。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="d4a8e-242">`[ManifestUri <String>]`：指向包含磁碟機資訊清單檔案之 blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="d4a8e-243">`[PercentComplete <Int32?>]`：已完成磁片磁碟機的百分比。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="d4a8e-244">`[State <DriveState?>]`：磁片磁碟機的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="d4a8e-245">`[VerboseLogUri <String>]`：指向內含資料傳輸作業詳細資料記錄之 blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="d4a8e-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="d4a8e-246">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4a8e-246">RELATED LINKS</span></span>

