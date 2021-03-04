---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: cb7abd3c54d263ae9516344237588ecf9a1297ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916832"
---
# <span data-ttu-id="dc03f-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="dc03f-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="dc03f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dc03f-102">SYNOPSIS</span></span>
<span data-ttu-id="dc03f-103">檢查 Synapse Analytics Spark 資料庫是否存在。</span><span class="sxs-lookup"><span data-stu-id="dc03f-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="dc03f-104">語法</span><span class="sxs-lookup"><span data-stu-id="dc03f-104">SYNTAX</span></span>

### <span data-ttu-id="dc03f-105">TestByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dc03f-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc03f-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc03f-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc03f-107">描述</span><span class="sxs-lookup"><span data-stu-id="dc03f-107">DESCRIPTION</span></span>
<span data-ttu-id="dc03f-108">**Test-AzSynapseSparkPool** Cmdlet 會檢查 Synapse Analytics Spark Pool 是否存在。</span><span class="sxs-lookup"><span data-stu-id="dc03f-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="dc03f-109">例子</span><span class="sxs-lookup"><span data-stu-id="dc03f-109">EXAMPLES</span></span>

### <span data-ttu-id="dc03f-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="dc03f-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="dc03f-111">此命令會檢查指定的 Spark 資料庫是否存在。</span><span class="sxs-lookup"><span data-stu-id="dc03f-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="dc03f-112">參數</span><span class="sxs-lookup"><span data-stu-id="dc03f-112">PARAMETERS</span></span>

### <span data-ttu-id="dc03f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc03f-113">-DefaultProfile</span></span>
<span data-ttu-id="dc03f-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc03f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc03f-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc03f-115">-Name</span></span>
<span data-ttu-id="dc03f-116">Synapse Spark Pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc03f-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="dc03f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc03f-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc03f-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="dc03f-118">Resource group name.</span></span>

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

### <span data-ttu-id="dc03f-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dc03f-119">-WorkspaceName</span></span>
<span data-ttu-id="dc03f-120">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc03f-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="dc03f-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="dc03f-121">-WorkspaceObject</span></span>
<span data-ttu-id="dc03f-122">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="dc03f-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="dc03f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc03f-123">CommonParameters</span></span>
<span data-ttu-id="dc03f-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dc03f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc03f-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc03f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc03f-126">輸入</span><span class="sxs-lookup"><span data-stu-id="dc03f-126">INPUTS</span></span>

### <span data-ttu-id="dc03f-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dc03f-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="dc03f-128">輸出</span><span class="sxs-lookup"><span data-stu-id="dc03f-128">OUTPUTS</span></span>

### <span data-ttu-id="dc03f-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="dc03f-129">System.Object</span></span>
## <span data-ttu-id="dc03f-130">筆記</span><span class="sxs-lookup"><span data-stu-id="dc03f-130">NOTES</span></span>

## <span data-ttu-id="dc03f-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc03f-131">RELATED LINKS</span></span>
