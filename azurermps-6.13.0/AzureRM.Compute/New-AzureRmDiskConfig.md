---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: 693d121bac5a618c5ad588cf4d34f63d8c6d0fd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624449"
---
# <span data-ttu-id="e5810-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="e5810-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="e5810-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5810-102">SYNOPSIS</span></span>
<span data-ttu-id="e5810-103">建立可設定的磁片物件。</span><span class="sxs-lookup"><span data-stu-id="e5810-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5810-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5810-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-DiskIOPSReadWrite <Int32>] [-DiskMBpsReadWrite <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5810-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5810-105">DESCRIPTION</span></span>
<span data-ttu-id="e5810-106">**新的-AzureRmDiskConfig** Cmdlet 會建立可設定的磁片物件。</span><span class="sxs-lookup"><span data-stu-id="e5810-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="e5810-107">示例</span><span class="sxs-lookup"><span data-stu-id="e5810-107">EXAMPLES</span></span>

### <span data-ttu-id="e5810-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e5810-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="e5810-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，建立一個大小為5GB 的本機空白磁片物件。</span><span class="sxs-lookup"><span data-stu-id="e5810-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="e5810-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="e5810-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="e5810-111">第二個和第三個命令會設定磁片物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="e5810-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="e5810-112">最後一個命令會取得磁片物件，並在 [資源] 群組的 [ResourceGroup01] 中建立名為 "Disk01" 的磁片。</span><span class="sxs-lookup"><span data-stu-id="e5810-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e5810-113">參數</span><span class="sxs-lookup"><span data-stu-id="e5810-113">PARAMETERS</span></span>

### <span data-ttu-id="e5810-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="e5810-114">-CreateOption</span></span>
<span data-ttu-id="e5810-115">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片、建立空白磁片，或附加現有磁片。</span><span class="sxs-lookup"><span data-stu-id="e5810-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="e5810-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5810-116">-DefaultProfile</span></span>
<span data-ttu-id="e5810-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5810-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5810-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e5810-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="e5810-119">指定磁片上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="e5810-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="e5810-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="e5810-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="e5810-121">此磁片允許的 IOPS 數;僅可設定 UltraSSD 磁片。</span><span class="sxs-lookup"><span data-stu-id="e5810-121">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="e5810-122">一項操作可在4k 與256k 位元組之間進行傳輸。</span><span class="sxs-lookup"><span data-stu-id="e5810-122">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="e5810-123">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="e5810-123">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="e5810-124">此磁片允許的頻寬;僅可設定 UltraSSD 磁片。</span><span class="sxs-lookup"><span data-stu-id="e5810-124">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="e5810-125">Mbits （MBps）代表每秒數百萬個位元組，就會使用 ISO 符號（10的冪）。</span><span class="sxs-lookup"><span data-stu-id="e5810-125">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="e5810-126">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="e5810-126">-DiskSizeGB</span></span>
<span data-ttu-id="e5810-127">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="e5810-127">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="e5810-128">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="e5810-128">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="e5810-129">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="e5810-129">Enable encryption settings.</span></span>

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

### <span data-ttu-id="e5810-130">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="e5810-130">-ImageReference</span></span>
<span data-ttu-id="e5810-131">指定磁片上的影像參照。</span><span class="sxs-lookup"><span data-stu-id="e5810-131">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="e5810-132">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e5810-132">-KeyEncryptionKey</span></span>
<span data-ttu-id="e5810-133">指定磁片上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="e5810-133">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="e5810-134">-位置</span><span class="sxs-lookup"><span data-stu-id="e5810-134">-Location</span></span>
<span data-ttu-id="e5810-135">指定位置。</span><span class="sxs-lookup"><span data-stu-id="e5810-135">Specifies a location.</span></span>

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

### <span data-ttu-id="e5810-136">-OsType</span><span class="sxs-lookup"><span data-stu-id="e5810-136">-OsType</span></span>
<span data-ttu-id="e5810-137">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="e5810-137">Specifies the OS type.</span></span>

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

### <span data-ttu-id="e5810-138">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e5810-138">-SkuName</span></span>
<span data-ttu-id="e5810-139">指定儲存空間帳戶的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="e5810-139">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="e5810-140">可用的值為 Standard_LRS、Premium_LRS、StandardSSD_LRS 和 UltraSSD_LRS。</span><span class="sxs-lookup"><span data-stu-id="e5810-140">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="e5810-141">UltraSSD_LRS 只能與 CreateOption 參數的空值搭配使用。</span><span class="sxs-lookup"><span data-stu-id="e5810-141">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="e5810-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="e5810-142">-SourceResourceId</span></span>
<span data-ttu-id="e5810-143">指定來源資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5810-143">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="e5810-144">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="e5810-144">-SourceUri</span></span>
<span data-ttu-id="e5810-145">指定來源 Uri。</span><span class="sxs-lookup"><span data-stu-id="e5810-145">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="e5810-146">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e5810-146">-StorageAccountId</span></span>
<span data-ttu-id="e5810-147">指定儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="e5810-147">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="e5810-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="e5810-148">-Tag</span></span>
<span data-ttu-id="e5810-149">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="e5810-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e5810-150">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e5810-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e5810-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="e5810-151">-Zone</span></span>
<span data-ttu-id="e5810-152">指定磁片的邏輯區域清單。</span><span class="sxs-lookup"><span data-stu-id="e5810-152">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="e5810-153">-確認</span><span class="sxs-lookup"><span data-stu-id="e5810-153">-Confirm</span></span>
<span data-ttu-id="e5810-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5810-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5810-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5810-155">-WhatIf</span></span>
<span data-ttu-id="e5810-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5810-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5810-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5810-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5810-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5810-158">CommonParameters</span></span>
<span data-ttu-id="e5810-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5810-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5810-160">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5810-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5810-161">輸入</span><span class="sxs-lookup"><span data-stu-id="e5810-161">INPUTS</span></span>

### <span data-ttu-id="e5810-162">System.object</span><span class="sxs-lookup"><span data-stu-id="e5810-162">System.String</span></span>

### <span data-ttu-id="e5810-163">"OperatingSystemTypes" 1 [[21.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="e5810-163">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e5810-164">System.object</span><span class="sxs-lookup"><span data-stu-id="e5810-164">System.Int32</span></span>

### <span data-ttu-id="e5810-165">System.object []</span><span class="sxs-lookup"><span data-stu-id="e5810-165">System.String[]</span></span>

### <span data-ttu-id="e5810-166">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e5810-166">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e5810-167">ImageDiskReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="e5810-167">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="e5810-168">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e5810-168">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e5810-169">KeyVaultAndSecretReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="e5810-169">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="e5810-170">KeyVaultAndKeyReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="e5810-170">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="e5810-171">輸出</span><span class="sxs-lookup"><span data-stu-id="e5810-171">OUTPUTS</span></span>

### <span data-ttu-id="e5810-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="e5810-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="e5810-173">筆記</span><span class="sxs-lookup"><span data-stu-id="e5810-173">NOTES</span></span>

## <span data-ttu-id="e5810-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5810-174">RELATED LINKS</span></span>
