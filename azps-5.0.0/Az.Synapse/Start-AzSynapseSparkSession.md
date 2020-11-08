---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
ms.openlocfilehash: b066807d812fc9a74b36b2826cc978589d39ea49
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139404"
---
# <span data-ttu-id="6f5d4-101">Start-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="6f5d4-101">Start-AzSynapseSparkSession</span></span>

## <span data-ttu-id="6f5d4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="6f5d4-103">啟動 Synapse 分析 Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-103">Starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="6f5d4-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f5d4-104">SYNTAX</span></span>

### <span data-ttu-id="6f5d4-105">CreateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6f5d4-105">CreateByNameParameterSet (Default)</span></span>
```
Start-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f5d4-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f5d4-106">CreateByParentObjectParameterSet</span></span>
```
Start-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f5d4-107">說明</span><span class="sxs-lookup"><span data-stu-id="6f5d4-107">DESCRIPTION</span></span>
<span data-ttu-id="6f5d4-108">**Start-AzSynapseSparkSession** Cmdlet 會啟動 Synapse 分析 Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-108">The **Start-AzSynapseSparkSession** cmdlet starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="6f5d4-109">示例</span><span class="sxs-lookup"><span data-stu-id="6f5d4-109">EXAMPLES</span></span>

### <span data-ttu-id="6f5d4-110">範例1</span><span class="sxs-lookup"><span data-stu-id="6f5d4-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="6f5d4-111">這個命令會啟動 Azure Synapse 分析 Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-111">This command starts an Azure Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="6f5d4-112">範例2</span><span class="sxs-lookup"><span data-stu-id="6f5d4-112">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Start-AzSynapseSparkSession -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="6f5d4-113">這個命令會啟動經由管線的 Azure Synapse 分析 Spark 會話。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-113">This command starts an Azure Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="6f5d4-114">參數</span><span class="sxs-lookup"><span data-stu-id="6f5d4-114">PARAMETERS</span></span>

### <span data-ttu-id="6f5d4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f5d4-115">-AsJob</span></span>
<span data-ttu-id="6f5d4-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6f5d4-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5d4-117">-配置</span><span class="sxs-lookup"><span data-stu-id="6f5d4-117">-Configuration</span></span>
<span data-ttu-id="6f5d4-118">Spark 配置屬性。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-118">Spark configuration properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f5d4-119">-DefaultProfile</span></span>
<span data-ttu-id="6f5d4-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f5d4-121">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="6f5d4-121">-ExecutorCount</span></span>
<span data-ttu-id="6f5d4-122">要在指定的 Spark 池中為作業指派的執行次數。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-122">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5d4-123">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="6f5d4-123">-ExecutorSize</span></span>
<span data-ttu-id="6f5d4-124">在作業的指定 Spark 池中，要用於執行程式的核心和記憶體數目。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-124">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5d4-125">-語言</span><span class="sxs-lookup"><span data-stu-id="6f5d4-125">-Language</span></span>
<span data-ttu-id="6f5d4-126">執行程式碼的語言。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-126">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5d4-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f5d4-127">-Name</span></span>
<span data-ttu-id="6f5d4-128">Spark 會話的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-128">Name of Spark session.</span></span>

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

### <span data-ttu-id="6f5d4-129">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="6f5d4-129">-ReferenceFile</span></span>
<span data-ttu-id="6f5d4-130">在主要定義檔案中用於參考的其他檔案。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-130">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="6f5d4-131">以逗號分隔的儲存空間 URI 清單。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-131">Comma-separated storage URI list.</span></span> <span data-ttu-id="6f5d4-132">例如 " abfss://filesystem@account.dfs.core.windows.net/file1.txt ， abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="6f5d4-132">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5d4-133">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="6f5d4-133">-SparkPoolName</span></span>
<span data-ttu-id="6f5d4-134">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-134">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5d4-135">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="6f5d4-135">-SparkPoolObject</span></span>
<span data-ttu-id="6f5d4-136">Spark 池輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-136">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f5d4-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6f5d4-137">-WorkspaceName</span></span>
<span data-ttu-id="6f5d4-138">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5d4-139">-確認</span><span class="sxs-lookup"><span data-stu-id="6f5d4-139">-Confirm</span></span>
<span data-ttu-id="6f5d4-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5d4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f5d4-141">-WhatIf</span></span>
<span data-ttu-id="6f5d4-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f5d4-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5d4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f5d4-144">CommonParameters</span></span>
<span data-ttu-id="6f5d4-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f5d4-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f5d4-147">輸入</span><span class="sxs-lookup"><span data-stu-id="6f5d4-147">INPUTS</span></span>

### <span data-ttu-id="6f5d4-148">PSSynapseSparkPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="6f5d4-149">輸出</span><span class="sxs-lookup"><span data-stu-id="6f5d4-149">OUTPUTS</span></span>

### <span data-ttu-id="6f5d4-150">PSSynapseSparkSession 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="6f5d4-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="6f5d4-151">筆記</span><span class="sxs-lookup"><span data-stu-id="6f5d4-151">NOTES</span></span>

## <span data-ttu-id="6f5d4-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f5d4-152">RELATED LINKS</span></span>
