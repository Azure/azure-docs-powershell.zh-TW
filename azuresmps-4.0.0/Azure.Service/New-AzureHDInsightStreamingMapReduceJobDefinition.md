---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 824F6302-6285-4AEC-A63C-E2519DE4C7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2597d66e87de682bbf5702085612f7338d75deac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967455"
---
# <span data-ttu-id="8f825-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8f825-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="8f825-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f825-102">SYNOPSIS</span></span>
<span data-ttu-id="8f825-103">定義新的流式處理 MapReduce 作業。</span><span class="sxs-lookup"><span data-stu-id="8f825-103">Defines a new streaming MapReduce job.</span></span>

## <span data-ttu-id="8f825-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f825-104">SYNTAX</span></span>

```
New-AzureHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-CmdEnv <String[]>]
 [-Combiner <String>] [-Defines <Hashtable>] [-Files <String[]>] [-InputPath <String>] [-JobName <String>]
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8f825-105">說明</span><span class="sxs-lookup"><span data-stu-id="8f825-105">DESCRIPTION</span></span>
<span data-ttu-id="8f825-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="8f825-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="8f825-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="8f825-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="8f825-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="8f825-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="8f825-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="8f825-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="8f825-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="8f825-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="8f825-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="8f825-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="8f825-112">**新的-AzureHDInsightStreamingMapReduceJobDefinition** Cmdlet 會定義一個代表 Hadoop 串流作業參數的新作業定義物件。</span><span class="sxs-lookup"><span data-stu-id="8f825-112">The **New-AzureHDInsightStreamingMapReduceJobDefinition** cmdlet defines a new job definition object that represents the parameters of a Hadoop streaming job.</span></span>

## <span data-ttu-id="8f825-113">示例</span><span class="sxs-lookup"><span data-stu-id="8f825-113">EXAMPLES</span></span>

### <span data-ttu-id="8f825-114">範例1：建立流式處理 MapReduce 作業定義</span><span class="sxs-lookup"><span data-stu-id="8f825-114">Example 1: Create a streaming MapReduce job definition</span></span>
```
PS C:\>$StreamingWordCount = New-AzureHDInsightStreamingMapReduceJobDefinition -Files "/Example/Apps/WordCount.exe", "/Example/Apps/Cat.exe" -InputPath "/Example/Data/Gutenberg/Davinci.txt" -OutputPath "/Example/Data/StreamingOutput/WordCount.txt" -Mapper "Cat.exe" -Reducer "WordCount.exe"
```

<span data-ttu-id="8f825-115">這個命令會建立指定的流式處理 MapReduce 作業定義，然後將它儲存在 $StreamingWordCount 變數中。</span><span class="sxs-lookup"><span data-stu-id="8f825-115">This command creates the specified streaming MapReduce job definition, and then stores it in the $StreamingWordCount variable.</span></span>

## <span data-ttu-id="8f825-116">參數</span><span class="sxs-lookup"><span data-stu-id="8f825-116">PARAMETERS</span></span>

### <span data-ttu-id="8f825-117">-引數</span><span class="sxs-lookup"><span data-stu-id="8f825-117">-Arguments</span></span>
<span data-ttu-id="8f825-118">指定 Hadoop 作業的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="8f825-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="8f825-119">引數會以命令列引數的形式傳遞給每個任務。</span><span class="sxs-lookup"><span data-stu-id="8f825-119">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Args

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f825-120">-CmdEnv</span><span class="sxs-lookup"><span data-stu-id="8f825-120">-CmdEnv</span></span>
<span data-ttu-id="8f825-121">指定要在工作在資料節點上執行作業時所設定的命令列環境變數陣列。</span><span class="sxs-lookup"><span data-stu-id="8f825-121">Specifies an array of command-line environment variables to set when a job runs on data nodes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f825-122">-Combiner</span><span class="sxs-lookup"><span data-stu-id="8f825-122">-Combiner</span></span>
<span data-ttu-id="8f825-123">指定 Combiner 檔案名。</span><span class="sxs-lookup"><span data-stu-id="8f825-123">Specifies a Combiner file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f825-124">-定義</span><span class="sxs-lookup"><span data-stu-id="8f825-124">-Defines</span></span>
<span data-ttu-id="8f825-125">指定要在作業執行時設定的 Hadoop 配置值。</span><span class="sxs-lookup"><span data-stu-id="8f825-125">Specifies Hadoop configuration values to set when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f825-126">-檔案</span><span class="sxs-lookup"><span data-stu-id="8f825-126">-Files</span></span>
<span data-ttu-id="8f825-127">指定作業所需的檔案陣列。</span><span class="sxs-lookup"><span data-stu-id="8f825-127">Specifies an array of files that are required for a job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f825-128">-InputPath</span><span class="sxs-lookup"><span data-stu-id="8f825-128">-InputPath</span></span>
<span data-ttu-id="8f825-129">指定輸入檔的 WASB 路徑。</span><span class="sxs-lookup"><span data-stu-id="8f825-129">Specifies the WASB path to the input files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Input

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f825-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="8f825-130">-JobName</span></span>
<span data-ttu-id="8f825-131">指定新的 MapReduce 作業定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f825-131">Specifies the name of the new MapReduce job definition.</span></span>
<span data-ttu-id="8f825-132">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="8f825-132">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f825-133">-映射器</span><span class="sxs-lookup"><span data-stu-id="8f825-133">-Mapper</span></span>
<span data-ttu-id="8f825-134">指定映射器檔案名。</span><span class="sxs-lookup"><span data-stu-id="8f825-134">Specifies a Mapper file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f825-135">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="8f825-135">-OutputPath</span></span>
<span data-ttu-id="8f825-136">指定作業輸出的 WASB 路徑。</span><span class="sxs-lookup"><span data-stu-id="8f825-136">Specifies the WASB path for the job output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Output

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f825-137">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8f825-137">-Profile</span></span>
<span data-ttu-id="8f825-138">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8f825-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8f825-139">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8f825-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f825-140">-Reducer</span><span class="sxs-lookup"><span data-stu-id="8f825-140">-Reducer</span></span>
<span data-ttu-id="8f825-141">指定 Reducer 檔案名。</span><span class="sxs-lookup"><span data-stu-id="8f825-141">Specifies a Reducer file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f825-142">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="8f825-142">-StatusFolder</span></span>
<span data-ttu-id="8f825-143">指定包含作業標準輸出和錯誤輸出的資料夾，包括其結束代碼和任務記錄。</span><span class="sxs-lookup"><span data-stu-id="8f825-143">Specifies the folder that contains the standard outputs and error outputs for the job, including its exit code and task logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f825-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f825-144">CommonParameters</span></span>
<span data-ttu-id="8f825-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f825-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f825-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f825-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f825-147">輸入</span><span class="sxs-lookup"><span data-stu-id="8f825-147">INPUTS</span></span>

## <span data-ttu-id="8f825-148">輸出</span><span class="sxs-lookup"><span data-stu-id="8f825-148">OUTPUTS</span></span>

## <span data-ttu-id="8f825-149">筆記</span><span class="sxs-lookup"><span data-stu-id="8f825-149">NOTES</span></span>

## <span data-ttu-id="8f825-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f825-150">RELATED LINKS</span></span>

[<span data-ttu-id="8f825-151">新-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8f825-151">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="8f825-152">新-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8f825-152">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="8f825-153">新-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8f825-153">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="8f825-154">新-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8f825-154">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)


