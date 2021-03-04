---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: 7b604c22878d3d76e66a6d615deb1b46cedaad32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907654"
---
# <span data-ttu-id="cbc4e-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="cbc4e-101">Update-AzImportExport</span></span>

## <span data-ttu-id="cbc4e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cbc4e-102">SYNOPSIS</span></span>
<span data-ttu-id="cbc4e-103">更新工作的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="cbc4e-104">您可以撥打此作業來通知匯進/匯出服務，指出包含匯進或匯出工作的硬碟已運送至 Microsoft 資料中心。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="cbc4e-105">它也可以用來取消現有的工作。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="cbc4e-106">語法</span><span class="sxs-lookup"><span data-stu-id="cbc4e-106">SYNTAX</span></span>

### <span data-ttu-id="cbc4e-107">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="cbc4e-107">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="cbc4e-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cbc4e-108">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="cbc4e-109">描述</span><span class="sxs-lookup"><span data-stu-id="cbc4e-109">DESCRIPTION</span></span>
<span data-ttu-id="cbc4e-110">更新工作的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="cbc4e-111">您可以撥打此作業來通知匯進/匯出服務，指出包含匯進或匯出工作的硬碟已運送至 Microsoft 資料中心。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="cbc4e-112">它也可以用來取消現有的工作。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="cbc4e-113">例子</span><span class="sxs-lookup"><span data-stu-id="cbc4e-113">EXAMPLES</span></span>

### <span data-ttu-id="cbc4e-114">範例 1：根據資源群組和伺服器名稱更新 ImportExport 工作</span><span class="sxs-lookup"><span data-stu-id="cbc4e-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="cbc4e-115">此 Cmdlet 會根據資源群組和伺服器名稱更新 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="cbc4e-116">範例 2：根據身分識別更新 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="cbc4e-117">此 Cmdlet 會以身分識別更新 ImportExport 工作。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="cbc4e-118">參數</span><span class="sxs-lookup"><span data-stu-id="cbc4e-118">PARAMETERS</span></span>

### <span data-ttu-id="cbc4e-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="cbc4e-119">-AcceptLanguage</span></span>
<span data-ttu-id="cbc4e-120">指定回應的偏好語言。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-120">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="cbc4e-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="cbc4e-121">-BackupDriveManifest</span></span>
<span data-ttu-id="cbc4e-122">指出是否應該複製磁片磁碟機上的清單檔案以封鎖 Blob。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="cbc4e-123">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="cbc4e-123">-CancelRequested</span></span>
<span data-ttu-id="cbc4e-124">如果指定，值必須為 True。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-124">If specified, the value must be true.</span></span>
<span data-ttu-id="cbc4e-125">服務會嘗試取消該工作。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-125">The service will attempt to cancel the job.</span></span>

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

### <span data-ttu-id="cbc4e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbc4e-126">-DefaultProfile</span></span>
<span data-ttu-id="cbc4e-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbc4e-128">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="cbc4e-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="cbc4e-129">用來出貨匯進或匯出磁片磁碟機的電信業者名稱。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-129">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="cbc4e-130">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="cbc4e-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="cbc4e-131">套件中包含的磁片磁碟機數量。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-131">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="cbc4e-132">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="cbc4e-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="cbc4e-133">包裹出貨日期。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-133">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="cbc4e-134">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="cbc4e-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="cbc4e-135">包裹的追蹤編號。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-135">The tracking number of the package.</span></span>

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

### <span data-ttu-id="cbc4e-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="cbc4e-136">-DriveList</span></span>
<span data-ttu-id="cbc4e-137">組成工作的磁片磁碟機清單。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="cbc4e-138">若要建構，請參閱 DRIVELIST 屬性的附注區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="cbc4e-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbc4e-139">-InputObject</span></span>
<span data-ttu-id="cbc4e-140">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cbc4e-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="cbc4e-141">-LogLevel</span></span>
<span data-ttu-id="cbc4e-142">指出是否已啟用錯誤記錄或詳細記錄。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-142">Indicates whether error logging or verbose logging is enabled.</span></span>

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

### <span data-ttu-id="cbc4e-143">-名稱</span><span class="sxs-lookup"><span data-stu-id="cbc4e-143">-Name</span></span>
<span data-ttu-id="cbc4e-144">匯進/匯出工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-144">The name of the import/export job.</span></span>

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

### <span data-ttu-id="cbc4e-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbc4e-145">-ResourceGroupName</span></span>
<span data-ttu-id="cbc4e-146">資源組名可唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="cbc4e-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="cbc4e-147">-ReturnAddressCity</span></span>
<span data-ttu-id="cbc4e-148">要用於退回磁片磁碟機的城市名稱。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-148">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="cbc4e-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="cbc4e-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="cbc4e-150">退回磁片磁碟機時要使用的國家/地區或地區。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-150">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="cbc4e-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="cbc4e-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="cbc4e-152">所退回磁片磁碟機收件者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-152">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="cbc4e-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="cbc4e-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="cbc4e-154">所退回磁片磁碟機收件者的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-154">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="cbc4e-155">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="cbc4e-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="cbc4e-156">退回磁片磁碟機時使用的郵遞區號。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-156">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="cbc4e-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="cbc4e-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="cbc4e-158">收到硬碟的收件者名稱。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="cbc4e-159">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="cbc4e-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="cbc4e-160">退回磁片磁碟機時所使用之省/市。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-160">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="cbc4e-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="cbc4e-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="cbc4e-162">退回磁片磁碟機時，所使用街地道號的第一行。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-162">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="cbc4e-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="cbc4e-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="cbc4e-164">退回磁片磁碟機時，所使用之街地道道的第二行。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-164">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="cbc4e-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="cbc4e-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="cbc4e-166">客戶與電信公司的帳戶號碼。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-166">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="cbc4e-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="cbc4e-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="cbc4e-168">電信公司的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-168">The carrier's name.</span></span>

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

### <span data-ttu-id="cbc4e-169">-State</span><span class="sxs-lookup"><span data-stu-id="cbc4e-169">-State</span></span>
<span data-ttu-id="cbc4e-170">如果指定，值必須是出貨，這告訴匯進/匯出服務該工作的套件已出貨。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="cbc4e-171">必須在此要求或之前的要求中設定 ReturnAddress 和 DeliveryPackage 屬性，否則要求將會失敗。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

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

### <span data-ttu-id="cbc4e-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cbc4e-172">-SubscriptionId</span></span>
<span data-ttu-id="cbc4e-173">Azure 使用者的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-173">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="cbc4e-174">-標記</span><span class="sxs-lookup"><span data-stu-id="cbc4e-174">-Tag</span></span>
<span data-ttu-id="cbc4e-175">指定要指派給工作的標記</span><span class="sxs-lookup"><span data-stu-id="cbc4e-175">Specifies the tags that will be assigned to the job</span></span>

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

### <span data-ttu-id="cbc4e-176">-確認</span><span class="sxs-lookup"><span data-stu-id="cbc4e-176">-Confirm</span></span>
<span data-ttu-id="cbc4e-177">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbc4e-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbc4e-178">-WhatIf</span></span>
<span data-ttu-id="cbc4e-179">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbc4e-180">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbc4e-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbc4e-181">CommonParameters</span></span>
<span data-ttu-id="cbc4e-182">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbc4e-183">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbc4e-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbc4e-184">輸入</span><span class="sxs-lookup"><span data-stu-id="cbc4e-184">INPUTS</span></span>

### <span data-ttu-id="cbc4e-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="cbc4e-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="cbc4e-186">輸出</span><span class="sxs-lookup"><span data-stu-id="cbc4e-186">OUTPUTS</span></span>

### <span data-ttu-id="cbc4e-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="cbc4e-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="cbc4e-188">筆記</span><span class="sxs-lookup"><span data-stu-id="cbc4e-188">NOTES</span></span>

<span data-ttu-id="cbc4e-189">別名</span><span class="sxs-lookup"><span data-stu-id="cbc4e-189">ALIASES</span></span>

<span data-ttu-id="cbc4e-190">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="cbc4e-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cbc4e-191">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cbc4e-192">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cbc4e-193">DRIVELIST <IDriveStatus[]>：組成工作的磁片磁碟機清單。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="cbc4e-194">`[BitLockerKey <String>]`：用來加密硬碟的 BitLocker 金鑰。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="cbc4e-195">`[BytesSucceeded <Int64?>]`：已成功傳輸硬碟的位元組。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="cbc4e-196">`[CopyStatus <String>]`：資料傳輸程式的詳細狀態。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="cbc4e-197">在磁碟機位於傳輸狀態之前，此欄位不會在回應中返回。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="cbc4e-198">`[DriveHeaderHash <String>]`：磁碟機頭雜湊值。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="cbc4e-199">`[DriveId <String>]`：不含空格的硬碟硬體序號。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="cbc4e-200">`[ErrorLogUri <String>]`：指向包含資料傳輸作業錯誤記錄之 Blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="cbc4e-201">`[ManifestFile <String>]`：磁碟機上之清單檔案的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="cbc4e-202">`[ManifestHash <String>]`：雲端硬碟上清單檔案的 Base16 編碼 MD5 雜湊。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="cbc4e-203">`[ManifestUri <String>]`：指向包含磁碟機清單檔案之 Blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="cbc4e-204">`[PercentComplete <Int32?>]`：完成磁碟機的百分比。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="cbc4e-205">`[State <DriveState?>]`：磁碟機的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="cbc4e-206">`[VerboseLogUri <String>]`：指向包含資料傳輸作業詳細記錄之 Blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="cbc4e-207">INPUTOBJECT： <IImportExportIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="cbc4e-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cbc4e-208">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="cbc4e-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cbc4e-209">`[JobName <String>]`：匯進/匯出工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="cbc4e-210">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="cbc4e-211">例如，美國西部或西部。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="cbc4e-212">`[ResourceGroupName <String>]`：資源組名可唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="cbc4e-213">`[SubscriptionId <String>]`：Azure 使用者的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbc4e-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="cbc4e-214">相關連結</span><span class="sxs-lookup"><span data-stu-id="cbc4e-214">RELATED LINKS</span></span>

