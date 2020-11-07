---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 227D933A-9272-4C53-89AF-711379B47A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c32a80bec0820123a8ccf1a85f5c99bdac3195d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967456"
---
# <span data-ttu-id="3705d-101">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3705d-101">New-AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="3705d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3705d-102">SYNOPSIS</span></span>
<span data-ttu-id="3705d-103">為 HDInsight 服務定義新的豬作業。</span><span class="sxs-lookup"><span data-stu-id="3705d-103">Defines a new Pig job for an HDInsight service.</span></span>

## <span data-ttu-id="3705d-104">句法</span><span class="sxs-lookup"><span data-stu-id="3705d-104">SYNTAX</span></span>

```
New-AzureHDInsightPigJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-Query <String>] [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3705d-105">說明</span><span class="sxs-lookup"><span data-stu-id="3705d-105">DESCRIPTION</span></span>
<span data-ttu-id="3705d-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="3705d-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="3705d-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="3705d-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="3705d-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="3705d-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="3705d-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="3705d-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="3705d-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="3705d-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="3705d-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="3705d-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="3705d-112">**新-AzureHDInsightPigJobDefinition** 會定義 Azure HDInsight 服務的豬作業。</span><span class="sxs-lookup"><span data-stu-id="3705d-112">The **New-AzureHDInsightPigJobDefinition** defines a Pig job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="3705d-113">示例</span><span class="sxs-lookup"><span data-stu-id="3705d-113">EXAMPLES</span></span>

### <span data-ttu-id="3705d-114">範例1：定義新的豬工作</span><span class="sxs-lookup"><span data-stu-id="3705d-114">Example 1: Define a new Pig job</span></span>
```
PS C:\>$0 = '$0';
PS C:\> $QueryString =  "LOGS = LOAD 'wasb:///example/data/sample.log';" + "LEVELS = foreach LOGS generate REGEX_EXTRACT($0, '(TRACE|DEBUG|INFO|WARN|ERROR|FATAL)', 1) as LOGLEVEL;" + "FILTEREDLEVELS = FILTER LEVELS by LOGLEVEL is not null;" + "GROUPEDLEVELS = GROUP FILTEREDLEVELS by LOGLEVEL;" + "FREQUENCIES = foreach GROUPEDLEVELS generate group as LOGLEVEL, COUNT(FILTEREDLEVELS.LOGLEVEL) as COUNT;" + "RESULT = order FREQUENCIES by COUNT desc;" + "DUMP RESULT;"
PS C:\> $PigJobDefinition = New-AzureHDInsightPigJobDefinition -Query $QueryString
```

<span data-ttu-id="3705d-115">第一個命令會宣告字串值，然後將其儲存在 $0 變數中。</span><span class="sxs-lookup"><span data-stu-id="3705d-115">The first command declares a string value, and then stores in the $0 variable.</span></span>

<span data-ttu-id="3705d-116">第二個命令會建立豬工作查詢，然後將它儲存在 $QueryString 變數中。</span><span class="sxs-lookup"><span data-stu-id="3705d-116">The second command creates a Pig job query, and then stores it in the $QueryString variable.</span></span>

<span data-ttu-id="3705d-117">最後一個命令會建立在 $QueryString 中使用查詢的豬作業定義，然後將作業定義儲存在 $PigJobDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="3705d-117">The final command creates a Pig job definition that uses the query in $QueryString, and then stores the job definition in the $PigJobDefinition variable.</span></span>

## <span data-ttu-id="3705d-118">參數</span><span class="sxs-lookup"><span data-stu-id="3705d-118">PARAMETERS</span></span>

### <span data-ttu-id="3705d-119">-引數</span><span class="sxs-lookup"><span data-stu-id="3705d-119">-Arguments</span></span>
<span data-ttu-id="3705d-120">指定豬工作的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="3705d-120">Specifies an array of arguments for a Pig job.</span></span>
<span data-ttu-id="3705d-121">引數會以命令列引數的形式傳遞給每個任務。</span><span class="sxs-lookup"><span data-stu-id="3705d-121">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="3705d-122">檔案</span><span class="sxs-lookup"><span data-stu-id="3705d-122">-File</span></span>
<span data-ttu-id="3705d-123">指定包含要執行之查詢之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="3705d-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="3705d-124">您可以使用這個參數，而不是 *Query* 參數。</span><span class="sxs-lookup"><span data-stu-id="3705d-124">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3705d-125">-檔案</span><span class="sxs-lookup"><span data-stu-id="3705d-125">-Files</span></span>
<span data-ttu-id="3705d-126">指定與豬作業相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="3705d-126">Specifies a collection of files that are associated with a Pig job.</span></span>

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

### <span data-ttu-id="3705d-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3705d-127">-Profile</span></span>
<span data-ttu-id="3705d-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3705d-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3705d-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3705d-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3705d-130">-Query</span><span class="sxs-lookup"><span data-stu-id="3705d-130">-Query</span></span>
<span data-ttu-id="3705d-131">指定豬工作查詢。</span><span class="sxs-lookup"><span data-stu-id="3705d-131">Specifies a Pig job query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryText

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3705d-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="3705d-132">-StatusFolder</span></span>
<span data-ttu-id="3705d-133">指定包含作業之標準輸出和錯誤輸出的資料夾位置，包括其結束代碼和任務記錄。</span><span class="sxs-lookup"><span data-stu-id="3705d-133">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="3705d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3705d-134">CommonParameters</span></span>
<span data-ttu-id="3705d-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3705d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3705d-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3705d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3705d-137">輸入</span><span class="sxs-lookup"><span data-stu-id="3705d-137">INPUTS</span></span>

## <span data-ttu-id="3705d-138">輸出</span><span class="sxs-lookup"><span data-stu-id="3705d-138">OUTPUTS</span></span>

## <span data-ttu-id="3705d-139">筆記</span><span class="sxs-lookup"><span data-stu-id="3705d-139">NOTES</span></span>

## <span data-ttu-id="3705d-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="3705d-140">RELATED LINKS</span></span>

[<span data-ttu-id="3705d-141">新-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3705d-141">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="3705d-142">新-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3705d-142">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="3705d-143">新-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3705d-143">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="3705d-144">新-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3705d-144">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


