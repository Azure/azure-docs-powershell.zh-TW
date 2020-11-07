---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: fa77808eddc0e51fa76a0883980b34552589f4ef
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801793"
---
# <span data-ttu-id="9ff39-101">New-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="9ff39-101">New-AzureRmSnapshot</span></span>

## <span data-ttu-id="9ff39-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ff39-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff39-103">建立快照。</span><span class="sxs-lookup"><span data-stu-id="9ff39-103">Creates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ff39-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ff39-104">SYNTAX</span></span>

```
New-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ff39-105">說明</span><span class="sxs-lookup"><span data-stu-id="9ff39-105">DESCRIPTION</span></span>
<span data-ttu-id="9ff39-106">**新的-AzureRmSnapshot** Cmdlet 會建立快照。</span><span class="sxs-lookup"><span data-stu-id="9ff39-106">The **New-AzureRmSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="9ff39-107">示例</span><span class="sxs-lookup"><span data-stu-id="9ff39-107">EXAMPLES</span></span>

### <span data-ttu-id="9ff39-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9ff39-108">Example 1</span></span>
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

<span data-ttu-id="9ff39-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，使用大小為5GB 來建立本機空快照物件。</span><span class="sxs-lookup"><span data-stu-id="9ff39-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="9ff39-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="9ff39-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="9ff39-111">第二個和第三個命令會設定快照物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="9ff39-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="9ff39-112">最後一個命令會採用快照物件，並會在資源群組 "ResourceGroup01" 中建立名為 "Snapshot01" 的快照。</span><span class="sxs-lookup"><span data-stu-id="9ff39-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="9ff39-113">參數</span><span class="sxs-lookup"><span data-stu-id="9ff39-113">PARAMETERS</span></span>

### <span data-ttu-id="9ff39-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ff39-114">-AsJob</span></span>
<span data-ttu-id="9ff39-115">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="9ff39-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff39-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff39-116">-DefaultProfile</span></span>
<span data-ttu-id="9ff39-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ff39-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ff39-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ff39-118">-ResourceGroupName</span></span>
<span data-ttu-id="9ff39-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ff39-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9ff39-120">-快照</span><span class="sxs-lookup"><span data-stu-id="9ff39-120">-Snapshot</span></span>
<span data-ttu-id="9ff39-121">指定本機快照物件。</span><span class="sxs-lookup"><span data-stu-id="9ff39-121">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff39-122">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="9ff39-122">-SnapshotName</span></span>
<span data-ttu-id="9ff39-123">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ff39-123">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="9ff39-124">-確認</span><span class="sxs-lookup"><span data-stu-id="9ff39-124">-Confirm</span></span>
<span data-ttu-id="9ff39-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9ff39-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ff39-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ff39-126">-WhatIf</span></span>
<span data-ttu-id="9ff39-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9ff39-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ff39-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9ff39-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ff39-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff39-129">CommonParameters</span></span>
<span data-ttu-id="9ff39-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ff39-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff39-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9ff39-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff39-132">輸入</span><span class="sxs-lookup"><span data-stu-id="9ff39-132">INPUTS</span></span>

### <span data-ttu-id="9ff39-133">System.object</span><span class="sxs-lookup"><span data-stu-id="9ff39-133">System.String</span></span>
<span data-ttu-id="9ff39-134">PSSnapshot 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="9ff39-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="9ff39-135">輸出</span><span class="sxs-lookup"><span data-stu-id="9ff39-135">OUTPUTS</span></span>

### <span data-ttu-id="9ff39-136">PSSnapshot 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="9ff39-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="9ff39-137">System.object</span><span class="sxs-lookup"><span data-stu-id="9ff39-137">System.Object</span></span>

## <span data-ttu-id="9ff39-138">筆記</span><span class="sxs-lookup"><span data-stu-id="9ff39-138">NOTES</span></span>

## <span data-ttu-id="9ff39-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ff39-139">RELATED LINKS</span></span>

