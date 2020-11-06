---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshot.md
ms.openlocfilehash: 2b135efcd36a838bd4fa3c1a907fe7385e2b179c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449940"
---
# <span data-ttu-id="4a582-101">New-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="4a582-101">New-AzureRmSnapshot</span></span>

## <span data-ttu-id="4a582-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a582-102">SYNOPSIS</span></span>
<span data-ttu-id="4a582-103">建立快照。</span><span class="sxs-lookup"><span data-stu-id="4a582-103">Creates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a582-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a582-104">SYNTAX</span></span>

```
New-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <Snapshot> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a582-105">說明</span><span class="sxs-lookup"><span data-stu-id="4a582-105">DESCRIPTION</span></span>
<span data-ttu-id="4a582-106">**新的-AzureRmSnapshot** Cmdlet 會建立快照。</span><span class="sxs-lookup"><span data-stu-id="4a582-106">The **New-AzureRmSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="4a582-107">示例</span><span class="sxs-lookup"><span data-stu-id="4a582-107">EXAMPLES</span></span>

### <span data-ttu-id="4a582-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4a582-108">Example 1</span></span>
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

<span data-ttu-id="4a582-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，使用大小為5GB 來建立本機空快照物件。</span><span class="sxs-lookup"><span data-stu-id="4a582-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="4a582-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="4a582-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="4a582-111">第二個和第三個命令會設定快照物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="4a582-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="4a582-112">最後一個命令會採用快照物件，並會在資源群組 "ResourceGroup01" 中建立名為 "Snapshot01" 的快照。</span><span class="sxs-lookup"><span data-stu-id="4a582-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4a582-113">參數</span><span class="sxs-lookup"><span data-stu-id="4a582-113">PARAMETERS</span></span>

### <span data-ttu-id="4a582-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a582-114">-ResourceGroupName</span></span>
<span data-ttu-id="4a582-115">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a582-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4a582-116">-快照</span><span class="sxs-lookup"><span data-stu-id="4a582-116">-Snapshot</span></span>
<span data-ttu-id="4a582-117">指定本機快照物件。</span><span class="sxs-lookup"><span data-stu-id="4a582-117">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a582-118">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="4a582-118">-SnapshotName</span></span>
<span data-ttu-id="4a582-119">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a582-119">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="4a582-120">-確認</span><span class="sxs-lookup"><span data-stu-id="4a582-120">-Confirm</span></span>
<span data-ttu-id="4a582-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4a582-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a582-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a582-122">-WhatIf</span></span>
<span data-ttu-id="4a582-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4a582-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a582-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a582-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a582-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a582-125">CommonParameters</span></span>
<span data-ttu-id="4a582-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a582-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a582-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4a582-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a582-128">輸入</span><span class="sxs-lookup"><span data-stu-id="4a582-128">INPUTS</span></span>

### <span data-ttu-id="4a582-129">System.object</span><span class="sxs-lookup"><span data-stu-id="4a582-129">System.String</span></span>
<span data-ttu-id="4a582-130">[Azure. 管理]-[計算] 模型. 快照</span><span class="sxs-lookup"><span data-stu-id="4a582-130">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="4a582-131">輸出</span><span class="sxs-lookup"><span data-stu-id="4a582-131">OUTPUTS</span></span>

### <span data-ttu-id="4a582-132">System.object</span><span class="sxs-lookup"><span data-stu-id="4a582-132">System.Object</span></span>

## <span data-ttu-id="4a582-133">筆記</span><span class="sxs-lookup"><span data-stu-id="4a582-133">NOTES</span></span>

## <span data-ttu-id="4a582-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a582-134">RELATED LINKS</span></span>

