---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: c37ed947441789951d8523f38e7950ad6d9d2066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613327"
---
# <span data-ttu-id="aae17-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="aae17-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="aae17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aae17-102">SYNOPSIS</span></span>
<span data-ttu-id="aae17-103">建立可設定的磁片物件。</span><span class="sxs-lookup"><span data-stu-id="aae17-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="aae17-104">句法</span><span class="sxs-lookup"><span data-stu-id="aae17-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aae17-105">說明</span><span class="sxs-lookup"><span data-stu-id="aae17-105">DESCRIPTION</span></span>
<span data-ttu-id="aae17-106">**新的-AzDiskConfig** Cmdlet 會建立可設定的磁片物件。</span><span class="sxs-lookup"><span data-stu-id="aae17-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="aae17-107">示例</span><span class="sxs-lookup"><span data-stu-id="aae17-107">EXAMPLES</span></span>

### <span data-ttu-id="aae17-108">範例1</span><span class="sxs-lookup"><span data-stu-id="aae17-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="aae17-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，建立一個大小為5GB 的本機空白磁片物件。</span><span class="sxs-lookup"><span data-stu-id="aae17-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="aae17-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="aae17-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="aae17-111">第二個和第三個命令會設定磁片物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="aae17-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="aae17-112">最後一個命令會取得磁片物件，並在 [資源] 群組的 [ResourceGroup01] 中建立名為 "Disk01" 的磁片。</span><span class="sxs-lookup"><span data-stu-id="aae17-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="aae17-113">範例2</span><span class="sxs-lookup"><span data-stu-id="aae17-113">Example 2</span></span>
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

<span data-ttu-id="aae17-114">第一個命令會建立要上傳的本機磁片物件。</span><span class="sxs-lookup"><span data-stu-id="aae17-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="aae17-115">第二個命令會取得磁片物件，並在資源群組 ' ResourceGroup01 ' 中建立名為「Disk01」的磁片。</span><span class="sxs-lookup"><span data-stu-id="aae17-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="aae17-116">第三個命令會取得磁片的 SAS Url。</span><span class="sxs-lookup"><span data-stu-id="aae17-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="aae17-117">第四個命令會取得磁片的狀態。</span><span class="sxs-lookup"><span data-stu-id="aae17-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="aae17-118">如果磁片狀態是 [ReadyToUpload]，使用者可以使用 AzCopy 將磁片從 blob 儲存體上傳到磁片 SAS Url。</span><span class="sxs-lookup"><span data-stu-id="aae17-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="aae17-119">在上傳期間，磁片狀態會變更為 [ActiveUpload]。</span><span class="sxs-lookup"><span data-stu-id="aae17-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="aae17-120">最後一個命令會吊銷 SAS Url 的磁片存取權。</span><span class="sxs-lookup"><span data-stu-id="aae17-120">The last command revokes the disk access for the SAS Url.</span></span>

## <span data-ttu-id="aae17-121">參數</span><span class="sxs-lookup"><span data-stu-id="aae17-121">PARAMETERS</span></span>

### <span data-ttu-id="aae17-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="aae17-122">-CreateOption</span></span>
<span data-ttu-id="aae17-123">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片、建立空白磁片，或附加現有磁片。</span><span class="sxs-lookup"><span data-stu-id="aae17-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="aae17-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae17-124">-DefaultProfile</span></span>
<span data-ttu-id="aae17-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aae17-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aae17-126">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="aae17-126">-DiskEncryptionKey</span></span>
<span data-ttu-id="aae17-127">指定磁片上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="aae17-127">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="aae17-128">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="aae17-128">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="aae17-129">此磁片允許的 IOPS 數;僅可設定 UltraSSD 磁片。</span><span class="sxs-lookup"><span data-stu-id="aae17-129">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="aae17-130">一項操作可在4k 與256k 位元組之間進行傳輸。</span><span class="sxs-lookup"><span data-stu-id="aae17-130">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="aae17-131">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="aae17-131">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="aae17-132">此磁片允許的頻寬;僅可設定 UltraSSD 磁片。</span><span class="sxs-lookup"><span data-stu-id="aae17-132">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="aae17-133">Mbits （MBps）代表每秒數百萬個位元組，就會使用 ISO 符號（10的冪）。</span><span class="sxs-lookup"><span data-stu-id="aae17-133">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="aae17-134">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="aae17-134">-DiskSizeGB</span></span>
<span data-ttu-id="aae17-135">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="aae17-135">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="aae17-136">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="aae17-136">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="aae17-137">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="aae17-137">Enable encryption settings.</span></span>

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

### <span data-ttu-id="aae17-138">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="aae17-138">-HyperVGeneration</span></span>
<span data-ttu-id="aae17-139">虛擬機器的虛擬機器監控程式產生。</span><span class="sxs-lookup"><span data-stu-id="aae17-139">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="aae17-140">僅適用于作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="aae17-140">Applicable to OS disks only.</span></span>  <span data-ttu-id="aae17-141">允許的值為 V1 和 V2。</span><span class="sxs-lookup"><span data-stu-id="aae17-141">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="aae17-142">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="aae17-142">-ImageReference</span></span>
<span data-ttu-id="aae17-143">指定磁片上的影像參照。</span><span class="sxs-lookup"><span data-stu-id="aae17-143">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="aae17-144">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="aae17-144">-KeyEncryptionKey</span></span>
<span data-ttu-id="aae17-145">指定磁片上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="aae17-145">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="aae17-146">-位置</span><span class="sxs-lookup"><span data-stu-id="aae17-146">-Location</span></span>
<span data-ttu-id="aae17-147">指定位置。</span><span class="sxs-lookup"><span data-stu-id="aae17-147">Specifies a location.</span></span>

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

### <span data-ttu-id="aae17-148">-OsType</span><span class="sxs-lookup"><span data-stu-id="aae17-148">-OsType</span></span>
<span data-ttu-id="aae17-149">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="aae17-149">Specifies the OS type.</span></span>

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

### <span data-ttu-id="aae17-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="aae17-150">-SkuName</span></span>
<span data-ttu-id="aae17-151">指定儲存空間帳戶的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="aae17-151">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="aae17-152">可用的值為 Standard_LRS、Premium_LRS、StandardSSD_LRS 和 UltraSSD_LRS。</span><span class="sxs-lookup"><span data-stu-id="aae17-152">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="aae17-153">UltraSSD_LRS 只能與 CreateOption 參數的空值搭配使用。</span><span class="sxs-lookup"><span data-stu-id="aae17-153">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="aae17-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="aae17-154">-SourceResourceId</span></span>
<span data-ttu-id="aae17-155">指定來源資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="aae17-155">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="aae17-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="aae17-156">-SourceUri</span></span>
<span data-ttu-id="aae17-157">指定來源 Uri。</span><span class="sxs-lookup"><span data-stu-id="aae17-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="aae17-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="aae17-158">-StorageAccountId</span></span>
<span data-ttu-id="aae17-159">指定儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="aae17-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="aae17-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="aae17-160">-Tag</span></span>
<span data-ttu-id="aae17-161">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="aae17-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="aae17-162">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="aae17-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="aae17-163">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="aae17-163">-UploadSizeInBytes</span></span>
<span data-ttu-id="aae17-164">指定 CreateOption 上傳時，包括 VHD 頁尾在內的上傳內容大小。</span><span class="sxs-lookup"><span data-stu-id="aae17-164">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="aae17-165">此值應該在 20972032 (20 MiB + 512 位元組（適用于 vhd 頁尾) 與35183298347520位元組 (32 TiB + 512 位元組）) 。</span><span class="sxs-lookup"><span data-stu-id="aae17-165">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="aae17-166">-Zone</span><span class="sxs-lookup"><span data-stu-id="aae17-166">-Zone</span></span>
<span data-ttu-id="aae17-167">指定磁片的邏輯區域清單。</span><span class="sxs-lookup"><span data-stu-id="aae17-167">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="aae17-168">-確認</span><span class="sxs-lookup"><span data-stu-id="aae17-168">-Confirm</span></span>
<span data-ttu-id="aae17-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aae17-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aae17-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aae17-170">-WhatIf</span></span>
<span data-ttu-id="aae17-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aae17-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aae17-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aae17-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aae17-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae17-173">CommonParameters</span></span>
<span data-ttu-id="aae17-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aae17-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae17-175">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="aae17-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae17-176">輸入</span><span class="sxs-lookup"><span data-stu-id="aae17-176">INPUTS</span></span>

### <span data-ttu-id="aae17-177">System.object</span><span class="sxs-lookup"><span data-stu-id="aae17-177">System.String</span></span>

### <span data-ttu-id="aae17-178">"OperatingSystemTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="aae17-178">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="aae17-179">System.object</span><span class="sxs-lookup"><span data-stu-id="aae17-179">System.Int32</span></span>

### <span data-ttu-id="aae17-180">System.object []</span><span class="sxs-lookup"><span data-stu-id="aae17-180">System.String[]</span></span>

### <span data-ttu-id="aae17-181">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="aae17-181">System.Collections.Hashtable</span></span>

### <span data-ttu-id="aae17-182">ImageDiskReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="aae17-182">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="aae17-183">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="aae17-183">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="aae17-184">KeyVaultAndSecretReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="aae17-184">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="aae17-185">KeyVaultAndKeyReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="aae17-185">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="aae17-186">輸出</span><span class="sxs-lookup"><span data-stu-id="aae17-186">OUTPUTS</span></span>

### <span data-ttu-id="aae17-187">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="aae17-187">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="aae17-188">筆記</span><span class="sxs-lookup"><span data-stu-id="aae17-188">NOTES</span></span>

## <span data-ttu-id="aae17-189">相關連結</span><span class="sxs-lookup"><span data-stu-id="aae17-189">RELATED LINKS</span></span>
