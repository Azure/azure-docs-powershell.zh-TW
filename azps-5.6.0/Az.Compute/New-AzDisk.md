---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDisk.md
ms.openlocfilehash: 1337482e880bca353e4824a00b73aef831db6b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909754"
---
# <span data-ttu-id="dba42-101">New-AzDisk</span><span class="sxs-lookup"><span data-stu-id="dba42-101">New-AzDisk</span></span>

## <span data-ttu-id="dba42-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dba42-102">SYNOPSIS</span></span>
<span data-ttu-id="dba42-103">建立受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="dba42-103">Creates a managed disk.</span></span>

## <span data-ttu-id="dba42-104">語法</span><span class="sxs-lookup"><span data-stu-id="dba42-104">SYNTAX</span></span>

```
New-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dba42-105">描述</span><span class="sxs-lookup"><span data-stu-id="dba42-105">DESCRIPTION</span></span>
<span data-ttu-id="dba42-106">**New-Az在 Cmdlet** 中會建立受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="dba42-106">The **New-AzDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="dba42-107">例子</span><span class="sxs-lookup"><span data-stu-id="dba42-107">EXAMPLES</span></span>

### <span data-ttu-id="dba42-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="dba42-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="dba42-109">第一個命令會建立大小為 5 GB 的儲存Standard_LRS物件。</span><span class="sxs-lookup"><span data-stu-id="dba42-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="dba42-110">它也設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="dba42-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="dba42-111">第二個和第三個命令會設定磁片物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="dba42-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="dba42-112">最後一個命令會取用磁片物件，在資源群組 'ResourceGroup01' 中建立名稱為 'Disk01' 的磁片。</span><span class="sxs-lookup"><span data-stu-id="dba42-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="dba42-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="dba42-113">Example 2</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $diskConfig.EncryptionSettingsCollection = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsCollection

PS C:\> $encryptionSettingsElement1 = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsElement
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SourceVault.Id = $disk_encryption_key_id_1
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SecretUrl = $disk_encryption_secret_url_1
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.SourceVault.Id = $key_encryption_key_id_1
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.KeyUrl = $key_encryption_key_url_1

PS C:\> $encryptionSettingsElement2 = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsElement
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SourceVault.Id = $disk_encryption_key_id_2
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SecretUrl = $disk_encryption_secret_url_2
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.SourceVault.Id = $key_encryption_key_id_2
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.KeyUrl = $key_encryption_key_url_2

PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettings += $encryptionSettingsElement1
PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettings += $encryptionSettingsElement2
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="dba42-114">上述命令會建立一個磁片，具有兩個加密設定。</span><span class="sxs-lookup"><span data-stu-id="dba42-114">The above command creates a disk with two encryption settings.</span></span>

## <span data-ttu-id="dba42-115">參數</span><span class="sxs-lookup"><span data-stu-id="dba42-115">PARAMETERS</span></span>

### <span data-ttu-id="dba42-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dba42-116">-AsJob</span></span>
<span data-ttu-id="dba42-117">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="dba42-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dba42-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba42-118">-DefaultProfile</span></span>
<span data-ttu-id="dba42-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dba42-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dba42-120">-磁片</span><span class="sxs-lookup"><span data-stu-id="dba42-120">-Disk</span></span>
<span data-ttu-id="dba42-121">指定一個本地磁片物件。</span><span class="sxs-lookup"><span data-stu-id="dba42-121">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dba42-122">-DiskName</span><span class="sxs-lookup"><span data-stu-id="dba42-122">-DiskName</span></span>
<span data-ttu-id="dba42-123">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="dba42-123">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dba42-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dba42-124">-ResourceGroupName</span></span>
<span data-ttu-id="dba42-125">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dba42-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dba42-126">-確認</span><span class="sxs-lookup"><span data-stu-id="dba42-126">-Confirm</span></span>
<span data-ttu-id="dba42-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="dba42-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dba42-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dba42-128">-WhatIf</span></span>
<span data-ttu-id="dba42-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dba42-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dba42-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dba42-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dba42-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba42-131">CommonParameters</span></span>
<span data-ttu-id="dba42-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dba42-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba42-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dba42-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba42-134">輸入</span><span class="sxs-lookup"><span data-stu-id="dba42-134">INPUTS</span></span>

### <span data-ttu-id="dba42-135">System.String</span><span class="sxs-lookup"><span data-stu-id="dba42-135">System.String</span></span>

### <span data-ttu-id="dba42-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="dba42-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="dba42-137">輸出</span><span class="sxs-lookup"><span data-stu-id="dba42-137">OUTPUTS</span></span>

### <span data-ttu-id="dba42-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="dba42-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="dba42-139">筆記</span><span class="sxs-lookup"><span data-stu-id="dba42-139">NOTES</span></span>

## <span data-ttu-id="dba42-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="dba42-140">RELATED LINKS</span></span>
