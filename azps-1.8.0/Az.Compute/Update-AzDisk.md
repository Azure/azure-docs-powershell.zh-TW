---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
ms.openlocfilehash: bc3deca978895da5eb6c634d255f2c5ddb6a6fe4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788258"
---
# <span data-ttu-id="15216-101">Update-AzDisk</span><span class="sxs-lookup"><span data-stu-id="15216-101">Update-AzDisk</span></span>

## <span data-ttu-id="15216-102">摘要</span><span class="sxs-lookup"><span data-stu-id="15216-102">SYNOPSIS</span></span>
<span data-ttu-id="15216-103">更新磁片。</span><span class="sxs-lookup"><span data-stu-id="15216-103">Updates a disk.</span></span>

## <span data-ttu-id="15216-104">句法</span><span class="sxs-lookup"><span data-stu-id="15216-104">SYNTAX</span></span>

### <span data-ttu-id="15216-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="15216-105">DefaultParameter (Default)</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15216-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="15216-106">FriendMethod</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15216-107">說明</span><span class="sxs-lookup"><span data-stu-id="15216-107">DESCRIPTION</span></span>
<span data-ttu-id="15216-108">**更新-AzDisk** Cmdlet 會更新磁片。</span><span class="sxs-lookup"><span data-stu-id="15216-108">The **Update-AzDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="15216-109">示例</span><span class="sxs-lookup"><span data-stu-id="15216-109">EXAMPLES</span></span>

### <span data-ttu-id="15216-110">範例1</span><span class="sxs-lookup"><span data-stu-id="15216-110">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="15216-111">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機空白磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="15216-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="15216-112">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="15216-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="15216-113">第二個和第三個命令會設定磁片更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="15216-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="15216-114">最後一個命令會取得磁片更新物件，並更新資源群組 "ResourceGroup01" 中名為「Disk01」的現有磁片。</span><span class="sxs-lookup"><span data-stu-id="15216-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="15216-115">範例2</span><span class="sxs-lookup"><span data-stu-id="15216-115">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="15216-116">這個命令會將資源群組 ' ResourceGroup01 ' 中的名稱為 ' Disk01 ' 的現有磁片更新為 10 GB 磁片大小。</span><span class="sxs-lookup"><span data-stu-id="15216-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="15216-117">範例3</span><span class="sxs-lookup"><span data-stu-id="15216-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="15216-118">這些命令也會將資源群組 ' ResourceGroup01 ' 中的名為 ' Disk01 ' 的現有磁片更新為 10 GB 磁片大小。</span><span class="sxs-lookup"><span data-stu-id="15216-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="15216-119">參數</span><span class="sxs-lookup"><span data-stu-id="15216-119">PARAMETERS</span></span>

### <span data-ttu-id="15216-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15216-120">-AsJob</span></span>
<span data-ttu-id="15216-121">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="15216-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="15216-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15216-122">-DefaultProfile</span></span>
<span data-ttu-id="15216-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="15216-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15216-124">-磁片</span><span class="sxs-lookup"><span data-stu-id="15216-124">-Disk</span></span>
<span data-ttu-id="15216-125">指定本機磁片物件。</span><span class="sxs-lookup"><span data-stu-id="15216-125">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15216-126">-DiskName</span><span class="sxs-lookup"><span data-stu-id="15216-126">-DiskName</span></span>
<span data-ttu-id="15216-127">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="15216-127">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="15216-128">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="15216-128">-DiskUpdate</span></span>
<span data-ttu-id="15216-129">指定本機磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="15216-129">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15216-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15216-130">-ResourceGroupName</span></span>
<span data-ttu-id="15216-131">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="15216-131">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="15216-132">-確認</span><span class="sxs-lookup"><span data-stu-id="15216-132">-Confirm</span></span>
<span data-ttu-id="15216-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="15216-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15216-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15216-134">-WhatIf</span></span>
<span data-ttu-id="15216-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="15216-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15216-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="15216-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15216-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15216-137">CommonParameters</span></span>
<span data-ttu-id="15216-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="15216-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15216-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="15216-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15216-140">輸入</span><span class="sxs-lookup"><span data-stu-id="15216-140">INPUTS</span></span>

### <span data-ttu-id="15216-141">System.object</span><span class="sxs-lookup"><span data-stu-id="15216-141">System.String</span></span>

### <span data-ttu-id="15216-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="15216-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="15216-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="15216-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="15216-144">輸出</span><span class="sxs-lookup"><span data-stu-id="15216-144">OUTPUTS</span></span>

### <span data-ttu-id="15216-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="15216-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="15216-146">筆記</span><span class="sxs-lookup"><span data-stu-id="15216-146">NOTES</span></span>

## <span data-ttu-id="15216-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="15216-147">RELATED LINKS</span></span>
