---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDisk.md
ms.openlocfilehash: bbb450aebe4b24aa887c8592acfab04e84bfd944
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282856"
---
# <span data-ttu-id="4884c-101">New-AzDisk</span><span class="sxs-lookup"><span data-stu-id="4884c-101">New-AzDisk</span></span>

## <span data-ttu-id="4884c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4884c-102">SYNOPSIS</span></span>
<span data-ttu-id="4884c-103">建立受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="4884c-103">Creates a managed disk.</span></span>

## <span data-ttu-id="4884c-104">句法</span><span class="sxs-lookup"><span data-stu-id="4884c-104">SYNTAX</span></span>

```
New-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4884c-105">說明</span><span class="sxs-lookup"><span data-stu-id="4884c-105">DESCRIPTION</span></span>
<span data-ttu-id="4884c-106">**新的-AzDisk** Cmdlet 會建立受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="4884c-106">The **New-AzDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="4884c-107">示例</span><span class="sxs-lookup"><span data-stu-id="4884c-107">EXAMPLES</span></span>

### <span data-ttu-id="4884c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4884c-108">Example 1</span></span>
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

<span data-ttu-id="4884c-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，建立一個大小為5GB 的本機空白磁片物件。</span><span class="sxs-lookup"><span data-stu-id="4884c-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="4884c-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="4884c-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="4884c-111">第二個和第三個命令會設定磁片物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="4884c-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="4884c-112">最後一個命令會取得磁片物件，並在 [資源] 群組的 [ResourceGroup01] 中建立名為 "Disk01" 的磁片。</span><span class="sxs-lookup"><span data-stu-id="4884c-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="4884c-113">範例2</span><span class="sxs-lookup"><span data-stu-id="4884c-113">Example 2</span></span>
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

<span data-ttu-id="4884c-114">上述命令會建立具有兩個加密設定的磁片。</span><span class="sxs-lookup"><span data-stu-id="4884c-114">The above command creates a disk with two encryption settings.</span></span>

## <span data-ttu-id="4884c-115">參數</span><span class="sxs-lookup"><span data-stu-id="4884c-115">PARAMETERS</span></span>

### <span data-ttu-id="4884c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4884c-116">-AsJob</span></span>
<span data-ttu-id="4884c-117">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="4884c-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4884c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4884c-118">-DefaultProfile</span></span>
<span data-ttu-id="4884c-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4884c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4884c-120">-磁片</span><span class="sxs-lookup"><span data-stu-id="4884c-120">-Disk</span></span>
<span data-ttu-id="4884c-121">指定本機磁片物件。</span><span class="sxs-lookup"><span data-stu-id="4884c-121">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="4884c-122">-DiskName</span><span class="sxs-lookup"><span data-stu-id="4884c-122">-DiskName</span></span>
<span data-ttu-id="4884c-123">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="4884c-123">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="4884c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4884c-124">-ResourceGroupName</span></span>
<span data-ttu-id="4884c-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4884c-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4884c-126">-確認</span><span class="sxs-lookup"><span data-stu-id="4884c-126">-Confirm</span></span>
<span data-ttu-id="4884c-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4884c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4884c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4884c-128">-WhatIf</span></span>
<span data-ttu-id="4884c-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4884c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4884c-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4884c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4884c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4884c-131">CommonParameters</span></span>
<span data-ttu-id="4884c-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4884c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4884c-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4884c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4884c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="4884c-134">INPUTS</span></span>

### <span data-ttu-id="4884c-135">System.object</span><span class="sxs-lookup"><span data-stu-id="4884c-135">System.String</span></span>

### <span data-ttu-id="4884c-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="4884c-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="4884c-137">輸出</span><span class="sxs-lookup"><span data-stu-id="4884c-137">OUTPUTS</span></span>

### <span data-ttu-id="4884c-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="4884c-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="4884c-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4884c-139">NOTES</span></span>

## <span data-ttu-id="4884c-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4884c-140">RELATED LINKS</span></span>
