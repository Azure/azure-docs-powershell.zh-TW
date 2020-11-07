---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 1afd1631e398b5726a8e1002b6739fc7ac9b67a8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796134"
---
# <span data-ttu-id="a4b20-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a4b20-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="a4b20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4b20-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b20-103">建立可設定的快照物件。</span><span class="sxs-lookup"><span data-stu-id="a4b20-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="a4b20-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4b20-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4b20-105">說明</span><span class="sxs-lookup"><span data-stu-id="a4b20-105">DESCRIPTION</span></span>
<span data-ttu-id="a4b20-106">**新的-AzSnapshotConfig** Cmdlet 會建立可設定的快照物件。</span><span class="sxs-lookup"><span data-stu-id="a4b20-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="a4b20-107">示例</span><span class="sxs-lookup"><span data-stu-id="a4b20-107">EXAMPLES</span></span>

### <span data-ttu-id="a4b20-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a4b20-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="a4b20-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，使用大小為5GB 來建立本機空快照物件。</span><span class="sxs-lookup"><span data-stu-id="a4b20-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="a4b20-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="a4b20-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="a4b20-111">第二個和第三個命令會設定快照物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="a4b20-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="a4b20-112">最後一個命令會採用快照物件，並會在資源群組 "ResourceGroup01" 中建立名為 "Snapshot01" 的快照。</span><span class="sxs-lookup"><span data-stu-id="a4b20-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a4b20-113">參數</span><span class="sxs-lookup"><span data-stu-id="a4b20-113">PARAMETERS</span></span>

### <span data-ttu-id="a4b20-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="a4b20-114">-CreateOption</span></span>
<span data-ttu-id="a4b20-115">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片、建立空白磁片，或附加現有磁片。</span><span class="sxs-lookup"><span data-stu-id="a4b20-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="a4b20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b20-116">-DefaultProfile</span></span>
<span data-ttu-id="a4b20-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4b20-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4b20-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a4b20-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="a4b20-119">指定快照上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="a4b20-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="a4b20-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="a4b20-120">-DiskSizeGB</span></span>
<span data-ttu-id="a4b20-121">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="a4b20-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="a4b20-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="a4b20-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="a4b20-123">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="a4b20-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="a4b20-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="a4b20-124">-ImageReference</span></span>
<span data-ttu-id="a4b20-125">指定快照上的影像參照。</span><span class="sxs-lookup"><span data-stu-id="a4b20-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="a4b20-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a4b20-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="a4b20-127">指定快照上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="a4b20-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="a4b20-128">-位置</span><span class="sxs-lookup"><span data-stu-id="a4b20-128">-Location</span></span>
<span data-ttu-id="a4b20-129">指定位置。</span><span class="sxs-lookup"><span data-stu-id="a4b20-129">Specifies a location.</span></span>

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

### <span data-ttu-id="a4b20-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="a4b20-130">-OsType</span></span>
<span data-ttu-id="a4b20-131">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="a4b20-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="a4b20-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a4b20-132">-SkuName</span></span>
<span data-ttu-id="a4b20-133">指定儲存空間帳戶的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="a4b20-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="a4b20-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="a4b20-134">-SourceResourceId</span></span>
<span data-ttu-id="a4b20-135">指定來源資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4b20-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="a4b20-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="a4b20-136">-SourceUri</span></span>
<span data-ttu-id="a4b20-137">指定來源 Uri。</span><span class="sxs-lookup"><span data-stu-id="a4b20-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="a4b20-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a4b20-138">-StorageAccountId</span></span>
<span data-ttu-id="a4b20-139">指定儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="a4b20-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="a4b20-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="a4b20-140">-Tag</span></span>
<span data-ttu-id="a4b20-141">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="a4b20-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a4b20-142">例如：</span><span class="sxs-lookup"><span data-stu-id="a4b20-142">For example:</span></span>

<span data-ttu-id="a4b20-143">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a4b20-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a4b20-144">-確認</span><span class="sxs-lookup"><span data-stu-id="a4b20-144">-Confirm</span></span>
<span data-ttu-id="a4b20-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a4b20-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4b20-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4b20-146">-WhatIf</span></span>
<span data-ttu-id="a4b20-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4b20-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4b20-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4b20-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4b20-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b20-149">CommonParameters</span></span>
<span data-ttu-id="a4b20-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4b20-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b20-151">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a4b20-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b20-152">輸入</span><span class="sxs-lookup"><span data-stu-id="a4b20-152">INPUTS</span></span>

### <span data-ttu-id="a4b20-153">所有</span><span class="sxs-lookup"><span data-stu-id="a4b20-153">None</span></span>
<span data-ttu-id="a4b20-154">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a4b20-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4b20-155">輸出</span><span class="sxs-lookup"><span data-stu-id="a4b20-155">OUTPUTS</span></span>

### <span data-ttu-id="a4b20-156">PSSnapshot 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="a4b20-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="a4b20-157">筆記</span><span class="sxs-lookup"><span data-stu-id="a4b20-157">NOTES</span></span>

## <span data-ttu-id="a4b20-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4b20-158">RELATED LINKS</span></span>

