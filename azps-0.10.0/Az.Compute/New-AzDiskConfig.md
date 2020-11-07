---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 851687bdc00b25bd283433fbc00254380a8ef3a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796157"
---
# <span data-ttu-id="66e84-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="66e84-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="66e84-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66e84-102">SYNOPSIS</span></span>
<span data-ttu-id="66e84-103">建立可設定的磁片物件。</span><span class="sxs-lookup"><span data-stu-id="66e84-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="66e84-104">句法</span><span class="sxs-lookup"><span data-stu-id="66e84-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>] [-Tag <Hashtable>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66e84-105">說明</span><span class="sxs-lookup"><span data-stu-id="66e84-105">DESCRIPTION</span></span>
<span data-ttu-id="66e84-106">**新的-AzDiskConfig** Cmdlet 會建立可設定的磁片物件。</span><span class="sxs-lookup"><span data-stu-id="66e84-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="66e84-107">示例</span><span class="sxs-lookup"><span data-stu-id="66e84-107">EXAMPLES</span></span>

### <span data-ttu-id="66e84-108">範例1</span><span class="sxs-lookup"><span data-stu-id="66e84-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="66e84-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，建立一個大小為5GB 的本機空白磁片物件。</span><span class="sxs-lookup"><span data-stu-id="66e84-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="66e84-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="66e84-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="66e84-111">第二個和第三個命令會設定磁片物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="66e84-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="66e84-112">最後一個命令會取得磁片物件，並在 [資源] 群組的 [ResourceGroup01] 中建立名為 "Disk01" 的磁片。</span><span class="sxs-lookup"><span data-stu-id="66e84-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="66e84-113">參數</span><span class="sxs-lookup"><span data-stu-id="66e84-113">PARAMETERS</span></span>

### <span data-ttu-id="66e84-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="66e84-114">-CreateOption</span></span>
<span data-ttu-id="66e84-115">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片、建立空白磁片，或附加現有磁片。</span><span class="sxs-lookup"><span data-stu-id="66e84-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e84-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66e84-116">-DefaultProfile</span></span>
<span data-ttu-id="66e84-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66e84-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e84-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="66e84-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="66e84-119">指定磁片上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="66e84-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="66e84-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="66e84-120">-DiskSizeGB</span></span>
<span data-ttu-id="66e84-121">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="66e84-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="66e84-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="66e84-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="66e84-123">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="66e84-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="66e84-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="66e84-124">-ImageReference</span></span>
<span data-ttu-id="66e84-125">指定磁片上的影像參照。</span><span class="sxs-lookup"><span data-stu-id="66e84-125">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="66e84-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="66e84-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="66e84-127">指定磁片上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="66e84-127">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="66e84-128">-位置</span><span class="sxs-lookup"><span data-stu-id="66e84-128">-Location</span></span>
<span data-ttu-id="66e84-129">指定位置。</span><span class="sxs-lookup"><span data-stu-id="66e84-129">Specifies a location.</span></span>

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

### <span data-ttu-id="66e84-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="66e84-130">-OsType</span></span>
<span data-ttu-id="66e84-131">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="66e84-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="66e84-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="66e84-132">-SkuName</span></span>
<span data-ttu-id="66e84-133">指定儲存空間帳戶的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="66e84-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e84-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="66e84-134">-SourceResourceId</span></span>
<span data-ttu-id="66e84-135">指定來源資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="66e84-135">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="66e84-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="66e84-136">-SourceUri</span></span>
<span data-ttu-id="66e84-137">指定來源 Uri。</span><span class="sxs-lookup"><span data-stu-id="66e84-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="66e84-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="66e84-138">-StorageAccountId</span></span>
<span data-ttu-id="66e84-139">指定儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="66e84-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="66e84-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="66e84-140">-Tag</span></span>
<span data-ttu-id="66e84-141">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="66e84-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="66e84-142">例如：</span><span class="sxs-lookup"><span data-stu-id="66e84-142">For example:</span></span>

<span data-ttu-id="66e84-143">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="66e84-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="66e84-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="66e84-144">-Zone</span></span>
<span data-ttu-id="66e84-145">指定磁片的邏輯區域清單。</span><span class="sxs-lookup"><span data-stu-id="66e84-145">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e84-146">-確認</span><span class="sxs-lookup"><span data-stu-id="66e84-146">-Confirm</span></span>
<span data-ttu-id="66e84-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="66e84-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66e84-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66e84-148">-WhatIf</span></span>
<span data-ttu-id="66e84-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66e84-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66e84-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66e84-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66e84-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66e84-151">CommonParameters</span></span>
<span data-ttu-id="66e84-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66e84-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66e84-153">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66e84-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66e84-154">輸入</span><span class="sxs-lookup"><span data-stu-id="66e84-154">INPUTS</span></span>

### <span data-ttu-id="66e84-155">所有</span><span class="sxs-lookup"><span data-stu-id="66e84-155">None</span></span>
<span data-ttu-id="66e84-156">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="66e84-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="66e84-157">輸出</span><span class="sxs-lookup"><span data-stu-id="66e84-157">OUTPUTS</span></span>

### <span data-ttu-id="66e84-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="66e84-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="66e84-159">筆記</span><span class="sxs-lookup"><span data-stu-id="66e84-159">NOTES</span></span>

## <span data-ttu-id="66e84-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="66e84-160">RELATED LINKS</span></span>

