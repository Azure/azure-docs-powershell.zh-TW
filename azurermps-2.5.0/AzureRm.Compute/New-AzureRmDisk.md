---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdisk
schema: 2.0.0
ms.openlocfilehash: 2cb1cad343f57f164529e3607c1ad0b1ec74df05
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800178"
---
# <span data-ttu-id="ae876-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="ae876-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="ae876-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae876-102">SYNOPSIS</span></span>
<span data-ttu-id="ae876-103">建立受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="ae876-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae876-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae876-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae876-105">說明</span><span class="sxs-lookup"><span data-stu-id="ae876-105">DESCRIPTION</span></span>
<span data-ttu-id="ae876-106">**新的-AzureRmDisk** Cmdlet 會建立受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="ae876-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="ae876-107">示例</span><span class="sxs-lookup"><span data-stu-id="ae876-107">EXAMPLES</span></span>

### <span data-ttu-id="ae876-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ae876-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="ae876-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，建立一個大小為5GB 的本機空白磁片物件。</span><span class="sxs-lookup"><span data-stu-id="ae876-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="ae876-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="ae876-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ae876-111">第二個和第三個命令會設定磁片物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="ae876-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="ae876-112">最後一個命令會取得磁片物件，並在 [資源] 群組的 [ResourceGroup01] 中建立名為 "Disk01" 的磁片。</span><span class="sxs-lookup"><span data-stu-id="ae876-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ae876-113">參數</span><span class="sxs-lookup"><span data-stu-id="ae876-113">PARAMETERS</span></span>

### <span data-ttu-id="ae876-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae876-114">-AsJob</span></span>
<span data-ttu-id="ae876-115">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="ae876-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ae876-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae876-116">-DefaultProfile</span></span>
<span data-ttu-id="ae876-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae876-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae876-118">-磁片</span><span class="sxs-lookup"><span data-stu-id="ae876-118">-Disk</span></span>
<span data-ttu-id="ae876-119">指定本機磁片物件。</span><span class="sxs-lookup"><span data-stu-id="ae876-119">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="ae876-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="ae876-120">-DiskName</span></span>
<span data-ttu-id="ae876-121">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae876-121">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="ae876-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae876-122">-ResourceGroupName</span></span>
<span data-ttu-id="ae876-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae876-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ae876-124">-確認</span><span class="sxs-lookup"><span data-stu-id="ae876-124">-Confirm</span></span>
<span data-ttu-id="ae876-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ae876-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae876-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae876-126">-WhatIf</span></span>
<span data-ttu-id="ae876-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae876-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae876-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae876-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae876-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae876-129">CommonParameters</span></span>
<span data-ttu-id="ae876-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae876-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae876-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ae876-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae876-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ae876-132">INPUTS</span></span>

### <span data-ttu-id="ae876-133">System.object</span><span class="sxs-lookup"><span data-stu-id="ae876-133">System.String</span></span>
<span data-ttu-id="ae876-134">[Azure. 管理]. 磁片</span><span class="sxs-lookup"><span data-stu-id="ae876-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="ae876-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ae876-135">OUTPUTS</span></span>

### <span data-ttu-id="ae876-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="ae876-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="ae876-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ae876-137">NOTES</span></span>

## <span data-ttu-id="ae876-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae876-138">RELATED LINKS</span></span>

