---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: c42aae31bb525f9da6a2963a945a6244373ac8db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613304"
---
# <span data-ttu-id="2d435-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="2d435-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="2d435-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2d435-102">SYNOPSIS</span></span>
<span data-ttu-id="2d435-103">建立可設定的快照物件。</span><span class="sxs-lookup"><span data-stu-id="2d435-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="2d435-104">句法</span><span class="sxs-lookup"><span data-stu-id="2d435-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d435-105">說明</span><span class="sxs-lookup"><span data-stu-id="2d435-105">DESCRIPTION</span></span>
<span data-ttu-id="2d435-106">**新的-AzSnapshotConfig** Cmdlet 會建立可設定的快照物件。</span><span class="sxs-lookup"><span data-stu-id="2d435-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="2d435-107">示例</span><span class="sxs-lookup"><span data-stu-id="2d435-107">EXAMPLES</span></span>

### <span data-ttu-id="2d435-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2d435-108">Example 1</span></span>
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

<span data-ttu-id="2d435-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，使用大小為5GB 來建立本機空快照物件。</span><span class="sxs-lookup"><span data-stu-id="2d435-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="2d435-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="2d435-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="2d435-111">第二個和第三個命令會設定快照物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="2d435-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="2d435-112">最後一個命令會採用快照物件，並會在資源群組 "ResourceGroup01" 中建立名為 "Snapshot01" 的快照。</span><span class="sxs-lookup"><span data-stu-id="2d435-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="2d435-113">參數</span><span class="sxs-lookup"><span data-stu-id="2d435-113">PARAMETERS</span></span>

### <span data-ttu-id="2d435-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="2d435-114">-CreateOption</span></span>
<span data-ttu-id="2d435-115">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片、建立空白磁片，或附加現有磁片。</span><span class="sxs-lookup"><span data-stu-id="2d435-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="2d435-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d435-116">-DefaultProfile</span></span>
<span data-ttu-id="2d435-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d435-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d435-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="2d435-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="2d435-119">指定快照上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="2d435-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="2d435-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="2d435-120">-DiskSizeGB</span></span>
<span data-ttu-id="2d435-121">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="2d435-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="2d435-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="2d435-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="2d435-123">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="2d435-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="2d435-124">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="2d435-124">-HyperVGeneration</span></span>
<span data-ttu-id="2d435-125">虛擬機器的虛擬機器監控程式產生。</span><span class="sxs-lookup"><span data-stu-id="2d435-125">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="2d435-126">僅適用于作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="2d435-126">Applicable to OS disks only.</span></span>  <span data-ttu-id="2d435-127">允許的值為 V1 和 V2。</span><span class="sxs-lookup"><span data-stu-id="2d435-127">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="2d435-128">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="2d435-128">-ImageReference</span></span>
<span data-ttu-id="2d435-129">指定快照上的影像參照。</span><span class="sxs-lookup"><span data-stu-id="2d435-129">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="2d435-130">-增量式</span><span class="sxs-lookup"><span data-stu-id="2d435-130">-Incremental</span></span>
<span data-ttu-id="2d435-131">指定增量快照。</span><span class="sxs-lookup"><span data-stu-id="2d435-131">Specifies an incremental snapshot.</span></span> <span data-ttu-id="2d435-132">同一磁片上的增量快照佔用的空間比完全快照還少，而且可以 diffed。</span><span class="sxs-lookup"><span data-stu-id="2d435-132">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d435-133">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="2d435-133">-KeyEncryptionKey</span></span>
<span data-ttu-id="2d435-134">指定快照上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="2d435-134">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="2d435-135">-位置</span><span class="sxs-lookup"><span data-stu-id="2d435-135">-Location</span></span>
<span data-ttu-id="2d435-136">指定位置。</span><span class="sxs-lookup"><span data-stu-id="2d435-136">Specifies a location.</span></span>

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

### <span data-ttu-id="2d435-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="2d435-137">-OsType</span></span>
<span data-ttu-id="2d435-138">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="2d435-138">Specifies the OS type.</span></span>

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

### <span data-ttu-id="2d435-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2d435-139">-SkuName</span></span>
<span data-ttu-id="2d435-140">指定儲存空間帳戶的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="2d435-140">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="2d435-141">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="2d435-141">-SourceResourceId</span></span>
<span data-ttu-id="2d435-142">指定來源資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d435-142">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="2d435-143">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="2d435-143">-SourceUri</span></span>
<span data-ttu-id="2d435-144">指定來源 Uri。</span><span class="sxs-lookup"><span data-stu-id="2d435-144">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="2d435-145">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2d435-145">-StorageAccountId</span></span>
<span data-ttu-id="2d435-146">指定儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="2d435-146">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="2d435-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="2d435-147">-Tag</span></span>
<span data-ttu-id="2d435-148">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="2d435-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2d435-149">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2d435-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2d435-150">-確認</span><span class="sxs-lookup"><span data-stu-id="2d435-150">-Confirm</span></span>
<span data-ttu-id="2d435-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2d435-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d435-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d435-152">-WhatIf</span></span>
<span data-ttu-id="2d435-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2d435-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d435-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d435-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d435-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d435-155">CommonParameters</span></span>
<span data-ttu-id="2d435-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2d435-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d435-157">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2d435-157">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d435-158">輸入</span><span class="sxs-lookup"><span data-stu-id="2d435-158">INPUTS</span></span>

### <span data-ttu-id="2d435-159">System.object</span><span class="sxs-lookup"><span data-stu-id="2d435-159">System.String</span></span>

### <span data-ttu-id="2d435-160">"OperatingSystemTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="2d435-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2d435-161">System.object</span><span class="sxs-lookup"><span data-stu-id="2d435-161">System.Int32</span></span>

### <span data-ttu-id="2d435-162">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2d435-162">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2d435-163">ImageDiskReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="2d435-163">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="2d435-164">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2d435-164">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2d435-165">KeyVaultAndSecretReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="2d435-165">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="2d435-166">KeyVaultAndKeyReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="2d435-166">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="2d435-167">輸出</span><span class="sxs-lookup"><span data-stu-id="2d435-167">OUTPUTS</span></span>

### <span data-ttu-id="2d435-168">PSSnapshot 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="2d435-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="2d435-169">筆記</span><span class="sxs-lookup"><span data-stu-id="2d435-169">NOTES</span></span>

## <span data-ttu-id="2d435-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d435-170">RELATED LINKS</span></span>
