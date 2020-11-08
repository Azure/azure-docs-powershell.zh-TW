---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: 9c267a01629922408f25669ab93aa9a20a01b02b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970582"
---
# <span data-ttu-id="24f83-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="24f83-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="24f83-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24f83-102">SYNOPSIS</span></span>
<span data-ttu-id="24f83-103">建立可設定的磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="24f83-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="24f83-104">句法</span><span class="sxs-lookup"><span data-stu-id="24f83-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24f83-105">說明</span><span class="sxs-lookup"><span data-stu-id="24f83-105">DESCRIPTION</span></span>
<span data-ttu-id="24f83-106">**新的-AzDiskUpdateConfig** Cmdlet 會建立一個可設定的磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="24f83-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="24f83-107">示例</span><span class="sxs-lookup"><span data-stu-id="24f83-107">EXAMPLES</span></span>

### <span data-ttu-id="24f83-108">範例1</span><span class="sxs-lookup"><span data-stu-id="24f83-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="24f83-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機空白磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="24f83-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="24f83-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="24f83-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="24f83-111">第二個和第三個命令會設定磁片更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="24f83-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="24f83-112">最後一個命令會取得磁片更新物件，並更新資源群組 "ResourceGroup01" 中名為「Disk01」的現有磁片。</span><span class="sxs-lookup"><span data-stu-id="24f83-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="24f83-113">範例2</span><span class="sxs-lookup"><span data-stu-id="24f83-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="24f83-114">這個命令會將資源群組 ' ResourceGroup01 ' 中的名稱為 ' Disk01 ' 的現有磁片更新為 10 GB 磁片大小。</span><span class="sxs-lookup"><span data-stu-id="24f83-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="24f83-115">參數</span><span class="sxs-lookup"><span data-stu-id="24f83-115">PARAMETERS</span></span>

### <span data-ttu-id="24f83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f83-116">-DefaultProfile</span></span>
<span data-ttu-id="24f83-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24f83-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24f83-118">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="24f83-118">-DiskAccessId</span></span>
<span data-ttu-id="24f83-119">{{Fill DiskAccessId 說明}}</span><span class="sxs-lookup"><span data-stu-id="24f83-119">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="24f83-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="24f83-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="24f83-121">指定磁片上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="24f83-121">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="24f83-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="24f83-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="24f83-123">指定磁片加密集的資源識別碼，以用於在 rest 上啟用加密。</span><span class="sxs-lookup"><span data-stu-id="24f83-123">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="24f83-124">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="24f83-124">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="24f83-125">此磁片允許的 IOPS 數;僅可設定 UltraSSD 磁片。</span><span class="sxs-lookup"><span data-stu-id="24f83-125">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="24f83-126">一項操作可在4k 與256k 位元組之間進行傳輸。</span><span class="sxs-lookup"><span data-stu-id="24f83-126">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="24f83-127">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="24f83-127">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="24f83-128">此磁片允許的頻寬;僅可設定 UltraSSD 磁片。</span><span class="sxs-lookup"><span data-stu-id="24f83-128">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="24f83-129">Mbits （MBps）代表每秒數百萬個位元組，就會使用 ISO 符號（10的冪）。</span><span class="sxs-lookup"><span data-stu-id="24f83-129">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="24f83-130">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="24f83-130">-DiskSizeGB</span></span>
<span data-ttu-id="24f83-131">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="24f83-131">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="24f83-132">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="24f83-132">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="24f83-133">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="24f83-133">Enable encryption settings.</span></span>

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

### <span data-ttu-id="24f83-134">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="24f83-134">-EncryptionType</span></span>
<span data-ttu-id="24f83-135">用來加密磁片資料的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="24f83-135">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="24f83-136">可用的值為： "EncryptionAtRestWithPlatformKey"、"EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="24f83-136">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="24f83-137">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="24f83-137">-KeyEncryptionKey</span></span>
<span data-ttu-id="24f83-138">指定磁片上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="24f83-138">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="24f83-139">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="24f83-139">-NetworkAccessPolicy</span></span>
<span data-ttu-id="24f83-140">{{Fill NetworkAccessPolicy 說明}}</span><span class="sxs-lookup"><span data-stu-id="24f83-140">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="24f83-141">-OsType</span><span class="sxs-lookup"><span data-stu-id="24f83-141">-OsType</span></span>
<span data-ttu-id="24f83-142">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="24f83-142">Specifies the OS type.</span></span>

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

### <span data-ttu-id="24f83-143">-SkuName</span><span class="sxs-lookup"><span data-stu-id="24f83-143">-SkuName</span></span>
<span data-ttu-id="24f83-144">指定儲存空間帳戶的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="24f83-144">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="24f83-145">可用的值為 Standard_LRS、Premium_LRS、StandardSSD_LRS 和 UltraSSD_LRS。</span><span class="sxs-lookup"><span data-stu-id="24f83-145">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="24f83-146">UltraSSD_LRS 只能與 CreateOption 參數的空值搭配使用。</span><span class="sxs-lookup"><span data-stu-id="24f83-146">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="24f83-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="24f83-147">-Tag</span></span>
<span data-ttu-id="24f83-148">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="24f83-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="24f83-149">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="24f83-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="24f83-150">-確認</span><span class="sxs-lookup"><span data-stu-id="24f83-150">-Confirm</span></span>
<span data-ttu-id="24f83-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24f83-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24f83-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24f83-152">-WhatIf</span></span>
<span data-ttu-id="24f83-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24f83-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24f83-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24f83-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24f83-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f83-155">CommonParameters</span></span>
<span data-ttu-id="24f83-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24f83-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f83-157">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="24f83-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f83-158">輸入</span><span class="sxs-lookup"><span data-stu-id="24f83-158">INPUTS</span></span>

### <span data-ttu-id="24f83-159">System.object</span><span class="sxs-lookup"><span data-stu-id="24f83-159">System.String</span></span>

### <span data-ttu-id="24f83-160">"OperatingSystemTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="24f83-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="24f83-161">System.object</span><span class="sxs-lookup"><span data-stu-id="24f83-161">System.Int32</span></span>

### <span data-ttu-id="24f83-162">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="24f83-162">System.Collections.Hashtable</span></span>

### <span data-ttu-id="24f83-163">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="24f83-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="24f83-164">KeyVaultAndSecretReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="24f83-164">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="24f83-165">KeyVaultAndKeyReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="24f83-165">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="24f83-166">輸出</span><span class="sxs-lookup"><span data-stu-id="24f83-166">OUTPUTS</span></span>

### <span data-ttu-id="24f83-167">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="24f83-167">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="24f83-168">筆記</span><span class="sxs-lookup"><span data-stu-id="24f83-168">NOTES</span></span>

## <span data-ttu-id="24f83-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="24f83-169">RELATED LINKS</span></span>
