---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133387"
---
# <span data-ttu-id="4c7c0-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="4c7c0-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="4c7c0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c7c0-102">SYNOPSIS</span></span>
<span data-ttu-id="4c7c0-103">檢查是否存在 Synapse 分析 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="4c7c0-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="4c7c0-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c7c0-104">SYNTAX</span></span>

### <span data-ttu-id="4c7c0-105">TestByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4c7c0-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c7c0-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c7c0-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c7c0-107">說明</span><span class="sxs-lookup"><span data-stu-id="4c7c0-107">DESCRIPTION</span></span>
<span data-ttu-id="4c7c0-108">**Test AzSynapseSparkPool** Cmdlet 會檢查是否存在 Synapse 分析 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="4c7c0-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="4c7c0-109">示例</span><span class="sxs-lookup"><span data-stu-id="4c7c0-109">EXAMPLES</span></span>

### <span data-ttu-id="4c7c0-110">範例1</span><span class="sxs-lookup"><span data-stu-id="4c7c0-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="4c7c0-111">這個命令會檢查指定的 Spark 池是否存在。</span><span class="sxs-lookup"><span data-stu-id="4c7c0-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="4c7c0-112">參數</span><span class="sxs-lookup"><span data-stu-id="4c7c0-112">PARAMETERS</span></span>

### <span data-ttu-id="4c7c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c7c0-113">-DefaultProfile</span></span>
<span data-ttu-id="4c7c0-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c7c0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c7c0-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="4c7c0-115">-Name</span></span>
<span data-ttu-id="4c7c0-116">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c7c0-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="4c7c0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c7c0-117">-ResourceGroupName</span></span>
<span data-ttu-id="4c7c0-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4c7c0-118">Resource group name.</span></span>

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

### <span data-ttu-id="4c7c0-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4c7c0-119">-WorkspaceName</span></span>
<span data-ttu-id="4c7c0-120">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c7c0-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4c7c0-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4c7c0-121">-WorkspaceObject</span></span>
<span data-ttu-id="4c7c0-122">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="4c7c0-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4c7c0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c7c0-123">CommonParameters</span></span>
<span data-ttu-id="4c7c0-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c7c0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c7c0-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4c7c0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c7c0-126">輸入</span><span class="sxs-lookup"><span data-stu-id="4c7c0-126">INPUTS</span></span>

### <span data-ttu-id="4c7c0-127">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="4c7c0-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4c7c0-128">輸出</span><span class="sxs-lookup"><span data-stu-id="4c7c0-128">OUTPUTS</span></span>

### <span data-ttu-id="4c7c0-129">System.object</span><span class="sxs-lookup"><span data-stu-id="4c7c0-129">System.Object</span></span>
## <span data-ttu-id="4c7c0-130">筆記</span><span class="sxs-lookup"><span data-stu-id="4c7c0-130">NOTES</span></span>

## <span data-ttu-id="4c7c0-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c7c0-131">RELATED LINKS</span></span>
