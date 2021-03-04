---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: f8fc68c94142f9c215a6662e7bf41423c1b5de40
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912521"
---
# <span data-ttu-id="fa84c-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fa84c-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="fa84c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fa84c-102">SYNOPSIS</span></span>
<span data-ttu-id="fa84c-103">刪除 Synapse Analytics 工作區。</span><span class="sxs-lookup"><span data-stu-id="fa84c-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="fa84c-104">語法</span><span class="sxs-lookup"><span data-stu-id="fa84c-104">SYNTAX</span></span>

### <span data-ttu-id="fa84c-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fa84c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa84c-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa84c-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa84c-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa84c-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa84c-108">描述</span><span class="sxs-lookup"><span data-stu-id="fa84c-108">DESCRIPTION</span></span>
<span data-ttu-id="fa84c-109">**Remove-AzSynapseWorkspace** Cmdlet 會永久刪除 Azure Synapse Analytics 工作區。</span><span class="sxs-lookup"><span data-stu-id="fa84c-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="fa84c-110">例子</span><span class="sxs-lookup"><span data-stu-id="fa84c-110">EXAMPLES</span></span>

### <span data-ttu-id="fa84c-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="fa84c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="fa84c-112">此命令會刪除 Azure Synapse Analytics 工作區。</span><span class="sxs-lookup"><span data-stu-id="fa84c-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="fa84c-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="fa84c-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="fa84c-114">此命令會透過管線刪除 Azure Synapse Analytics 工作區。</span><span class="sxs-lookup"><span data-stu-id="fa84c-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="fa84c-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="fa84c-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="fa84c-116">此命令會透過具有指定資源識別碼的管道刪除 Azure Synapse Analytics 工作區。</span><span class="sxs-lookup"><span data-stu-id="fa84c-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="fa84c-117">參數</span><span class="sxs-lookup"><span data-stu-id="fa84c-117">PARAMETERS</span></span>

### <span data-ttu-id="fa84c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa84c-118">-AsJob</span></span>
<span data-ttu-id="fa84c-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fa84c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa84c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa84c-120">-DefaultProfile</span></span>
<span data-ttu-id="fa84c-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fa84c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa84c-122">-強制</span><span class="sxs-lookup"><span data-stu-id="fa84c-122">-Force</span></span>
<span data-ttu-id="fa84c-123">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="fa84c-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fa84c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa84c-124">-InputObject</span></span>
<span data-ttu-id="fa84c-125">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="fa84c-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa84c-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="fa84c-126">-Name</span></span>
<span data-ttu-id="fa84c-127">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa84c-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa84c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa84c-128">-PassThru</span></span>
<span data-ttu-id="fa84c-129">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="fa84c-129">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="fa84c-130">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="fa84c-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="fa84c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa84c-131">-ResourceGroupName</span></span>
<span data-ttu-id="fa84c-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="fa84c-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa84c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa84c-133">-ResourceId</span></span>
<span data-ttu-id="fa84c-134">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fa84c-134">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa84c-135">-確認</span><span class="sxs-lookup"><span data-stu-id="fa84c-135">-Confirm</span></span>
<span data-ttu-id="fa84c-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fa84c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa84c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa84c-137">-WhatIf</span></span>
<span data-ttu-id="fa84c-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa84c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa84c-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa84c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa84c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa84c-140">CommonParameters</span></span>
<span data-ttu-id="fa84c-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fa84c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa84c-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa84c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa84c-143">輸入</span><span class="sxs-lookup"><span data-stu-id="fa84c-143">INPUTS</span></span>

### <span data-ttu-id="fa84c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fa84c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fa84c-145">輸出</span><span class="sxs-lookup"><span data-stu-id="fa84c-145">OUTPUTS</span></span>

### <span data-ttu-id="fa84c-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fa84c-146">System.Boolean</span></span>

## <span data-ttu-id="fa84c-147">筆記</span><span class="sxs-lookup"><span data-stu-id="fa84c-147">NOTES</span></span>

## <span data-ttu-id="fa84c-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa84c-148">RELATED LINKS</span></span>
