---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
ms.openlocfilehash: c203e9c80978f50bd7879627b733de2ec0c6cf7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137766"
---
# <span data-ttu-id="4f198-101">Get-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4f198-101">Get-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="4f198-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f198-102">SYNOPSIS</span></span>
<span data-ttu-id="4f198-103">取得 Synapse 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="4f198-103">Gets a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="4f198-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f198-104">SYNTAX</span></span>

### <span data-ttu-id="4f198-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4f198-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f198-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f198-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlDatabase [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f198-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f198-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlDatabase -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f198-108">說明</span><span class="sxs-lookup"><span data-stu-id="4f198-108">DESCRIPTION</span></span>
<span data-ttu-id="4f198-109">[這項功能在有限預覽中，最初隻能在特定訂閱中存取。」 **AzSynapseSqlDatabase** Cmdlet 會取得有關 Azure SYNAPSE 分析 SQL 資料庫的資訊。</span><span class="sxs-lookup"><span data-stu-id="4f198-109">[This feature is in a limited preview, initially accessible only to certain subscriptions.] The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="4f198-110">示例</span><span class="sxs-lookup"><span data-stu-id="4f198-110">EXAMPLES</span></span>

### <span data-ttu-id="4f198-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4f198-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="4f198-112">這個命令會在工作區中取得所有的 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="4f198-112">This command gets all SQL databases under a workspace.</span></span>

### <span data-ttu-id="4f198-113">範例2</span><span class="sxs-lookup"><span data-stu-id="4f198-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="4f198-114">這個命令會在 [工作區 ContosoWorkspace] 下取得 name ContosoSqlDatabase 的 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="4f198-114">This command gets the SQL database under workspace ContosoWorkspace with name ContosoSqlDatabase.</span></span>

### <span data-ttu-id="4f198-115">範例3</span><span class="sxs-lookup"><span data-stu-id="4f198-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlDatabase
```

<span data-ttu-id="4f198-116">這個命令會透過管線在工作區下取得所有的 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="4f198-116">This command gets all the SQL databases under a workspace through pipeline.</span></span>

### <span data-ttu-id="4f198-117">範例4</span><span class="sxs-lookup"><span data-stu-id="4f198-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase"
```

<span data-ttu-id="4f198-118">這個命令會取得具有指定資源識別碼的 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="4f198-118">This command gets the SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="4f198-119">參數</span><span class="sxs-lookup"><span data-stu-id="4f198-119">PARAMETERS</span></span>

### <span data-ttu-id="4f198-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f198-120">-DefaultProfile</span></span>
<span data-ttu-id="4f198-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f198-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f198-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f198-122">-Name</span></span>
<span data-ttu-id="4f198-123">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f198-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="4f198-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f198-124">-ResourceGroupName</span></span>
<span data-ttu-id="4f198-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4f198-125">Resource group name.</span></span>

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

### <span data-ttu-id="4f198-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f198-126">-ResourceId</span></span>
<span data-ttu-id="4f198-127">Synapse SQL 資料庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4f198-127">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="4f198-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4f198-128">-WorkspaceName</span></span>
<span data-ttu-id="4f198-129">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f198-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4f198-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4f198-130">-WorkspaceObject</span></span>
<span data-ttu-id="4f198-131">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="4f198-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4f198-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f198-132">CommonParameters</span></span>
<span data-ttu-id="4f198-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f198-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f198-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4f198-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f198-135">輸入</span><span class="sxs-lookup"><span data-stu-id="4f198-135">INPUTS</span></span>

### <span data-ttu-id="4f198-136">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="4f198-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4f198-137">輸出</span><span class="sxs-lookup"><span data-stu-id="4f198-137">OUTPUTS</span></span>

### <span data-ttu-id="4f198-138">PSSynapseSqlDatabase 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="4f198-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="4f198-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4f198-139">NOTES</span></span>

## <span data-ttu-id="4f198-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f198-140">RELATED LINKS</span></span>
