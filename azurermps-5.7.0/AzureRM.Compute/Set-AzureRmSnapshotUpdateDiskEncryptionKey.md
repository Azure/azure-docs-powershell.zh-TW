---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: 52f6a58f74312b96d09f8dacd8b6ced23db5c26e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623478"
---
# <span data-ttu-id="71cf5-101">Set-AzureRmSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="71cf5-101">Set-AzureRmSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="71cf5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="71cf5-103">在快照更新物件上設定磁片加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="71cf5-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71cf5-104">句法</span><span class="sxs-lookup"><span data-stu-id="71cf5-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <SnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71cf5-105">說明</span><span class="sxs-lookup"><span data-stu-id="71cf5-105">DESCRIPTION</span></span>
<span data-ttu-id="71cf5-106">**AzureRmSnapshotUpdateDiskEncryptionKey** Cmdlet 會在快照更新物件上設定磁片加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="71cf5-106">The **Set-AzureRmSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="71cf5-107">示例</span><span class="sxs-lookup"><span data-stu-id="71cf5-107">EXAMPLES</span></span>

### <span data-ttu-id="71cf5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="71cf5-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="71cf5-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機空白快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="71cf5-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="71cf5-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="71cf5-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="71cf5-111">第二個和第三個命令會設定快照更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="71cf5-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="71cf5-112">最後一個命令會採用快照更新物件，並更新資源群組 "ResourceGroup01" 中名稱為 "Snapshot01" 的現有快照。</span><span class="sxs-lookup"><span data-stu-id="71cf5-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="71cf5-113">參數</span><span class="sxs-lookup"><span data-stu-id="71cf5-113">PARAMETERS</span></span>

### <span data-ttu-id="71cf5-114">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="71cf5-114">-SecretUrl</span></span>
<span data-ttu-id="71cf5-115">Specifes 機密 Url。</span><span class="sxs-lookup"><span data-stu-id="71cf5-115">Specifes the secret Url.</span></span>

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

### <span data-ttu-id="71cf5-116">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="71cf5-116">-SnapshotUpdate</span></span>
<span data-ttu-id="71cf5-117">指定本機快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="71cf5-117">Specifies a local snapshot update object.</span></span>

```yaml
Type: SnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71cf5-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="71cf5-118">-SourceVaultId</span></span>
<span data-ttu-id="71cf5-119">指定來源電子倉庫 ID。</span><span class="sxs-lookup"><span data-stu-id="71cf5-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="71cf5-120">-確認</span><span class="sxs-lookup"><span data-stu-id="71cf5-120">-Confirm</span></span>
<span data-ttu-id="71cf5-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="71cf5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71cf5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71cf5-122">-WhatIf</span></span>
<span data-ttu-id="71cf5-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71cf5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71cf5-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71cf5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71cf5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71cf5-125">CommonParameters</span></span>
<span data-ttu-id="71cf5-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71cf5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71cf5-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="71cf5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71cf5-128">輸入</span><span class="sxs-lookup"><span data-stu-id="71cf5-128">INPUTS</span></span>

### <span data-ttu-id="71cf5-129">SnapshotUpdate 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="71cf5-129">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="71cf5-130">System.object</span><span class="sxs-lookup"><span data-stu-id="71cf5-130">System.String</span></span>

## <span data-ttu-id="71cf5-131">輸出</span><span class="sxs-lookup"><span data-stu-id="71cf5-131">OUTPUTS</span></span>

### <span data-ttu-id="71cf5-132">SnapshotUpdate 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="71cf5-132">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="71cf5-133">筆記</span><span class="sxs-lookup"><span data-stu-id="71cf5-133">NOTES</span></span>

## <span data-ttu-id="71cf5-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="71cf5-134">RELATED LINKS</span></span>

