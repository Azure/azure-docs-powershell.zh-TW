---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotKeyEncryptionKey.md
ms.openlocfilehash: 9c6debcae0aa83dd08374c7e390e3a42c4e5233a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444707"
---
# <span data-ttu-id="647e5-101">Set-AzureRmSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="647e5-101">Set-AzureRmSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="647e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="647e5-102">SYNOPSIS</span></span>
<span data-ttu-id="647e5-103">在快照物件上設定金鑰加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="647e5-103">Sets the key encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="647e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="647e5-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotKeyEncryptionKey [-Snapshot] <Snapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="647e5-105">說明</span><span class="sxs-lookup"><span data-stu-id="647e5-105">DESCRIPTION</span></span>
<span data-ttu-id="647e5-106">**AzureRmSnapshotKeyEncryptionKey** Cmdlet 會設定快照物件上的金鑰加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="647e5-106">The **Set-AzureRmSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="647e5-107">示例</span><span class="sxs-lookup"><span data-stu-id="647e5-107">EXAMPLES</span></span>

### <span data-ttu-id="647e5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="647e5-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="647e5-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，使用大小為5GB 來建立本機空快照物件。</span><span class="sxs-lookup"><span data-stu-id="647e5-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="647e5-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="647e5-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="647e5-111">第二個和第三個命令會設定快照物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="647e5-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="647e5-112">最後一個命令會採用快照物件，並會在資源群組 "ResourceGroup01" 中建立名為 "Snapshot01" 的快照。</span><span class="sxs-lookup"><span data-stu-id="647e5-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="647e5-113">參數</span><span class="sxs-lookup"><span data-stu-id="647e5-113">PARAMETERS</span></span>

### <span data-ttu-id="647e5-114">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="647e5-114">-KeyUrl</span></span>
<span data-ttu-id="647e5-115">Specifes [金鑰 Url]。</span><span class="sxs-lookup"><span data-stu-id="647e5-115">Specifes the key Url.</span></span>

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

### <span data-ttu-id="647e5-116">-快照</span><span class="sxs-lookup"><span data-stu-id="647e5-116">-Snapshot</span></span>
<span data-ttu-id="647e5-117">指定本機快照物件。</span><span class="sxs-lookup"><span data-stu-id="647e5-117">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="647e5-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="647e5-118">-SourceVaultId</span></span>
<span data-ttu-id="647e5-119">指定來源電子倉庫 ID。</span><span class="sxs-lookup"><span data-stu-id="647e5-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="647e5-120">-確認</span><span class="sxs-lookup"><span data-stu-id="647e5-120">-Confirm</span></span>
<span data-ttu-id="647e5-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="647e5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="647e5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="647e5-122">-WhatIf</span></span>
<span data-ttu-id="647e5-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="647e5-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="647e5-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="647e5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="647e5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="647e5-125">CommonParameters</span></span>
<span data-ttu-id="647e5-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="647e5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="647e5-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="647e5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="647e5-128">輸入</span><span class="sxs-lookup"><span data-stu-id="647e5-128">INPUTS</span></span>

### <span data-ttu-id="647e5-129">[Azure. 管理]-[計算] 模型. 快照</span><span class="sxs-lookup"><span data-stu-id="647e5-129">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="647e5-130">System.object</span><span class="sxs-lookup"><span data-stu-id="647e5-130">System.String</span></span>

## <span data-ttu-id="647e5-131">輸出</span><span class="sxs-lookup"><span data-stu-id="647e5-131">OUTPUTS</span></span>

### <span data-ttu-id="647e5-132">[Azure. 管理]-[計算] 模型. 快照</span><span class="sxs-lookup"><span data-stu-id="647e5-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="647e5-133">筆記</span><span class="sxs-lookup"><span data-stu-id="647e5-133">NOTES</span></span>

## <span data-ttu-id="647e5-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="647e5-134">RELATED LINKS</span></span>

