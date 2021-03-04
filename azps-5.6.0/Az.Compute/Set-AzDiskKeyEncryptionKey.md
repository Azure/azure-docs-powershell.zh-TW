---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azdiskkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
ms.openlocfilehash: 4a130755b4cfd84b0394d51c7dcf65b0437925e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902118"
---
# <span data-ttu-id="5e7f8-101">Set-AzDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5e7f8-101">Set-AzDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="5e7f8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5e7f8-102">SYNOPSIS</span></span>
<span data-ttu-id="5e7f8-103">設定磁片物件上的金鑰加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="5e7f8-103">Sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="5e7f8-104">語法</span><span class="sxs-lookup"><span data-stu-id="5e7f8-104">SYNTAX</span></span>

```
Set-AzDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e7f8-105">描述</span><span class="sxs-lookup"><span data-stu-id="5e7f8-105">DESCRIPTION</span></span>
<span data-ttu-id="5e7f8-106">**Set-AzKeyEncryptionKey** Cmdlet 會設定磁片物件上的金鑰加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="5e7f8-106">The **Set-AzDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="5e7f8-107">例子</span><span class="sxs-lookup"><span data-stu-id="5e7f8-107">EXAMPLES</span></span>

### <span data-ttu-id="5e7f8-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="5e7f8-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> $diskconfig.EncryptionSettingsCollection.EncryptionSettingsVersion = '1.1';
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="5e7f8-109">第一個命令會建立大小為 5 GB 的儲存Standard_LRS物件。</span><span class="sxs-lookup"><span data-stu-id="5e7f8-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="5e7f8-110">它也設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="5e7f8-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="5e7f8-111">第二個和第三個命令會設定磁片物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="5e7f8-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="5e7f8-112">最後一個命令會取用磁片物件，在資源群組 'ResourceGroup01' 中建立名稱為 'Disk01' 的磁片。</span><span class="sxs-lookup"><span data-stu-id="5e7f8-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5e7f8-113">參數</span><span class="sxs-lookup"><span data-stu-id="5e7f8-113">PARAMETERS</span></span>

### <span data-ttu-id="5e7f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e7f8-114">-DefaultProfile</span></span>
<span data-ttu-id="5e7f8-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e7f8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e7f8-116">-磁片</span><span class="sxs-lookup"><span data-stu-id="5e7f8-116">-Disk</span></span>
<span data-ttu-id="5e7f8-117">指定一個本地磁片物件。</span><span class="sxs-lookup"><span data-stu-id="5e7f8-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e7f8-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="5e7f8-118">-KeyUrl</span></span>
<span data-ttu-id="5e7f8-119">指定金鑰 URL。</span><span class="sxs-lookup"><span data-stu-id="5e7f8-119">Specifies the key Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e7f8-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="5e7f8-120">-SourceVaultId</span></span>
<span data-ttu-id="5e7f8-121">指定來源庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e7f8-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e7f8-122">-確認</span><span class="sxs-lookup"><span data-stu-id="5e7f8-122">-Confirm</span></span>
<span data-ttu-id="5e7f8-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5e7f8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e7f8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e7f8-124">-WhatIf</span></span>
<span data-ttu-id="5e7f8-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5e7f8-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e7f8-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5e7f8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e7f8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e7f8-127">CommonParameters</span></span>
<span data-ttu-id="5e7f8-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5e7f8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e7f8-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e7f8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e7f8-130">輸入</span><span class="sxs-lookup"><span data-stu-id="5e7f8-130">INPUTS</span></span>

### <span data-ttu-id="5e7f8-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="5e7f8-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="5e7f8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5e7f8-132">System.String</span></span>

## <span data-ttu-id="5e7f8-133">輸出</span><span class="sxs-lookup"><span data-stu-id="5e7f8-133">OUTPUTS</span></span>

### <span data-ttu-id="5e7f8-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="5e7f8-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="5e7f8-135">筆記</span><span class="sxs-lookup"><span data-stu-id="5e7f8-135">NOTES</span></span>

## <span data-ttu-id="5e7f8-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e7f8-136">RELATED LINKS</span></span>
