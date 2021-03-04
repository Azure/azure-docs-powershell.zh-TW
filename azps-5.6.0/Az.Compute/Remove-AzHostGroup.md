---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: f05855c7fa677c384e9d8d0c5385d6014d80d312
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909749"
---
# <span data-ttu-id="1598d-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="1598d-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="1598d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1598d-102">SYNOPSIS</span></span>
<span data-ttu-id="1598d-103">移除主機群組。</span><span class="sxs-lookup"><span data-stu-id="1598d-103">Removes a host group.</span></span>

## <span data-ttu-id="1598d-104">語法</span><span class="sxs-lookup"><span data-stu-id="1598d-104">SYNTAX</span></span>

### <span data-ttu-id="1598d-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="1598d-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1598d-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="1598d-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1598d-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="1598d-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1598d-108">描述</span><span class="sxs-lookup"><span data-stu-id="1598d-108">DESCRIPTION</span></span>
<span data-ttu-id="1598d-109">此 Cmdlet 會刪除主機群組</span><span class="sxs-lookup"><span data-stu-id="1598d-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="1598d-110">例子</span><span class="sxs-lookup"><span data-stu-id="1598d-110">EXAMPLES</span></span>

### <span data-ttu-id="1598d-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="1598d-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="1598d-112">此命令會獲得並移除所給予的主機群組。</span><span class="sxs-lookup"><span data-stu-id="1598d-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="1598d-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="1598d-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="1598d-114">此命令會移除所給予的主機群組。</span><span class="sxs-lookup"><span data-stu-id="1598d-114">This command removes the given host group.</span></span>

## <span data-ttu-id="1598d-115">參數</span><span class="sxs-lookup"><span data-stu-id="1598d-115">PARAMETERS</span></span>

### <span data-ttu-id="1598d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1598d-116">-AsJob</span></span>
<span data-ttu-id="1598d-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1598d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1598d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1598d-118">-DefaultProfile</span></span>
<span data-ttu-id="1598d-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1598d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1598d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1598d-120">-InputObject</span></span>
<span data-ttu-id="1598d-121">主機群組的本機物件。</span><span class="sxs-lookup"><span data-stu-id="1598d-121">The local object of the host group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup
Parameter Sets: ObjectParameter
Aliases: HostGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1598d-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="1598d-122">-Name</span></span>
<span data-ttu-id="1598d-123">主機組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1598d-123">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1598d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1598d-124">-ResourceGroupName</span></span>
<span data-ttu-id="1598d-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1598d-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="1598d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1598d-126">-ResourceId</span></span>
<span data-ttu-id="1598d-127">資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1598d-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="1598d-128">-確認</span><span class="sxs-lookup"><span data-stu-id="1598d-128">-Confirm</span></span>
<span data-ttu-id="1598d-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1598d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1598d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1598d-130">-WhatIf</span></span>
<span data-ttu-id="1598d-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1598d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1598d-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1598d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1598d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1598d-133">CommonParameters</span></span>
<span data-ttu-id="1598d-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1598d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1598d-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1598d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1598d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1598d-136">INPUTS</span></span>

### <span data-ttu-id="1598d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1598d-137">System.String</span></span>

### <span data-ttu-id="1598d-138">Microsoft.Azure.Commands.Compute.Automation.models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="1598d-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="1598d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="1598d-139">OUTPUTS</span></span>

### <span data-ttu-id="1598d-140">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="1598d-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="1598d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="1598d-141">NOTES</span></span>

## <span data-ttu-id="1598d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="1598d-142">RELATED LINKS</span></span>
