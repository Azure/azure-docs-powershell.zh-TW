---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: d6ed55cef91dc93f0ce9101adf94d9dc6931d07c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140819"
---
# <span data-ttu-id="5fdc3-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="5fdc3-101">Update-AzImportExport</span></span>

## <span data-ttu-id="5fdc3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5fdc3-102">SYNOPSIS</span></span>
<span data-ttu-id="5fdc3-103">更新作業的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="5fdc3-104">您可以呼叫此操作，通知匯入/匯出服務，包含匯入或匯出作業的硬驅已傳送至 Microsoft 資料中心。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="5fdc3-105">您也可以用來取消現有作業。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="5fdc3-106">句法</span><span class="sxs-lookup"><span data-stu-id="5fdc3-106">SYNTAX</span></span>

### <span data-ttu-id="5fdc3-107">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="5fdc3-107">UpdateExpanded (Default)</span></span>
```
Update-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-BackupDriveManifest] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>] [-LogLevel <String>]
 [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>]
 [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnShippingCarrierAccountNumber <String>]
 [-ReturnShippingCarrierName <String>] [-State <String>] [-Tag <IUpdateJobParametersTags>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5fdc3-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5fdc3-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>] [-BackupDriveManifest]
 [-CancelRequested] [-DeliveryPackageCarrierName <String>] [-DeliveryPackageDriveCount <Int32>]
 [-DeliveryPackageShipDate <String>] [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>]
 [-LogLevel <String>] [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>]
 [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>]
 [-ReturnAddressRecipientName <String>] [-ReturnAddressStateOrProvince <String>]
 [-ReturnAddressStreetAddress1 <String>] [-ReturnAddressStreetAddress2 <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>] [-State <String>]
 [-Tag <IUpdateJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5fdc3-109">說明</span><span class="sxs-lookup"><span data-stu-id="5fdc3-109">DESCRIPTION</span></span>
<span data-ttu-id="5fdc3-110">更新作業的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="5fdc3-111">您可以呼叫此操作，通知匯入/匯出服務，包含匯入或匯出作業的硬驅已傳送至 Microsoft 資料中心。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="5fdc3-112">您也可以用來取消現有作業。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="5fdc3-113">示例</span><span class="sxs-lookup"><span data-stu-id="5fdc3-113">EXAMPLES</span></span>

### <span data-ttu-id="5fdc3-114">範例1：依資源群組和伺服器名稱更新 ImportExport 工作</span><span class="sxs-lookup"><span data-stu-id="5fdc3-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="5fdc3-115">這個 Cmdlet 會依資源群組和伺服器名稱來更新 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="5fdc3-116">範例2：依身分識別來更新 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="5fdc3-117">這個 Cmdlet 會依身分識別來更新 ImportExport 作業。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="5fdc3-118">參數</span><span class="sxs-lookup"><span data-stu-id="5fdc3-118">PARAMETERS</span></span>

### <span data-ttu-id="5fdc3-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="5fdc3-119">-AcceptLanguage</span></span>
<span data-ttu-id="5fdc3-120">指定回應的喜好語言。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-120">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="5fdc3-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="5fdc3-121">-BackupDriveManifest</span></span>
<span data-ttu-id="5fdc3-122">指出是否應該將磁片上的資訊清單檔案複製到封鎖 blob。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="5fdc3-123">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="5fdc3-123">-CancelRequested</span></span>
<span data-ttu-id="5fdc3-124">如果已指定，值必須為 true。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-124">If specified, the value must be true.</span></span>
<span data-ttu-id="5fdc3-125">服務將會嘗試取消作業。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-125">The service will attempt to cancel the job.</span></span>

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

### <span data-ttu-id="5fdc3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fdc3-126">-DefaultProfile</span></span>
<span data-ttu-id="5fdc3-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fdc3-128">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="5fdc3-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="5fdc3-129">用來傳送匯入或匯出磁碟機的載波名稱。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-129">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="5fdc3-130">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="5fdc3-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="5fdc3-131">套件中包含的磁片磁碟機數。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-131">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="5fdc3-132">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="5fdc3-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="5fdc3-133">傳送套件的日期。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-133">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="5fdc3-134">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="5fdc3-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="5fdc3-135">套件的追蹤號碼。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-135">The tracking number of the package.</span></span>

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

### <span data-ttu-id="5fdc3-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="5fdc3-136">-DriveList</span></span>
<span data-ttu-id="5fdc3-137">組成作業的磁片磁碟機清單。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="5fdc3-138">若要建立，請參閱 DRIVELIST 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="5fdc3-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fdc3-139">-InputObject</span></span>
<span data-ttu-id="5fdc3-140">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fdc3-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="5fdc3-141">-LogLevel</span></span>
<span data-ttu-id="5fdc3-142">指出是否已啟用錯誤記錄或詳細記錄。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-142">Indicates whether error logging or verbose logging is enabled.</span></span>

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

### <span data-ttu-id="5fdc3-143">-名稱</span><span class="sxs-lookup"><span data-stu-id="5fdc3-143">-Name</span></span>
<span data-ttu-id="5fdc3-144">匯入/匯出作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-144">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fdc3-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fdc3-145">-ResourceGroupName</span></span>
<span data-ttu-id="5fdc3-146">資源群組名稱會唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fdc3-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="5fdc3-147">-ReturnAddressCity</span></span>
<span data-ttu-id="5fdc3-148">返回磁碟機時要使用的城市名稱。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-148">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="5fdc3-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="5fdc3-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="5fdc3-150">返回磁碟機時所要使用的國家或地區。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-150">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="5fdc3-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="5fdc3-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="5fdc3-152">傳回的磁碟機收件者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-152">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="5fdc3-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="5fdc3-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="5fdc3-154">傳回的磁碟機收件者的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-154">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="5fdc3-155">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="5fdc3-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="5fdc3-156">返回磁碟機時要使用的郵遞區號。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-156">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="5fdc3-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="5fdc3-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="5fdc3-158">要在傳回硬碟時接收硬碟的收件者名稱。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="5fdc3-159">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="5fdc3-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="5fdc3-160">返回磁片磁碟機時所要使用的省或直轄市。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-160">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="5fdc3-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="5fdc3-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="5fdc3-162">在傳回磁片磁碟機時要使用之街道位址的第一行。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-162">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="5fdc3-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="5fdc3-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="5fdc3-164">在傳回磁片磁碟機時要使用之街道位址的第二行。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-164">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="5fdc3-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="5fdc3-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="5fdc3-166">含承運人的客戶帳戶號碼。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-166">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="5fdc3-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="5fdc3-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="5fdc3-168">承運人名稱。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-168">The carrier's name.</span></span>

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

### <span data-ttu-id="5fdc3-169">-State</span><span class="sxs-lookup"><span data-stu-id="5fdc3-169">-State</span></span>
<span data-ttu-id="5fdc3-170">如果已指定，則必須傳送值，這會告訴您匯入/匯出服務已傳送作業的套件。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="5fdc3-171">ReturnAddress 和 DeliveryPackage 屬性必須是在此要求中或在前一個要求中設定，否則要求將會失敗。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

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

### <span data-ttu-id="5fdc3-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5fdc3-172">-SubscriptionId</span></span>
<span data-ttu-id="5fdc3-173">Azure 使用者的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-173">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fdc3-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="5fdc3-174">-Tag</span></span>
<span data-ttu-id="5fdc3-175">指定將指派給作業的標記</span><span class="sxs-lookup"><span data-stu-id="5fdc3-175">Specifies the tags that will be assigned to the job</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IUpdateJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fdc3-176">-確認</span><span class="sxs-lookup"><span data-stu-id="5fdc3-176">-Confirm</span></span>
<span data-ttu-id="5fdc3-177">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fdc3-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fdc3-178">-WhatIf</span></span>
<span data-ttu-id="5fdc3-179">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fdc3-180">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fdc3-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fdc3-181">CommonParameters</span></span>
<span data-ttu-id="5fdc3-182">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fdc3-183">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fdc3-184">輸入</span><span class="sxs-lookup"><span data-stu-id="5fdc3-184">INPUTS</span></span>

### <span data-ttu-id="5fdc3-185">IImportExportIdentity （ImportExport）的</span><span class="sxs-lookup"><span data-stu-id="5fdc3-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="5fdc3-186">輸出</span><span class="sxs-lookup"><span data-stu-id="5fdc3-186">OUTPUTS</span></span>

### <span data-ttu-id="5fdc3-187">IJobResponse （ImportExport）。 Api20161101。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="5fdc3-188">筆記</span><span class="sxs-lookup"><span data-stu-id="5fdc3-188">NOTES</span></span>

<span data-ttu-id="5fdc3-189">別名</span><span class="sxs-lookup"><span data-stu-id="5fdc3-189">ALIASES</span></span>

<span data-ttu-id="5fdc3-190">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5fdc3-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5fdc3-191">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5fdc3-192">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5fdc3-193">DRIVELIST <IDriveStatus [] >：組成作業的磁片磁碟機清單。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="5fdc3-194">`[BitLockerKey <String>]`：用來加密磁片磁碟機的 BitLocker 金鑰。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="5fdc3-195">`[BytesSucceeded <Int64?>]`：已成功地傳送磁片磁碟機的位元組數。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="5fdc3-196">`[CopyStatus <String>]`：資料傳輸處理常式的詳細狀態。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="5fdc3-197">除非磁碟機處於轉移狀態，否則不會在回應中傳回此欄位。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="5fdc3-198">`[DriveHeaderHash <String>]`：磁碟機標頭雜湊值。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="5fdc3-199">`[DriveId <String>]`：磁片磁碟機的硬體序列值（不含空格）。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="5fdc3-200">`[ErrorLogUri <String>]`：指向內含資料傳輸作業錯誤記錄的 blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="5fdc3-201">`[ManifestFile <String>]`：磁碟機上資訊清單檔案的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="5fdc3-202">`[ManifestHash <String>]`：磁碟機上的資訊清單檔案的 Base16 編碼 MD5 雜湊。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="5fdc3-203">`[ManifestUri <String>]`：指向包含磁碟機資訊清單檔案之 blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="5fdc3-204">`[PercentComplete <Int32?>]`：已完成磁片磁碟機的百分比。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="5fdc3-205">`[State <DriveState?>]`：磁片磁碟機的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="5fdc3-206">`[VerboseLogUri <String>]`：指向內含資料傳輸作業詳細資料記錄之 blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="5fdc3-207">INPUTOBJECT <IImportExportIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5fdc3-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5fdc3-208">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="5fdc3-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5fdc3-209">`[JobName <String>]`：匯入/匯出作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="5fdc3-210">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="5fdc3-211">例如，美國西部或 westus。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="5fdc3-212">`[ResourceGroupName <String>]`：資源群組名稱會唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="5fdc3-213">`[SubscriptionId <String>]`： Azure 使用者的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="5fdc3-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="5fdc3-214">相關連結</span><span class="sxs-lookup"><span data-stu-id="5fdc3-214">RELATED LINKS</span></span>

