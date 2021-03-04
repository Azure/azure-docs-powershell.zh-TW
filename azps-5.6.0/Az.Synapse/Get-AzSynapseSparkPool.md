---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: 48ecf7e0c840ca5054e19a250bc53d95de82c08d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917858"
---
# <span data-ttu-id="46395-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="46395-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="46395-102">簡介</span><span class="sxs-lookup"><span data-stu-id="46395-102">SYNOPSIS</span></span>
<span data-ttu-id="46395-103">獲得 Synapse Analytics Spark Pool。</span><span class="sxs-lookup"><span data-stu-id="46395-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="46395-104">語法</span><span class="sxs-lookup"><span data-stu-id="46395-104">SYNTAX</span></span>

### <span data-ttu-id="46395-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="46395-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46395-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46395-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46395-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46395-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46395-108">描述</span><span class="sxs-lookup"><span data-stu-id="46395-108">DESCRIPTION</span></span>
<span data-ttu-id="46395-109">**Get-AzSynapseSparkPool** Cmdlet 會取得有關 Azure Synapse Analytics Spark 資料庫的資訊。</span><span class="sxs-lookup"><span data-stu-id="46395-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="46395-110">例子</span><span class="sxs-lookup"><span data-stu-id="46395-110">EXAMPLES</span></span>

### <span data-ttu-id="46395-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="46395-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="46395-112">此命令會獲得工作區下的所有 Spark 資料庫。</span><span class="sxs-lookup"><span data-stu-id="46395-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="46395-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="46395-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="46395-114">此命令會獲得 Workspace ContosoWorkspace 下的 Spark 資料格，名稱為 ContosoSparkPool。</span><span class="sxs-lookup"><span data-stu-id="46395-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="46395-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="46395-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="46395-116">此命令會透過管線在工作區下的所有 Spark 資料庫。</span><span class="sxs-lookup"><span data-stu-id="46395-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="46395-117">範例 4</span><span class="sxs-lookup"><span data-stu-id="46395-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="46395-118">此命令會獲得具有指定資源識別碼的 Spark 資料庫。</span><span class="sxs-lookup"><span data-stu-id="46395-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="46395-119">參數</span><span class="sxs-lookup"><span data-stu-id="46395-119">PARAMETERS</span></span>

### <span data-ttu-id="46395-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46395-120">-DefaultProfile</span></span>
<span data-ttu-id="46395-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="46395-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46395-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="46395-122">-Name</span></span>
<span data-ttu-id="46395-123">Synapse Spark Pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="46395-123">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SparkPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46395-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46395-124">-ResourceGroupName</span></span>
<span data-ttu-id="46395-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="46395-125">Resource group name.</span></span>

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

### <span data-ttu-id="46395-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46395-126">-ResourceId</span></span>
<span data-ttu-id="46395-127">Synapse Spark 資料格的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="46395-127">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="46395-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="46395-128">-WorkspaceName</span></span>
<span data-ttu-id="46395-129">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="46395-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="46395-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="46395-130">-WorkspaceObject</span></span>
<span data-ttu-id="46395-131">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="46395-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="46395-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46395-132">CommonParameters</span></span>
<span data-ttu-id="46395-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="46395-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46395-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46395-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46395-135">輸入</span><span class="sxs-lookup"><span data-stu-id="46395-135">INPUTS</span></span>

### <span data-ttu-id="46395-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="46395-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="46395-137">輸出</span><span class="sxs-lookup"><span data-stu-id="46395-137">OUTPUTS</span></span>

### <span data-ttu-id="46395-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="46395-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="46395-139">筆記</span><span class="sxs-lookup"><span data-stu-id="46395-139">NOTES</span></span>

## <span data-ttu-id="46395-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="46395-140">RELATED LINKS</span></span>
