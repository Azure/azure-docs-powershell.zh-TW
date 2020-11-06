---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskDiskEncryptionKey.md
ms.openlocfilehash: e16b57c4fd674897192714c44620c6913838fc7e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450672"
---
# <span data-ttu-id="82ba4-101">Set-AzureRmDiskDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="82ba4-101">Set-AzureRmDiskDiskEncryptionKey</span></span>

## <span data-ttu-id="82ba4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="82ba4-103">在磁片物件上設定磁片加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="82ba4-103">Sets the disk encryption key properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82ba4-104">句法</span><span class="sxs-lookup"><span data-stu-id="82ba4-104">SYNTAX</span></span>

```
Set-AzureRmDiskDiskEncryptionKey [-Disk] <Disk> [[-SecretUrl] <String>] [[-SourceVaultId] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82ba4-105">說明</span><span class="sxs-lookup"><span data-stu-id="82ba4-105">DESCRIPTION</span></span>
<span data-ttu-id="82ba4-106">**AzureRmDiskDiskEncryptionKey** Cmdlet 會在磁片物件上設定磁片加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="82ba4-106">The **Set-AzureRmDiskDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="82ba4-107">示例</span><span class="sxs-lookup"><span data-stu-id="82ba4-107">EXAMPLES</span></span>

### <span data-ttu-id="82ba4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="82ba4-108">Example 1</span></span>
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

<span data-ttu-id="82ba4-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，建立一個大小為5GB 的本機空白磁片物件。</span><span class="sxs-lookup"><span data-stu-id="82ba4-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="82ba4-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="82ba4-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="82ba4-111">第二個和第三個命令會設定磁片物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="82ba4-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="82ba4-112">最後一個命令會取得磁片物件，並在 [資源] 群組的 [ResourceGroup01] 中建立名為 "Disk01" 的磁片。</span><span class="sxs-lookup"><span data-stu-id="82ba4-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="82ba4-113">參數</span><span class="sxs-lookup"><span data-stu-id="82ba4-113">PARAMETERS</span></span>

### <span data-ttu-id="82ba4-114">-磁片</span><span class="sxs-lookup"><span data-stu-id="82ba4-114">-Disk</span></span>
<span data-ttu-id="82ba4-115">指定本機磁片物件。</span><span class="sxs-lookup"><span data-stu-id="82ba4-115">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82ba4-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="82ba4-116">-SecretUrl</span></span>
<span data-ttu-id="82ba4-117">指定機密 Url。</span><span class="sxs-lookup"><span data-stu-id="82ba4-117">Specifies the secret Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ba4-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="82ba4-118">-SourceVaultId</span></span>
<span data-ttu-id="82ba4-119">指定來源電子倉庫 ID。</span><span class="sxs-lookup"><span data-stu-id="82ba4-119">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ba4-120">-確認</span><span class="sxs-lookup"><span data-stu-id="82ba4-120">-Confirm</span></span>
<span data-ttu-id="82ba4-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="82ba4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82ba4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82ba4-122">-WhatIf</span></span>
<span data-ttu-id="82ba4-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="82ba4-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82ba4-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82ba4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82ba4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ba4-125">CommonParameters</span></span>
<span data-ttu-id="82ba4-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82ba4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ba4-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="82ba4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ba4-128">輸入</span><span class="sxs-lookup"><span data-stu-id="82ba4-128">INPUTS</span></span>

### <span data-ttu-id="82ba4-129">[Azure. 管理]. 磁片</span><span class="sxs-lookup"><span data-stu-id="82ba4-129">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="82ba4-130">System.object</span><span class="sxs-lookup"><span data-stu-id="82ba4-130">System.String</span></span>

## <span data-ttu-id="82ba4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="82ba4-131">OUTPUTS</span></span>

### <span data-ttu-id="82ba4-132">[Azure. 管理]. 磁片</span><span class="sxs-lookup"><span data-stu-id="82ba4-132">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="82ba4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="82ba4-133">NOTES</span></span>

## <span data-ttu-id="82ba4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="82ba4-134">RELATED LINKS</span></span>
