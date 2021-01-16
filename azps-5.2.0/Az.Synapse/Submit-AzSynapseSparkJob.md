---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/submit-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
ms.openlocfilehash: c8e710db383aae6698278ac4fb5ad7eb4344641b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280062"
---
# <span data-ttu-id="948c1-101">Submit-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="948c1-101">Submit-AzSynapseSparkJob</span></span>

## <span data-ttu-id="948c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="948c1-102">SYNOPSIS</span></span>
<span data-ttu-id="948c1-103">提交 Synapse 分析 Spark 作業。</span><span class="sxs-lookup"><span data-stu-id="948c1-103">Submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="948c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="948c1-104">SYNTAX</span></span>

### <span data-ttu-id="948c1-105">RunSparkJobParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="948c1-105">RunSparkJobParameterSetName (Default)</span></span>
```
Submit-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="948c1-106">RunSparkJobByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="948c1-106">RunSparkJobByParentObjectParameterSet</span></span>
```
Submit-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="948c1-107">說明</span><span class="sxs-lookup"><span data-stu-id="948c1-107">DESCRIPTION</span></span>
<span data-ttu-id="948c1-108">**AzSynapseSparkJob** Cmdlet 會提交 Synapse 分析 Spark 作業。</span><span class="sxs-lookup"><span data-stu-id="948c1-108">The **Submit-AzSynapseSparkJob** cmdlet submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="948c1-109">示例</span><span class="sxs-lookup"><span data-stu-id="948c1-109">EXAMPLES</span></span>

### <span data-ttu-id="948c1-110">範例1</span><span class="sxs-lookup"><span data-stu-id="948c1-110">Example 1</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language Spark -Name WordCount_Java -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/wordcount.jar -MainClassName WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="948c1-111">這個命令會提交 Synapse 分析 Spark 作業。</span><span class="sxs-lookup"><span data-stu-id="948c1-111">This command submits a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="948c1-112">範例2</span><span class="sxs-lookup"><span data-stu-id="948c1-112">Example 2</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language SparkDotNet -Name WordCount_Dotnet -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/wordcount.zip -MainExecutableFile WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/result -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="948c1-113">這個命令會提交 Synapse 分析 Spark .NET 作業。</span><span class="sxs-lookup"><span data-stu-id="948c1-113">This command submits a Synapse Analytics Spark .NET job.</span></span>

### <span data-ttu-id="948c1-114">範例3</span><span class="sxs-lookup"><span data-stu-id="948c1-114">Example 3</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language PySpark -Name WordCount_Python -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/wordcount.py -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="948c1-115">這個命令會提交 Synapse 分析 PySpark 作業。</span><span class="sxs-lookup"><span data-stu-id="948c1-115">This command submits a Synapse Analytics PySpark job.</span></span>

## <span data-ttu-id="948c1-116">參數</span><span class="sxs-lookup"><span data-stu-id="948c1-116">PARAMETERS</span></span>

### <span data-ttu-id="948c1-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="948c1-117">-CommandLineArgument</span></span>
<span data-ttu-id="948c1-118">作業的選擇性引數。</span><span class="sxs-lookup"><span data-stu-id="948c1-118">Optional arguments to the job.</span></span> <span data-ttu-id="948c1-119">例如，"--反覆運算 10000--timeout 20s"</span><span class="sxs-lookup"><span data-stu-id="948c1-119">e.g. "--iteration 10000 --timeout 20s"</span></span>

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

### <span data-ttu-id="948c1-120">-配置</span><span class="sxs-lookup"><span data-stu-id="948c1-120">-Configuration</span></span>
<span data-ttu-id="948c1-121">Spark 配置屬性。</span><span class="sxs-lookup"><span data-stu-id="948c1-121">Spark configuration properties.</span></span>

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

### <span data-ttu-id="948c1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="948c1-122">-DefaultProfile</span></span>
<span data-ttu-id="948c1-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="948c1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="948c1-124">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="948c1-124">-ExecutorCount</span></span>
<span data-ttu-id="948c1-125">要在指定的 Spark 池中為作業指派的執行次數。</span><span class="sxs-lookup"><span data-stu-id="948c1-125">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="948c1-126">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="948c1-126">-ExecutorSize</span></span>
<span data-ttu-id="948c1-127">在作業的指定 Spark 池中，要用於執行程式的核心和記憶體數目。</span><span class="sxs-lookup"><span data-stu-id="948c1-127">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="948c1-128">-語言</span><span class="sxs-lookup"><span data-stu-id="948c1-128">-Language</span></span>
<span data-ttu-id="948c1-129">要提交的作業語言。</span><span class="sxs-lookup"><span data-stu-id="948c1-129">Language of the job to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="948c1-130">-MainClassName</span><span class="sxs-lookup"><span data-stu-id="948c1-130">-MainClassName</span></span>
<span data-ttu-id="948c1-131">在主要定義檔案中的完整識別碼或主要類別。</span><span class="sxs-lookup"><span data-stu-id="948c1-131">The fully-qualified identifier or the main class that is in the main definition file.</span></span>
<span data-ttu-id="948c1-132">對於 Spark 和 .NET Spark 作業是必要的。</span><span class="sxs-lookup"><span data-stu-id="948c1-132">Required for Spark and .NET Spark job.</span></span>
<span data-ttu-id="948c1-133">例如，"org. SparkPi"</span><span class="sxs-lookup"><span data-stu-id="948c1-133">e.g. "org.apache.spark.examples.SparkPi"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MainExecutableFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="948c1-134">-MainDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="948c1-134">-MainDefinitionFile</span></span>
<span data-ttu-id="948c1-135">作業所用的主要檔案。</span><span class="sxs-lookup"><span data-stu-id="948c1-135">The main file used for the job.</span></span>
<span data-ttu-id="948c1-136">例如 " abfss://filesystem@account.dfs.core.windows.net/mySpark.jar "</span><span class="sxs-lookup"><span data-stu-id="948c1-136">e.g. "abfss://filesystem@account.dfs.core.windows.net/mySpark.jar"</span></span>

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

### <span data-ttu-id="948c1-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="948c1-137">-Name</span></span>
<span data-ttu-id="948c1-138">Spark 作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="948c1-138">Name of Spark job.</span></span>

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

### <span data-ttu-id="948c1-139">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="948c1-139">-ReferenceFile</span></span>
<span data-ttu-id="948c1-140">在主要定義檔案中用於參考的其他檔案。</span><span class="sxs-lookup"><span data-stu-id="948c1-140">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="948c1-141">以逗號分隔的儲存空間 URI 清單。</span><span class="sxs-lookup"><span data-stu-id="948c1-141">Comma-separated storage URI list.</span></span> <span data-ttu-id="948c1-142">例如 " abfss://filesystem@account.dfs.core.windows.net/file1.txt ， abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="948c1-142">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="948c1-143">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="948c1-143">-SparkPoolName</span></span>
<span data-ttu-id="948c1-144">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="948c1-144">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="948c1-145">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="948c1-145">-SparkPoolObject</span></span>
<span data-ttu-id="948c1-146">Spark 池輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="948c1-146">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: RunSparkJobByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="948c1-147">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="948c1-147">-WorkspaceName</span></span>
<span data-ttu-id="948c1-148">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="948c1-148">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="948c1-149">-確認</span><span class="sxs-lookup"><span data-stu-id="948c1-149">-Confirm</span></span>
<span data-ttu-id="948c1-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="948c1-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="948c1-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="948c1-151">-WhatIf</span></span>
<span data-ttu-id="948c1-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="948c1-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="948c1-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="948c1-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="948c1-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948c1-154">CommonParameters</span></span>
<span data-ttu-id="948c1-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="948c1-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="948c1-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="948c1-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948c1-157">輸入</span><span class="sxs-lookup"><span data-stu-id="948c1-157">INPUTS</span></span>

### <span data-ttu-id="948c1-158">PSSynapseSparkPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="948c1-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="948c1-159">輸出</span><span class="sxs-lookup"><span data-stu-id="948c1-159">OUTPUTS</span></span>

### <span data-ttu-id="948c1-160">PSSynapseSparkJob 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="948c1-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="948c1-161">筆記</span><span class="sxs-lookup"><span data-stu-id="948c1-161">NOTES</span></span>

## <span data-ttu-id="948c1-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="948c1-162">RELATED LINKS</span></span>
