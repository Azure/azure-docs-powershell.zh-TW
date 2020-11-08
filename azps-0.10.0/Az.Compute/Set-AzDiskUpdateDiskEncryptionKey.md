---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 0f55058bc3419805bf7270e4d03c75db2208669e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795945"
---
# <span data-ttu-id="90a8f-101">Set-AzDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="90a8f-101">Set-AzDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="90a8f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="90a8f-103">在磁片更新物件上設定磁片加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="90a8f-103">Sets the disk encryption key properties on on a disk update object.</span></span>

## <span data-ttu-id="90a8f-104">句法</span><span class="sxs-lookup"><span data-stu-id="90a8f-104">SYNTAX</span></span>

```
Set-AzDiskUpdateDiskEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90a8f-105">說明</span><span class="sxs-lookup"><span data-stu-id="90a8f-105">DESCRIPTION</span></span>
<span data-ttu-id="90a8f-106">**AzDiskUpdateDiskEncryptionKey** Cmdlet 會在磁片更新物件上設定磁片加密金鑰屬性。</span><span class="sxs-lookup"><span data-stu-id="90a8f-106">The **Set-AzDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on on a disk update object.</span></span>

## <span data-ttu-id="90a8f-107">示例</span><span class="sxs-lookup"><span data-stu-id="90a8f-107">EXAMPLES</span></span>

### <span data-ttu-id="90a8f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="90a8f-108">Example 1</span></span>
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

<span data-ttu-id="90a8f-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機空白磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="90a8f-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="90a8f-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="90a8f-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="90a8f-111">第二個和第三個命令會設定磁片更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="90a8f-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="90a8f-112">最後一個命令會取得磁片更新物件，並更新資源群組 "ResourceGroup01" 中名為「Disk01」的現有磁片。</span><span class="sxs-lookup"><span data-stu-id="90a8f-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="90a8f-113">參數</span><span class="sxs-lookup"><span data-stu-id="90a8f-113">PARAMETERS</span></span>

### <span data-ttu-id="90a8f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a8f-114">-DefaultProfile</span></span>
<span data-ttu-id="90a8f-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90a8f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90a8f-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="90a8f-116">-DiskUpdate</span></span>
<span data-ttu-id="90a8f-117">指定本機磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="90a8f-117">Specifies a local disk update object.</span></span>

```yaml
Type: PSDiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90a8f-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="90a8f-118">-SecretUrl</span></span>
<span data-ttu-id="90a8f-119">指定機密 Url。</span><span class="sxs-lookup"><span data-stu-id="90a8f-119">Specifies the secret Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90a8f-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="90a8f-120">-SourceVaultId</span></span>
<span data-ttu-id="90a8f-121">指定來源電子倉庫 ID。</span><span class="sxs-lookup"><span data-stu-id="90a8f-121">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90a8f-122">-確認</span><span class="sxs-lookup"><span data-stu-id="90a8f-122">-Confirm</span></span>
<span data-ttu-id="90a8f-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="90a8f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90a8f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90a8f-124">-WhatIf</span></span>
<span data-ttu-id="90a8f-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90a8f-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90a8f-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90a8f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90a8f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a8f-127">CommonParameters</span></span>
<span data-ttu-id="90a8f-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90a8f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a8f-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="90a8f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a8f-130">輸入</span><span class="sxs-lookup"><span data-stu-id="90a8f-130">INPUTS</span></span>

### <span data-ttu-id="90a8f-131">DiskUpdate 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="90a8f-131">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="90a8f-132">System.object</span><span class="sxs-lookup"><span data-stu-id="90a8f-132">System.String</span></span>

## <span data-ttu-id="90a8f-133">輸出</span><span class="sxs-lookup"><span data-stu-id="90a8f-133">OUTPUTS</span></span>

### <span data-ttu-id="90a8f-134">DiskUpdate 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="90a8f-134">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="90a8f-135">筆記</span><span class="sxs-lookup"><span data-stu-id="90a8f-135">NOTES</span></span>

## <span data-ttu-id="90a8f-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="90a8f-136">RELATED LINKS</span></span>
