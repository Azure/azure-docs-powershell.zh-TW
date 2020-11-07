---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDisk.md
ms.openlocfilehash: 1eea8504f974e7ffc504520a5b5abc036c4d3e2a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796161"
---
# <span data-ttu-id="ee8b4-101">New-AzDisk</span><span class="sxs-lookup"><span data-stu-id="ee8b4-101">New-AzDisk</span></span>

## <span data-ttu-id="ee8b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ee8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="ee8b4-103">建立受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="ee8b4-103">Creates a managed disk.</span></span>

## <span data-ttu-id="ee8b4-104">句法</span><span class="sxs-lookup"><span data-stu-id="ee8b4-104">SYNTAX</span></span>

```
New-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee8b4-105">說明</span><span class="sxs-lookup"><span data-stu-id="ee8b4-105">DESCRIPTION</span></span>
<span data-ttu-id="ee8b4-106">**新的-AzDisk** Cmdlet 會建立受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="ee8b4-106">The **New-AzDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="ee8b4-107">示例</span><span class="sxs-lookup"><span data-stu-id="ee8b4-107">EXAMPLES</span></span>

### <span data-ttu-id="ee8b4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ee8b4-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="ee8b4-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，建立一個大小為5GB 的本機空白磁片物件。</span><span class="sxs-lookup"><span data-stu-id="ee8b4-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="ee8b4-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="ee8b4-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ee8b4-111">第二個和第三個命令會設定磁片物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="ee8b4-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="ee8b4-112">最後一個命令會取得磁片物件，並在 [資源] 群組的 [ResourceGroup01] 中建立名為 "Disk01" 的磁片。</span><span class="sxs-lookup"><span data-stu-id="ee8b4-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ee8b4-113">參數</span><span class="sxs-lookup"><span data-stu-id="ee8b4-113">PARAMETERS</span></span>

### <span data-ttu-id="ee8b4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee8b4-114">-AsJob</span></span>
<span data-ttu-id="ee8b4-115">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="ee8b4-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ee8b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee8b4-116">-DefaultProfile</span></span>
<span data-ttu-id="ee8b4-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee8b4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee8b4-118">-磁片</span><span class="sxs-lookup"><span data-stu-id="ee8b4-118">-Disk</span></span>
<span data-ttu-id="ee8b4-119">指定本機磁片物件。</span><span class="sxs-lookup"><span data-stu-id="ee8b4-119">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee8b4-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="ee8b4-120">-DiskName</span></span>
<span data-ttu-id="ee8b4-121">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee8b4-121">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="ee8b4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee8b4-122">-ResourceGroupName</span></span>
<span data-ttu-id="ee8b4-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee8b4-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ee8b4-124">-確認</span><span class="sxs-lookup"><span data-stu-id="ee8b4-124">-Confirm</span></span>
<span data-ttu-id="ee8b4-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ee8b4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee8b4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee8b4-126">-WhatIf</span></span>
<span data-ttu-id="ee8b4-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ee8b4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee8b4-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee8b4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee8b4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee8b4-129">CommonParameters</span></span>
<span data-ttu-id="ee8b4-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ee8b4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee8b4-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ee8b4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee8b4-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ee8b4-132">INPUTS</span></span>

### <span data-ttu-id="ee8b4-133">System.object</span><span class="sxs-lookup"><span data-stu-id="ee8b4-133">System.String</span></span>
<span data-ttu-id="ee8b4-134">[Azure. 管理]. 磁片</span><span class="sxs-lookup"><span data-stu-id="ee8b4-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="ee8b4-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ee8b4-135">OUTPUTS</span></span>

### <span data-ttu-id="ee8b4-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="ee8b4-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="ee8b4-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ee8b4-137">NOTES</span></span>

## <span data-ttu-id="ee8b4-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee8b4-138">RELATED LINKS</span></span>

