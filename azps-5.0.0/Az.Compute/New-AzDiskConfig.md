---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: ec4d0444ad88fa7536fbf1ee050dc8dcb6a76af3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137694"
---
# <span data-ttu-id="8ab74-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="8ab74-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="8ab74-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ab74-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab74-103">建立可設定的磁片物件。</span><span class="sxs-lookup"><span data-stu-id="8ab74-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="8ab74-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ab74-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [-Tier <String>] [-LogicalSectorSize <Int32>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>]
 [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>]
 [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-Tag <Hashtable>]
 [-CreateOption <String>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ab74-105">說明</span><span class="sxs-lookup"><span data-stu-id="8ab74-105">DESCRIPTION</span></span>
<span data-ttu-id="8ab74-106">**新的-AzDiskConfig** Cmdlet 會建立可設定的磁片物件。</span><span class="sxs-lookup"><span data-stu-id="8ab74-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="8ab74-107">示例</span><span class="sxs-lookup"><span data-stu-id="8ab74-107">EXAMPLES</span></span>

### <span data-ttu-id="8ab74-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8ab74-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="8ab74-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，建立一個大小為5GB 的本機空白磁片物件。</span><span class="sxs-lookup"><span data-stu-id="8ab74-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="8ab74-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="8ab74-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="8ab74-111">第二個和第三個命令會設定磁片物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="8ab74-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="8ab74-112">最後一個命令會取得磁片物件，並在 [資源] 群組的 [ResourceGroup01] 中建立名為 "Disk01" 的磁片。</span><span class="sxs-lookup"><span data-stu-id="8ab74-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="8ab74-113">範例2</span><span class="sxs-lookup"><span data-stu-id="8ab74-113">Example 2</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
PS C:\> $diskSas = Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DurationInSecond 86400 -Access 'Write'
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ReadyToUpload'
PS C:\> AzCopy /Source:https://myaccount.blob.core.windows.net/mycontainer1 /Dest:$diskSas
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ActiveUpload'
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="8ab74-114">第一個命令會建立要上傳的本機磁片物件。</span><span class="sxs-lookup"><span data-stu-id="8ab74-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="8ab74-115">第二個命令會取得磁片物件，並在資源群組 ' ResourceGroup01 ' 中建立名為「Disk01」的磁片。</span><span class="sxs-lookup"><span data-stu-id="8ab74-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="8ab74-116">第三個命令會取得磁片的 SAS Url。</span><span class="sxs-lookup"><span data-stu-id="8ab74-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="8ab74-117">第四個命令會取得磁片的狀態。</span><span class="sxs-lookup"><span data-stu-id="8ab74-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="8ab74-118">如果磁片狀態是 [ReadyToUpload]，使用者可以使用 AzCopy 將磁片從 blob 儲存體上傳到磁片 SAS Url。</span><span class="sxs-lookup"><span data-stu-id="8ab74-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="8ab74-119">在上傳期間，磁片狀態會變更為 [ActiveUpload]。</span><span class="sxs-lookup"><span data-stu-id="8ab74-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="8ab74-120">最後一個命令會吊銷 SAS Url 的磁片存取權。</span><span class="sxs-lookup"><span data-stu-id="8ab74-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="8ab74-121">範例3</span><span class="sxs-lookup"><span data-stu-id="8ab74-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="8ab74-122">從共用圖庫影像版本建立磁片。</span><span class="sxs-lookup"><span data-stu-id="8ab74-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="8ab74-123">[識別碼] 是共用圖庫影像版本的 id。</span><span class="sxs-lookup"><span data-stu-id="8ab74-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="8ab74-124">只有當來源是資料磁片時，才需要 Lun。</span><span class="sxs-lookup"><span data-stu-id="8ab74-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="8ab74-125">參數</span><span class="sxs-lookup"><span data-stu-id="8ab74-125">PARAMETERS</span></span>

### <span data-ttu-id="8ab74-126">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="8ab74-126">-CreateOption</span></span>
<span data-ttu-id="8ab74-127">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片、建立空白磁片，或附加現有磁片。</span><span class="sxs-lookup"><span data-stu-id="8ab74-127">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab74-128">-DefaultProfile</span></span>
<span data-ttu-id="8ab74-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ab74-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-130">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="8ab74-130">-DiskAccessId</span></span>
<span data-ttu-id="8ab74-131">取得或設定在上使用 private 端點的 DiskAccess 資源的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="8ab74-131">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-132">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8ab74-132">-DiskEncryptionKey</span></span>
<span data-ttu-id="8ab74-133">指定磁片上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="8ab74-133">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-134">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="8ab74-134">-DiskEncryptionSetId</span></span>
<span data-ttu-id="8ab74-135">指定磁片加密集的資源識別碼，以用於在 rest 上啟用加密。</span><span class="sxs-lookup"><span data-stu-id="8ab74-135">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-136">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="8ab74-136">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="8ab74-137">將共用磁片以唯讀方式裝載到所有 Vm 的總 IOPS 數。</span><span class="sxs-lookup"><span data-stu-id="8ab74-137">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="8ab74-138">一項操作可在4k 與256k 位元組之間進行傳輸。</span><span class="sxs-lookup"><span data-stu-id="8ab74-138">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-139">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="8ab74-139">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="8ab74-140">此磁片允許的 IOPS 數;僅可設定 UltraSSD 磁片。</span><span class="sxs-lookup"><span data-stu-id="8ab74-140">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="8ab74-141">一項操作可在4k 與256k 位元組之間進行傳輸。</span><span class="sxs-lookup"><span data-stu-id="8ab74-141">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-142">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="8ab74-142">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="8ab74-143">"描述"： "在將共用磁片設為 ReadOnly 的所有 Vm 中，允許的總輸送量 (MBps) 。</span><span class="sxs-lookup"><span data-stu-id="8ab74-143">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="8ab74-144">Mbits （MBps）代表每秒數百萬個位元組，就會使用 ISO 符號（10的冪）。</span><span class="sxs-lookup"><span data-stu-id="8ab74-144">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-145">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="8ab74-145">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="8ab74-146">此磁片允許的頻寬;僅可設定 UltraSSD 磁片。</span><span class="sxs-lookup"><span data-stu-id="8ab74-146">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="8ab74-147">Mbits （MBps）代表每秒數百萬個位元組，就會使用 ISO 符號（10的冪）。</span><span class="sxs-lookup"><span data-stu-id="8ab74-147">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-148">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="8ab74-148">-DiskSizeGB</span></span>
<span data-ttu-id="8ab74-149">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="8ab74-149">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-150">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="8ab74-150">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="8ab74-151">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="8ab74-151">Enable encryption settings.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-152">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="8ab74-152">-EncryptionType</span></span>
<span data-ttu-id="8ab74-153">用來加密磁片資料的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="8ab74-153">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="8ab74-154">可用的值為： "EncryptionAtRestWithPlatformKey"、"EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="8ab74-154">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-155">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="8ab74-155">-GalleryImageReference</span></span>
<span data-ttu-id="8ab74-156">GalleryImageReference 物件。</span><span class="sxs-lookup"><span data-stu-id="8ab74-156">The GalleryImageReference object.</span></span>  <span data-ttu-id="8ab74-157">如果是從圖庫影像建立，則為必要。</span><span class="sxs-lookup"><span data-stu-id="8ab74-157">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="8ab74-158">識別碼將是建立磁片所用的共用條樣影像版本的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ab74-158">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="8ab74-159">如果複本來源是圖庫影像中的其中一個資料磁片，則需要 lun;如果是 null，則會複製影像的 OS 磁片。</span><span class="sxs-lookup"><span data-stu-id="8ab74-159">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-160">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="8ab74-160">-HyperVGeneration</span></span>
<span data-ttu-id="8ab74-161">虛擬機器的虛擬機器監控程式產生。</span><span class="sxs-lookup"><span data-stu-id="8ab74-161">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="8ab74-162">僅適用于作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="8ab74-162">Applicable to OS disks only.</span></span>  <span data-ttu-id="8ab74-163">允許的值為 V1 和 V2。</span><span class="sxs-lookup"><span data-stu-id="8ab74-163">Allowed values are V1 and V2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-164">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="8ab74-164">-ImageReference</span></span>
<span data-ttu-id="8ab74-165">指定磁片上的影像參照。</span><span class="sxs-lookup"><span data-stu-id="8ab74-165">Specifies the image reference on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-166">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8ab74-166">-KeyEncryptionKey</span></span>
<span data-ttu-id="8ab74-167">指定磁片上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="8ab74-167">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-168">-位置</span><span class="sxs-lookup"><span data-stu-id="8ab74-168">-Location</span></span>
<span data-ttu-id="8ab74-169">指定位置。</span><span class="sxs-lookup"><span data-stu-id="8ab74-169">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-170">-LogicalSectorSize</span><span class="sxs-lookup"><span data-stu-id="8ab74-170">-LogicalSectorSize</span></span>
<span data-ttu-id="8ab74-171">超磁片的邏輯磁區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8ab74-171">Logical sector size in bytes for Ultra disks.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-172">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="8ab74-172">-MaxSharesCount</span></span>
<span data-ttu-id="8ab74-173">可以在同一時間附加至磁片的 Vm 數目上限。</span><span class="sxs-lookup"><span data-stu-id="8ab74-173">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="8ab74-174">大於1的值表示可以同時在多個 Vm 上裝載的磁片。</span><span class="sxs-lookup"><span data-stu-id="8ab74-174">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-175">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8ab74-175">-NetworkAccessPolicy</span></span>
<span data-ttu-id="8ab74-176">網路存取原則定義網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="8ab74-176">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="8ab74-177">可能的值包括： "AllowAll"、"AllowPrivate"、"DenyAll"</span><span class="sxs-lookup"><span data-stu-id="8ab74-177">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-178">-OsType</span><span class="sxs-lookup"><span data-stu-id="8ab74-178">-OsType</span></span>
<span data-ttu-id="8ab74-179">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="8ab74-179">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-180">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8ab74-180">-SkuName</span></span>
<span data-ttu-id="8ab74-181">指定儲存空間帳戶的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="8ab74-181">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="8ab74-182">可用的值為 Standard_LRS、Premium_LRS、StandardSSD_LRS 和 UltraSSD_LRS。</span><span class="sxs-lookup"><span data-stu-id="8ab74-182">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="8ab74-183">UltraSSD_LRS 只能與 CreateOption 參數的空值搭配使用。</span><span class="sxs-lookup"><span data-stu-id="8ab74-183">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-184">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="8ab74-184">-SourceResourceId</span></span>
<span data-ttu-id="8ab74-185">指定來源資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ab74-185">Specifies the  source resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-186">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="8ab74-186">-SourceUri</span></span>
<span data-ttu-id="8ab74-187">指定來源 Uri。</span><span class="sxs-lookup"><span data-stu-id="8ab74-187">Specifies the source Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-188">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8ab74-188">-StorageAccountId</span></span>
<span data-ttu-id="8ab74-189">指定儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="8ab74-189">Specifies the storage account ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-190">-Tag</span><span class="sxs-lookup"><span data-stu-id="8ab74-190">-Tag</span></span>
<span data-ttu-id="8ab74-191">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="8ab74-191">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8ab74-192">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8ab74-192">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-193">層級</span><span class="sxs-lookup"><span data-stu-id="8ab74-193">-Tier</span></span>
<span data-ttu-id="8ab74-194">磁片效能層。</span><span class="sxs-lookup"><span data-stu-id="8ab74-194">Performance tier of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-195">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="8ab74-195">-UploadSizeInBytes</span></span>
<span data-ttu-id="8ab74-196">指定 CreateOption 上傳時，包括 VHD 頁尾在內的上傳內容大小。</span><span class="sxs-lookup"><span data-stu-id="8ab74-196">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="8ab74-197">此值應該在 20972032 (20 MiB + 512 位元組（適用于 vhd 頁尾) 與35183298347520位元組 (32 TiB + 512 位元組）) 。</span><span class="sxs-lookup"><span data-stu-id="8ab74-197">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-198">-Zone</span><span class="sxs-lookup"><span data-stu-id="8ab74-198">-Zone</span></span>
<span data-ttu-id="8ab74-199">指定磁片的邏輯區域清單。</span><span class="sxs-lookup"><span data-stu-id="8ab74-199">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab74-200">-確認</span><span class="sxs-lookup"><span data-stu-id="8ab74-200">-Confirm</span></span>
<span data-ttu-id="8ab74-201">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8ab74-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ab74-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ab74-202">-WhatIf</span></span>
<span data-ttu-id="8ab74-203">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8ab74-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ab74-204">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ab74-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ab74-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab74-205">CommonParameters</span></span>
<span data-ttu-id="8ab74-206">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ab74-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab74-207">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8ab74-207">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab74-208">輸入</span><span class="sxs-lookup"><span data-stu-id="8ab74-208">INPUTS</span></span>

### <span data-ttu-id="8ab74-209">System.object</span><span class="sxs-lookup"><span data-stu-id="8ab74-209">System.String</span></span>

### <span data-ttu-id="8ab74-210">"OperatingSystemTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="8ab74-210">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="8ab74-211">System.object</span><span class="sxs-lookup"><span data-stu-id="8ab74-211">System.Int32</span></span>

### <span data-ttu-id="8ab74-212">System.object []</span><span class="sxs-lookup"><span data-stu-id="8ab74-212">System.String[]</span></span>

### <span data-ttu-id="8ab74-213">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8ab74-213">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8ab74-214">ImageDiskReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="8ab74-214">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="8ab74-215">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8ab74-215">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8ab74-216">KeyVaultAndSecretReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="8ab74-216">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="8ab74-217">KeyVaultAndKeyReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="8ab74-217">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="8ab74-218">輸出</span><span class="sxs-lookup"><span data-stu-id="8ab74-218">OUTPUTS</span></span>

### <span data-ttu-id="8ab74-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="8ab74-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="8ab74-220">筆記</span><span class="sxs-lookup"><span data-stu-id="8ab74-220">NOTES</span></span>

## <span data-ttu-id="8ab74-221">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ab74-221">RELATED LINKS</span></span>