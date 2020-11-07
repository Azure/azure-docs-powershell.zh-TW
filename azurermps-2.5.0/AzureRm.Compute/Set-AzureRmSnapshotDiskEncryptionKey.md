---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotdiskencryptionkey
schema: 2.0.0
ms.openlocfilehash: f78b680f5872301236c5d001ce9920d2edd61f02
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800169"
---
# <span data-ttu-id="62fcd-101">Set-AzureRmSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="62fcd-101">Set-AzureRmSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="62fcd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62fcd-102">SYNOPSIS</span></span>
<span data-ttu-id="62fcd-103">在快照物件上設定磁片加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="62fcd-103">Sets the disk encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62fcd-104">句法</span><span class="sxs-lookup"><span data-stu-id="62fcd-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotDiskEncryptionKey [-Snapshot] <PSSnapshot> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62fcd-105">說明</span><span class="sxs-lookup"><span data-stu-id="62fcd-105">DESCRIPTION</span></span>
<span data-ttu-id="62fcd-106">**AzureRmSnapshotDiskEncryptionKey** Cmdlet 會在快照物件上設定磁片加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="62fcd-106">The **Set-AzureRmSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="62fcd-107">示例</span><span class="sxs-lookup"><span data-stu-id="62fcd-107">EXAMPLES</span></span>

### <span data-ttu-id="62fcd-108">範例1</span><span class="sxs-lookup"><span data-stu-id="62fcd-108">Example 1</span></span>
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

<span data-ttu-id="62fcd-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，使用大小為5GB 來建立本機空快照物件。</span><span class="sxs-lookup"><span data-stu-id="62fcd-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="62fcd-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="62fcd-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="62fcd-111">第二個和第三個命令會設定快照物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="62fcd-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="62fcd-112">最後一個命令會採用快照物件，並會在資源群組 "ResourceGroup01" 中建立名為 "Snapshot01" 的快照。</span><span class="sxs-lookup"><span data-stu-id="62fcd-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="62fcd-113">參數</span><span class="sxs-lookup"><span data-stu-id="62fcd-113">PARAMETERS</span></span>

### <span data-ttu-id="62fcd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62fcd-114">-DefaultProfile</span></span>
<span data-ttu-id="62fcd-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62fcd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62fcd-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="62fcd-116">-SecretUrl</span></span>
<span data-ttu-id="62fcd-117">指定機密 Url。</span><span class="sxs-lookup"><span data-stu-id="62fcd-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="62fcd-118">-快照</span><span class="sxs-lookup"><span data-stu-id="62fcd-118">-Snapshot</span></span>
<span data-ttu-id="62fcd-119">指定本機快照物件。</span><span class="sxs-lookup"><span data-stu-id="62fcd-119">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62fcd-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="62fcd-120">-SourceVaultId</span></span>
<span data-ttu-id="62fcd-121">指定來源電子倉庫 ID。</span><span class="sxs-lookup"><span data-stu-id="62fcd-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="62fcd-122">-確認</span><span class="sxs-lookup"><span data-stu-id="62fcd-122">-Confirm</span></span>
<span data-ttu-id="62fcd-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="62fcd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62fcd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62fcd-124">-WhatIf</span></span>
<span data-ttu-id="62fcd-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62fcd-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62fcd-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62fcd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62fcd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62fcd-127">CommonParameters</span></span>
<span data-ttu-id="62fcd-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62fcd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62fcd-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62fcd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62fcd-130">輸入</span><span class="sxs-lookup"><span data-stu-id="62fcd-130">INPUTS</span></span>

### <span data-ttu-id="62fcd-131">[Azure. 管理]-[計算] 模型. 快照</span><span class="sxs-lookup"><span data-stu-id="62fcd-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="62fcd-132">System.object</span><span class="sxs-lookup"><span data-stu-id="62fcd-132">System.String</span></span>

## <span data-ttu-id="62fcd-133">輸出</span><span class="sxs-lookup"><span data-stu-id="62fcd-133">OUTPUTS</span></span>

### <span data-ttu-id="62fcd-134">[Azure. 管理]-[計算] 模型. 快照</span><span class="sxs-lookup"><span data-stu-id="62fcd-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="62fcd-135">筆記</span><span class="sxs-lookup"><span data-stu-id="62fcd-135">NOTES</span></span>

## <span data-ttu-id="62fcd-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="62fcd-136">RELATED LINKS</span></span>

