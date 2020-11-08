---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: d07ec757fd5ab589de6234caac23992d6ff320fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136590"
---
# <span data-ttu-id="b272a-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b272a-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="b272a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b272a-102">SYNOPSIS</span></span>
<span data-ttu-id="b272a-103">檢查是否存在 Synapse Analytics SQL pool。</span><span class="sxs-lookup"><span data-stu-id="b272a-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b272a-104">句法</span><span class="sxs-lookup"><span data-stu-id="b272a-104">SYNTAX</span></span>

### <span data-ttu-id="b272a-105">TestByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b272a-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b272a-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b272a-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b272a-107">說明</span><span class="sxs-lookup"><span data-stu-id="b272a-107">DESCRIPTION</span></span>
<span data-ttu-id="b272a-108">**Test AzSynapseSqlPool** Cmdlet 會檢查是否存在 SYNAPSE 分析 SQL 池。</span><span class="sxs-lookup"><span data-stu-id="b272a-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b272a-109">示例</span><span class="sxs-lookup"><span data-stu-id="b272a-109">EXAMPLES</span></span>

### <span data-ttu-id="b272a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b272a-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="b272a-111">這個命令會檢查指定的 SQL pool 是否存在。</span><span class="sxs-lookup"><span data-stu-id="b272a-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="b272a-112">參數</span><span class="sxs-lookup"><span data-stu-id="b272a-112">PARAMETERS</span></span>

### <span data-ttu-id="b272a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b272a-113">-DefaultProfile</span></span>
<span data-ttu-id="b272a-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b272a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b272a-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b272a-115">-Name</span></span>
<span data-ttu-id="b272a-116">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b272a-116">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="b272a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b272a-117">-ResourceGroupName</span></span>
<span data-ttu-id="b272a-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b272a-118">Resource group name.</span></span>

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

### <span data-ttu-id="b272a-119">-版本</span><span class="sxs-lookup"><span data-stu-id="b272a-119">-Version</span></span>
<span data-ttu-id="b272a-120">Synapse SQL pool 的版本。</span><span class="sxs-lookup"><span data-stu-id="b272a-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="b272a-121">例如，2或3。</span><span class="sxs-lookup"><span data-stu-id="b272a-121">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="b272a-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b272a-122">-WorkspaceName</span></span>
<span data-ttu-id="b272a-123">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b272a-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b272a-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b272a-124">-WorkspaceObject</span></span>
<span data-ttu-id="b272a-125">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="b272a-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b272a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b272a-126">CommonParameters</span></span>
<span data-ttu-id="b272a-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b272a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b272a-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b272a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b272a-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b272a-129">INPUTS</span></span>

### <span data-ttu-id="b272a-130">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="b272a-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b272a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b272a-131">OUTPUTS</span></span>

### <span data-ttu-id="b272a-132">System.object</span><span class="sxs-lookup"><span data-stu-id="b272a-132">System.Object</span></span>
## <span data-ttu-id="b272a-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b272a-133">NOTES</span></span>

## <span data-ttu-id="b272a-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b272a-134">RELATED LINKS</span></span>
