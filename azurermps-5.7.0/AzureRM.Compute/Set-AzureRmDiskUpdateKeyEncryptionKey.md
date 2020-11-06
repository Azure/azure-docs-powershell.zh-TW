---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: 3e1667cb7a8e8bd078e03d2ddafab559ca7b143f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450652"
---
# <span data-ttu-id="bf8b8-101">Set-AzureRmDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="bf8b8-101">Set-AzureRmDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="bf8b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf8b8-102">SYNOPSIS</span></span>
<span data-ttu-id="bf8b8-103">在磁片更新物件上設定金鑰加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="bf8b8-103">Sets the key encryption key properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf8b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf8b8-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateKeyEncryptionKey [-DiskUpdate] <DiskUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf8b8-105">說明</span><span class="sxs-lookup"><span data-stu-id="bf8b8-105">DESCRIPTION</span></span>
<span data-ttu-id="bf8b8-106">**AzureRmDiskUpdateKeyEncryptionKey** Cmdlet 會在磁片更新物件上設定金鑰加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="bf8b8-106">The **Set-AzureRmDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="bf8b8-107">示例</span><span class="sxs-lookup"><span data-stu-id="bf8b8-107">EXAMPLES</span></span>

### <span data-ttu-id="bf8b8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bf8b8-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="bf8b8-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機空白磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="bf8b8-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="bf8b8-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="bf8b8-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="bf8b8-111">第二個和第三個命令會設定磁片更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="bf8b8-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="bf8b8-112">最後一個命令會取得磁片更新物件，並更新資源群組 "ResourceGroup01" 中名為「Disk01」的現有磁片。</span><span class="sxs-lookup"><span data-stu-id="bf8b8-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="bf8b8-113">參數</span><span class="sxs-lookup"><span data-stu-id="bf8b8-113">PARAMETERS</span></span>

### <span data-ttu-id="bf8b8-114">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="bf8b8-114">-DiskUpdate</span></span>
<span data-ttu-id="bf8b8-115">指定本機磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="bf8b8-115">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf8b8-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="bf8b8-116">-KeyUrl</span></span>
<span data-ttu-id="bf8b8-117">Specifes [金鑰 Url]。</span><span class="sxs-lookup"><span data-stu-id="bf8b8-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="bf8b8-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="bf8b8-118">-SourceVaultId</span></span>
<span data-ttu-id="bf8b8-119">指定來源電子倉庫 ID。</span><span class="sxs-lookup"><span data-stu-id="bf8b8-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="bf8b8-120">-確認</span><span class="sxs-lookup"><span data-stu-id="bf8b8-120">-Confirm</span></span>
<span data-ttu-id="bf8b8-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bf8b8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf8b8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf8b8-122">-WhatIf</span></span>
<span data-ttu-id="bf8b8-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bf8b8-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf8b8-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bf8b8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf8b8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf8b8-125">CommonParameters</span></span>
<span data-ttu-id="bf8b8-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf8b8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf8b8-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bf8b8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf8b8-128">輸入</span><span class="sxs-lookup"><span data-stu-id="bf8b8-128">INPUTS</span></span>

### <span data-ttu-id="bf8b8-129">DiskUpdate 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="bf8b8-129">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="bf8b8-130">System.object</span><span class="sxs-lookup"><span data-stu-id="bf8b8-130">System.String</span></span>

## <span data-ttu-id="bf8b8-131">輸出</span><span class="sxs-lookup"><span data-stu-id="bf8b8-131">OUTPUTS</span></span>

### <span data-ttu-id="bf8b8-132">DiskUpdate 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="bf8b8-132">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="bf8b8-133">筆記</span><span class="sxs-lookup"><span data-stu-id="bf8b8-133">NOTES</span></span>

## <span data-ttu-id="bf8b8-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf8b8-134">RELATED LINKS</span></span>
