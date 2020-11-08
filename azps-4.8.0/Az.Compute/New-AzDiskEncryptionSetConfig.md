---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: bfcb306b12c047c9207e0ef2f1d82bf6eaffc4d3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970586"
---
# <span data-ttu-id="d8cb1-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="d8cb1-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="d8cb1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="d8cb1-103">建立可設定的磁片加密集物件。</span><span class="sxs-lookup"><span data-stu-id="d8cb1-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="d8cb1-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8cb1-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8cb1-105">說明</span><span class="sxs-lookup"><span data-stu-id="d8cb1-105">DESCRIPTION</span></span>
<span data-ttu-id="d8cb1-106">建立可設定的磁片加密集物件。</span><span class="sxs-lookup"><span data-stu-id="d8cb1-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="d8cb1-107">示例</span><span class="sxs-lookup"><span data-stu-id="d8cb1-107">EXAMPLES</span></span>

### <span data-ttu-id="d8cb1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d8cb1-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="d8cb1-109">使用 [金鑰保存庫] 中指定的作用中金鑰來建立磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="d8cb1-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="d8cb1-110">參數</span><span class="sxs-lookup"><span data-stu-id="d8cb1-110">PARAMETERS</span></span>

### <span data-ttu-id="d8cb1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8cb1-111">-DefaultProfile</span></span>
<span data-ttu-id="d8cb1-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8cb1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8cb1-113">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="d8cb1-113">-EncryptionType</span></span>
<span data-ttu-id="d8cb1-114">使用此設定來設定磁片加密集的加密類型。</span><span class="sxs-lookup"><span data-stu-id="d8cb1-114">Use this to set the encryption type of the disk encryption set.</span></span> <span data-ttu-id="d8cb1-115">可用的值為： "EncryptionAtRestWithPlatformKey"、"EncryptionAtRestWithCustomerKey"。</span><span class="sxs-lookup"><span data-stu-id="d8cb1-115">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span></span>

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

### <span data-ttu-id="d8cb1-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d8cb1-116">-IdentityType</span></span>
<span data-ttu-id="d8cb1-117">DiskEncryptionSet 所使用的 Managed 身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="d8cb1-117">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="d8cb1-118">僅支援 SystemAssigned。</span><span class="sxs-lookup"><span data-stu-id="d8cb1-118">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="d8cb1-119">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="d8cb1-119">-KeyUrl</span></span>
<span data-ttu-id="d8cb1-120">指向 KeyVault 中作用中的索引鍵的 Url</span><span class="sxs-lookup"><span data-stu-id="d8cb1-120">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="d8cb1-121">-位置</span><span class="sxs-lookup"><span data-stu-id="d8cb1-121">-Location</span></span>
<span data-ttu-id="d8cb1-122">指定位置。</span><span class="sxs-lookup"><span data-stu-id="d8cb1-122">Specifies a location.</span></span>

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

### <span data-ttu-id="d8cb1-123">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="d8cb1-123">-SourceVaultId</span></span>
<span data-ttu-id="d8cb1-124">包含作用中金鑰之 KeyVault 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8cb1-124">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="d8cb1-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="d8cb1-125">-Tag</span></span>
<span data-ttu-id="d8cb1-126">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="d8cb1-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d8cb1-127">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d8cb1-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d8cb1-128">-確認</span><span class="sxs-lookup"><span data-stu-id="d8cb1-128">-Confirm</span></span>
<span data-ttu-id="d8cb1-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d8cb1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8cb1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8cb1-130">-WhatIf</span></span>
<span data-ttu-id="d8cb1-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d8cb1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8cb1-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d8cb1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8cb1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8cb1-133">CommonParameters</span></span>
<span data-ttu-id="d8cb1-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8cb1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8cb1-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d8cb1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8cb1-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d8cb1-136">INPUTS</span></span>

### <span data-ttu-id="d8cb1-137">System.object</span><span class="sxs-lookup"><span data-stu-id="d8cb1-137">System.String</span></span>

### <span data-ttu-id="d8cb1-138">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d8cb1-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d8cb1-139">輸出</span><span class="sxs-lookup"><span data-stu-id="d8cb1-139">OUTPUTS</span></span>

### <span data-ttu-id="d8cb1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d8cb1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="d8cb1-141">筆記</span><span class="sxs-lookup"><span data-stu-id="d8cb1-141">NOTES</span></span>

## <span data-ttu-id="d8cb1-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8cb1-142">RELATED LINKS</span></span>
