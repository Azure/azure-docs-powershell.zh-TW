---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 574c41fe8b0f3266a6fff80c020b60c9832cb431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281275"
---
# <span data-ttu-id="e2e8e-101">New-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="e2e8e-101">New-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="e2e8e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e8e-103">在 Azure Synapse Analytics SQL pool 中建立新的還原點。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-103">Creates a new restore point in an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e2e8e-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2e8e-104">SYNTAX</span></span>

### <span data-ttu-id="e2e8e-105">CreateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e2e8e-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2e8e-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2e8e-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2e8e-107">CreateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2e8e-107">CreateByInputObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2e8e-108">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2e8e-108">CreateByResourceIdParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -ResourceId <String> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2e8e-109">說明</span><span class="sxs-lookup"><span data-stu-id="e2e8e-109">DESCRIPTION</span></span>
<span data-ttu-id="e2e8e-110">**新的-AzSynapseSqlPoolRestorePoint** Cmdlet 會建立新的還原點，以供您還原 Azure SYNAPSE 分析 SQL pool。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-110">The **New-AzSynapseSqlPoolRestorePoint** cmdlet creates a new restore point that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="e2e8e-111">示例</span><span class="sxs-lookup"><span data-stu-id="e2e8e-111">EXAMPLES</span></span>

### <span data-ttu-id="e2e8e-112">範例1</span><span class="sxs-lookup"><span data-stu-id="e2e8e-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -RestorePointLabel ContosoRestorePoint
```

<span data-ttu-id="e2e8e-113">這個命令會在工作區 ContosoWorkspace 中建立名為 ContosoSqlPool 的 SQL pool 的還原點。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-113">This command creates a restore point for SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="e2e8e-114">參數</span><span class="sxs-lookup"><span data-stu-id="e2e8e-114">PARAMETERS</span></span>

### <span data-ttu-id="e2e8e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2e8e-115">-AsJob</span></span>
<span data-ttu-id="e2e8e-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2e8e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2e8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e8e-117">-DefaultProfile</span></span>
<span data-ttu-id="e2e8e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2e8e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2e8e-119">-InputObject</span></span>
<span data-ttu-id="e2e8e-120">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e8e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e2e8e-121">-Name</span></span>
<span data-ttu-id="e2e8e-122">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e8e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2e8e-123">-ResourceGroupName</span></span>
<span data-ttu-id="e2e8e-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e8e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2e8e-125">-ResourceId</span></span>
<span data-ttu-id="e2e8e-126">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-126">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e8e-127">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="e2e8e-127">-RestorePointLabel</span></span>
<span data-ttu-id="e2e8e-128">我們將與還原點關聯的標籤，可能不是唯一的。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-128">The label we associate a restore point with, may not be unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e8e-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e2e8e-129">-WorkspaceName</span></span>
<span data-ttu-id="e2e8e-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e8e-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e2e8e-131">-WorkspaceObject</span></span>
<span data-ttu-id="e2e8e-132">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e8e-133">-確認</span><span class="sxs-lookup"><span data-stu-id="e2e8e-133">-Confirm</span></span>
<span data-ttu-id="e2e8e-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2e8e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2e8e-135">-WhatIf</span></span>
<span data-ttu-id="e2e8e-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2e8e-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2e8e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e8e-138">CommonParameters</span></span>
<span data-ttu-id="e2e8e-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e8e-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e8e-141">輸入</span><span class="sxs-lookup"><span data-stu-id="e2e8e-141">INPUTS</span></span>

### <span data-ttu-id="e2e8e-142">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e2e8e-143">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e2e8e-144">輸出</span><span class="sxs-lookup"><span data-stu-id="e2e8e-144">OUTPUTS</span></span>

### <span data-ttu-id="e2e8e-145">PSRestorePoint 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e2e8e-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

## <span data-ttu-id="e2e8e-146">筆記</span><span class="sxs-lookup"><span data-stu-id="e2e8e-146">NOTES</span></span>

## <span data-ttu-id="e2e8e-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2e8e-147">RELATED LINKS</span></span>
