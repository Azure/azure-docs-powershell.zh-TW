---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: 1a90a1ff260d143cf4df52ad160b4c05e781bd2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143379"
---
# <span data-ttu-id="7e80a-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="7e80a-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="7e80a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7e80a-102">SYNOPSIS</span></span>
<span data-ttu-id="7e80a-103">建立可設定的快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="7e80a-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="7e80a-104">句法</span><span class="sxs-lookup"><span data-stu-id="7e80a-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DiskEncryptionSetId <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e80a-105">說明</span><span class="sxs-lookup"><span data-stu-id="7e80a-105">DESCRIPTION</span></span>
<span data-ttu-id="7e80a-106">**新的-AzSnapshotUpdateConfig** Cmdlet 會建立可設定的快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="7e80a-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="7e80a-107">示例</span><span class="sxs-lookup"><span data-stu-id="7e80a-107">EXAMPLES</span></span>

### <span data-ttu-id="7e80a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7e80a-108">Example 1</span></span>
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

<span data-ttu-id="7e80a-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機空白快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="7e80a-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="7e80a-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="7e80a-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="7e80a-111">第二個和第三個命令會設定快照更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="7e80a-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="7e80a-112">最後一個命令會採用快照更新物件，並更新資源群組 "ResourceGroup01" 中名稱為 "Snapshot01" 的現有快照。</span><span class="sxs-lookup"><span data-stu-id="7e80a-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="7e80a-113">範例2</span><span class="sxs-lookup"><span data-stu-id="7e80a-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="7e80a-114">這個命令會將資源群組 ' ResourceGroup01 ' 中名稱為 ' Snapshot01 ' 的現有快照更新為 10 GB 磁片大小。</span><span class="sxs-lookup"><span data-stu-id="7e80a-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="7e80a-115">參數</span><span class="sxs-lookup"><span data-stu-id="7e80a-115">PARAMETERS</span></span>

### <span data-ttu-id="7e80a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e80a-116">-DefaultProfile</span></span>
<span data-ttu-id="7e80a-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e80a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e80a-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7e80a-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="7e80a-119">指定快照上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="7e80a-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="7e80a-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="7e80a-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="7e80a-121">指定磁片加密集的資源識別碼，以用於在 rest 上啟用加密。</span><span class="sxs-lookup"><span data-stu-id="7e80a-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="7e80a-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="7e80a-122">-DiskSizeGB</span></span>
<span data-ttu-id="7e80a-123">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="7e80a-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="7e80a-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="7e80a-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="7e80a-125">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="7e80a-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="7e80a-126">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="7e80a-126">-EncryptionType</span></span>
<span data-ttu-id="7e80a-127">用來加密磁片資料的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="7e80a-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="7e80a-128">可用的值為： "EncryptionAtRestWithPlatformKey"、"EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="7e80a-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="7e80a-129">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7e80a-129">-KeyEncryptionKey</span></span>
<span data-ttu-id="7e80a-130">指定快照上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="7e80a-130">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="7e80a-131">-OsType</span><span class="sxs-lookup"><span data-stu-id="7e80a-131">-OsType</span></span>
<span data-ttu-id="7e80a-132">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="7e80a-132">Specifies the OS type.</span></span>

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

### <span data-ttu-id="7e80a-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7e80a-133">-SkuName</span></span>
<span data-ttu-id="7e80a-134">指定儲存空間帳戶的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="7e80a-134">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="7e80a-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e80a-135">-Tag</span></span>
<span data-ttu-id="7e80a-136">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="7e80a-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7e80a-137">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7e80a-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7e80a-138">-確認</span><span class="sxs-lookup"><span data-stu-id="7e80a-138">-Confirm</span></span>
<span data-ttu-id="7e80a-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7e80a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e80a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e80a-140">-WhatIf</span></span>
<span data-ttu-id="7e80a-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7e80a-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e80a-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e80a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e80a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e80a-143">CommonParameters</span></span>
<span data-ttu-id="7e80a-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7e80a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e80a-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7e80a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e80a-146">輸入</span><span class="sxs-lookup"><span data-stu-id="7e80a-146">INPUTS</span></span>

### <span data-ttu-id="7e80a-147">System.object</span><span class="sxs-lookup"><span data-stu-id="7e80a-147">System.String</span></span>

### <span data-ttu-id="7e80a-148">"OperatingSystemTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="7e80a-148">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7e80a-149">System.object</span><span class="sxs-lookup"><span data-stu-id="7e80a-149">System.Int32</span></span>

### <span data-ttu-id="7e80a-150">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7e80a-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7e80a-151">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7e80a-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7e80a-152">KeyVaultAndSecretReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="7e80a-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="7e80a-153">KeyVaultAndKeyReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="7e80a-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="7e80a-154">輸出</span><span class="sxs-lookup"><span data-stu-id="7e80a-154">OUTPUTS</span></span>

### <span data-ttu-id="7e80a-155">PSSnapshotUpdate 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="7e80a-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="7e80a-156">筆記</span><span class="sxs-lookup"><span data-stu-id="7e80a-156">NOTES</span></span>

## <span data-ttu-id="7e80a-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e80a-157">RELATED LINKS</span></span>
