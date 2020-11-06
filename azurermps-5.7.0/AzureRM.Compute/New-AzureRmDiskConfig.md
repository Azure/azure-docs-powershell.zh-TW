---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: b2c922a1dcce683636d61b68c66ab8cfb82535c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448755"
---
# <span data-ttu-id="46c2d-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="46c2d-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="46c2d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="46c2d-103">建立可設定的磁片物件。</span><span class="sxs-lookup"><span data-stu-id="46c2d-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46c2d-104">句法</span><span class="sxs-lookup"><span data-stu-id="46c2d-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46c2d-105">說明</span><span class="sxs-lookup"><span data-stu-id="46c2d-105">DESCRIPTION</span></span>
<span data-ttu-id="46c2d-106">**新的-AzureRmDiskConfig** Cmdlet 會建立可設定的磁片物件。</span><span class="sxs-lookup"><span data-stu-id="46c2d-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="46c2d-107">示例</span><span class="sxs-lookup"><span data-stu-id="46c2d-107">EXAMPLES</span></span>

### <span data-ttu-id="46c2d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="46c2d-108">Example 1</span></span>
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

<span data-ttu-id="46c2d-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，建立一個大小為5GB 的本機空白磁片物件。</span><span class="sxs-lookup"><span data-stu-id="46c2d-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="46c2d-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="46c2d-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="46c2d-111">第二個和第三個命令會設定磁片物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="46c2d-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="46c2d-112">最後一個命令會取得磁片物件，並在 [資源] 群組的 [ResourceGroup01] 中建立名為 "Disk01" 的磁片。</span><span class="sxs-lookup"><span data-stu-id="46c2d-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="46c2d-113">參數</span><span class="sxs-lookup"><span data-stu-id="46c2d-113">PARAMETERS</span></span>

### <span data-ttu-id="46c2d-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="46c2d-114">-CreateOption</span></span>
<span data-ttu-id="46c2d-115">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片、建立空白磁片，或附加現有磁片。</span><span class="sxs-lookup"><span data-stu-id="46c2d-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy, Restore

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c2d-116">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="46c2d-116">-DiskEncryptionKey</span></span>
<span data-ttu-id="46c2d-117">指定磁片上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="46c2d-117">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c2d-118">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="46c2d-118">-DiskSizeGB</span></span>
<span data-ttu-id="46c2d-119">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="46c2d-119">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c2d-120">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="46c2d-120">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="46c2d-121">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="46c2d-121">Enable encryption settings.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c2d-122">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="46c2d-122">-ImageReference</span></span>
<span data-ttu-id="46c2d-123">指定磁片上的影像參照。</span><span class="sxs-lookup"><span data-stu-id="46c2d-123">Specifies the image reference on a disk.</span></span>

```yaml
Type: ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c2d-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="46c2d-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="46c2d-125">指定磁片上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="46c2d-125">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c2d-126">-位置</span><span class="sxs-lookup"><span data-stu-id="46c2d-126">-Location</span></span>
<span data-ttu-id="46c2d-127">指定位置。</span><span class="sxs-lookup"><span data-stu-id="46c2d-127">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c2d-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="46c2d-128">-OsType</span></span>
<span data-ttu-id="46c2d-129">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="46c2d-129">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c2d-130">-SkuName</span><span class="sxs-lookup"><span data-stu-id="46c2d-130">-SkuName</span></span>
<span data-ttu-id="46c2d-131">指定儲存空間帳戶的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="46c2d-131">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c2d-132">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="46c2d-132">-SourceResourceId</span></span>
<span data-ttu-id="46c2d-133">指定來源資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="46c2d-133">Specifies the  source resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c2d-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="46c2d-134">-SourceUri</span></span>
<span data-ttu-id="46c2d-135">指定來源 Uri。</span><span class="sxs-lookup"><span data-stu-id="46c2d-135">Specifies the source Uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c2d-136">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="46c2d-136">-StorageAccountId</span></span>
<span data-ttu-id="46c2d-137">指定儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="46c2d-137">Specifies the storage account ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c2d-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="46c2d-138">-Tag</span></span>
<span data-ttu-id="46c2d-139">指定可以使用一組名稱值對來標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="46c2d-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c2d-140">-確認</span><span class="sxs-lookup"><span data-stu-id="46c2d-140">-Confirm</span></span>
<span data-ttu-id="46c2d-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="46c2d-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46c2d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46c2d-142">-WhatIf</span></span>
<span data-ttu-id="46c2d-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46c2d-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46c2d-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46c2d-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46c2d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c2d-145">CommonParameters</span></span>
<span data-ttu-id="46c2d-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46c2d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c2d-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="46c2d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c2d-148">輸入</span><span class="sxs-lookup"><span data-stu-id="46c2d-148">INPUTS</span></span>

### <span data-ttu-id="46c2d-149">"StorageAccountTypes" 1 [[14.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="46c2d-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="46c2d-150">可為 Null 的 `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[system. Int32、mscorlib、版本 = 4.0.0.0、Culture = 中立、publickeytoken = b77a5c561934e089 "] system. 字串 system. 集合. 雜湊表系統為 Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[system.object，Mscorlib，版本 = 4.0.0.0，區域性 = 中性，publickeytoken = b77a5c561934e089]]，Culture =</span><span class="sxs-lookup"><span data-stu-id="46c2d-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="46c2d-151">輸出</span><span class="sxs-lookup"><span data-stu-id="46c2d-151">OUTPUTS</span></span>

### <span data-ttu-id="46c2d-152">[Azure. 管理]. 磁片</span><span class="sxs-lookup"><span data-stu-id="46c2d-152">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="46c2d-153">筆記</span><span class="sxs-lookup"><span data-stu-id="46c2d-153">NOTES</span></span>

## <span data-ttu-id="46c2d-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="46c2d-154">RELATED LINKS</span></span>

