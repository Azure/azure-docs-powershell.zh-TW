---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
ms.openlocfilehash: 30a6ac1a3d74423302cc8b39e8b494e2f1ee2e22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623474"
---
# <span data-ttu-id="ad71a-101">Update-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="ad71a-101">Update-AzureRmDisk</span></span>

## <span data-ttu-id="ad71a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad71a-102">SYNOPSIS</span></span>
<span data-ttu-id="ad71a-103">更新磁片。</span><span class="sxs-lookup"><span data-stu-id="ad71a-103">Updates a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad71a-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad71a-104">SYNTAX</span></span>

### <span data-ttu-id="ad71a-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="ad71a-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <DiskUpdate> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad71a-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="ad71a-106">FriendMethod</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <Disk> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad71a-107">說明</span><span class="sxs-lookup"><span data-stu-id="ad71a-107">DESCRIPTION</span></span>
<span data-ttu-id="ad71a-108">**更新-AzureRmDisk** Cmdlet 會更新磁片。</span><span class="sxs-lookup"><span data-stu-id="ad71a-108">The **Update-AzureRmDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="ad71a-109">示例</span><span class="sxs-lookup"><span data-stu-id="ad71a-109">EXAMPLES</span></span>

### <span data-ttu-id="ad71a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="ad71a-110">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="ad71a-111">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機空白磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="ad71a-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="ad71a-112">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="ad71a-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ad71a-113">第二個和第三個命令會設定磁片更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="ad71a-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="ad71a-114">最後一個命令會取得磁片更新物件，並更新資源群組 "ResourceGroup01" 中名為「Disk01」的現有磁片。</span><span class="sxs-lookup"><span data-stu-id="ad71a-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ad71a-115">範例2</span><span class="sxs-lookup"><span data-stu-id="ad71a-115">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="ad71a-116">這個命令會將資源群組 ' ResourceGroup01 ' 中的名稱為 ' Disk01 ' 的現有磁片更新為 10 GB 磁片大小。</span><span class="sxs-lookup"><span data-stu-id="ad71a-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="ad71a-117">範例3</span><span class="sxs-lookup"><span data-stu-id="ad71a-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="ad71a-118">這些命令也會將資源群組 ' ResourceGroup01 ' 中的名為 ' Disk01 ' 的現有磁片更新為 10 GB 磁片大小。</span><span class="sxs-lookup"><span data-stu-id="ad71a-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="ad71a-119">參數</span><span class="sxs-lookup"><span data-stu-id="ad71a-119">PARAMETERS</span></span>

### <span data-ttu-id="ad71a-120">-磁片</span><span class="sxs-lookup"><span data-stu-id="ad71a-120">-Disk</span></span>
<span data-ttu-id="ad71a-121">指定本機磁片物件。</span><span class="sxs-lookup"><span data-stu-id="ad71a-121">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71a-122">-DiskName</span><span class="sxs-lookup"><span data-stu-id="ad71a-122">-DiskName</span></span>
<span data-ttu-id="ad71a-123">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad71a-123">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="ad71a-124">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="ad71a-124">-DiskUpdate</span></span>
<span data-ttu-id="ad71a-125">指定本機磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="ad71a-125">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad71a-126">-ResourceGroupName</span></span>
<span data-ttu-id="ad71a-127">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad71a-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ad71a-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ad71a-128">-Confirm</span></span>
<span data-ttu-id="ad71a-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ad71a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad71a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad71a-130">-WhatIf</span></span>
<span data-ttu-id="ad71a-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ad71a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad71a-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad71a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad71a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad71a-133">CommonParameters</span></span>
<span data-ttu-id="ad71a-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad71a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad71a-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ad71a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad71a-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ad71a-136">INPUTS</span></span>

### <span data-ttu-id="ad71a-137">System.object</span><span class="sxs-lookup"><span data-stu-id="ad71a-137">System.String</span></span>
<span data-ttu-id="ad71a-138">DiskUpdate-azure. 管理. 磁片上的 "計算模型"</span><span class="sxs-lookup"><span data-stu-id="ad71a-138">Microsoft.Azure.Management.Compute.Models.DiskUpdate Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="ad71a-139">輸出</span><span class="sxs-lookup"><span data-stu-id="ad71a-139">OUTPUTS</span></span>

### <span data-ttu-id="ad71a-140">System.object</span><span class="sxs-lookup"><span data-stu-id="ad71a-140">System.Object</span></span>

## <span data-ttu-id="ad71a-141">筆記</span><span class="sxs-lookup"><span data-stu-id="ad71a-141">NOTES</span></span>

## <span data-ttu-id="ad71a-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad71a-142">RELATED LINKS</span></span>

