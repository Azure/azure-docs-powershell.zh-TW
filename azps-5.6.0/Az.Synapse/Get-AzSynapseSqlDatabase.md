---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
ms.openlocfilehash: 56674f2696e5d7cebdaa9f84072f890c69535223
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917845"
---
# <span data-ttu-id="ecae0-101">Get-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ecae0-101">Get-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="ecae0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ecae0-102">SYNOPSIS</span></span>
<span data-ttu-id="ecae0-103">獲得 Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="ecae0-103">Gets a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="ecae0-104">語法</span><span class="sxs-lookup"><span data-stu-id="ecae0-104">SYNTAX</span></span>

### <span data-ttu-id="ecae0-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ecae0-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecae0-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecae0-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlDatabase [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecae0-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecae0-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlDatabase -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecae0-108">描述</span><span class="sxs-lookup"><span data-stu-id="ecae0-108">DESCRIPTION</span></span>
<span data-ttu-id="ecae0-109">[此功能在有限的預覽版中，一開始只有特定訂閱才能使用。] **Get-AzSynapseSqlDatabase** Cmdlet 會取得 Azure Synapse Analytics SQL 資料庫相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ecae0-109">[This feature is in a limited preview, initially accessible only to certain subscriptions.] The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="ecae0-110">例子</span><span class="sxs-lookup"><span data-stu-id="ecae0-110">EXAMPLES</span></span>

### <span data-ttu-id="ecae0-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ecae0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="ecae0-112">此命令會獲得工作區下的所有 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="ecae0-112">This command gets all SQL databases under a workspace.</span></span>

### <span data-ttu-id="ecae0-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="ecae0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="ecae0-114">此命令會使用名稱為 ContosoSqlDatabase 的工作區 ContosoWorkspace 下獲得 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="ecae0-114">This command gets the SQL database under workspace ContosoWorkspace with name ContosoSqlDatabase.</span></span>

### <span data-ttu-id="ecae0-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="ecae0-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlDatabase
```

<span data-ttu-id="ecae0-116">此命令會透過管線在工作區下的所有 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="ecae0-116">This command gets all the SQL databases under a workspace through pipeline.</span></span>

### <span data-ttu-id="ecae0-117">範例 4</span><span class="sxs-lookup"><span data-stu-id="ecae0-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase"
```

<span data-ttu-id="ecae0-118">此命令會獲得具有指定資源識別碼的 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="ecae0-118">This command gets the SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="ecae0-119">參數</span><span class="sxs-lookup"><span data-stu-id="ecae0-119">PARAMETERS</span></span>

### <span data-ttu-id="ecae0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecae0-120">-DefaultProfile</span></span>
<span data-ttu-id="ecae0-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ecae0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecae0-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ecae0-122">-Name</span></span>
<span data-ttu-id="ecae0-123">Synapse SQL Database 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecae0-123">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecae0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecae0-124">-ResourceGroupName</span></span>
<span data-ttu-id="ecae0-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ecae0-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecae0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecae0-126">-ResourceId</span></span>
<span data-ttu-id="ecae0-127">Synapse SQL Database 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ecae0-127">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecae0-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ecae0-128">-WorkspaceName</span></span>
<span data-ttu-id="ecae0-129">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecae0-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecae0-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ecae0-130">-WorkspaceObject</span></span>
<span data-ttu-id="ecae0-131">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="ecae0-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecae0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecae0-132">CommonParameters</span></span>
<span data-ttu-id="ecae0-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ecae0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecae0-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecae0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecae0-135">輸入</span><span class="sxs-lookup"><span data-stu-id="ecae0-135">INPUTS</span></span>

### <span data-ttu-id="ecae0-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ecae0-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ecae0-137">輸出</span><span class="sxs-lookup"><span data-stu-id="ecae0-137">OUTPUTS</span></span>

### <span data-ttu-id="ecae0-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ecae0-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="ecae0-139">筆記</span><span class="sxs-lookup"><span data-stu-id="ecae0-139">NOTES</span></span>

## <span data-ttu-id="ecae0-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="ecae0-140">RELATED LINKS</span></span>
