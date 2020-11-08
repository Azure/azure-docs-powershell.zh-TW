---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
ms.openlocfilehash: 5812bdf70a7661603aad60ece9577926ef10ffb6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795930"
---
# <span data-ttu-id="aeb75-101">Set-AzSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="aeb75-101">Set-AzSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="aeb75-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aeb75-102">SYNOPSIS</span></span>
<span data-ttu-id="aeb75-103">在快照物件上設定金鑰加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="aeb75-103">Sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="aeb75-104">句法</span><span class="sxs-lookup"><span data-stu-id="aeb75-104">SYNTAX</span></span>

```
Set-AzSnapshotKeyEncryptionKey [-Snapshot] <PSSnapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aeb75-105">說明</span><span class="sxs-lookup"><span data-stu-id="aeb75-105">DESCRIPTION</span></span>
<span data-ttu-id="aeb75-106">**AzSnapshotKeyEncryptionKey** Cmdlet 會設定快照物件上的金鑰加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="aeb75-106">The **Set-AzSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="aeb75-107">示例</span><span class="sxs-lookup"><span data-stu-id="aeb75-107">EXAMPLES</span></span>

### <span data-ttu-id="aeb75-108">範例1</span><span class="sxs-lookup"><span data-stu-id="aeb75-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="aeb75-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，使用大小為5GB 來建立本機空快照物件。</span><span class="sxs-lookup"><span data-stu-id="aeb75-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="aeb75-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="aeb75-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="aeb75-111">第二個和第三個命令會設定快照物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="aeb75-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="aeb75-112">最後一個命令會採用快照物件，並會在資源群組 "ResourceGroup01" 中建立名為 "Snapshot01" 的快照。</span><span class="sxs-lookup"><span data-stu-id="aeb75-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="aeb75-113">參數</span><span class="sxs-lookup"><span data-stu-id="aeb75-113">PARAMETERS</span></span>

### <span data-ttu-id="aeb75-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeb75-114">-DefaultProfile</span></span>
<span data-ttu-id="aeb75-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aeb75-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aeb75-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="aeb75-116">-KeyUrl</span></span>
<span data-ttu-id="aeb75-117">Specifes [金鑰 Url]。</span><span class="sxs-lookup"><span data-stu-id="aeb75-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="aeb75-118">-快照</span><span class="sxs-lookup"><span data-stu-id="aeb75-118">-Snapshot</span></span>
<span data-ttu-id="aeb75-119">指定本機快照物件。</span><span class="sxs-lookup"><span data-stu-id="aeb75-119">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="aeb75-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="aeb75-120">-SourceVaultId</span></span>
<span data-ttu-id="aeb75-121">指定來源電子倉庫 ID。</span><span class="sxs-lookup"><span data-stu-id="aeb75-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="aeb75-122">-確認</span><span class="sxs-lookup"><span data-stu-id="aeb75-122">-Confirm</span></span>
<span data-ttu-id="aeb75-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aeb75-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeb75-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeb75-124">-WhatIf</span></span>
<span data-ttu-id="aeb75-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aeb75-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aeb75-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aeb75-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeb75-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeb75-127">CommonParameters</span></span>
<span data-ttu-id="aeb75-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aeb75-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeb75-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aeb75-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeb75-130">輸入</span><span class="sxs-lookup"><span data-stu-id="aeb75-130">INPUTS</span></span>

### <span data-ttu-id="aeb75-131">[Azure. 管理]-[計算] 模型. 快照</span><span class="sxs-lookup"><span data-stu-id="aeb75-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="aeb75-132">System.object</span><span class="sxs-lookup"><span data-stu-id="aeb75-132">System.String</span></span>

## <span data-ttu-id="aeb75-133">輸出</span><span class="sxs-lookup"><span data-stu-id="aeb75-133">OUTPUTS</span></span>

### <span data-ttu-id="aeb75-134">[Azure. 管理]-[計算] 模型. 快照</span><span class="sxs-lookup"><span data-stu-id="aeb75-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="aeb75-135">筆記</span><span class="sxs-lookup"><span data-stu-id="aeb75-135">NOTES</span></span>

## <span data-ttu-id="aeb75-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="aeb75-136">RELATED LINKS</span></span>
