---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 1f30dd8d0757e857934c1f8337e879cf1de8384e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904790"
---
# <span data-ttu-id="44e33-101">New-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="44e33-101">New-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="44e33-102">簡介</span><span class="sxs-lookup"><span data-stu-id="44e33-102">SYNOPSIS</span></span>
<span data-ttu-id="44e33-103">在 Azure Synapse Analytics SQL 資料庫中建立新還原點。</span><span class="sxs-lookup"><span data-stu-id="44e33-103">Creates a new restore point in an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="44e33-104">語法</span><span class="sxs-lookup"><span data-stu-id="44e33-104">SYNTAX</span></span>

### <span data-ttu-id="44e33-105">CreateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="44e33-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44e33-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44e33-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44e33-107">CreateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44e33-107">CreateByInputObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44e33-108">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44e33-108">CreateByResourceIdParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -ResourceId <String> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44e33-109">描述</span><span class="sxs-lookup"><span data-stu-id="44e33-109">DESCRIPTION</span></span>
<span data-ttu-id="44e33-110">**New-AzSynapseSqlPoolRestorePoint** Cmdlet 會建立一個新的還原點，以還原 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="44e33-110">The **New-AzSynapseSqlPoolRestorePoint** cmdlet creates a new restore point that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="44e33-111">例子</span><span class="sxs-lookup"><span data-stu-id="44e33-111">EXAMPLES</span></span>

### <span data-ttu-id="44e33-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="44e33-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -RestorePointLabel ContosoRestorePoint
```

<span data-ttu-id="44e33-113">此命令為工作區 ContosoWorkspace 中的 SQL 資料庫建立還原點，稱為 ContosoSqlPool。</span><span class="sxs-lookup"><span data-stu-id="44e33-113">This command creates a restore point for SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="44e33-114">參數</span><span class="sxs-lookup"><span data-stu-id="44e33-114">PARAMETERS</span></span>

### <span data-ttu-id="44e33-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44e33-115">-AsJob</span></span>
<span data-ttu-id="44e33-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="44e33-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44e33-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44e33-117">-DefaultProfile</span></span>
<span data-ttu-id="44e33-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="44e33-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44e33-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44e33-119">-InputObject</span></span>
<span data-ttu-id="44e33-120">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="44e33-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="44e33-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="44e33-121">-Name</span></span>
<span data-ttu-id="44e33-122">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="44e33-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="44e33-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44e33-123">-ResourceGroupName</span></span>
<span data-ttu-id="44e33-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="44e33-124">Resource group name.</span></span>

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

### <span data-ttu-id="44e33-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44e33-125">-ResourceId</span></span>
<span data-ttu-id="44e33-126">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="44e33-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="44e33-127">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="44e33-127">-RestorePointLabel</span></span>
<span data-ttu-id="44e33-128">與還原點關聯的標籤不一定是唯一的。</span><span class="sxs-lookup"><span data-stu-id="44e33-128">The label we associate a restore point with, may not be unique.</span></span>

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

### <span data-ttu-id="44e33-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="44e33-129">-WorkspaceName</span></span>
<span data-ttu-id="44e33-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="44e33-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="44e33-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="44e33-131">-WorkspaceObject</span></span>
<span data-ttu-id="44e33-132">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="44e33-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="44e33-133">-確認</span><span class="sxs-lookup"><span data-stu-id="44e33-133">-Confirm</span></span>
<span data-ttu-id="44e33-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="44e33-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44e33-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44e33-135">-WhatIf</span></span>
<span data-ttu-id="44e33-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="44e33-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44e33-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="44e33-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44e33-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44e33-138">CommonParameters</span></span>
<span data-ttu-id="44e33-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="44e33-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44e33-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44e33-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44e33-141">輸入</span><span class="sxs-lookup"><span data-stu-id="44e33-141">INPUTS</span></span>

### <span data-ttu-id="44e33-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="44e33-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="44e33-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="44e33-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="44e33-144">輸出</span><span class="sxs-lookup"><span data-stu-id="44e33-144">OUTPUTS</span></span>

### <span data-ttu-id="44e33-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="44e33-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

## <span data-ttu-id="44e33-146">筆記</span><span class="sxs-lookup"><span data-stu-id="44e33-146">NOTES</span></span>

## <span data-ttu-id="44e33-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="44e33-147">RELATED LINKS</span></span>
