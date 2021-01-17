---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: 80d615f5a2a26869d748f652feeaa8909aca30d3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288032"
---
# <span data-ttu-id="dbc33-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="dbc33-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="dbc33-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dbc33-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc33-103">檢查是否存在 Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="dbc33-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="dbc33-104">句法</span><span class="sxs-lookup"><span data-stu-id="dbc33-104">SYNTAX</span></span>

### <span data-ttu-id="dbc33-105">TestByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dbc33-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbc33-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbc33-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbc33-107">說明</span><span class="sxs-lookup"><span data-stu-id="dbc33-107">DESCRIPTION</span></span>
<span data-ttu-id="dbc33-108">**Test AzSynapseSqlPool** Cmdlet 會檢查是否存在 SYNAPSE 分析 SQL 池。</span><span class="sxs-lookup"><span data-stu-id="dbc33-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="dbc33-109">示例</span><span class="sxs-lookup"><span data-stu-id="dbc33-109">EXAMPLES</span></span>

### <span data-ttu-id="dbc33-110">範例1</span><span class="sxs-lookup"><span data-stu-id="dbc33-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="dbc33-111">這個命令會檢查指定的 SQL pool 是否存在。</span><span class="sxs-lookup"><span data-stu-id="dbc33-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="dbc33-112">參數</span><span class="sxs-lookup"><span data-stu-id="dbc33-112">PARAMETERS</span></span>

### <span data-ttu-id="dbc33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc33-113">-DefaultProfile</span></span>
<span data-ttu-id="dbc33-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbc33-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbc33-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="dbc33-115">-Name</span></span>
<span data-ttu-id="dbc33-116">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbc33-116">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="dbc33-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbc33-117">-ResourceGroupName</span></span>
<span data-ttu-id="dbc33-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="dbc33-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc33-119">-版本</span><span class="sxs-lookup"><span data-stu-id="dbc33-119">-Version</span></span>
<span data-ttu-id="dbc33-120">Synapse SQL pool 的版本。</span><span class="sxs-lookup"><span data-stu-id="dbc33-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="dbc33-121">例如，2或3。</span><span class="sxs-lookup"><span data-stu-id="dbc33-121">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="dbc33-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dbc33-122">-WorkspaceName</span></span>
<span data-ttu-id="dbc33-123">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbc33-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc33-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="dbc33-124">-WorkspaceObject</span></span>
<span data-ttu-id="dbc33-125">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="dbc33-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbc33-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc33-126">CommonParameters</span></span>
<span data-ttu-id="dbc33-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dbc33-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc33-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dbc33-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc33-129">輸入</span><span class="sxs-lookup"><span data-stu-id="dbc33-129">INPUTS</span></span>

### <span data-ttu-id="dbc33-130">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="dbc33-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="dbc33-131">輸出</span><span class="sxs-lookup"><span data-stu-id="dbc33-131">OUTPUTS</span></span>

### <span data-ttu-id="dbc33-132">System.object</span><span class="sxs-lookup"><span data-stu-id="dbc33-132">System.Object</span></span>
## <span data-ttu-id="dbc33-133">筆記</span><span class="sxs-lookup"><span data-stu-id="dbc33-133">NOTES</span></span>

## <span data-ttu-id="dbc33-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbc33-134">RELATED LINKS</span></span>
