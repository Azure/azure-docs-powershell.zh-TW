---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 0e95179dcd2b1948b55526f3f2a8bfd5bb1a8834
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129341"
---
# <span data-ttu-id="2a53c-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="2a53c-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="2a53c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a53c-102">SYNOPSIS</span></span>
<span data-ttu-id="2a53c-103">更新磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="2a53c-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="2a53c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a53c-104">SYNTAX</span></span>

### <span data-ttu-id="2a53c-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="2a53c-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a53c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2a53c-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a53c-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="2a53c-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a53c-108">說明</span><span class="sxs-lookup"><span data-stu-id="2a53c-108">DESCRIPTION</span></span>
<span data-ttu-id="2a53c-109">更新磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="2a53c-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="2a53c-110">示例</span><span class="sxs-lookup"><span data-stu-id="2a53c-110">EXAMPLES</span></span>

### <span data-ttu-id="2a53c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2a53c-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="2a53c-112">使用 [金鑰保存庫] 中指定的作用中金鑰更新磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="2a53c-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="2a53c-113">參數</span><span class="sxs-lookup"><span data-stu-id="2a53c-113">PARAMETERS</span></span>

### <span data-ttu-id="2a53c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a53c-114">-AsJob</span></span>
<span data-ttu-id="2a53c-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2a53c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a53c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a53c-116">-DefaultProfile</span></span>
<span data-ttu-id="2a53c-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a53c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a53c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a53c-118">-InputObject</span></span>
<span data-ttu-id="2a53c-119">磁片加密集的本機物件。</span><span class="sxs-lookup"><span data-stu-id="2a53c-119">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="2a53c-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="2a53c-120">-KeyUrl</span></span>
<span data-ttu-id="2a53c-121">指向 KeyVault 中作用中的索引鍵的 Url</span><span class="sxs-lookup"><span data-stu-id="2a53c-121">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="2a53c-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a53c-122">-Name</span></span>
<span data-ttu-id="2a53c-123">磁片加密集的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a53c-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="2a53c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a53c-124">-ResourceGroupName</span></span>
<span data-ttu-id="2a53c-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a53c-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2a53c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a53c-126">-ResourceId</span></span>
<span data-ttu-id="2a53c-127">資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2a53c-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="2a53c-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="2a53c-128">-SourceVaultId</span></span>
<span data-ttu-id="2a53c-129">包含作用中金鑰之 KeyVault 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2a53c-129">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="2a53c-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="2a53c-130">-Tag</span></span>
<span data-ttu-id="2a53c-131">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="2a53c-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2a53c-132">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2a53c-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2a53c-133">-確認</span><span class="sxs-lookup"><span data-stu-id="2a53c-133">-Confirm</span></span>
<span data-ttu-id="2a53c-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2a53c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a53c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a53c-135">-WhatIf</span></span>
<span data-ttu-id="2a53c-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2a53c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a53c-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a53c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a53c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a53c-138">CommonParameters</span></span>
<span data-ttu-id="2a53c-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a53c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a53c-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2a53c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a53c-141">輸入</span><span class="sxs-lookup"><span data-stu-id="2a53c-141">INPUTS</span></span>

### <span data-ttu-id="2a53c-142">System.object</span><span class="sxs-lookup"><span data-stu-id="2a53c-142">System.String</span></span>

### <span data-ttu-id="2a53c-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="2a53c-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="2a53c-144">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2a53c-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2a53c-145">輸出</span><span class="sxs-lookup"><span data-stu-id="2a53c-145">OUTPUTS</span></span>

### <span data-ttu-id="2a53c-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="2a53c-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="2a53c-147">筆記</span><span class="sxs-lookup"><span data-stu-id="2a53c-147">NOTES</span></span>

## <span data-ttu-id="2a53c-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a53c-148">RELATED LINKS</span></span>
