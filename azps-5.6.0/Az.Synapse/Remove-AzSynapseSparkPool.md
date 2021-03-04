---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: 22b006d096d1ab2457d53a97a6265bf950c4658e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904785"
---
# <span data-ttu-id="1e665-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="1e665-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="1e665-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1e665-102">SYNOPSIS</span></span>
<span data-ttu-id="1e665-103">刪除 Synapse Analytics Spark 資料庫。</span><span class="sxs-lookup"><span data-stu-id="1e665-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="1e665-104">語法</span><span class="sxs-lookup"><span data-stu-id="1e665-104">SYNTAX</span></span>

### <span data-ttu-id="1e665-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1e665-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e665-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e665-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e665-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e665-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e665-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e665-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e665-109">描述</span><span class="sxs-lookup"><span data-stu-id="1e665-109">DESCRIPTION</span></span>
<span data-ttu-id="1e665-110">**Remove-AzSynapseSparkPool Cmdlet** 會永久刪除 Azure Synapse Analytics Spark 資料庫。</span><span class="sxs-lookup"><span data-stu-id="1e665-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="1e665-111">例子</span><span class="sxs-lookup"><span data-stu-id="1e665-111">EXAMPLES</span></span>

### <span data-ttu-id="1e665-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="1e665-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="1e665-113">此命令會刪除 Azure Synapse Analytics Spark 資料庫。</span><span class="sxs-lookup"><span data-stu-id="1e665-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="1e665-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="1e665-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="1e665-115">此命令會刪除透過管線的 Azure Synapse Analytics Spark 資料庫。</span><span class="sxs-lookup"><span data-stu-id="1e665-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="1e665-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="1e665-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="1e665-117">此命令會刪除透過管線的 Azure Synapse Analytics Spark 資料庫。</span><span class="sxs-lookup"><span data-stu-id="1e665-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="1e665-118">範例 4</span><span class="sxs-lookup"><span data-stu-id="1e665-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="1e665-119">此命令會刪除具有資源識別碼的 Azure Synapse Analytics Spark 資料庫。</span><span class="sxs-lookup"><span data-stu-id="1e665-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="1e665-120">參數</span><span class="sxs-lookup"><span data-stu-id="1e665-120">PARAMETERS</span></span>

### <span data-ttu-id="1e665-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e665-121">-AsJob</span></span>
<span data-ttu-id="1e665-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1e665-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e665-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e665-123">-DefaultProfile</span></span>
<span data-ttu-id="1e665-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e665-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e665-125">-強制</span><span class="sxs-lookup"><span data-stu-id="1e665-125">-Force</span></span>
<span data-ttu-id="1e665-126">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="1e665-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1e665-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e665-127">-InputObject</span></span>
<span data-ttu-id="1e665-128">Spark Pool 輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="1e665-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e665-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="1e665-129">-Name</span></span>
<span data-ttu-id="1e665-130">Synapse Spark Pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e665-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e665-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e665-131">-PassThru</span></span>
<span data-ttu-id="1e665-132">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="1e665-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="1e665-133">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="1e665-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1e665-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e665-134">-ResourceGroupName</span></span>
<span data-ttu-id="1e665-135">資源組名。</span><span class="sxs-lookup"><span data-stu-id="1e665-135">Resource group name.</span></span>

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

### <span data-ttu-id="1e665-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e665-136">-ResourceId</span></span>
<span data-ttu-id="1e665-137">Synapse Spark 資料格的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e665-137">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="1e665-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1e665-138">-WorkspaceName</span></span>
<span data-ttu-id="1e665-139">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e665-139">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e665-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1e665-140">-WorkspaceObject</span></span>
<span data-ttu-id="1e665-141">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="1e665-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e665-142">-確認</span><span class="sxs-lookup"><span data-stu-id="1e665-142">-Confirm</span></span>
<span data-ttu-id="1e665-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1e665-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e665-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e665-144">-WhatIf</span></span>
<span data-ttu-id="1e665-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e665-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e665-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e665-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e665-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e665-147">CommonParameters</span></span>
<span data-ttu-id="1e665-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1e665-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e665-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e665-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e665-150">輸入</span><span class="sxs-lookup"><span data-stu-id="1e665-150">INPUTS</span></span>

### <span data-ttu-id="1e665-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1e665-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1e665-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="1e665-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="1e665-153">輸出</span><span class="sxs-lookup"><span data-stu-id="1e665-153">OUTPUTS</span></span>

### <span data-ttu-id="1e665-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1e665-154">System.Boolean</span></span>

## <span data-ttu-id="1e665-155">筆記</span><span class="sxs-lookup"><span data-stu-id="1e665-155">NOTES</span></span>

## <span data-ttu-id="1e665-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e665-156">RELATED LINKS</span></span>
