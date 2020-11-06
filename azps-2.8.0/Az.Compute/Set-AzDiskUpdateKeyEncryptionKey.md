---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: 5a6ea0eede8c7e9f6311c5d951f8e19176f532c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613189"
---
# <span data-ttu-id="4f808-101">Set-AzDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="4f808-101">Set-AzDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="4f808-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f808-102">SYNOPSIS</span></span>
<span data-ttu-id="4f808-103">在磁片更新物件上設定金鑰加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="4f808-103">Sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="4f808-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f808-104">SYNTAX</span></span>

```
Set-AzDiskUpdateKeyEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f808-105">說明</span><span class="sxs-lookup"><span data-stu-id="4f808-105">DESCRIPTION</span></span>
<span data-ttu-id="4f808-106">**AzDiskUpdateKeyEncryptionKey** Cmdlet 會在磁片更新物件上設定金鑰加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="4f808-106">The **Set-AzDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="4f808-107">示例</span><span class="sxs-lookup"><span data-stu-id="4f808-107">EXAMPLES</span></span>

### <span data-ttu-id="4f808-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4f808-108">Example 1</span></span>
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

<span data-ttu-id="4f808-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機空白磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="4f808-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="4f808-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="4f808-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="4f808-111">第二個和第三個命令會設定磁片更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="4f808-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="4f808-112">最後一個命令會取得磁片更新物件，並更新資源群組 "ResourceGroup01" 中名為「Disk01」的現有磁片。</span><span class="sxs-lookup"><span data-stu-id="4f808-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4f808-113">參數</span><span class="sxs-lookup"><span data-stu-id="4f808-113">PARAMETERS</span></span>

### <span data-ttu-id="4f808-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f808-114">-DefaultProfile</span></span>
<span data-ttu-id="4f808-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f808-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f808-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="4f808-116">-DiskUpdate</span></span>
<span data-ttu-id="4f808-117">指定本機磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="4f808-117">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="4f808-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="4f808-118">-KeyUrl</span></span>
<span data-ttu-id="4f808-119">指定金鑰 Url。</span><span class="sxs-lookup"><span data-stu-id="4f808-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="4f808-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="4f808-120">-SourceVaultId</span></span>
<span data-ttu-id="4f808-121">指定來源電子倉庫 ID。</span><span class="sxs-lookup"><span data-stu-id="4f808-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="4f808-122">-確認</span><span class="sxs-lookup"><span data-stu-id="4f808-122">-Confirm</span></span>
<span data-ttu-id="4f808-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4f808-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f808-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f808-124">-WhatIf</span></span>
<span data-ttu-id="4f808-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4f808-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f808-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4f808-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f808-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f808-127">CommonParameters</span></span>
<span data-ttu-id="4f808-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f808-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f808-129">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4f808-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f808-130">輸入</span><span class="sxs-lookup"><span data-stu-id="4f808-130">INPUTS</span></span>

### <span data-ttu-id="4f808-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="4f808-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="4f808-132">System.object</span><span class="sxs-lookup"><span data-stu-id="4f808-132">System.String</span></span>

## <span data-ttu-id="4f808-133">輸出</span><span class="sxs-lookup"><span data-stu-id="4f808-133">OUTPUTS</span></span>

### <span data-ttu-id="4f808-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="4f808-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="4f808-135">筆記</span><span class="sxs-lookup"><span data-stu-id="4f808-135">NOTES</span></span>

## <span data-ttu-id="4f808-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f808-136">RELATED LINKS</span></span>
