---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: c7137e9fda6c947755c8bd2e0091dd33347027fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285064"
---
# <span data-ttu-id="6dc36-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="6dc36-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="6dc36-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6dc36-102">SYNOPSIS</span></span>
<span data-ttu-id="6dc36-103">等待 Synapse 分析 Spark 作業完成。</span><span class="sxs-lookup"><span data-stu-id="6dc36-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="6dc36-104">句法</span><span class="sxs-lookup"><span data-stu-id="6dc36-104">SYNTAX</span></span>

### <span data-ttu-id="6dc36-105">WaitSparkJobByIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6dc36-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6dc36-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dc36-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dc36-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dc36-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dc36-108">說明</span><span class="sxs-lookup"><span data-stu-id="6dc36-108">DESCRIPTION</span></span>
<span data-ttu-id="6dc36-109">**AzSynapseSparkJob** Cmdlet 會等待 Azure Synapse 分析作業完成。</span><span class="sxs-lookup"><span data-stu-id="6dc36-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="6dc36-110">示例</span><span class="sxs-lookup"><span data-stu-id="6dc36-110">EXAMPLES</span></span>

### <span data-ttu-id="6dc36-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6dc36-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="6dc36-112">這個命令會等待具有指定識別碼的作業完成。</span><span class="sxs-lookup"><span data-stu-id="6dc36-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="6dc36-113">參數</span><span class="sxs-lookup"><span data-stu-id="6dc36-113">PARAMETERS</span></span>

### <span data-ttu-id="6dc36-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dc36-114">-DefaultProfile</span></span>
<span data-ttu-id="6dc36-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6dc36-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dc36-116">-LivyId</span><span class="sxs-lookup"><span data-stu-id="6dc36-116">-LivyId</span></span>
<span data-ttu-id="6dc36-117">Spark 作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6dc36-117">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdParameterSet, WaitSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc36-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="6dc36-118">-SparkJobObject</span></span>
<span data-ttu-id="6dc36-119">Spark 作業輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="6dc36-119">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6dc36-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="6dc36-120">-SparkPoolName</span></span>
<span data-ttu-id="6dc36-121">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="6dc36-121">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc36-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="6dc36-122">-SparkPoolObject</span></span>
<span data-ttu-id="6dc36-123">Spark 池輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="6dc36-123">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: WaitSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6dc36-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="6dc36-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="6dc36-125">在 erroring 超時之前所需等待的最長時間。預設值為永不超時。</span><span class="sxs-lookup"><span data-stu-id="6dc36-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="6dc36-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="6dc36-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="6dc36-127">作業狀態檢查的輪詢間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6dc36-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="6dc36-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6dc36-128">-WorkspaceName</span></span>
<span data-ttu-id="6dc36-129">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="6dc36-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc36-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dc36-130">CommonParameters</span></span>
<span data-ttu-id="6dc36-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6dc36-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dc36-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6dc36-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dc36-133">輸入</span><span class="sxs-lookup"><span data-stu-id="6dc36-133">INPUTS</span></span>

### <span data-ttu-id="6dc36-134">PSSynapseSparkPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="6dc36-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="6dc36-135">PSSynapseSparkJob 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="6dc36-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="6dc36-136">輸出</span><span class="sxs-lookup"><span data-stu-id="6dc36-136">OUTPUTS</span></span>

### <span data-ttu-id="6dc36-137">System.object</span><span class="sxs-lookup"><span data-stu-id="6dc36-137">System.Boolean</span></span>

## <span data-ttu-id="6dc36-138">筆記</span><span class="sxs-lookup"><span data-stu-id="6dc36-138">NOTES</span></span>

## <span data-ttu-id="6dc36-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="6dc36-139">RELATED LINKS</span></span>
