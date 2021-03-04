---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: 73664b619670f17a92bd915f6e4d8501a8ac9f6d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907937"
---
# <span data-ttu-id="5ca8f-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ca8f-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="5ca8f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5ca8f-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca8f-103">建立 Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="5ca8f-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="5ca8f-104">語法</span><span class="sxs-lookup"><span data-stu-id="5ca8f-104">SYNTAX</span></span>

### <span data-ttu-id="5ca8f-105">CreateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5ca8f-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ca8f-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ca8f-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ca8f-107">描述</span><span class="sxs-lookup"><span data-stu-id="5ca8f-107">DESCRIPTION</span></span>
<span data-ttu-id="5ca8f-108">**Get-AzSynapseSqlDatabase** Cmdlet 會取得 Azure Synapse Analytics SQL 資料庫相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5ca8f-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="5ca8f-109">例子</span><span class="sxs-lookup"><span data-stu-id="5ca8f-109">EXAMPLES</span></span>

### <span data-ttu-id="5ca8f-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="5ca8f-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="5ca8f-111">此命令會建立 Azure Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="5ca8f-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="5ca8f-112">參數</span><span class="sxs-lookup"><span data-stu-id="5ca8f-112">PARAMETERS</span></span>

### <span data-ttu-id="5ca8f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ca8f-113">-AsJob</span></span>
<span data-ttu-id="5ca8f-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5ca8f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ca8f-115">-排序</span><span class="sxs-lookup"><span data-stu-id="5ca8f-115">-Collation</span></span>
<span data-ttu-id="5ca8f-116">自動排序會定義排序及比較資料的規則，且在建立 SQL 資料庫之後無法變更。</span><span class="sxs-lookup"><span data-stu-id="5ca8f-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="5ca8f-117">預設會SQL_Latin1_General_CP1_CI_AS。</span><span class="sxs-lookup"><span data-stu-id="5ca8f-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="5ca8f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca8f-118">-DefaultProfile</span></span>
<span data-ttu-id="5ca8f-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ca8f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ca8f-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="5ca8f-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="5ca8f-121">指定資料庫的大小上限 ，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="5ca8f-121">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca8f-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ca8f-122">-Name</span></span>
<span data-ttu-id="5ca8f-123">Synapse SQL Database 的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ca8f-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="5ca8f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ca8f-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ca8f-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="5ca8f-125">Resource group name.</span></span>

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

### <span data-ttu-id="5ca8f-126">-標記</span><span class="sxs-lookup"><span data-stu-id="5ca8f-126">-Tag</span></span>
<span data-ttu-id="5ca8f-127">與資源關聯的標記字串字典。</span><span class="sxs-lookup"><span data-stu-id="5ca8f-127">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="5ca8f-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5ca8f-128">-WorkspaceName</span></span>
<span data-ttu-id="5ca8f-129">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ca8f-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5ca8f-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5ca8f-130">-WorkspaceObject</span></span>
<span data-ttu-id="5ca8f-131">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="5ca8f-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5ca8f-132">-確認</span><span class="sxs-lookup"><span data-stu-id="5ca8f-132">-Confirm</span></span>
<span data-ttu-id="5ca8f-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5ca8f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ca8f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ca8f-134">-WhatIf</span></span>
<span data-ttu-id="5ca8f-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ca8f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ca8f-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ca8f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ca8f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca8f-137">CommonParameters</span></span>
<span data-ttu-id="5ca8f-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5ca8f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca8f-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ca8f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca8f-140">輸入</span><span class="sxs-lookup"><span data-stu-id="5ca8f-140">INPUTS</span></span>

### <span data-ttu-id="5ca8f-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5ca8f-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5ca8f-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5ca8f-142">OUTPUTS</span></span>

### <span data-ttu-id="5ca8f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ca8f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="5ca8f-144">筆記</span><span class="sxs-lookup"><span data-stu-id="5ca8f-144">NOTES</span></span>

## <span data-ttu-id="5ca8f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ca8f-145">RELATED LINKS</span></span>
