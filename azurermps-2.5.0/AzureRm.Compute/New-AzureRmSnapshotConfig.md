---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotconfig
schema: 2.0.0
ms.openlocfilehash: a18eb8513e419d174efac9179cb65fe175d12dd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802109"
---
# <span data-ttu-id="e8deb-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e8deb-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="e8deb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8deb-102">SYNOPSIS</span></span>
<span data-ttu-id="e8deb-103">建立可設定的快照物件。</span><span class="sxs-lookup"><span data-stu-id="e8deb-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8deb-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8deb-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8deb-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8deb-105">DESCRIPTION</span></span>
<span data-ttu-id="e8deb-106">**新的-AzureRmSnapshotConfig** Cmdlet 會建立可設定的快照物件。</span><span class="sxs-lookup"><span data-stu-id="e8deb-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="e8deb-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8deb-107">EXAMPLES</span></span>

### <span data-ttu-id="e8deb-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e8deb-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="e8deb-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，使用大小為5GB 來建立本機空快照物件。</span><span class="sxs-lookup"><span data-stu-id="e8deb-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="e8deb-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="e8deb-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="e8deb-111">第二個和第三個命令會設定快照物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="e8deb-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="e8deb-112">最後一個命令會採用快照物件，並會在資源群組 "ResourceGroup01" 中建立名為 "Snapshot01" 的快照。</span><span class="sxs-lookup"><span data-stu-id="e8deb-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e8deb-113">參數</span><span class="sxs-lookup"><span data-stu-id="e8deb-113">PARAMETERS</span></span>

### <span data-ttu-id="e8deb-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="e8deb-114">-CreateOption</span></span>
<span data-ttu-id="e8deb-115">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片、建立空白磁片，或附加現有磁片。</span><span class="sxs-lookup"><span data-stu-id="e8deb-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="e8deb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8deb-116">-DefaultProfile</span></span>
<span data-ttu-id="e8deb-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8deb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8deb-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e8deb-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="e8deb-119">指定快照上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="e8deb-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="e8deb-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="e8deb-120">-DiskSizeGB</span></span>
<span data-ttu-id="e8deb-121">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="e8deb-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="e8deb-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="e8deb-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="e8deb-123">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="e8deb-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="e8deb-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="e8deb-124">-ImageReference</span></span>
<span data-ttu-id="e8deb-125">指定快照上的影像參照。</span><span class="sxs-lookup"><span data-stu-id="e8deb-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="e8deb-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e8deb-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="e8deb-127">指定快照上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="e8deb-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="e8deb-128">-位置</span><span class="sxs-lookup"><span data-stu-id="e8deb-128">-Location</span></span>
<span data-ttu-id="e8deb-129">指定位置。</span><span class="sxs-lookup"><span data-stu-id="e8deb-129">Specifies a location.</span></span>

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

### <span data-ttu-id="e8deb-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="e8deb-130">-OsType</span></span>
<span data-ttu-id="e8deb-131">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="e8deb-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="e8deb-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e8deb-132">-SkuName</span></span>
<span data-ttu-id="e8deb-133">指定儲存空間帳戶的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="e8deb-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="e8deb-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="e8deb-134">-SourceResourceId</span></span>
<span data-ttu-id="e8deb-135">指定來源資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8deb-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="e8deb-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="e8deb-136">-SourceUri</span></span>
<span data-ttu-id="e8deb-137">指定來源 Uri。</span><span class="sxs-lookup"><span data-stu-id="e8deb-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="e8deb-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e8deb-138">-StorageAccountId</span></span>
<span data-ttu-id="e8deb-139">指定儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="e8deb-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="e8deb-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8deb-140">-Tag</span></span>
<span data-ttu-id="e8deb-141">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="e8deb-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e8deb-142">例如：</span><span class="sxs-lookup"><span data-stu-id="e8deb-142">For example:</span></span>

<span data-ttu-id="e8deb-143">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e8deb-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e8deb-144">-確認</span><span class="sxs-lookup"><span data-stu-id="e8deb-144">-Confirm</span></span>
<span data-ttu-id="e8deb-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8deb-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8deb-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8deb-146">-WhatIf</span></span>
<span data-ttu-id="e8deb-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8deb-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8deb-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8deb-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8deb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8deb-149">CommonParameters</span></span>
<span data-ttu-id="e8deb-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8deb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8deb-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8deb-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8deb-152">輸入</span><span class="sxs-lookup"><span data-stu-id="e8deb-152">INPUTS</span></span>

### <span data-ttu-id="e8deb-153">所有</span><span class="sxs-lookup"><span data-stu-id="e8deb-153">None</span></span>
<span data-ttu-id="e8deb-154">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e8deb-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8deb-155">輸出</span><span class="sxs-lookup"><span data-stu-id="e8deb-155">OUTPUTS</span></span>

### <span data-ttu-id="e8deb-156">PSSnapshot 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="e8deb-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="e8deb-157">筆記</span><span class="sxs-lookup"><span data-stu-id="e8deb-157">NOTES</span></span>

## <span data-ttu-id="e8deb-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8deb-158">RELATED LINKS</span></span>

