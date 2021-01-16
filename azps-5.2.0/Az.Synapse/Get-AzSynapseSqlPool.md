---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: d37012ee5188b6dea15968aee8659387e06a87f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281686"
---
# <span data-ttu-id="0b1be-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0b1be-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="0b1be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b1be-102">SYNOPSIS</span></span>
<span data-ttu-id="0b1be-103">取得 Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="0b1be-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0b1be-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b1be-104">SYNTAX</span></span>

### <span data-ttu-id="0b1be-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0b1be-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b1be-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b1be-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b1be-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b1be-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b1be-108">說明</span><span class="sxs-lookup"><span data-stu-id="0b1be-108">DESCRIPTION</span></span>
<span data-ttu-id="0b1be-109">**AzSynapseSqlPool** Cmdlet 會取得 Azure SYNAPSE Analytics SQL pool 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0b1be-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0b1be-110">示例</span><span class="sxs-lookup"><span data-stu-id="0b1be-110">EXAMPLES</span></span>

### <span data-ttu-id="0b1be-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0b1be-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="0b1be-112">這個命令會在工作區中取得所有的 SQL pool。</span><span class="sxs-lookup"><span data-stu-id="0b1be-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="0b1be-113">範例2</span><span class="sxs-lookup"><span data-stu-id="0b1be-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="0b1be-114">這個命令會在 [工作區 ContosoWorkspace] 下取得名稱為 ContosoSqlPool 的 SQL pool。</span><span class="sxs-lookup"><span data-stu-id="0b1be-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="0b1be-115">範例3</span><span class="sxs-lookup"><span data-stu-id="0b1be-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="0b1be-116">這個命令會透過管線在工作區下取得所有的 SQL pool。</span><span class="sxs-lookup"><span data-stu-id="0b1be-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="0b1be-117">範例4</span><span class="sxs-lookup"><span data-stu-id="0b1be-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="0b1be-118">這個命令會取得具有指定資源識別碼的 SQL pool。</span><span class="sxs-lookup"><span data-stu-id="0b1be-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="0b1be-119">參數</span><span class="sxs-lookup"><span data-stu-id="0b1be-119">PARAMETERS</span></span>

### <span data-ttu-id="0b1be-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b1be-120">-DefaultProfile</span></span>
<span data-ttu-id="0b1be-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b1be-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b1be-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="0b1be-122">-Name</span></span>
<span data-ttu-id="0b1be-123">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b1be-123">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="0b1be-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b1be-124">-ResourceGroupName</span></span>
<span data-ttu-id="0b1be-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0b1be-125">Resource group name.</span></span>

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

### <span data-ttu-id="0b1be-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b1be-126">-ResourceId</span></span>
<span data-ttu-id="0b1be-127">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b1be-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="0b1be-128">-版本</span><span class="sxs-lookup"><span data-stu-id="0b1be-128">-Version</span></span>
<span data-ttu-id="0b1be-129">[這項功能在有限預覽中，最初隻能在特定訂閱中存取。」Synapse SQL pool 的版本。</span><span class="sxs-lookup"><span data-stu-id="0b1be-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="0b1be-130">例如，2或3。</span><span class="sxs-lookup"><span data-stu-id="0b1be-130">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="0b1be-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0b1be-131">-WorkspaceName</span></span>
<span data-ttu-id="0b1be-132">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b1be-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0b1be-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0b1be-133">-WorkspaceObject</span></span>
<span data-ttu-id="0b1be-134">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="0b1be-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0b1be-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b1be-135">CommonParameters</span></span>
<span data-ttu-id="0b1be-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b1be-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b1be-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0b1be-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b1be-138">輸入</span><span class="sxs-lookup"><span data-stu-id="0b1be-138">INPUTS</span></span>

### <span data-ttu-id="0b1be-139">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="0b1be-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0b1be-140">輸出</span><span class="sxs-lookup"><span data-stu-id="0b1be-140">OUTPUTS</span></span>

### <span data-ttu-id="0b1be-141">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="0b1be-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="0b1be-142">筆記</span><span class="sxs-lookup"><span data-stu-id="0b1be-142">NOTES</span></span>

## <span data-ttu-id="0b1be-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b1be-143">RELATED LINKS</span></span>
