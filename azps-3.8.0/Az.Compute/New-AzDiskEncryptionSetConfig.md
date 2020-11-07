---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: 5d38a1104d1f2d1f569560027c540a2c8605bdae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957409"
---
# <span data-ttu-id="1020c-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="1020c-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="1020c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1020c-102">SYNOPSIS</span></span>
<span data-ttu-id="1020c-103">建立可設定的磁片加密集物件。</span><span class="sxs-lookup"><span data-stu-id="1020c-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="1020c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1020c-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1020c-105">說明</span><span class="sxs-lookup"><span data-stu-id="1020c-105">DESCRIPTION</span></span>
<span data-ttu-id="1020c-106">建立可設定的磁片加密集物件。</span><span class="sxs-lookup"><span data-stu-id="1020c-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="1020c-107">示例</span><span class="sxs-lookup"><span data-stu-id="1020c-107">EXAMPLES</span></span>

### <span data-ttu-id="1020c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1020c-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="1020c-109">使用 [金鑰保存庫] 中指定的作用中金鑰來建立磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="1020c-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="1020c-110">參數</span><span class="sxs-lookup"><span data-stu-id="1020c-110">PARAMETERS</span></span>

### <span data-ttu-id="1020c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1020c-111">-DefaultProfile</span></span>
<span data-ttu-id="1020c-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1020c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1020c-113">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="1020c-113">-IdentityType</span></span>
<span data-ttu-id="1020c-114">DiskEncryptionSet 所使用的 Managed 身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="1020c-114">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="1020c-115">僅支援 SystemAssigned。</span><span class="sxs-lookup"><span data-stu-id="1020c-115">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="1020c-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="1020c-116">-KeyUrl</span></span>
<span data-ttu-id="1020c-117">指向 KeyVault 中作用中的索引鍵的 Url</span><span class="sxs-lookup"><span data-stu-id="1020c-117">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="1020c-118">-位置</span><span class="sxs-lookup"><span data-stu-id="1020c-118">-Location</span></span>
<span data-ttu-id="1020c-119">指定位置。</span><span class="sxs-lookup"><span data-stu-id="1020c-119">Specifies a location.</span></span>

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

### <span data-ttu-id="1020c-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="1020c-120">-SourceVaultId</span></span>
<span data-ttu-id="1020c-121">包含作用中金鑰之 KeyVault 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1020c-121">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="1020c-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="1020c-122">-Tag</span></span>
<span data-ttu-id="1020c-123">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="1020c-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1020c-124">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1020c-124">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1020c-125">-確認</span><span class="sxs-lookup"><span data-stu-id="1020c-125">-Confirm</span></span>
<span data-ttu-id="1020c-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1020c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1020c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1020c-127">-WhatIf</span></span>
<span data-ttu-id="1020c-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1020c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1020c-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1020c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1020c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1020c-130">CommonParameters</span></span>
<span data-ttu-id="1020c-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1020c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1020c-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1020c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1020c-133">輸入</span><span class="sxs-lookup"><span data-stu-id="1020c-133">INPUTS</span></span>

### <span data-ttu-id="1020c-134">System.object</span><span class="sxs-lookup"><span data-stu-id="1020c-134">System.String</span></span>

### <span data-ttu-id="1020c-135">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1020c-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1020c-136">輸出</span><span class="sxs-lookup"><span data-stu-id="1020c-136">OUTPUTS</span></span>

### <span data-ttu-id="1020c-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1020c-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="1020c-138">筆記</span><span class="sxs-lookup"><span data-stu-id="1020c-138">NOTES</span></span>

## <span data-ttu-id="1020c-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="1020c-139">RELATED LINKS</span></span>
