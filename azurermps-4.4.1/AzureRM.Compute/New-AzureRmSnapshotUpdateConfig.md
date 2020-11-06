---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
ms.openlocfilehash: 00519ec40e4f173c7ecfbb37189835711184f2e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456827"
---
# <span data-ttu-id="08c11-101">New-AzureRmSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="08c11-101">New-AzureRmSnapshotUpdateConfig</span></span>

## <span data-ttu-id="08c11-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08c11-102">SYNOPSIS</span></span>
<span data-ttu-id="08c11-103">建立可設定的快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="08c11-103">Creates a configurable snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08c11-104">句法</span><span class="sxs-lookup"><span data-stu-id="08c11-104">SYNTAX</span></span>

```
New-AzureRmSnapshotUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08c11-105">說明</span><span class="sxs-lookup"><span data-stu-id="08c11-105">DESCRIPTION</span></span>
<span data-ttu-id="08c11-106">**新的-AzureRmSnapshotUpdateConfig** Cmdlet 會建立可設定的快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="08c11-106">The **New-AzureRmSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="08c11-107">示例</span><span class="sxs-lookup"><span data-stu-id="08c11-107">EXAMPLES</span></span>

### <span data-ttu-id="08c11-108">範例1</span><span class="sxs-lookup"><span data-stu-id="08c11-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="08c11-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機空白快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="08c11-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="08c11-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="08c11-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="08c11-111">第二個和第三個命令會設定快照更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="08c11-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="08c11-112">最後一個命令會採用快照更新物件，並更新資源群組 "ResourceGroup01" 中名稱為 "Snapshot01" 的現有快照。</span><span class="sxs-lookup"><span data-stu-id="08c11-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="08c11-113">範例2</span><span class="sxs-lookup"><span data-stu-id="08c11-113">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="08c11-114">這個命令會將資源群組 ' ResourceGroup01 ' 中名稱為 ' Snapshot01 ' 的現有快照更新為 10 GB 磁片大小。</span><span class="sxs-lookup"><span data-stu-id="08c11-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="08c11-115">參數</span><span class="sxs-lookup"><span data-stu-id="08c11-115">PARAMETERS</span></span>

### <span data-ttu-id="08c11-116">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="08c11-116">-CreateOption</span></span>
<span data-ttu-id="08c11-117">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立快照、建立空白磁片，或附加現有磁片。</span><span class="sxs-lookup"><span data-stu-id="08c11-117">Specifies whether this cmdlet creates a snapshot in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c11-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08c11-118">-DefaultProfile</span></span>
<span data-ttu-id="08c11-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="08c11-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08c11-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="08c11-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="08c11-121">指定快照上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="08c11-121">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="08c11-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="08c11-122">-DiskSizeGB</span></span>
<span data-ttu-id="08c11-123">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="08c11-123">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c11-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="08c11-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="08c11-125">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="08c11-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="08c11-126">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="08c11-126">-ImageReference</span></span>
<span data-ttu-id="08c11-127">指定快照上的影像參照。</span><span class="sxs-lookup"><span data-stu-id="08c11-127">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="08c11-128">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="08c11-128">-KeyEncryptionKey</span></span>
<span data-ttu-id="08c11-129">指定快照上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="08c11-129">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="08c11-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="08c11-130">-OsType</span></span>
<span data-ttu-id="08c11-131">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="08c11-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="08c11-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="08c11-132">-SkuName</span></span>
<span data-ttu-id="08c11-133">指定儲存空間帳戶的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="08c11-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c11-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="08c11-134">-SourceResourceId</span></span>
<span data-ttu-id="08c11-135">指定來源資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="08c11-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="08c11-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="08c11-136">-SourceUri</span></span>
<span data-ttu-id="08c11-137">指定來源 Uri。</span><span class="sxs-lookup"><span data-stu-id="08c11-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="08c11-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="08c11-138">-StorageAccountId</span></span>
<span data-ttu-id="08c11-139">指定儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="08c11-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="08c11-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="08c11-140">-Tag</span></span>
<span data-ttu-id="08c11-141">指定可以使用一組名稱值對來標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="08c11-141">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c11-142">-確認</span><span class="sxs-lookup"><span data-stu-id="08c11-142">-Confirm</span></span>
<span data-ttu-id="08c11-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="08c11-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08c11-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08c11-144">-WhatIf</span></span>
<span data-ttu-id="08c11-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="08c11-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08c11-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08c11-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08c11-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08c11-147">CommonParameters</span></span>
<span data-ttu-id="08c11-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08c11-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08c11-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="08c11-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08c11-150">輸入</span><span class="sxs-lookup"><span data-stu-id="08c11-150">INPUTS</span></span>

### <span data-ttu-id="08c11-151">"StorageAccountTypes" 1 [[14.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="08c11-151">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="08c11-152">系統. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [System. Int32，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = b77a5c561934e089]] system. 集合. Hashtable = `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]，區域性 = 中立，PublicKeyToken =]]，</span><span class="sxs-lookup"><span data-stu-id="08c11-152">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="08c11-153">輸出</span><span class="sxs-lookup"><span data-stu-id="08c11-153">OUTPUTS</span></span>

### <span data-ttu-id="08c11-154">SnapshotUpdate 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="08c11-154">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="08c11-155">筆記</span><span class="sxs-lookup"><span data-stu-id="08c11-155">NOTES</span></span>

## <span data-ttu-id="08c11-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="08c11-156">RELATED LINKS</span></span>

