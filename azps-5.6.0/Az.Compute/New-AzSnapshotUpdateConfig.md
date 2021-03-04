---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: 82d7c1768b9e7f702b87a2bd23afcc76257b937f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906233"
---
# <span data-ttu-id="8c49a-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="8c49a-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="8c49a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8c49a-102">SYNOPSIS</span></span>
<span data-ttu-id="8c49a-103">建立可配置的快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="8c49a-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="8c49a-104">語法</span><span class="sxs-lookup"><span data-stu-id="8c49a-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DiskEncryptionSetId <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c49a-105">描述</span><span class="sxs-lookup"><span data-stu-id="8c49a-105">DESCRIPTION</span></span>
<span data-ttu-id="8c49a-106">**New-AzSnapshotUpdateConfig** Cmdlet 會建立可配置的快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="8c49a-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="8c49a-107">例子</span><span class="sxs-lookup"><span data-stu-id="8c49a-107">EXAMPLES</span></span>

### <span data-ttu-id="8c49a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="8c49a-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="8c49a-109">第一個命令會以儲存帳戶類型建立大小為 10 GB 的Premium_LRS快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="8c49a-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="8c49a-110">它也設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="8c49a-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="8c49a-111">第二個和第三個命令會設定快照更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="8c49a-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="8c49a-112">最後一個命令會拍攝快照更新物件，並更新資源群組 "ResourceGroup01" 中名稱為 "Snapshot01" 的現有快照。</span><span class="sxs-lookup"><span data-stu-id="8c49a-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="8c49a-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="8c49a-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="8c49a-114">此命令會更新資源群組中名稱為 "Snapshot01" 的現有快照，將磁片大小更新為 10 GB。</span><span class="sxs-lookup"><span data-stu-id="8c49a-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="8c49a-115">參數</span><span class="sxs-lookup"><span data-stu-id="8c49a-115">PARAMETERS</span></span>

### <span data-ttu-id="8c49a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c49a-116">-DefaultProfile</span></span>
<span data-ttu-id="8c49a-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c49a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c49a-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8c49a-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="8c49a-119">指定快照上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="8c49a-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="8c49a-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="8c49a-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="8c49a-121">指定磁片加密集的資源識別碼，以用於啟用靜態加密。</span><span class="sxs-lookup"><span data-stu-id="8c49a-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="8c49a-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="8c49a-122">-DiskSizeGB</span></span>
<span data-ttu-id="8c49a-123">指定磁片大小 ，以 GB 為單位。</span><span class="sxs-lookup"><span data-stu-id="8c49a-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="8c49a-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="8c49a-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="8c49a-125">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="8c49a-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="8c49a-126">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="8c49a-126">-EncryptionType</span></span>
<span data-ttu-id="8c49a-127">用來加密磁片資料的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="8c49a-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="8c49a-128">可用的值為：'EncryptionAtLatWithPlatformKey'，'EncryptionAtWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="8c49a-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="8c49a-129">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8c49a-129">-KeyEncryptionKey</span></span>
<span data-ttu-id="8c49a-130">指定快照上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="8c49a-130">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="8c49a-131">-OsType</span><span class="sxs-lookup"><span data-stu-id="8c49a-131">-OsType</span></span>
<span data-ttu-id="8c49a-132">指定作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="8c49a-132">Specifies the OS type.</span></span>

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

### <span data-ttu-id="8c49a-133">-SKUName</span><span class="sxs-lookup"><span data-stu-id="8c49a-133">-SkuName</span></span>
<span data-ttu-id="8c49a-134">指定儲存空間帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="8c49a-134">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="8c49a-135">-標記</span><span class="sxs-lookup"><span data-stu-id="8c49a-135">-Tag</span></span>
<span data-ttu-id="8c49a-136">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="8c49a-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8c49a-137">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="8c49a-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8c49a-138">-確認</span><span class="sxs-lookup"><span data-stu-id="8c49a-138">-Confirm</span></span>
<span data-ttu-id="8c49a-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8c49a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c49a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c49a-140">-WhatIf</span></span>
<span data-ttu-id="8c49a-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c49a-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c49a-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c49a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c49a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c49a-143">CommonParameters</span></span>
<span data-ttu-id="8c49a-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8c49a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c49a-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c49a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c49a-146">輸入</span><span class="sxs-lookup"><span data-stu-id="8c49a-146">INPUTS</span></span>

### <span data-ttu-id="8c49a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="8c49a-147">System.String</span></span>

### <span data-ttu-id="8c49a-148">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8c49a-148">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="8c49a-149">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8c49a-149">System.Int32</span></span>

### <span data-ttu-id="8c49a-150">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8c49a-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8c49a-151">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8c49a-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8c49a-152">Microsoft.Azure.management.Compute.models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="8c49a-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="8c49a-153">Microsoft.Azure.management.Compute.models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="8c49a-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="8c49a-154">輸出</span><span class="sxs-lookup"><span data-stu-id="8c49a-154">OUTPUTS</span></span>

### <span data-ttu-id="8c49a-155">Microsoft.Azure.Commands.Compute.Automation.models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="8c49a-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="8c49a-156">筆記</span><span class="sxs-lookup"><span data-stu-id="8c49a-156">NOTES</span></span>

## <span data-ttu-id="8c49a-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c49a-157">RELATED LINKS</span></span>
