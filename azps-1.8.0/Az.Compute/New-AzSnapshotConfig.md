---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 293e894704509fe1b869ca23bd726c49f400de48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622755"
---
# <span data-ttu-id="d1147-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="d1147-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="d1147-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d1147-102">SYNOPSIS</span></span>
<span data-ttu-id="d1147-103">建立可設定的快照物件。</span><span class="sxs-lookup"><span data-stu-id="d1147-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="d1147-104">句法</span><span class="sxs-lookup"><span data-stu-id="d1147-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1147-105">說明</span><span class="sxs-lookup"><span data-stu-id="d1147-105">DESCRIPTION</span></span>
<span data-ttu-id="d1147-106">**新的-AzSnapshotConfig** Cmdlet 會建立可設定的快照物件。</span><span class="sxs-lookup"><span data-stu-id="d1147-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="d1147-107">示例</span><span class="sxs-lookup"><span data-stu-id="d1147-107">EXAMPLES</span></span>

### <span data-ttu-id="d1147-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d1147-108">Example 1</span></span>
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

<span data-ttu-id="d1147-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，使用大小為5GB 來建立本機空快照物件。</span><span class="sxs-lookup"><span data-stu-id="d1147-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="d1147-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="d1147-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d1147-111">第二個和第三個命令會設定快照物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="d1147-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="d1147-112">最後一個命令會採用快照物件，並會在資源群組 "ResourceGroup01" 中建立名為 "Snapshot01" 的快照。</span><span class="sxs-lookup"><span data-stu-id="d1147-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d1147-113">參數</span><span class="sxs-lookup"><span data-stu-id="d1147-113">PARAMETERS</span></span>

### <span data-ttu-id="d1147-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="d1147-114">-CreateOption</span></span>
<span data-ttu-id="d1147-115">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片、建立空白磁片，或附加現有磁片。</span><span class="sxs-lookup"><span data-stu-id="d1147-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="d1147-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1147-116">-DefaultProfile</span></span>
<span data-ttu-id="d1147-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1147-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1147-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d1147-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="d1147-119">指定快照上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="d1147-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="d1147-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="d1147-120">-DiskSizeGB</span></span>
<span data-ttu-id="d1147-121">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="d1147-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="d1147-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="d1147-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="d1147-123">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="d1147-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="d1147-124">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="d1147-124">-HyperVGeneration</span></span>
<span data-ttu-id="d1147-125">虛擬機器的虛擬機器監控程式產生。</span><span class="sxs-lookup"><span data-stu-id="d1147-125">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="d1147-126">僅適用于作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="d1147-126">Applicable to OS disks only.</span></span>  <span data-ttu-id="d1147-127">允許的值為 V1 和 V2。</span><span class="sxs-lookup"><span data-stu-id="d1147-127">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="d1147-128">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="d1147-128">-ImageReference</span></span>
<span data-ttu-id="d1147-129">指定快照上的影像參照。</span><span class="sxs-lookup"><span data-stu-id="d1147-129">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="d1147-130">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d1147-130">-KeyEncryptionKey</span></span>
<span data-ttu-id="d1147-131">指定快照上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="d1147-131">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="d1147-132">-位置</span><span class="sxs-lookup"><span data-stu-id="d1147-132">-Location</span></span>
<span data-ttu-id="d1147-133">指定位置。</span><span class="sxs-lookup"><span data-stu-id="d1147-133">Specifies a location.</span></span>

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

### <span data-ttu-id="d1147-134">-OsType</span><span class="sxs-lookup"><span data-stu-id="d1147-134">-OsType</span></span>
<span data-ttu-id="d1147-135">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="d1147-135">Specifies the OS type.</span></span>

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

### <span data-ttu-id="d1147-136">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d1147-136">-SkuName</span></span>
<span data-ttu-id="d1147-137">指定儲存空間帳戶的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="d1147-137">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="d1147-138">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="d1147-138">-SourceResourceId</span></span>
<span data-ttu-id="d1147-139">指定來源資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1147-139">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="d1147-140">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="d1147-140">-SourceUri</span></span>
<span data-ttu-id="d1147-141">指定來源 Uri。</span><span class="sxs-lookup"><span data-stu-id="d1147-141">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="d1147-142">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d1147-142">-StorageAccountId</span></span>
<span data-ttu-id="d1147-143">指定儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="d1147-143">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="d1147-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="d1147-144">-Tag</span></span>
<span data-ttu-id="d1147-145">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="d1147-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d1147-146">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d1147-146">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d1147-147">-確認</span><span class="sxs-lookup"><span data-stu-id="d1147-147">-Confirm</span></span>
<span data-ttu-id="d1147-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d1147-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1147-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1147-149">-WhatIf</span></span>
<span data-ttu-id="d1147-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d1147-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1147-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d1147-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1147-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1147-152">CommonParameters</span></span>
<span data-ttu-id="d1147-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d1147-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1147-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d1147-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1147-155">輸入</span><span class="sxs-lookup"><span data-stu-id="d1147-155">INPUTS</span></span>

### <span data-ttu-id="d1147-156">System.object</span><span class="sxs-lookup"><span data-stu-id="d1147-156">System.String</span></span>

### <span data-ttu-id="d1147-157">"OperatingSystemTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="d1147-157">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d1147-158">System.object</span><span class="sxs-lookup"><span data-stu-id="d1147-158">System.Int32</span></span>

### <span data-ttu-id="d1147-159">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d1147-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d1147-160">ImageDiskReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="d1147-160">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="d1147-161">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d1147-161">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d1147-162">KeyVaultAndSecretReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="d1147-162">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="d1147-163">KeyVaultAndKeyReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="d1147-163">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="d1147-164">輸出</span><span class="sxs-lookup"><span data-stu-id="d1147-164">OUTPUTS</span></span>

### <span data-ttu-id="d1147-165">PSSnapshot 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="d1147-165">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="d1147-166">筆記</span><span class="sxs-lookup"><span data-stu-id="d1147-166">NOTES</span></span>

## <span data-ttu-id="d1147-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1147-167">RELATED LINKS</span></span>
