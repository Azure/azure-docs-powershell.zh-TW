---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azsnapshotupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
ms.openlocfilehash: b87dbef98f336d1171da4b33d4ced1cc86e04fdc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903834"
---
# <span data-ttu-id="0a49a-101">Set-AzSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0a49a-101">Set-AzSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="0a49a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0a49a-102">SYNOPSIS</span></span>
<span data-ttu-id="0a49a-103">設定快照更新物件上的金鑰加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="0a49a-103">Sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="0a49a-104">語法</span><span class="sxs-lookup"><span data-stu-id="0a49a-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a49a-105">描述</span><span class="sxs-lookup"><span data-stu-id="0a49a-105">DESCRIPTION</span></span>
<span data-ttu-id="0a49a-106">**Set-AzSnapshotUpdateKeyEncryptionKey** Cmdlet 會設定快照更新物件上的金鑰加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="0a49a-106">The **Set-AzSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="0a49a-107">例子</span><span class="sxs-lookup"><span data-stu-id="0a49a-107">EXAMPLES</span></span>

### <span data-ttu-id="0a49a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="0a49a-108">Example 1</span></span>
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

<span data-ttu-id="0a49a-109">第一個命令會以儲存帳戶類型建立大小為 10 GB 的Premium_LRS快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="0a49a-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="0a49a-110">它也設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="0a49a-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="0a49a-111">第二個和第三個命令會設定快照更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="0a49a-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="0a49a-112">最後一個命令會拍攝快照更新物件，並更新資源群組 "ResourceGroup01" 中名稱為 "Snapshot01" 的現有快照。</span><span class="sxs-lookup"><span data-stu-id="0a49a-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0a49a-113">參數</span><span class="sxs-lookup"><span data-stu-id="0a49a-113">PARAMETERS</span></span>

### <span data-ttu-id="0a49a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a49a-114">-DefaultProfile</span></span>
<span data-ttu-id="0a49a-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a49a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a49a-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="0a49a-116">-KeyUrl</span></span>
<span data-ttu-id="0a49a-117">指定金鑰 URL。</span><span class="sxs-lookup"><span data-stu-id="0a49a-117">Specifies the key Url.</span></span>

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

### <span data-ttu-id="0a49a-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="0a49a-118">-SnapshotUpdate</span></span>
<span data-ttu-id="0a49a-119">指定本地快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="0a49a-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="0a49a-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="0a49a-120">-SourceVaultId</span></span>
<span data-ttu-id="0a49a-121">指定來源庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a49a-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="0a49a-122">-確認</span><span class="sxs-lookup"><span data-stu-id="0a49a-122">-Confirm</span></span>
<span data-ttu-id="0a49a-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0a49a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a49a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a49a-124">-WhatIf</span></span>
<span data-ttu-id="0a49a-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a49a-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a49a-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a49a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a49a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a49a-127">CommonParameters</span></span>
<span data-ttu-id="0a49a-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0a49a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a49a-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a49a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a49a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="0a49a-130">INPUTS</span></span>

### <span data-ttu-id="0a49a-131">Microsoft.Azure.Commands.Compute.Automation.models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="0a49a-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="0a49a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="0a49a-132">System.String</span></span>

## <span data-ttu-id="0a49a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="0a49a-133">OUTPUTS</span></span>

### <span data-ttu-id="0a49a-134">Microsoft.Azure.Commands.Compute.Automation.models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="0a49a-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="0a49a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="0a49a-135">NOTES</span></span>

## <span data-ttu-id="0a49a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a49a-136">RELATED LINKS</span></span>
