---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: dcc73c78334fba9823ddc1d26463422bcc388bf2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138578"
---
# <span data-ttu-id="cc97b-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cc97b-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="cc97b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc97b-102">SYNOPSIS</span></span>
<span data-ttu-id="cc97b-103">刪除 Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="cc97b-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="cc97b-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc97b-104">SYNTAX</span></span>

### <span data-ttu-id="cc97b-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cc97b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc97b-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc97b-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc97b-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc97b-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc97b-108">說明</span><span class="sxs-lookup"><span data-stu-id="cc97b-108">DESCRIPTION</span></span>
<span data-ttu-id="cc97b-109">**AzSynapseWorkspace** Cmdlet 會永久刪除 Azure Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="cc97b-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="cc97b-110">示例</span><span class="sxs-lookup"><span data-stu-id="cc97b-110">EXAMPLES</span></span>

### <span data-ttu-id="cc97b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="cc97b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="cc97b-112">這個命令會刪除 Azure Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="cc97b-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="cc97b-113">範例2</span><span class="sxs-lookup"><span data-stu-id="cc97b-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="cc97b-114">這個命令會透過管線刪除 Azure Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="cc97b-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="cc97b-115">範例3</span><span class="sxs-lookup"><span data-stu-id="cc97b-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="cc97b-116">這個命令會透過具有指定資源識別碼的管線刪除 Azure Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="cc97b-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="cc97b-117">參數</span><span class="sxs-lookup"><span data-stu-id="cc97b-117">PARAMETERS</span></span>

### <span data-ttu-id="cc97b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc97b-118">-AsJob</span></span>
<span data-ttu-id="cc97b-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cc97b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc97b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc97b-120">-DefaultProfile</span></span>
<span data-ttu-id="cc97b-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc97b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc97b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc97b-122">-InputObject</span></span>
<span data-ttu-id="cc97b-123">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="cc97b-123">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cc97b-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="cc97b-124">-Name</span></span>
<span data-ttu-id="cc97b-125">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc97b-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cc97b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc97b-126">-PassThru</span></span>
<span data-ttu-id="cc97b-127">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="cc97b-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="cc97b-128">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="cc97b-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cc97b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc97b-129">-ResourceGroupName</span></span>
<span data-ttu-id="cc97b-130">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="cc97b-130">Resource group name.</span></span>

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

### <span data-ttu-id="cc97b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc97b-131">-ResourceId</span></span>
<span data-ttu-id="cc97b-132">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc97b-132">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="cc97b-133">-確認</span><span class="sxs-lookup"><span data-stu-id="cc97b-133">-Confirm</span></span>
<span data-ttu-id="cc97b-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cc97b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc97b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc97b-135">-WhatIf</span></span>
<span data-ttu-id="cc97b-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc97b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc97b-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc97b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc97b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc97b-138">CommonParameters</span></span>
<span data-ttu-id="cc97b-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc97b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc97b-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cc97b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc97b-141">輸入</span><span class="sxs-lookup"><span data-stu-id="cc97b-141">INPUTS</span></span>

### <span data-ttu-id="cc97b-142">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="cc97b-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cc97b-143">輸出</span><span class="sxs-lookup"><span data-stu-id="cc97b-143">OUTPUTS</span></span>

### <span data-ttu-id="cc97b-144">System.object</span><span class="sxs-lookup"><span data-stu-id="cc97b-144">System.Boolean</span></span>

## <span data-ttu-id="cc97b-145">筆記</span><span class="sxs-lookup"><span data-stu-id="cc97b-145">NOTES</span></span>

## <span data-ttu-id="cc97b-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc97b-146">RELATED LINKS</span></span>
