---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: ec146441e620580b5028dffa4e0f7f3e09c45b35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911157"
---
# <span data-ttu-id="0574f-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="0574f-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="0574f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0574f-102">SYNOPSIS</span></span>
<span data-ttu-id="0574f-103">移除磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="0574f-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="0574f-104">語法</span><span class="sxs-lookup"><span data-stu-id="0574f-104">SYNTAX</span></span>

### <span data-ttu-id="0574f-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="0574f-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0574f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="0574f-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0574f-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="0574f-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0574f-108">描述</span><span class="sxs-lookup"><span data-stu-id="0574f-108">DESCRIPTION</span></span>
<span data-ttu-id="0574f-109">移除磁片加密集。</span><span class="sxs-lookup"><span data-stu-id="0574f-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="0574f-110">例子</span><span class="sxs-lookup"><span data-stu-id="0574f-110">EXAMPLES</span></span>

### <span data-ttu-id="0574f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="0574f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="0574f-112">刪除 'rg1' 中的磁片加密集 'enc1'</span><span class="sxs-lookup"><span data-stu-id="0574f-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="0574f-113">參數</span><span class="sxs-lookup"><span data-stu-id="0574f-113">PARAMETERS</span></span>

### <span data-ttu-id="0574f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0574f-114">-AsJob</span></span>
<span data-ttu-id="0574f-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0574f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0574f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0574f-116">-DefaultProfile</span></span>
<span data-ttu-id="0574f-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0574f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0574f-118">-強制</span><span class="sxs-lookup"><span data-stu-id="0574f-118">-Force</span></span>
<span data-ttu-id="0574f-119">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="0574f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0574f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0574f-120">-InputObject</span></span>
<span data-ttu-id="0574f-121">磁片加密集的本機物件。</span><span class="sxs-lookup"><span data-stu-id="0574f-121">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="0574f-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="0574f-122">-Name</span></span>
<span data-ttu-id="0574f-123">磁片加密集的名稱。</span><span class="sxs-lookup"><span data-stu-id="0574f-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="0574f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0574f-124">-ResourceGroupName</span></span>
<span data-ttu-id="0574f-125">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0574f-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0574f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0574f-126">-ResourceId</span></span>
<span data-ttu-id="0574f-127">資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0574f-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="0574f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="0574f-128">-Confirm</span></span>
<span data-ttu-id="0574f-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0574f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0574f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0574f-130">-WhatIf</span></span>
<span data-ttu-id="0574f-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0574f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0574f-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0574f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0574f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0574f-133">CommonParameters</span></span>
<span data-ttu-id="0574f-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0574f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0574f-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0574f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0574f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="0574f-136">INPUTS</span></span>

### <span data-ttu-id="0574f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0574f-137">System.String</span></span>

### <span data-ttu-id="0574f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="0574f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="0574f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="0574f-139">OUTPUTS</span></span>

### <span data-ttu-id="0574f-140">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="0574f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="0574f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="0574f-141">NOTES</span></span>

## <span data-ttu-id="0574f-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="0574f-142">RELATED LINKS</span></span>
