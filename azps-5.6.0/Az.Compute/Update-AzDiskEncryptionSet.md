---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 2567d43220193e9233322fbf8715f7b7698890b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909741"
---
# <span data-ttu-id="5a23b-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="5a23b-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="5a23b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5a23b-102">SYNOPSIS</span></span>
<span data-ttu-id="5a23b-103">更新磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="5a23b-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="5a23b-104">語法</span><span class="sxs-lookup"><span data-stu-id="5a23b-104">SYNTAX</span></span>

### <span data-ttu-id="5a23b-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="5a23b-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a23b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="5a23b-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a23b-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="5a23b-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a23b-108">描述</span><span class="sxs-lookup"><span data-stu-id="5a23b-108">DESCRIPTION</span></span>
<span data-ttu-id="5a23b-109">更新磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="5a23b-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="5a23b-110">例子</span><span class="sxs-lookup"><span data-stu-id="5a23b-110">EXAMPLES</span></span>

### <span data-ttu-id="5a23b-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="5a23b-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="5a23b-112">使用金鑰庫中的已使用金鑰更新磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="5a23b-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="5a23b-113">參數</span><span class="sxs-lookup"><span data-stu-id="5a23b-113">PARAMETERS</span></span>

### <span data-ttu-id="5a23b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a23b-114">-AsJob</span></span>
<span data-ttu-id="5a23b-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5a23b-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a23b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a23b-116">-DefaultProfile</span></span>
<span data-ttu-id="5a23b-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a23b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a23b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a23b-118">-InputObject</span></span>
<span data-ttu-id="5a23b-119">磁片加密集的本機物件。</span><span class="sxs-lookup"><span data-stu-id="5a23b-119">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a23b-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="5a23b-120">-KeyUrl</span></span>
<span data-ttu-id="5a23b-121">指向 KeyVault 中使用中金鑰的 URL</span><span class="sxs-lookup"><span data-stu-id="5a23b-121">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="5a23b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a23b-122">-Name</span></span>
<span data-ttu-id="5a23b-123">磁片加密集的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a23b-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a23b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a23b-124">-ResourceGroupName</span></span>
<span data-ttu-id="5a23b-125">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a23b-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a23b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a23b-126">-ResourceId</span></span>
<span data-ttu-id="5a23b-127">資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a23b-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a23b-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="5a23b-128">-SourceVaultId</span></span>
<span data-ttu-id="5a23b-129">包含使用中金鑰的 KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a23b-129">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="5a23b-130">-標記</span><span class="sxs-lookup"><span data-stu-id="5a23b-130">-Tag</span></span>
<span data-ttu-id="5a23b-131">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="5a23b-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5a23b-132">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="5a23b-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5a23b-133">-確認</span><span class="sxs-lookup"><span data-stu-id="5a23b-133">-Confirm</span></span>
<span data-ttu-id="5a23b-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5a23b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a23b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a23b-135">-WhatIf</span></span>
<span data-ttu-id="5a23b-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a23b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a23b-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a23b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a23b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a23b-138">CommonParameters</span></span>
<span data-ttu-id="5a23b-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5a23b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a23b-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a23b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a23b-141">輸入</span><span class="sxs-lookup"><span data-stu-id="5a23b-141">INPUTS</span></span>

### <span data-ttu-id="5a23b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5a23b-142">System.String</span></span>

### <span data-ttu-id="5a23b-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="5a23b-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="5a23b-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5a23b-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5a23b-145">輸出</span><span class="sxs-lookup"><span data-stu-id="5a23b-145">OUTPUTS</span></span>

### <span data-ttu-id="5a23b-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="5a23b-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="5a23b-147">筆記</span><span class="sxs-lookup"><span data-stu-id="5a23b-147">NOTES</span></span>

## <span data-ttu-id="5a23b-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a23b-148">RELATED LINKS</span></span>
