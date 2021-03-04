---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: d932a875957f1649976966a9f2e115e93dfea351
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916830"
---
# <span data-ttu-id="73eaf-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="73eaf-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="73eaf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="73eaf-102">SYNOPSIS</span></span>
<span data-ttu-id="73eaf-103">檢查 Synapse Analytics SQL 資料庫是否存在。</span><span class="sxs-lookup"><span data-stu-id="73eaf-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="73eaf-104">語法</span><span class="sxs-lookup"><span data-stu-id="73eaf-104">SYNTAX</span></span>

### <span data-ttu-id="73eaf-105">TestByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="73eaf-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73eaf-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73eaf-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73eaf-107">描述</span><span class="sxs-lookup"><span data-stu-id="73eaf-107">DESCRIPTION</span></span>
<span data-ttu-id="73eaf-108">**Test-AzSynapseSqlPool** Cmdlet 會檢查 Synapse Analytics SQL 資料庫是否存在。</span><span class="sxs-lookup"><span data-stu-id="73eaf-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="73eaf-109">例子</span><span class="sxs-lookup"><span data-stu-id="73eaf-109">EXAMPLES</span></span>

### <span data-ttu-id="73eaf-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="73eaf-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="73eaf-111">此命令會檢查指定的 SQL 資料庫是否存在。</span><span class="sxs-lookup"><span data-stu-id="73eaf-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="73eaf-112">參數</span><span class="sxs-lookup"><span data-stu-id="73eaf-112">PARAMETERS</span></span>

### <span data-ttu-id="73eaf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73eaf-113">-DefaultProfile</span></span>
<span data-ttu-id="73eaf-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="73eaf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73eaf-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="73eaf-115">-Name</span></span>
<span data-ttu-id="73eaf-116">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="73eaf-116">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="73eaf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73eaf-117">-ResourceGroupName</span></span>
<span data-ttu-id="73eaf-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="73eaf-118">Resource group name.</span></span>

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

### <span data-ttu-id="73eaf-119">-版本</span><span class="sxs-lookup"><span data-stu-id="73eaf-119">-Version</span></span>
<span data-ttu-id="73eaf-120">Synapse SQL 資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="73eaf-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="73eaf-121">例如 2 或 3。</span><span class="sxs-lookup"><span data-stu-id="73eaf-121">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="73eaf-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="73eaf-122">-WorkspaceName</span></span>
<span data-ttu-id="73eaf-123">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="73eaf-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="73eaf-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="73eaf-124">-WorkspaceObject</span></span>
<span data-ttu-id="73eaf-125">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="73eaf-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="73eaf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73eaf-126">CommonParameters</span></span>
<span data-ttu-id="73eaf-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="73eaf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73eaf-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73eaf-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73eaf-129">輸入</span><span class="sxs-lookup"><span data-stu-id="73eaf-129">INPUTS</span></span>

### <span data-ttu-id="73eaf-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="73eaf-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="73eaf-131">輸出</span><span class="sxs-lookup"><span data-stu-id="73eaf-131">OUTPUTS</span></span>

### <span data-ttu-id="73eaf-132">System.Object</span><span class="sxs-lookup"><span data-stu-id="73eaf-132">System.Object</span></span>
## <span data-ttu-id="73eaf-133">筆記</span><span class="sxs-lookup"><span data-stu-id="73eaf-133">NOTES</span></span>

## <span data-ttu-id="73eaf-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="73eaf-134">RELATED LINKS</span></span>
