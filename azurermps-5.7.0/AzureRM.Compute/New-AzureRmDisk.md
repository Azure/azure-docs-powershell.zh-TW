---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
ms.openlocfilehash: 04106c91e99372b985c0a10ac12a7944fdcb4e41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625917"
---
# <span data-ttu-id="f55bf-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="f55bf-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="f55bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f55bf-102">SYNOPSIS</span></span>
<span data-ttu-id="f55bf-103">建立受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="f55bf-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f55bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="f55bf-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <Disk> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f55bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="f55bf-105">DESCRIPTION</span></span>
<span data-ttu-id="f55bf-106">**新的-AzureRmDisk** Cmdlet 會建立受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="f55bf-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="f55bf-107">示例</span><span class="sxs-lookup"><span data-stu-id="f55bf-107">EXAMPLES</span></span>

### <span data-ttu-id="f55bf-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f55bf-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="f55bf-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，建立一個大小為5GB 的本機空白磁片物件。</span><span class="sxs-lookup"><span data-stu-id="f55bf-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="f55bf-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="f55bf-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="f55bf-111">第二個和第三個命令會設定磁片物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="f55bf-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="f55bf-112">最後一個命令會取得磁片物件，並在 [資源] 群組的 [ResourceGroup01] 中建立名為 "Disk01" 的磁片。</span><span class="sxs-lookup"><span data-stu-id="f55bf-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f55bf-113">參數</span><span class="sxs-lookup"><span data-stu-id="f55bf-113">PARAMETERS</span></span>

### <span data-ttu-id="f55bf-114">-磁片</span><span class="sxs-lookup"><span data-stu-id="f55bf-114">-Disk</span></span>
<span data-ttu-id="f55bf-115">指定本機磁片物件。</span><span class="sxs-lookup"><span data-stu-id="f55bf-115">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f55bf-116">-DiskName</span><span class="sxs-lookup"><span data-stu-id="f55bf-116">-DiskName</span></span>
<span data-ttu-id="f55bf-117">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="f55bf-117">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f55bf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f55bf-118">-ResourceGroupName</span></span>
<span data-ttu-id="f55bf-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f55bf-119">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f55bf-120">-確認</span><span class="sxs-lookup"><span data-stu-id="f55bf-120">-Confirm</span></span>
<span data-ttu-id="f55bf-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f55bf-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55bf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f55bf-122">-WhatIf</span></span>
<span data-ttu-id="f55bf-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f55bf-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f55bf-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f55bf-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55bf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55bf-125">CommonParameters</span></span>
<span data-ttu-id="f55bf-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f55bf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55bf-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f55bf-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55bf-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f55bf-128">INPUTS</span></span>

### <span data-ttu-id="f55bf-129">System.object</span><span class="sxs-lookup"><span data-stu-id="f55bf-129">System.String</span></span>
<span data-ttu-id="f55bf-130">[Azure. 管理]. 磁片</span><span class="sxs-lookup"><span data-stu-id="f55bf-130">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="f55bf-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f55bf-131">OUTPUTS</span></span>

### <span data-ttu-id="f55bf-132">System.object</span><span class="sxs-lookup"><span data-stu-id="f55bf-132">System.Object</span></span>

## <span data-ttu-id="f55bf-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f55bf-133">NOTES</span></span>

## <span data-ttu-id="f55bf-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f55bf-134">RELATED LINKS</span></span>

