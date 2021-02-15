---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 574c41fe8b0f3266a6fff80c020b60c9832cb431
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130383"
---
# <span data-ttu-id="0d051-101">New-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="0d051-101">New-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="0d051-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d051-102">SYNOPSIS</span></span>
<span data-ttu-id="0d051-103">在 Azure Synapse Analytics SQL pool 中建立新的還原點。</span><span class="sxs-lookup"><span data-stu-id="0d051-103">Creates a new restore point in an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0d051-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d051-104">SYNTAX</span></span>

### <span data-ttu-id="0d051-105">CreateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0d051-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d051-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d051-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d051-107">CreateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d051-107">CreateByInputObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d051-108">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d051-108">CreateByResourceIdParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -ResourceId <String> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d051-109">說明</span><span class="sxs-lookup"><span data-stu-id="0d051-109">DESCRIPTION</span></span>
<span data-ttu-id="0d051-110">**新的-AzSynapseSqlPoolRestorePoint** Cmdlet 會建立新的還原點，以供您還原 Azure SYNAPSE 分析 SQL pool。</span><span class="sxs-lookup"><span data-stu-id="0d051-110">The **New-AzSynapseSqlPoolRestorePoint** cmdlet creates a new restore point that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="0d051-111">示例</span><span class="sxs-lookup"><span data-stu-id="0d051-111">EXAMPLES</span></span>

### <span data-ttu-id="0d051-112">範例1</span><span class="sxs-lookup"><span data-stu-id="0d051-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -RestorePointLabel ContosoRestorePoint
```

<span data-ttu-id="0d051-113">這個命令會在工作區 ContosoWorkspace 中建立名為 ContosoSqlPool 的 SQL pool 的還原點。</span><span class="sxs-lookup"><span data-stu-id="0d051-113">This command creates a restore point for SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="0d051-114">參數</span><span class="sxs-lookup"><span data-stu-id="0d051-114">PARAMETERS</span></span>

### <span data-ttu-id="0d051-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d051-115">-AsJob</span></span>
<span data-ttu-id="0d051-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0d051-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d051-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d051-117">-DefaultProfile</span></span>
<span data-ttu-id="0d051-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d051-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d051-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d051-119">-InputObject</span></span>
<span data-ttu-id="0d051-120">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="0d051-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0d051-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d051-121">-Name</span></span>
<span data-ttu-id="0d051-122">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d051-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="0d051-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d051-123">-ResourceGroupName</span></span>
<span data-ttu-id="0d051-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0d051-124">Resource group name.</span></span>

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

### <span data-ttu-id="0d051-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d051-125">-ResourceId</span></span>
<span data-ttu-id="0d051-126">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d051-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="0d051-127">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="0d051-127">-RestorePointLabel</span></span>
<span data-ttu-id="0d051-128">我們將與還原點關聯的標籤，可能不是唯一的。</span><span class="sxs-lookup"><span data-stu-id="0d051-128">The label we associate a restore point with, may not be unique.</span></span>

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

### <span data-ttu-id="0d051-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0d051-129">-WorkspaceName</span></span>
<span data-ttu-id="0d051-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d051-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0d051-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0d051-131">-WorkspaceObject</span></span>
<span data-ttu-id="0d051-132">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="0d051-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0d051-133">-確認</span><span class="sxs-lookup"><span data-stu-id="0d051-133">-Confirm</span></span>
<span data-ttu-id="0d051-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0d051-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d051-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d051-135">-WhatIf</span></span>
<span data-ttu-id="0d051-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d051-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d051-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d051-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d051-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d051-138">CommonParameters</span></span>
<span data-ttu-id="0d051-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d051-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d051-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0d051-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d051-141">輸入</span><span class="sxs-lookup"><span data-stu-id="0d051-141">INPUTS</span></span>

### <span data-ttu-id="0d051-142">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="0d051-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0d051-143">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="0d051-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="0d051-144">輸出</span><span class="sxs-lookup"><span data-stu-id="0d051-144">OUTPUTS</span></span>

### <span data-ttu-id="0d051-145">PSRestorePoint 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="0d051-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

## <span data-ttu-id="0d051-146">筆記</span><span class="sxs-lookup"><span data-stu-id="0d051-146">NOTES</span></span>

## <span data-ttu-id="0d051-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d051-147">RELATED LINKS</span></span>
