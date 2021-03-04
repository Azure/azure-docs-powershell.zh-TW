---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 34caab92645f610ed6ed71d907639060cf0c456a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903326"
---
# <span data-ttu-id="57d92-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="57d92-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="57d92-102">簡介</span><span class="sxs-lookup"><span data-stu-id="57d92-102">SYNOPSIS</span></span>
<span data-ttu-id="57d92-103">建立可配置的磁片物件。</span><span class="sxs-lookup"><span data-stu-id="57d92-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="57d92-104">語法</span><span class="sxs-lookup"><span data-stu-id="57d92-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [-Tier <String>] [-LogicalSectorSize <Int32>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Location] <String>]
 [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>]
 [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-Tag <Hashtable>]
 [-CreateOption <String>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-BurstingEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57d92-105">描述</span><span class="sxs-lookup"><span data-stu-id="57d92-105">DESCRIPTION</span></span>
<span data-ttu-id="57d92-106">**New-AzConfig Cmdlet** 會建立可配置的磁片物件。</span><span class="sxs-lookup"><span data-stu-id="57d92-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="57d92-107">例子</span><span class="sxs-lookup"><span data-stu-id="57d92-107">EXAMPLES</span></span>

### <span data-ttu-id="57d92-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="57d92-108">Example 1</span></span>
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

<span data-ttu-id="57d92-109">第一個命令會建立大小為 5 GB 的儲存Standard_LRS物件。</span><span class="sxs-lookup"><span data-stu-id="57d92-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="57d92-110">它也設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="57d92-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="57d92-111">第二個和第三個命令會設定磁片物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="57d92-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="57d92-112">最後一個命令會取用磁片物件，在資源群組 'ResourceGroup01' 中建立名稱為 'Disk01' 的磁片。</span><span class="sxs-lookup"><span data-stu-id="57d92-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="57d92-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="57d92-113">Example 2</span></span>
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

<span data-ttu-id="57d92-114">第一個命令會為上傳建立一個本地磁片物件。</span><span class="sxs-lookup"><span data-stu-id="57d92-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="57d92-115">第二個命令會取用磁片物件，在資源群組 'ResourceGroup01' 中建立名稱為 'Disk01' 的磁片。</span><span class="sxs-lookup"><span data-stu-id="57d92-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="57d92-116">第三個命令會獲得磁片的 SAS URL。</span><span class="sxs-lookup"><span data-stu-id="57d92-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="57d92-117">第四個命令會獲得磁片狀態。</span><span class="sxs-lookup"><span data-stu-id="57d92-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="57d92-118">如果磁片狀態為 'ReadyToUpload'，使用者可以使用 AzCopy 將磁片從 Blob 儲存空間上傳到磁片 SAS URL。</span><span class="sxs-lookup"><span data-stu-id="57d92-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="57d92-119">上傳期間，磁片狀態會變更為 'ActiveUpload'。</span><span class="sxs-lookup"><span data-stu-id="57d92-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="57d92-120">最後一個命令會撤銷 SAS URL 的磁片存取權。</span><span class="sxs-lookup"><span data-stu-id="57d92-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="57d92-121">範例 3</span><span class="sxs-lookup"><span data-stu-id="57d92-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="57d92-122">從共用圖庫圖像版本建立磁片。</span><span class="sxs-lookup"><span data-stu-id="57d92-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="57d92-123">識別碼是共用圖庫影像版本的識別碼。</span><span class="sxs-lookup"><span data-stu-id="57d92-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="57d92-124">只有當來源是資料磁片時，才需要使用這些資料。</span><span class="sxs-lookup"><span data-stu-id="57d92-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="57d92-125">參數</span><span class="sxs-lookup"><span data-stu-id="57d92-125">PARAMETERS</span></span>

### <span data-ttu-id="57d92-126">-連破Enabled</span><span class="sxs-lookup"><span data-stu-id="57d92-126">-BurstingEnabled</span></span>
<span data-ttu-id="57d92-127">啟用超出磁片所提供之績效目標的突然攻擊。</span><span class="sxs-lookup"><span data-stu-id="57d92-127">Enables bursting beyond the provisioned performance target of the disk.</span></span> <span data-ttu-id="57d92-128">根據預設，會停用連發功能。</span><span class="sxs-lookup"><span data-stu-id="57d92-128">Bursting is disabled by default.</span></span> <span data-ttu-id="57d92-129">不適用於 Ultra 磁片。</span><span class="sxs-lookup"><span data-stu-id="57d92-129">Does not apply to Ultra disks.</span></span>

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

### <span data-ttu-id="57d92-130">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="57d92-130">-CreateOption</span></span>
<span data-ttu-id="57d92-131">指定此 Cmdlet 是否要從平臺或使用者映射在虛擬機器中建立磁片、建立空白磁片，或附加到現有的磁片。</span><span class="sxs-lookup"><span data-stu-id="57d92-131">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="57d92-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57d92-132">-DefaultProfile</span></span>
<span data-ttu-id="57d92-133">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="57d92-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57d92-134">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="57d92-134">-DiskAccessId</span></span>
<span data-ttu-id="57d92-135">為使用私人端點而獲取或設定 DiskAccess 資源的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="57d92-135">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="57d92-136">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="57d92-136">-DiskEncryptionKey</span></span>
<span data-ttu-id="57d92-137">指定磁片上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="57d92-137">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="57d92-138">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="57d92-138">-DiskEncryptionSetId</span></span>
<span data-ttu-id="57d92-139">指定磁片加密集的資源識別碼，以用於啟用靜態加密。</span><span class="sxs-lookup"><span data-stu-id="57d92-139">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="57d92-140">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="57d92-140">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="57d92-141">所有將共用磁片裝載為 ReadOnly 的虛擬機器所允許的 IOPS 總數。</span><span class="sxs-lookup"><span data-stu-id="57d92-141">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="57d92-142">一個作業可在 4k 到 256k 位元組之間傳輸。</span><span class="sxs-lookup"><span data-stu-id="57d92-142">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="57d92-143">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="57d92-143">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="57d92-144">此磁片允許的 IOPS 數目;僅針對 UltraSSD 磁片設定。</span><span class="sxs-lookup"><span data-stu-id="57d92-144">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="57d92-145">一個作業可在 4k 到 256k 位元組之間傳輸。</span><span class="sxs-lookup"><span data-stu-id="57d92-145">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="57d92-146">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="57d92-146">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="57d92-147">「描述」：「MBps (總輸送量) 所有以 ReadOnly 方式安裝共用磁片的虛擬機器所允許的輸送量。</span><span class="sxs-lookup"><span data-stu-id="57d92-147">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="57d92-148">MBps 表示每秒 100 萬位元組 - MB 使用 10 次之 ISO 標記法。</span><span class="sxs-lookup"><span data-stu-id="57d92-148">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="57d92-149">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="57d92-149">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="57d92-150">此磁片允許的頻寬;僅針對 UltraSSD 磁片設定。</span><span class="sxs-lookup"><span data-stu-id="57d92-150">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="57d92-151">MBps 表示每秒 100 萬位元組 - MB 使用 10 次之 ISO 標記法。</span><span class="sxs-lookup"><span data-stu-id="57d92-151">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="57d92-152">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="57d92-152">-DiskSizeGB</span></span>
<span data-ttu-id="57d92-153">指定磁片大小 ，以 GB 為單位。</span><span class="sxs-lookup"><span data-stu-id="57d92-153">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="57d92-154">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="57d92-154">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="57d92-155">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="57d92-155">Enable encryption settings.</span></span>

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

### <span data-ttu-id="57d92-156">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="57d92-156">-EncryptionType</span></span>
<span data-ttu-id="57d92-157">用來加密磁片資料的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="57d92-157">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="57d92-158">可用的值為：'EncryptionAtLatWithPlatformKey'，'EncryptionAtWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="57d92-158">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="57d92-159">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="57d92-159">-GalleryImageReference</span></span>
<span data-ttu-id="57d92-160">GalleryImageReference 物件。</span><span class="sxs-lookup"><span data-stu-id="57d92-160">The GalleryImageReference object.</span></span>  <span data-ttu-id="57d92-161">從圖庫圖像建立時為必填專案。</span><span class="sxs-lookup"><span data-stu-id="57d92-161">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="57d92-162">識別碼即為共用 Galley 影像版本的 ARM 識別碼，可建立磁片。</span><span class="sxs-lookup"><span data-stu-id="57d92-162">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="57d92-163">如果複本的來源是圖庫影像中的其中一個資料磁片，則需要一個分片;如果 Null，將會複製影像的作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="57d92-163">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="57d92-164">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="57d92-164">-HyperVGeneration</span></span>
<span data-ttu-id="57d92-165">虛擬機器的超虛擬機器代。</span><span class="sxs-lookup"><span data-stu-id="57d92-165">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="57d92-166">僅適用于作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="57d92-166">Applicable to OS disks only.</span></span>  <span data-ttu-id="57d92-167">允許的值為 V1 和 V2。</span><span class="sxs-lookup"><span data-stu-id="57d92-167">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="57d92-168">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="57d92-168">-ImageReference</span></span>
<span data-ttu-id="57d92-169">指定磁片上的圖像參照。</span><span class="sxs-lookup"><span data-stu-id="57d92-169">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="57d92-170">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="57d92-170">-KeyEncryptionKey</span></span>
<span data-ttu-id="57d92-171">指定磁片上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="57d92-171">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="57d92-172">-位置</span><span class="sxs-lookup"><span data-stu-id="57d92-172">-Location</span></span>
<span data-ttu-id="57d92-173">指定位置。</span><span class="sxs-lookup"><span data-stu-id="57d92-173">Specifies a location.</span></span>

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

### <span data-ttu-id="57d92-174">-LogicalSectorSize</span><span class="sxs-lookup"><span data-stu-id="57d92-174">-LogicalSectorSize</span></span>
<span data-ttu-id="57d92-175">以位元組為單位的邏輯磁片區大小以位元組表示。</span><span class="sxs-lookup"><span data-stu-id="57d92-175">Logical sector size in bytes for Ultra disks.</span></span> 

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

### <span data-ttu-id="57d92-176">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="57d92-176">-MaxSharesCount</span></span>
<span data-ttu-id="57d92-177">可同時附加至磁片的虛擬機器數目上限。</span><span class="sxs-lookup"><span data-stu-id="57d92-177">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="57d92-178">大於 1 的值表示可以同時安裝在多個虛擬機器上的磁片。</span><span class="sxs-lookup"><span data-stu-id="57d92-178">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="57d92-179">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="57d92-179">-NetworkAccessPolicy</span></span>
<span data-ttu-id="57d92-180">網路存取策略會定義網路存取策略。</span><span class="sxs-lookup"><span data-stu-id="57d92-180">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="57d92-181">可能的值包括：'AllowAll'，'AllowPrivate'， 'DenyAll'</span><span class="sxs-lookup"><span data-stu-id="57d92-181">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="57d92-182">-OsType</span><span class="sxs-lookup"><span data-stu-id="57d92-182">-OsType</span></span>
<span data-ttu-id="57d92-183">指定作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="57d92-183">Specifies the OS type.</span></span>

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

### <span data-ttu-id="57d92-184">-SKUName</span><span class="sxs-lookup"><span data-stu-id="57d92-184">-SkuName</span></span>
<span data-ttu-id="57d92-185">指定儲存空間帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="57d92-185">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="57d92-186">可用的值有Standard_LRS、Premium_LRS、StandardSSD_LRS和UltraSSD_LRS。</span><span class="sxs-lookup"><span data-stu-id="57d92-186">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="57d92-187">UltraSSD_LRS只能與 CreateOption 參數的 Empty 值一起使用。</span><span class="sxs-lookup"><span data-stu-id="57d92-187">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="57d92-188">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="57d92-188">-SourceResourceId</span></span>
<span data-ttu-id="57d92-189">指定來源資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="57d92-189">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="57d92-190">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="57d92-190">-SourceUri</span></span>
<span data-ttu-id="57d92-191">指定來源 Uri。</span><span class="sxs-lookup"><span data-stu-id="57d92-191">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="57d92-192">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="57d92-192">-StorageAccountId</span></span>
<span data-ttu-id="57d92-193">指定儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="57d92-193">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="57d92-194">-標記</span><span class="sxs-lookup"><span data-stu-id="57d92-194">-Tag</span></span>
<span data-ttu-id="57d92-195">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="57d92-195">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="57d92-196">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="57d92-196">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="57d92-197">-Tier</span><span class="sxs-lookup"><span data-stu-id="57d92-197">-Tier</span></span>
<span data-ttu-id="57d92-198">磁片的績效層級。</span><span class="sxs-lookup"><span data-stu-id="57d92-198">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="57d92-199">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="57d92-199">-UploadSizeInBytes</span></span>
<span data-ttu-id="57d92-200">指定在 CreateOption 為上傳時上傳的內容大小，包括 VHD 頁腳。</span><span class="sxs-lookup"><span data-stu-id="57d92-200">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="57d92-201">此值應該是 VHD 頁腳) 的 20972032 (20 MiB + 512 位元組，以及 VHD 頁腳) 的 35183298347520 位元組 (32 TiB + 512 位元組。</span><span class="sxs-lookup"><span data-stu-id="57d92-201">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="57d92-202">-區域</span><span class="sxs-lookup"><span data-stu-id="57d92-202">-Zone</span></span>
<span data-ttu-id="57d92-203">指定磁片的邏輯區域清單。</span><span class="sxs-lookup"><span data-stu-id="57d92-203">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="57d92-204">-確認</span><span class="sxs-lookup"><span data-stu-id="57d92-204">-Confirm</span></span>
<span data-ttu-id="57d92-205">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="57d92-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57d92-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57d92-206">-WhatIf</span></span>
<span data-ttu-id="57d92-207">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57d92-207">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57d92-208">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57d92-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57d92-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d92-209">CommonParameters</span></span>
<span data-ttu-id="57d92-210">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="57d92-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57d92-211">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57d92-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d92-212">輸入</span><span class="sxs-lookup"><span data-stu-id="57d92-212">INPUTS</span></span>

### <span data-ttu-id="57d92-213">System.String</span><span class="sxs-lookup"><span data-stu-id="57d92-213">System.String</span></span>

### <span data-ttu-id="57d92-214">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="57d92-214">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="57d92-215">System.Int32</span><span class="sxs-lookup"><span data-stu-id="57d92-215">System.Int32</span></span>

### <span data-ttu-id="57d92-216">System.String[]</span><span class="sxs-lookup"><span data-stu-id="57d92-216">System.String[]</span></span>

### <span data-ttu-id="57d92-217">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="57d92-217">System.Collections.Hashtable</span></span>

### <span data-ttu-id="57d92-218">Microsoft.Azure.management.Compute.models.ImageAzReference</span><span class="sxs-lookup"><span data-stu-id="57d92-218">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="57d92-219">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="57d92-219">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="57d92-220">Microsoft.Azure.management.Compute.models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="57d92-220">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="57d92-221">Microsoft.Azure.management.Compute.models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="57d92-221">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="57d92-222">輸出</span><span class="sxs-lookup"><span data-stu-id="57d92-222">OUTPUTS</span></span>

### <span data-ttu-id="57d92-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="57d92-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="57d92-224">筆記</span><span class="sxs-lookup"><span data-stu-id="57d92-224">NOTES</span></span>

## <span data-ttu-id="57d92-225">相關連結</span><span class="sxs-lookup"><span data-stu-id="57d92-225">RELATED LINKS</span></span>
