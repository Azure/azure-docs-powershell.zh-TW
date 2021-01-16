---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 997132e201864653307af3d072920d36b19d5af3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283491"
---
# <span data-ttu-id="75307-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="75307-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="75307-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75307-102">SYNOPSIS</span></span>
<span data-ttu-id="75307-103">建立 Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="75307-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="75307-104">句法</span><span class="sxs-lookup"><span data-stu-id="75307-104">SYNTAX</span></span>

### <span data-ttu-id="75307-105">CreateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="75307-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75307-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75307-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75307-107">說明</span><span class="sxs-lookup"><span data-stu-id="75307-107">DESCRIPTION</span></span>
<span data-ttu-id="75307-108">**AzSynapseSqlPool** Cmdlet 會建立 Azure SYNAPSE 分析 SQL pool。</span><span class="sxs-lookup"><span data-stu-id="75307-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="75307-109">示例</span><span class="sxs-lookup"><span data-stu-id="75307-109">EXAMPLES</span></span>

### <span data-ttu-id="75307-110">範例1</span><span class="sxs-lookup"><span data-stu-id="75307-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="75307-111">這個命令會建立 Azure Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="75307-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="75307-112">參數</span><span class="sxs-lookup"><span data-stu-id="75307-112">PARAMETERS</span></span>

### <span data-ttu-id="75307-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75307-113">-AsJob</span></span>
<span data-ttu-id="75307-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="75307-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75307-115">-排序規則</span><span class="sxs-lookup"><span data-stu-id="75307-115">-Collation</span></span>
<span data-ttu-id="75307-116">排序規則定義排序與比較資料的規則，且無法在建立 SQL 池之後進行變更。</span><span class="sxs-lookup"><span data-stu-id="75307-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="75307-117">預設的排序規則為 [SQL_Latin1_General_CP1_CI_AS]。</span><span class="sxs-lookup"><span data-stu-id="75307-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75307-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75307-118">-DefaultProfile</span></span>
<span data-ttu-id="75307-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="75307-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75307-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="75307-120">-Name</span></span>
<span data-ttu-id="75307-121">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="75307-121">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="75307-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="75307-122">-PerformanceLevel</span></span>
<span data-ttu-id="75307-123">要指派給 SQL pool 的 SQL 服務層級和效能等級。</span><span class="sxs-lookup"><span data-stu-id="75307-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="75307-124">例如，DW2000c。</span><span class="sxs-lookup"><span data-stu-id="75307-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="75307-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75307-125">-ResourceGroupName</span></span>
<span data-ttu-id="75307-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="75307-126">Resource group name.</span></span>

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

### <span data-ttu-id="75307-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="75307-127">-Tag</span></span>
<span data-ttu-id="75307-128">與資源相關聯之標記的字串字典。</span><span class="sxs-lookup"><span data-stu-id="75307-128">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75307-129">-版本</span><span class="sxs-lookup"><span data-stu-id="75307-129">-Version</span></span>
<span data-ttu-id="75307-130">Synapse SQL pool 的版本。</span><span class="sxs-lookup"><span data-stu-id="75307-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="75307-131">例如，2或3。</span><span class="sxs-lookup"><span data-stu-id="75307-131">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75307-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="75307-132">-WorkspaceName</span></span>
<span data-ttu-id="75307-133">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="75307-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="75307-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="75307-134">-WorkspaceObject</span></span>
<span data-ttu-id="75307-135">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="75307-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="75307-136">-確認</span><span class="sxs-lookup"><span data-stu-id="75307-136">-Confirm</span></span>
<span data-ttu-id="75307-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="75307-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75307-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75307-138">-WhatIf</span></span>
<span data-ttu-id="75307-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="75307-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75307-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="75307-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75307-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75307-141">CommonParameters</span></span>
<span data-ttu-id="75307-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75307-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75307-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="75307-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75307-144">輸入</span><span class="sxs-lookup"><span data-stu-id="75307-144">INPUTS</span></span>

### <span data-ttu-id="75307-145">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="75307-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="75307-146">輸出</span><span class="sxs-lookup"><span data-stu-id="75307-146">OUTPUTS</span></span>

### <span data-ttu-id="75307-147">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="75307-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="75307-148">筆記</span><span class="sxs-lookup"><span data-stu-id="75307-148">NOTES</span></span>

## <span data-ttu-id="75307-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="75307-149">RELATED LINKS</span></span>
