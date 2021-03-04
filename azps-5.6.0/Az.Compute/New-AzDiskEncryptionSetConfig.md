---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: 358481a4c8ba20e8c8aa6f2ed47ebaa13225b939
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903322"
---
# <span data-ttu-id="20bce-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="20bce-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="20bce-102">簡介</span><span class="sxs-lookup"><span data-stu-id="20bce-102">SYNOPSIS</span></span>
<span data-ttu-id="20bce-103">建立可設定磁片加密集物件。</span><span class="sxs-lookup"><span data-stu-id="20bce-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="20bce-104">語法</span><span class="sxs-lookup"><span data-stu-id="20bce-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20bce-105">描述</span><span class="sxs-lookup"><span data-stu-id="20bce-105">DESCRIPTION</span></span>
<span data-ttu-id="20bce-106">建立可設定磁片加密集物件。</span><span class="sxs-lookup"><span data-stu-id="20bce-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="20bce-107">例子</span><span class="sxs-lookup"><span data-stu-id="20bce-107">EXAMPLES</span></span>

### <span data-ttu-id="20bce-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="20bce-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="20bce-109">使用金鑰庫中的已使用金鑰建立磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="20bce-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="20bce-110">參數</span><span class="sxs-lookup"><span data-stu-id="20bce-110">PARAMETERS</span></span>

### <span data-ttu-id="20bce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20bce-111">-DefaultProfile</span></span>
<span data-ttu-id="20bce-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="20bce-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20bce-113">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="20bce-113">-EncryptionType</span></span>
<span data-ttu-id="20bce-114">請使用這個設定磁片加密集的加密類型。</span><span class="sxs-lookup"><span data-stu-id="20bce-114">Use this to set the encryption type of the disk encryption set.</span></span> <span data-ttu-id="20bce-115">可用的值為：'encryptionAtWithPlatformKey'，'EncryptionAtWithCustomerKey'。</span><span class="sxs-lookup"><span data-stu-id="20bce-115">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bce-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="20bce-116">-IdentityType</span></span>
<span data-ttu-id="20bce-117">DiskEncryptionSet 所使用的受管理身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="20bce-117">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="20bce-118">僅支援 SystemAssigned。</span><span class="sxs-lookup"><span data-stu-id="20bce-118">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="20bce-119">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="20bce-119">-KeyUrl</span></span>
<span data-ttu-id="20bce-120">指向 KeyVault 中使用中金鑰的 URL</span><span class="sxs-lookup"><span data-stu-id="20bce-120">Url pointing to the active key in KeyVault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bce-121">-位置</span><span class="sxs-lookup"><span data-stu-id="20bce-121">-Location</span></span>
<span data-ttu-id="20bce-122">指定位置。</span><span class="sxs-lookup"><span data-stu-id="20bce-122">Specifies a location.</span></span>

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

### <span data-ttu-id="20bce-123">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="20bce-123">-SourceVaultId</span></span>
<span data-ttu-id="20bce-124">包含使用中金鑰的 KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="20bce-124">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bce-125">-標記</span><span class="sxs-lookup"><span data-stu-id="20bce-125">-Tag</span></span>
<span data-ttu-id="20bce-126">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="20bce-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="20bce-127">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="20bce-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bce-128">-確認</span><span class="sxs-lookup"><span data-stu-id="20bce-128">-Confirm</span></span>
<span data-ttu-id="20bce-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="20bce-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20bce-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20bce-130">-WhatIf</span></span>
<span data-ttu-id="20bce-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="20bce-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20bce-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="20bce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20bce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20bce-133">CommonParameters</span></span>
<span data-ttu-id="20bce-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="20bce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20bce-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20bce-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20bce-136">輸入</span><span class="sxs-lookup"><span data-stu-id="20bce-136">INPUTS</span></span>

### <span data-ttu-id="20bce-137">System.String</span><span class="sxs-lookup"><span data-stu-id="20bce-137">System.String</span></span>

### <span data-ttu-id="20bce-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="20bce-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="20bce-139">輸出</span><span class="sxs-lookup"><span data-stu-id="20bce-139">OUTPUTS</span></span>

### <span data-ttu-id="20bce-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="20bce-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="20bce-141">筆記</span><span class="sxs-lookup"><span data-stu-id="20bce-141">NOTES</span></span>

## <span data-ttu-id="20bce-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="20bce-142">RELATED LINKS</span></span>
