---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: 532246d6e672c4e1770802ab2a0fb01af03455b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917842"
---
# <span data-ttu-id="7ef1a-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7ef1a-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="7ef1a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7ef1a-102">SYNOPSIS</span></span>
<span data-ttu-id="7ef1a-103">獲得 Synapse Analytics SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="7ef1a-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="7ef1a-104">語法</span><span class="sxs-lookup"><span data-stu-id="7ef1a-104">SYNTAX</span></span>

### <span data-ttu-id="7ef1a-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7ef1a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ef1a-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ef1a-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ef1a-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ef1a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ef1a-108">描述</span><span class="sxs-lookup"><span data-stu-id="7ef1a-108">DESCRIPTION</span></span>
<span data-ttu-id="7ef1a-109">**Get-AzSynapseSqlPool** Cmdlet 會取得 Azure Synapse Analytics SQL 資料庫相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7ef1a-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="7ef1a-110">例子</span><span class="sxs-lookup"><span data-stu-id="7ef1a-110">EXAMPLES</span></span>

### <span data-ttu-id="7ef1a-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="7ef1a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="7ef1a-112">此命令會獲得工作區下的所有 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="7ef1a-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="7ef1a-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="7ef1a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="7ef1a-114">此命令會獲得工作區 ContosoWorkspace 下的 SQL 資料庫，名稱為 ContosoSqlPool。</span><span class="sxs-lookup"><span data-stu-id="7ef1a-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="7ef1a-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="7ef1a-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="7ef1a-116">此命令會透過管線在工作區下的所有 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="7ef1a-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="7ef1a-117">範例 4</span><span class="sxs-lookup"><span data-stu-id="7ef1a-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="7ef1a-118">此命令會獲得具有指定資源識別碼的 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="7ef1a-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="7ef1a-119">參數</span><span class="sxs-lookup"><span data-stu-id="7ef1a-119">PARAMETERS</span></span>

### <span data-ttu-id="7ef1a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ef1a-120">-DefaultProfile</span></span>
<span data-ttu-id="7ef1a-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ef1a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ef1a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="7ef1a-122">-Name</span></span>
<span data-ttu-id="7ef1a-123">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ef1a-123">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SqlPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ef1a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ef1a-124">-ResourceGroupName</span></span>
<span data-ttu-id="7ef1a-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="7ef1a-125">Resource group name.</span></span>

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

### <span data-ttu-id="7ef1a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ef1a-126">-ResourceId</span></span>
<span data-ttu-id="7ef1a-127">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ef1a-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="7ef1a-128">-版本</span><span class="sxs-lookup"><span data-stu-id="7ef1a-128">-Version</span></span>
<span data-ttu-id="7ef1a-129">[此功能在有限的預覽版中，一開始只有特定訂閱才能使用。]Synapse SQL 資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="7ef1a-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="7ef1a-130">例如 2 或 3。</span><span class="sxs-lookup"><span data-stu-id="7ef1a-130">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="7ef1a-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7ef1a-131">-WorkspaceName</span></span>
<span data-ttu-id="7ef1a-132">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ef1a-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7ef1a-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7ef1a-133">-WorkspaceObject</span></span>
<span data-ttu-id="7ef1a-134">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="7ef1a-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7ef1a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ef1a-135">CommonParameters</span></span>
<span data-ttu-id="7ef1a-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7ef1a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ef1a-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ef1a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ef1a-138">輸入</span><span class="sxs-lookup"><span data-stu-id="7ef1a-138">INPUTS</span></span>

### <span data-ttu-id="7ef1a-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7ef1a-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7ef1a-140">輸出</span><span class="sxs-lookup"><span data-stu-id="7ef1a-140">OUTPUTS</span></span>

### <span data-ttu-id="7ef1a-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7ef1a-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="7ef1a-142">筆記</span><span class="sxs-lookup"><span data-stu-id="7ef1a-142">NOTES</span></span>

## <span data-ttu-id="7ef1a-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ef1a-143">RELATED LINKS</span></span>
