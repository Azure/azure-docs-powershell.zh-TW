---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: 53b27c8144e0016962584baf40543dddf70b7bf3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906773"
---
# <span data-ttu-id="b3340-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="b3340-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="b3340-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b3340-102">SYNOPSIS</span></span>
<span data-ttu-id="b3340-103">更新快照。</span><span class="sxs-lookup"><span data-stu-id="b3340-103">Updates a snapshot.</span></span>

## <span data-ttu-id="b3340-104">語法</span><span class="sxs-lookup"><span data-stu-id="b3340-104">SYNTAX</span></span>

### <span data-ttu-id="b3340-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="b3340-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-SnapshotUpdate] <PSSnapshotUpdate>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3340-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b3340-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3340-107">描述</span><span class="sxs-lookup"><span data-stu-id="b3340-107">DESCRIPTION</span></span>
<span data-ttu-id="b3340-108">**Update-AzSnapshot** Cmdlet 會更新快照。</span><span class="sxs-lookup"><span data-stu-id="b3340-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="b3340-109">例子</span><span class="sxs-lookup"><span data-stu-id="b3340-109">EXAMPLES</span></span>

### <span data-ttu-id="b3340-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="b3340-110">Example 1</span></span>
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

<span data-ttu-id="b3340-111">第一個命令會以儲存帳戶類型建立大小為 10 GB 的Premium_LRS快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="b3340-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="b3340-112">它也設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="b3340-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="b3340-113">第二個和第三個命令會設定快照更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="b3340-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="b3340-114">最後一個命令會拍攝快照更新物件，並更新資源群組 "ResourceGroup01" 中名稱為 "Snapshot01" 的現有快照。</span><span class="sxs-lookup"><span data-stu-id="b3340-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b3340-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="b3340-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="b3340-116">此命令會更新資源群組中名稱為 "Snapshot01" 的現有快照，將磁片大小更新為 10 GB。</span><span class="sxs-lookup"><span data-stu-id="b3340-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="b3340-117">範例 3</span><span class="sxs-lookup"><span data-stu-id="b3340-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="b3340-118">這些命令也會將資源群組 "ResourceGroup01" 中名稱為 "Snapshot01" 的現有快照更新為 10 GB 磁片大小。</span><span class="sxs-lookup"><span data-stu-id="b3340-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="b3340-119">參數</span><span class="sxs-lookup"><span data-stu-id="b3340-119">PARAMETERS</span></span>

### <span data-ttu-id="b3340-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3340-120">-AsJob</span></span>
<span data-ttu-id="b3340-121">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="b3340-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3340-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3340-122">-DefaultProfile</span></span>
<span data-ttu-id="b3340-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3340-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3340-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3340-124">-ResourceGroupName</span></span>
<span data-ttu-id="b3340-125">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3340-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3340-126">-快照</span><span class="sxs-lookup"><span data-stu-id="b3340-126">-Snapshot</span></span>
<span data-ttu-id="b3340-127">指定本地快照物件。</span><span class="sxs-lookup"><span data-stu-id="b3340-127">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3340-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="b3340-128">-SnapshotName</span></span>
<span data-ttu-id="b3340-129">指定快照名稱。</span><span class="sxs-lookup"><span data-stu-id="b3340-129">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3340-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b3340-130">-SnapshotUpdate</span></span>
<span data-ttu-id="b3340-131">指定本地快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="b3340-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3340-132">-確認</span><span class="sxs-lookup"><span data-stu-id="b3340-132">-Confirm</span></span>
<span data-ttu-id="b3340-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b3340-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3340-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3340-134">-WhatIf</span></span>
<span data-ttu-id="b3340-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3340-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3340-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3340-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3340-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3340-137">CommonParameters</span></span>
<span data-ttu-id="b3340-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b3340-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3340-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3340-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3340-140">輸入</span><span class="sxs-lookup"><span data-stu-id="b3340-140">INPUTS</span></span>

### <span data-ttu-id="b3340-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b3340-141">System.String</span></span>

### <span data-ttu-id="b3340-142">Microsoft.Azure.Commands.Compute.Automation.models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b3340-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="b3340-143">Microsoft.Azure.Commands.Compute.Automation.models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="b3340-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="b3340-144">輸出</span><span class="sxs-lookup"><span data-stu-id="b3340-144">OUTPUTS</span></span>

### <span data-ttu-id="b3340-145">Microsoft.Azure.Commands.Compute.Automation.models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="b3340-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="b3340-146">筆記</span><span class="sxs-lookup"><span data-stu-id="b3340-146">NOTES</span></span>

## <span data-ttu-id="b3340-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3340-147">RELATED LINKS</span></span>
