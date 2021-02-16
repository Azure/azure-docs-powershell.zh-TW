---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
ms.openlocfilehash: 8ef1bccc711b96eb4b06c0b1234a426f9752208d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141239"
---
# <span data-ttu-id="cad00-101">Set-AzDiskDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="cad00-101">Set-AzDiskDiskEncryptionKey</span></span>

## <span data-ttu-id="cad00-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cad00-102">SYNOPSIS</span></span>
<span data-ttu-id="cad00-103">在磁片物件上設定磁片加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="cad00-103">Sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="cad00-104">句法</span><span class="sxs-lookup"><span data-stu-id="cad00-104">SYNTAX</span></span>

```
Set-AzDiskDiskEncryptionKey [-Disk] <PSDisk> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cad00-105">說明</span><span class="sxs-lookup"><span data-stu-id="cad00-105">DESCRIPTION</span></span>
<span data-ttu-id="cad00-106">**AzDiskDiskEncryptionKey** Cmdlet 會在磁片物件上設定磁片加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="cad00-106">The **Set-AzDiskDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="cad00-107">示例</span><span class="sxs-lookup"><span data-stu-id="cad00-107">EXAMPLES</span></span>

### <span data-ttu-id="cad00-108">範例1</span><span class="sxs-lookup"><span data-stu-id="cad00-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettingsVersion = '1.1'; 
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="cad00-109">第一個命令會在 Standard_LRS 儲存帳戶類型中，建立一個大小為5GB 的本機空白磁片物件。</span><span class="sxs-lookup"><span data-stu-id="cad00-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="cad00-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="cad00-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="cad00-111">第二個和第三個命令會設定磁片物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="cad00-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="cad00-112">最後一個命令會取得磁片物件，並在 [資源] 群組的 [ResourceGroup01] 中建立名為 "Disk01" 的磁片。</span><span class="sxs-lookup"><span data-stu-id="cad00-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cad00-113">參數</span><span class="sxs-lookup"><span data-stu-id="cad00-113">PARAMETERS</span></span>

### <span data-ttu-id="cad00-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cad00-114">-DefaultProfile</span></span>
<span data-ttu-id="cad00-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cad00-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cad00-116">-磁片</span><span class="sxs-lookup"><span data-stu-id="cad00-116">-Disk</span></span>
<span data-ttu-id="cad00-117">指定本機磁片物件。</span><span class="sxs-lookup"><span data-stu-id="cad00-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cad00-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="cad00-118">-SecretUrl</span></span>
<span data-ttu-id="cad00-119">指定機密 Url。</span><span class="sxs-lookup"><span data-stu-id="cad00-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="cad00-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="cad00-120">-SourceVaultId</span></span>
<span data-ttu-id="cad00-121">指定來源電子倉庫 ID。</span><span class="sxs-lookup"><span data-stu-id="cad00-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="cad00-122">-確認</span><span class="sxs-lookup"><span data-stu-id="cad00-122">-Confirm</span></span>
<span data-ttu-id="cad00-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cad00-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cad00-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cad00-124">-WhatIf</span></span>
<span data-ttu-id="cad00-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cad00-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cad00-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cad00-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cad00-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cad00-127">CommonParameters</span></span>
<span data-ttu-id="cad00-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cad00-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cad00-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cad00-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cad00-130">輸入</span><span class="sxs-lookup"><span data-stu-id="cad00-130">INPUTS</span></span>

### <span data-ttu-id="cad00-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="cad00-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="cad00-132">System.object</span><span class="sxs-lookup"><span data-stu-id="cad00-132">System.String</span></span>

## <span data-ttu-id="cad00-133">輸出</span><span class="sxs-lookup"><span data-stu-id="cad00-133">OUTPUTS</span></span>

### <span data-ttu-id="cad00-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="cad00-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="cad00-135">筆記</span><span class="sxs-lookup"><span data-stu-id="cad00-135">NOTES</span></span>

## <span data-ttu-id="cad00-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="cad00-136">RELATED LINKS</span></span>
