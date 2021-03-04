---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: fa658b7727c07b7457c2a10c1ac42e3fdb5fe347
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916452"
---
# <span data-ttu-id="37f81-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="37f81-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="37f81-102">簡介</span><span class="sxs-lookup"><span data-stu-id="37f81-102">SYNOPSIS</span></span>
<span data-ttu-id="37f81-103">等待 Synapse Analytics Spark 工作完成。</span><span class="sxs-lookup"><span data-stu-id="37f81-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="37f81-104">語法</span><span class="sxs-lookup"><span data-stu-id="37f81-104">SYNTAX</span></span>

### <span data-ttu-id="37f81-105">WaitSparkJobByIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="37f81-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37f81-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37f81-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37f81-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37f81-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37f81-108">描述</span><span class="sxs-lookup"><span data-stu-id="37f81-108">DESCRIPTION</span></span>
<span data-ttu-id="37f81-109">**Wait-AzSynapseSparkJob** Cmdlet 會等待 Azure Synapse Analytics 工作完成。</span><span class="sxs-lookup"><span data-stu-id="37f81-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="37f81-110">例子</span><span class="sxs-lookup"><span data-stu-id="37f81-110">EXAMPLES</span></span>

### <span data-ttu-id="37f81-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="37f81-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="37f81-112">此命令會等待具有指定識別碼的工作完成。</span><span class="sxs-lookup"><span data-stu-id="37f81-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="37f81-113">參數</span><span class="sxs-lookup"><span data-stu-id="37f81-113">PARAMETERS</span></span>

### <span data-ttu-id="37f81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37f81-114">-DefaultProfile</span></span>
<span data-ttu-id="37f81-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="37f81-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37f81-116">-利維Id</span><span class="sxs-lookup"><span data-stu-id="37f81-116">-LivyId</span></span>
<span data-ttu-id="37f81-117">Spark 工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="37f81-117">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="37f81-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="37f81-118">-SparkJobObject</span></span>
<span data-ttu-id="37f81-119">觸發工作輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="37f81-119">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="37f81-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="37f81-120">-SparkPoolName</span></span>
<span data-ttu-id="37f81-121">Synapse Spark Pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="37f81-121">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="37f81-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="37f81-122">-SparkPoolObject</span></span>
<span data-ttu-id="37f81-123">Spark Pool 輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="37f81-123">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="37f81-124">-TimeoutIn TimeoutIn Timeouts</span><span class="sxs-lookup"><span data-stu-id="37f81-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="37f81-125">在錯誤前等待的時間上限。預設值為永不超時。</span><span class="sxs-lookup"><span data-stu-id="37f81-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="37f81-126">-WaitIntervalIn用秒</span><span class="sxs-lookup"><span data-stu-id="37f81-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="37f81-127">檢查工作狀態之間的輪詢間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="37f81-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="37f81-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="37f81-128">-WorkspaceName</span></span>
<span data-ttu-id="37f81-129">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="37f81-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="37f81-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37f81-130">CommonParameters</span></span>
<span data-ttu-id="37f81-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="37f81-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37f81-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37f81-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37f81-133">輸入</span><span class="sxs-lookup"><span data-stu-id="37f81-133">INPUTS</span></span>

### <span data-ttu-id="37f81-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="37f81-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="37f81-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="37f81-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="37f81-136">輸出</span><span class="sxs-lookup"><span data-stu-id="37f81-136">OUTPUTS</span></span>

### <span data-ttu-id="37f81-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="37f81-137">System.Boolean</span></span>

## <span data-ttu-id="37f81-138">筆記</span><span class="sxs-lookup"><span data-stu-id="37f81-138">NOTES</span></span>

## <span data-ttu-id="37f81-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="37f81-139">RELATED LINKS</span></span>
