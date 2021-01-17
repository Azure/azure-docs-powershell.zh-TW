---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: b89feae28cee95c63184fd5c0e172a4cb005cac2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288180"
---
# <span data-ttu-id="1a6ff-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1a6ff-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="1a6ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1a6ff-102">SYNOPSIS</span></span>
<span data-ttu-id="1a6ff-103">建立 Synapse 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="1a6ff-104">句法</span><span class="sxs-lookup"><span data-stu-id="1a6ff-104">SYNTAX</span></span>

### <span data-ttu-id="1a6ff-105">CreateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1a6ff-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a6ff-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a6ff-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a6ff-107">說明</span><span class="sxs-lookup"><span data-stu-id="1a6ff-107">DESCRIPTION</span></span>
<span data-ttu-id="1a6ff-108">**AzSynapseSqlDatabase** Cmdlet 會取得有關 Azure SYNAPSE 分析 SQL 資料庫的資訊。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="1a6ff-109">示例</span><span class="sxs-lookup"><span data-stu-id="1a6ff-109">EXAMPLES</span></span>

### <span data-ttu-id="1a6ff-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1a6ff-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="1a6ff-111">這個命令會建立 Azure Synapse 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="1a6ff-112">參數</span><span class="sxs-lookup"><span data-stu-id="1a6ff-112">PARAMETERS</span></span>

### <span data-ttu-id="1a6ff-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a6ff-113">-AsJob</span></span>
<span data-ttu-id="1a6ff-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1a6ff-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a6ff-115">-排序規則</span><span class="sxs-lookup"><span data-stu-id="1a6ff-115">-Collation</span></span>
<span data-ttu-id="1a6ff-116">排序規則定義排序與比較資料的規則，且無法在建立 SQL 池之後進行變更。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="1a6ff-117">預設的排序規則為 [SQL_Latin1_General_CP1_CI_AS]。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="1a6ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a6ff-118">-DefaultProfile</span></span>
<span data-ttu-id="1a6ff-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a6ff-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="1a6ff-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="1a6ff-121">指定資料庫的最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-121">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="1a6ff-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="1a6ff-122">-Name</span></span>
<span data-ttu-id="1a6ff-123">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="1a6ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a6ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="1a6ff-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-125">Resource group name.</span></span>

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

### <span data-ttu-id="1a6ff-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="1a6ff-126">-Tag</span></span>
<span data-ttu-id="1a6ff-127">與資源相關聯之標記的字串字典。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-127">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="1a6ff-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1a6ff-128">-WorkspaceName</span></span>
<span data-ttu-id="1a6ff-129">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1a6ff-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1a6ff-130">-WorkspaceObject</span></span>
<span data-ttu-id="1a6ff-131">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1a6ff-132">-確認</span><span class="sxs-lookup"><span data-stu-id="1a6ff-132">-Confirm</span></span>
<span data-ttu-id="1a6ff-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a6ff-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a6ff-134">-WhatIf</span></span>
<span data-ttu-id="1a6ff-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a6ff-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a6ff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a6ff-137">CommonParameters</span></span>
<span data-ttu-id="1a6ff-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a6ff-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a6ff-140">輸入</span><span class="sxs-lookup"><span data-stu-id="1a6ff-140">INPUTS</span></span>

### <span data-ttu-id="1a6ff-141">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1a6ff-142">輸出</span><span class="sxs-lookup"><span data-stu-id="1a6ff-142">OUTPUTS</span></span>

### <span data-ttu-id="1a6ff-143">PSSynapseSqlDatabase 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="1a6ff-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="1a6ff-144">筆記</span><span class="sxs-lookup"><span data-stu-id="1a6ff-144">NOTES</span></span>

## <span data-ttu-id="1a6ff-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a6ff-145">RELATED LINKS</span></span>
