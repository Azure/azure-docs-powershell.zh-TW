---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
ms.openlocfilehash: a7a52aaa97518fd239e35ea7cf8e4d60689d8888
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956912"
---
# <span data-ttu-id="cb107-101">Set-AzSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="cb107-101">Set-AzSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="cb107-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb107-102">SYNOPSIS</span></span>
<span data-ttu-id="cb107-103">在快照更新物件上設定金鑰加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="cb107-103">Sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="cb107-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb107-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb107-105">說明</span><span class="sxs-lookup"><span data-stu-id="cb107-105">DESCRIPTION</span></span>
<span data-ttu-id="cb107-106">**AzSnapshotUpdateKeyEncryptionKey** Cmdlet 會在快照更新物件上設定金鑰加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="cb107-106">The **Set-AzSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="cb107-107">示例</span><span class="sxs-lookup"><span data-stu-id="cb107-107">EXAMPLES</span></span>

### <span data-ttu-id="cb107-108">範例1</span><span class="sxs-lookup"><span data-stu-id="cb107-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="cb107-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機空白快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="cb107-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="cb107-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="cb107-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="cb107-111">第二個和第三個命令會設定快照更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="cb107-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="cb107-112">最後一個命令會採用快照更新物件，並更新資源群組 "ResourceGroup01" 中名稱為 "Snapshot01" 的現有快照。</span><span class="sxs-lookup"><span data-stu-id="cb107-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cb107-113">參數</span><span class="sxs-lookup"><span data-stu-id="cb107-113">PARAMETERS</span></span>

### <span data-ttu-id="cb107-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb107-114">-DefaultProfile</span></span>
<span data-ttu-id="cb107-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb107-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb107-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="cb107-116">-KeyUrl</span></span>
<span data-ttu-id="cb107-117">指定金鑰 Url。</span><span class="sxs-lookup"><span data-stu-id="cb107-117">Specifies the key Url.</span></span>

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

### <span data-ttu-id="cb107-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="cb107-118">-SnapshotUpdate</span></span>
<span data-ttu-id="cb107-119">指定本機快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="cb107-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb107-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="cb107-120">-SourceVaultId</span></span>
<span data-ttu-id="cb107-121">指定來源電子倉庫 ID。</span><span class="sxs-lookup"><span data-stu-id="cb107-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="cb107-122">-確認</span><span class="sxs-lookup"><span data-stu-id="cb107-122">-Confirm</span></span>
<span data-ttu-id="cb107-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb107-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb107-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb107-124">-WhatIf</span></span>
<span data-ttu-id="cb107-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb107-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb107-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb107-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb107-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb107-127">CommonParameters</span></span>
<span data-ttu-id="cb107-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb107-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb107-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cb107-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb107-130">輸入</span><span class="sxs-lookup"><span data-stu-id="cb107-130">INPUTS</span></span>

### <span data-ttu-id="cb107-131">PSSnapshotUpdate 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="cb107-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="cb107-132">System.object</span><span class="sxs-lookup"><span data-stu-id="cb107-132">System.String</span></span>

## <span data-ttu-id="cb107-133">輸出</span><span class="sxs-lookup"><span data-stu-id="cb107-133">OUTPUTS</span></span>

### <span data-ttu-id="cb107-134">PSSnapshotUpdate 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="cb107-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="cb107-135">筆記</span><span class="sxs-lookup"><span data-stu-id="cb107-135">NOTES</span></span>

## <span data-ttu-id="cb107-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb107-136">RELATED LINKS</span></span>
