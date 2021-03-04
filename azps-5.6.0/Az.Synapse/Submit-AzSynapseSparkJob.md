---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/submit-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
ms.openlocfilehash: 0555d9ba860d9a8c4c036fa9171d1fadc7a167eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916837"
---
# <span data-ttu-id="17f36-101">Submit-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="17f36-101">Submit-AzSynapseSparkJob</span></span>

## <span data-ttu-id="17f36-102">簡介</span><span class="sxs-lookup"><span data-stu-id="17f36-102">SYNOPSIS</span></span>
<span data-ttu-id="17f36-103">提交 Synapse Analytics Spark 工作。</span><span class="sxs-lookup"><span data-stu-id="17f36-103">Submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="17f36-104">語法</span><span class="sxs-lookup"><span data-stu-id="17f36-104">SYNTAX</span></span>

### <span data-ttu-id="17f36-105">RunSparkJobParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="17f36-105">RunSparkJobParameterSetName (Default)</span></span>
```
Submit-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f36-106">RunSparkJobByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17f36-106">RunSparkJobByParentObjectParameterSet</span></span>
```
Submit-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17f36-107">描述</span><span class="sxs-lookup"><span data-stu-id="17f36-107">DESCRIPTION</span></span>
<span data-ttu-id="17f36-108">**Submit-AzSynapseSparkJob** Cmdlet 會提交 Synapse Analytics Spark 工作。</span><span class="sxs-lookup"><span data-stu-id="17f36-108">The **Submit-AzSynapseSparkJob** cmdlet submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="17f36-109">例子</span><span class="sxs-lookup"><span data-stu-id="17f36-109">EXAMPLES</span></span>

### <span data-ttu-id="17f36-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="17f36-110">Example 1</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language Spark -Name WordCount_Java -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/wordcount.jar -MainClassName WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="17f36-111">此命令會提交 Synapse Analytics Spark 工作。</span><span class="sxs-lookup"><span data-stu-id="17f36-111">This command submits a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="17f36-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="17f36-112">Example 2</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language SparkDotNet -Name WordCount_Dotnet -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/wordcount.zip -MainExecutableFile WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/result -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="17f36-113">此命令會提交 Synapse Analytics Spark .NET 工作。</span><span class="sxs-lookup"><span data-stu-id="17f36-113">This command submits a Synapse Analytics Spark .NET job.</span></span>

### <span data-ttu-id="17f36-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="17f36-114">Example 3</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language PySpark -Name WordCount_Python -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/wordcount.py -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="17f36-115">此命令會提交 Synapse Analytics PySpark 工作。</span><span class="sxs-lookup"><span data-stu-id="17f36-115">This command submits a Synapse Analytics PySpark job.</span></span>

## <span data-ttu-id="17f36-116">參數</span><span class="sxs-lookup"><span data-stu-id="17f36-116">PARAMETERS</span></span>

### <span data-ttu-id="17f36-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="17f36-117">-CommandLineArgument</span></span>
<span data-ttu-id="17f36-118">工作的選擇性引數。</span><span class="sxs-lookup"><span data-stu-id="17f36-118">Optional arguments to the job.</span></span> <span data-ttu-id="17f36-119">例如"--iteration 10000 --timeout 20s"</span><span class="sxs-lookup"><span data-stu-id="17f36-119">e.g. "--iteration 10000 --timeout 20s"</span></span>

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

### <span data-ttu-id="17f36-120">-組式</span><span class="sxs-lookup"><span data-stu-id="17f36-120">-Configuration</span></span>
<span data-ttu-id="17f36-121">Spark 組組屬性。</span><span class="sxs-lookup"><span data-stu-id="17f36-121">Spark configuration properties.</span></span>

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

### <span data-ttu-id="17f36-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f36-122">-DefaultProfile</span></span>
<span data-ttu-id="17f36-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="17f36-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17f36-124">-執行器計數</span><span class="sxs-lookup"><span data-stu-id="17f36-124">-ExecutorCount</span></span>
<span data-ttu-id="17f36-125">要配置於指定工作之 Spark 區中的執行者數目。</span><span class="sxs-lookup"><span data-stu-id="17f36-125">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="17f36-126">-執行器Size</span><span class="sxs-lookup"><span data-stu-id="17f36-126">-ExecutorSize</span></span>
<span data-ttu-id="17f36-127">要用於指定工作之 Spark 資料集中之執行者的核心和記憶體數目。</span><span class="sxs-lookup"><span data-stu-id="17f36-127">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="17f36-128">-語言</span><span class="sxs-lookup"><span data-stu-id="17f36-128">-Language</span></span>
<span data-ttu-id="17f36-129">要送出的工作語言。</span><span class="sxs-lookup"><span data-stu-id="17f36-129">Language of the job to submit.</span></span>

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

### <span data-ttu-id="17f36-130">-MainClassName</span><span class="sxs-lookup"><span data-stu-id="17f36-130">-MainClassName</span></span>
<span data-ttu-id="17f36-131">完整識別碼或主要定義檔案中的主要類別。</span><span class="sxs-lookup"><span data-stu-id="17f36-131">The fully-qualified identifier or the main class that is in the main definition file.</span></span>
<span data-ttu-id="17f36-132">Spark 和 .NET Spark 工作所需的專案。</span><span class="sxs-lookup"><span data-stu-id="17f36-132">Required for Spark and .NET Spark job.</span></span>
<span data-ttu-id="17f36-133">例如"org.apache.spark.examples.SparkPi"</span><span class="sxs-lookup"><span data-stu-id="17f36-133">e.g. "org.apache.spark.examples.SparkPi"</span></span>

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

### <span data-ttu-id="17f36-134">-MainDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="17f36-134">-MainDefinitionFile</span></span>
<span data-ttu-id="17f36-135">工作所使用的主檔案。</span><span class="sxs-lookup"><span data-stu-id="17f36-135">The main file used for the job.</span></span>
<span data-ttu-id="17f36-136">例如 " abfss://filesystem@account.dfs.core.windows.net/mySpark.jar "</span><span class="sxs-lookup"><span data-stu-id="17f36-136">e.g. "abfss://filesystem@account.dfs.core.windows.net/mySpark.jar"</span></span>

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

### <span data-ttu-id="17f36-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="17f36-137">-Name</span></span>
<span data-ttu-id="17f36-138">Spark 工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="17f36-138">Name of Spark job.</span></span>

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

### <span data-ttu-id="17f36-139">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="17f36-139">-ReferenceFile</span></span>
<span data-ttu-id="17f36-140">用於主要定義檔案中供參考的其他檔案。</span><span class="sxs-lookup"><span data-stu-id="17f36-140">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="17f36-141">逗號分隔儲存 URI 清單。</span><span class="sxs-lookup"><span data-stu-id="17f36-141">Comma-separated storage URI list.</span></span> <span data-ttu-id="17f36-142">例如 " abfss://filesystem@account.dfs.core.windows.net/file1.txt ， abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="17f36-142">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="17f36-143">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="17f36-143">-SparkPoolName</span></span>
<span data-ttu-id="17f36-144">Synapse Spark Pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="17f36-144">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="17f36-145">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="17f36-145">-SparkPoolObject</span></span>
<span data-ttu-id="17f36-146">Spark Pool 輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="17f36-146">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="17f36-147">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="17f36-147">-WorkspaceName</span></span>
<span data-ttu-id="17f36-148">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="17f36-148">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="17f36-149">-確認</span><span class="sxs-lookup"><span data-stu-id="17f36-149">-Confirm</span></span>
<span data-ttu-id="17f36-150">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="17f36-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17f36-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17f36-151">-WhatIf</span></span>
<span data-ttu-id="17f36-152">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="17f36-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17f36-153">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="17f36-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17f36-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f36-154">CommonParameters</span></span>
<span data-ttu-id="17f36-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="17f36-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f36-156">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17f36-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f36-157">輸入</span><span class="sxs-lookup"><span data-stu-id="17f36-157">INPUTS</span></span>

### <span data-ttu-id="17f36-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="17f36-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="17f36-159">輸出</span><span class="sxs-lookup"><span data-stu-id="17f36-159">OUTPUTS</span></span>

### <span data-ttu-id="17f36-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="17f36-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="17f36-161">筆記</span><span class="sxs-lookup"><span data-stu-id="17f36-161">NOTES</span></span>

## <span data-ttu-id="17f36-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="17f36-162">RELATED LINKS</span></span>
