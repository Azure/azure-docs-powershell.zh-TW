---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 829227e47c0c68ac8ebe44f1a365898baa6e123a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911830"
---
# <span data-ttu-id="b65cd-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b65cd-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="b65cd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b65cd-102">SYNOPSIS</span></span>
<span data-ttu-id="b65cd-103">建立 Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b65cd-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b65cd-104">語法</span><span class="sxs-lookup"><span data-stu-id="b65cd-104">SYNTAX</span></span>

### <span data-ttu-id="b65cd-105">CreateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b65cd-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b65cd-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b65cd-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b65cd-107">描述</span><span class="sxs-lookup"><span data-stu-id="b65cd-107">DESCRIPTION</span></span>
<span data-ttu-id="b65cd-108">**New-AzSynapseSqlPool** Cmdlet 會建立 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b65cd-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b65cd-109">例子</span><span class="sxs-lookup"><span data-stu-id="b65cd-109">EXAMPLES</span></span>

### <span data-ttu-id="b65cd-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="b65cd-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="b65cd-111">此命令會建立 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b65cd-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b65cd-112">參數</span><span class="sxs-lookup"><span data-stu-id="b65cd-112">PARAMETERS</span></span>

### <span data-ttu-id="b65cd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b65cd-113">-AsJob</span></span>
<span data-ttu-id="b65cd-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b65cd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b65cd-115">-排序</span><span class="sxs-lookup"><span data-stu-id="b65cd-115">-Collation</span></span>
<span data-ttu-id="b65cd-116">自動排序會定義排序及比較資料的規則，且在建立 SQL 資料庫之後無法變更。</span><span class="sxs-lookup"><span data-stu-id="b65cd-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="b65cd-117">預設會SQL_Latin1_General_CP1_CI_AS。</span><span class="sxs-lookup"><span data-stu-id="b65cd-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="b65cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b65cd-118">-DefaultProfile</span></span>
<span data-ttu-id="b65cd-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b65cd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b65cd-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="b65cd-120">-Name</span></span>
<span data-ttu-id="b65cd-121">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b65cd-121">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b65cd-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="b65cd-122">-PerformanceLevel</span></span>
<span data-ttu-id="b65cd-123">要指派給 SQL 資料庫的 SQL 服務層級和績效等級。</span><span class="sxs-lookup"><span data-stu-id="b65cd-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="b65cd-124">例如，2000c。</span><span class="sxs-lookup"><span data-stu-id="b65cd-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="b65cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b65cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="b65cd-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="b65cd-126">Resource group name.</span></span>

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

### <span data-ttu-id="b65cd-127">-標記</span><span class="sxs-lookup"><span data-stu-id="b65cd-127">-Tag</span></span>
<span data-ttu-id="b65cd-128">與資源關聯的標記字串字典。</span><span class="sxs-lookup"><span data-stu-id="b65cd-128">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="b65cd-129">-版本</span><span class="sxs-lookup"><span data-stu-id="b65cd-129">-Version</span></span>
<span data-ttu-id="b65cd-130">Synapse SQL 資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="b65cd-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="b65cd-131">例如 2 或 3。</span><span class="sxs-lookup"><span data-stu-id="b65cd-131">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="b65cd-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b65cd-132">-WorkspaceName</span></span>
<span data-ttu-id="b65cd-133">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b65cd-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b65cd-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b65cd-134">-WorkspaceObject</span></span>
<span data-ttu-id="b65cd-135">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="b65cd-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b65cd-136">-確認</span><span class="sxs-lookup"><span data-stu-id="b65cd-136">-Confirm</span></span>
<span data-ttu-id="b65cd-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b65cd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b65cd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b65cd-138">-WhatIf</span></span>
<span data-ttu-id="b65cd-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b65cd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b65cd-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b65cd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b65cd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b65cd-141">CommonParameters</span></span>
<span data-ttu-id="b65cd-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b65cd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b65cd-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b65cd-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b65cd-144">輸入</span><span class="sxs-lookup"><span data-stu-id="b65cd-144">INPUTS</span></span>

### <span data-ttu-id="b65cd-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b65cd-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b65cd-146">輸出</span><span class="sxs-lookup"><span data-stu-id="b65cd-146">OUTPUTS</span></span>

### <span data-ttu-id="b65cd-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b65cd-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="b65cd-148">筆記</span><span class="sxs-lookup"><span data-stu-id="b65cd-148">NOTES</span></span>

## <span data-ttu-id="b65cd-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="b65cd-149">RELATED LINKS</span></span>
