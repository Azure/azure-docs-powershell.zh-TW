---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: e73a6bc0d1bf1d2930396bce779bcb03f91d9936
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903318"
---
# <span data-ttu-id="0ed71-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="0ed71-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="0ed71-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0ed71-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed71-103">建立可配置的磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="0ed71-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="0ed71-104">語法</span><span class="sxs-lookup"><span data-stu-id="0ed71-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-Tier <String>] [-DiskIOPSReadOnly <Int64>]
 [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-BurstingEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ed71-105">描述</span><span class="sxs-lookup"><span data-stu-id="0ed71-105">DESCRIPTION</span></span>
<span data-ttu-id="0ed71-106">**New-AzConfigUpdateConfig** Cmdlet 會建立可配置的磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="0ed71-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="0ed71-107">例子</span><span class="sxs-lookup"><span data-stu-id="0ed71-107">EXAMPLES</span></span>

### <span data-ttu-id="0ed71-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="0ed71-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="0ed71-109">第一個命令會建立大小為 10 GB 的儲存空間帳戶類型的Premium_LRS磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="0ed71-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="0ed71-110">它也設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="0ed71-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="0ed71-111">第二個和第三個命令會設定磁片更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="0ed71-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="0ed71-112">最後一個命令會採用磁片更新物件，並更新資源群組 "ResourceGroup01" 中名稱為 "Disk01" 的現有磁片。</span><span class="sxs-lookup"><span data-stu-id="0ed71-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="0ed71-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="0ed71-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="0ed71-114">此命令將資源群組中名稱為 "Disk01" 的現有磁片更新為 10 GB 磁片大小。</span><span class="sxs-lookup"><span data-stu-id="0ed71-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="0ed71-115">參數</span><span class="sxs-lookup"><span data-stu-id="0ed71-115">PARAMETERS</span></span>

### <span data-ttu-id="0ed71-116">-連破Enabled</span><span class="sxs-lookup"><span data-stu-id="0ed71-116">-BurstingEnabled</span></span>
<span data-ttu-id="0ed71-117">啟用超出磁片所提供之績效目標的突然攻擊。</span><span class="sxs-lookup"><span data-stu-id="0ed71-117">Enables bursting beyond the provisioned performance target of the disk.</span></span> <span data-ttu-id="0ed71-118">根據預設，會停用連發功能。</span><span class="sxs-lookup"><span data-stu-id="0ed71-118">Bursting is disabled by default.</span></span> <span data-ttu-id="0ed71-119">不適用於 Ultra 磁片。</span><span class="sxs-lookup"><span data-stu-id="0ed71-119">Does not apply to Ultra disks.</span></span>

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

### <span data-ttu-id="0ed71-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed71-120">-DefaultProfile</span></span>
<span data-ttu-id="0ed71-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0ed71-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ed71-122">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="0ed71-122">-DiskAccessId</span></span>
<span data-ttu-id="0ed71-123">{{ Fill DiskAccessId Description }}</span><span class="sxs-lookup"><span data-stu-id="0ed71-123">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="0ed71-124">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0ed71-124">-DiskEncryptionKey</span></span>
<span data-ttu-id="0ed71-125">指定磁片上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="0ed71-125">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="0ed71-126">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="0ed71-126">-DiskEncryptionSetId</span></span>
<span data-ttu-id="0ed71-127">指定磁片加密集的資源識別碼，以用於啟用靜態加密。</span><span class="sxs-lookup"><span data-stu-id="0ed71-127">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="0ed71-128">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="0ed71-128">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="0ed71-129">所有將共用磁片裝載為 ReadOnly 的虛擬機器所允許的 IOPS 總數。</span><span class="sxs-lookup"><span data-stu-id="0ed71-129">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="0ed71-130">一個作業可在 4k 到 256k 位元組之間傳輸。</span><span class="sxs-lookup"><span data-stu-id="0ed71-130">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed71-131">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="0ed71-131">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="0ed71-132">此磁片允許的 IOPS 數目;僅針對 UltraSSD 磁片設定。</span><span class="sxs-lookup"><span data-stu-id="0ed71-132">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="0ed71-133">一個作業可在 4k 到 256k 位元組之間傳輸。</span><span class="sxs-lookup"><span data-stu-id="0ed71-133">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="0ed71-134">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="0ed71-134">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="0ed71-135">MBps (總輸送量) 所有將共用磁片裝載為 ReadOnly 的虛擬機器所允許。</span><span class="sxs-lookup"><span data-stu-id="0ed71-135">The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="0ed71-136">MBps 表示每秒 100 萬位元組 - MB 使用 10 次之 ISO 標記法。</span><span class="sxs-lookup"><span data-stu-id="0ed71-136">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed71-137">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="0ed71-137">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="0ed71-138">此磁片允許的頻寬;僅針對 UltraSSD 磁片設定。</span><span class="sxs-lookup"><span data-stu-id="0ed71-138">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="0ed71-139">MBps 表示每秒 100 萬位元組 - MB 使用 10 次之 ISO 標記法。</span><span class="sxs-lookup"><span data-stu-id="0ed71-139">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="0ed71-140">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="0ed71-140">-DiskSizeGB</span></span>
<span data-ttu-id="0ed71-141">指定磁片大小 ，以 GB 為單位。</span><span class="sxs-lookup"><span data-stu-id="0ed71-141">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="0ed71-142">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="0ed71-142">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="0ed71-143">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="0ed71-143">Enable encryption settings.</span></span>

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

### <span data-ttu-id="0ed71-144">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="0ed71-144">-EncryptionType</span></span>
<span data-ttu-id="0ed71-145">用來加密磁片資料的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="0ed71-145">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="0ed71-146">可用的值為：'EncryptionAtLatWithPlatformKey'，'EncryptionAtWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="0ed71-146">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="0ed71-147">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0ed71-147">-KeyEncryptionKey</span></span>
<span data-ttu-id="0ed71-148">指定磁片上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="0ed71-148">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="0ed71-149">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="0ed71-149">-MaxSharesCount</span></span>
<span data-ttu-id="0ed71-150">可同時附加至磁片的虛擬機器數目上限。</span><span class="sxs-lookup"><span data-stu-id="0ed71-150">The maximum number of VMs that can attach to the disk at the same time.</span></span> <span data-ttu-id="0ed71-151">大於 1 的值表示可以同時安裝在多個虛擬機器上的磁片。</span><span class="sxs-lookup"><span data-stu-id="0ed71-151">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed71-152">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0ed71-152">-NetworkAccessPolicy</span></span>
<span data-ttu-id="0ed71-153">{{ Fill NetworkAccessPolicy Description }}</span><span class="sxs-lookup"><span data-stu-id="0ed71-153">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="0ed71-154">-OsType</span><span class="sxs-lookup"><span data-stu-id="0ed71-154">-OsType</span></span>
<span data-ttu-id="0ed71-155">指定作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="0ed71-155">Specifies the OS type.</span></span>

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

### <span data-ttu-id="0ed71-156">-SKUName</span><span class="sxs-lookup"><span data-stu-id="0ed71-156">-SkuName</span></span>
<span data-ttu-id="0ed71-157">指定儲存空間帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="0ed71-157">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="0ed71-158">可用的值有Standard_LRS、Premium_LRS、StandardSSD_LRS和UltraSSD_LRS。</span><span class="sxs-lookup"><span data-stu-id="0ed71-158">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="0ed71-159">UltraSSD_LRS只能與 CreateOption 參數的 Empty 值一起使用。</span><span class="sxs-lookup"><span data-stu-id="0ed71-159">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="0ed71-160">-標記</span><span class="sxs-lookup"><span data-stu-id="0ed71-160">-Tag</span></span>
<span data-ttu-id="0ed71-161">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="0ed71-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0ed71-162">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="0ed71-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0ed71-163">-Tier</span><span class="sxs-lookup"><span data-stu-id="0ed71-163">-Tier</span></span>
<span data-ttu-id="0ed71-164">磁片的績效層級。</span><span class="sxs-lookup"><span data-stu-id="0ed71-164">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="0ed71-165">-確認</span><span class="sxs-lookup"><span data-stu-id="0ed71-165">-Confirm</span></span>
<span data-ttu-id="0ed71-166">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0ed71-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ed71-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ed71-167">-WhatIf</span></span>
<span data-ttu-id="0ed71-168">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0ed71-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ed71-169">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0ed71-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ed71-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed71-170">CommonParameters</span></span>
<span data-ttu-id="0ed71-171">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0ed71-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed71-172">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ed71-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed71-173">輸入</span><span class="sxs-lookup"><span data-stu-id="0ed71-173">INPUTS</span></span>

### <span data-ttu-id="0ed71-174">System.String</span><span class="sxs-lookup"><span data-stu-id="0ed71-174">System.String</span></span>

### <span data-ttu-id="0ed71-175">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0ed71-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0ed71-176">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0ed71-176">System.Int32</span></span>

### <span data-ttu-id="0ed71-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0ed71-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0ed71-178">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0ed71-178">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0ed71-179">Microsoft.Azure.management.Compute.models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="0ed71-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="0ed71-180">Microsoft.Azure.management.Compute.models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="0ed71-180">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="0ed71-181">輸出</span><span class="sxs-lookup"><span data-stu-id="0ed71-181">OUTPUTS</span></span>

### <span data-ttu-id="0ed71-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="0ed71-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="0ed71-183">筆記</span><span class="sxs-lookup"><span data-stu-id="0ed71-183">NOTES</span></span>

## <span data-ttu-id="0ed71-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ed71-184">RELATED LINKS</span></span>
