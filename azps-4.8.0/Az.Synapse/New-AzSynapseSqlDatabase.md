---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: 16f2df5900fcc522f0ff3afb7b9f5b14ea5f0b64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970008"
---
# <span data-ttu-id="cb22c-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cb22c-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="cb22c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb22c-102">SYNOPSIS</span></span>
<span data-ttu-id="cb22c-103">建立 Synapse 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="cb22c-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="cb22c-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb22c-104">SYNTAX</span></span>

### <span data-ttu-id="cb22c-105">CreateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cb22c-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb22c-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb22c-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb22c-107">說明</span><span class="sxs-lookup"><span data-stu-id="cb22c-107">DESCRIPTION</span></span>
<span data-ttu-id="cb22c-108">**AzSynapseSqlDatabase** Cmdlet 會取得有關 Azure SYNAPSE 分析 SQL 資料庫的資訊。</span><span class="sxs-lookup"><span data-stu-id="cb22c-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>


## <span data-ttu-id="cb22c-109">示例</span><span class="sxs-lookup"><span data-stu-id="cb22c-109">EXAMPLES</span></span>

### <span data-ttu-id="cb22c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="cb22c-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase 
```

<span data-ttu-id="cb22c-111">這個命令會建立 Azure Synapse 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="cb22c-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="cb22c-112">參數</span><span class="sxs-lookup"><span data-stu-id="cb22c-112">PARAMETERS</span></span>

### <span data-ttu-id="cb22c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb22c-113">-AsJob</span></span>
<span data-ttu-id="cb22c-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb22c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb22c-115">-排序規則</span><span class="sxs-lookup"><span data-stu-id="cb22c-115">-Collation</span></span>
<span data-ttu-id="cb22c-116">排序規則定義排序與比較資料的規則，且無法在建立 SQL 池之後進行變更。</span><span class="sxs-lookup"><span data-stu-id="cb22c-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="cb22c-117">預設的排序規則為 [SQL_Latin1_General_CP1_CI_AS]。</span><span class="sxs-lookup"><span data-stu-id="cb22c-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="cb22c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb22c-118">-DefaultProfile</span></span>
<span data-ttu-id="cb22c-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb22c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb22c-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="cb22c-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="cb22c-121">指定資料庫的最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cb22c-121">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="cb22c-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb22c-122">-Name</span></span>
<span data-ttu-id="cb22c-123">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb22c-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="cb22c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb22c-124">-ResourceGroupName</span></span>
<span data-ttu-id="cb22c-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="cb22c-125">Resource group name.</span></span>

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

### <span data-ttu-id="cb22c-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="cb22c-126">-Tag</span></span>
<span data-ttu-id="cb22c-127">與資源相關聯之標記的字串字典。</span><span class="sxs-lookup"><span data-stu-id="cb22c-127">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="cb22c-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cb22c-128">-WorkspaceName</span></span>
<span data-ttu-id="cb22c-129">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb22c-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cb22c-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cb22c-130">-WorkspaceObject</span></span>
<span data-ttu-id="cb22c-131">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="cb22c-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cb22c-132">-確認</span><span class="sxs-lookup"><span data-stu-id="cb22c-132">-Confirm</span></span>
<span data-ttu-id="cb22c-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb22c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb22c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb22c-134">-WhatIf</span></span>
<span data-ttu-id="cb22c-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb22c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb22c-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb22c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb22c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb22c-137">CommonParameters</span></span>
<span data-ttu-id="cb22c-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb22c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb22c-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cb22c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb22c-140">輸入</span><span class="sxs-lookup"><span data-stu-id="cb22c-140">INPUTS</span></span>

### <span data-ttu-id="cb22c-141">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="cb22c-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cb22c-142">輸出</span><span class="sxs-lookup"><span data-stu-id="cb22c-142">OUTPUTS</span></span>

### <span data-ttu-id="cb22c-143">PSSynapseSqlDatabase 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="cb22c-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="cb22c-144">筆記</span><span class="sxs-lookup"><span data-stu-id="cb22c-144">NOTES</span></span>

## <span data-ttu-id="cb22c-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb22c-145">RELATED LINKS</span></span>
