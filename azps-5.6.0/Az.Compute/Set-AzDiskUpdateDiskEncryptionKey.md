---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azdiskupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 06f0cf43e60bdf5e4172227937f786fed491f696
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917090"
---
# <span data-ttu-id="0b1b2-101">Set-AzDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0b1b2-101">Set-AzDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="0b1b2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0b1b2-102">SYNOPSIS</span></span>
<span data-ttu-id="0b1b2-103">設定磁片更新物件上的磁片加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-103">Sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="0b1b2-104">語法</span><span class="sxs-lookup"><span data-stu-id="0b1b2-104">SYNTAX</span></span>

```
Set-AzDiskUpdateDiskEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b1b2-105">描述</span><span class="sxs-lookup"><span data-stu-id="0b1b2-105">DESCRIPTION</span></span>
<span data-ttu-id="0b1b2-106">**Set-AzCryptUpdateCryptEncryptionKey** Cmdlet 會設定磁片更新物件上的磁片加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-106">The **Set-AzDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="0b1b2-107">例子</span><span class="sxs-lookup"><span data-stu-id="0b1b2-107">EXAMPLES</span></span>

### <span data-ttu-id="0b1b2-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="0b1b2-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="0b1b2-109">第一個命令會建立大小為 10 GB 的儲存空間帳戶類型的Premium_LRS磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="0b1b2-110">它也設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="0b1b2-111">第二個和第三個命令會設定磁片更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="0b1b2-112">最後一個命令會採用磁片更新物件，並更新資源群組 "ResourceGroup01" 中名稱為 "Disk01" 的現有磁片。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0b1b2-113">參數</span><span class="sxs-lookup"><span data-stu-id="0b1b2-113">PARAMETERS</span></span>

### <span data-ttu-id="0b1b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b1b2-114">-DefaultProfile</span></span>
<span data-ttu-id="0b1b2-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b1b2-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="0b1b2-116">-DiskUpdate</span></span>
<span data-ttu-id="0b1b2-117">指定一個本地磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b1b2-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="0b1b2-118">-SecretUrl</span></span>
<span data-ttu-id="0b1b2-119">指定機密 URL。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="0b1b2-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="0b1b2-120">-SourceVaultId</span></span>
<span data-ttu-id="0b1b2-121">指定來源庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="0b1b2-122">-確認</span><span class="sxs-lookup"><span data-stu-id="0b1b2-122">-Confirm</span></span>
<span data-ttu-id="0b1b2-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b1b2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b1b2-124">-WhatIf</span></span>
<span data-ttu-id="0b1b2-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b1b2-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b1b2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b1b2-127">CommonParameters</span></span>
<span data-ttu-id="0b1b2-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b1b2-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b1b2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b1b2-130">輸入</span><span class="sxs-lookup"><span data-stu-id="0b1b2-130">INPUTS</span></span>

### <span data-ttu-id="0b1b2-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="0b1b2-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="0b1b2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="0b1b2-132">System.String</span></span>

## <span data-ttu-id="0b1b2-133">輸出</span><span class="sxs-lookup"><span data-stu-id="0b1b2-133">OUTPUTS</span></span>

### <span data-ttu-id="0b1b2-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="0b1b2-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="0b1b2-135">筆記</span><span class="sxs-lookup"><span data-stu-id="0b1b2-135">NOTES</span></span>

## <span data-ttu-id="0b1b2-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b1b2-136">RELATED LINKS</span></span>
