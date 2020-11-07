---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0DFCB891-7431-4C00-98DD-263DC2794354
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea6fbc76a76533c07b11935e50e25418d10e38ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967363"
---
# <span data-ttu-id="eb4fe-101">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="eb4fe-101">New-AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="eb4fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb4fe-102">SYNOPSIS</span></span>
<span data-ttu-id="eb4fe-103">為 HDInsight 服務定義新的配置單元作業。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-103">Defines a new Hive job for an HDInsight service.</span></span>

## <span data-ttu-id="eb4fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb4fe-104">SYNTAX</span></span>

```
New-AzureHDInsightHiveJobDefinition [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="eb4fe-105">說明</span><span class="sxs-lookup"><span data-stu-id="eb4fe-105">DESCRIPTION</span></span>
<span data-ttu-id="eb4fe-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="eb4fe-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="eb4fe-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="eb4fe-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="eb4fe-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="eb4fe-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="eb4fe-112">**新的-AzureHDInsightHiveJobDefinition** Cmdlet 會定義 Azure HDInsight 服務的 Hive 作業。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-112">The **New-AzureHDInsightHiveJobDefinition** cmdlet defines a Hive job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="eb4fe-113">示例</span><span class="sxs-lookup"><span data-stu-id="eb4fe-113">EXAMPLES</span></span>

### <span data-ttu-id="eb4fe-114">範例1：建立蜂巢作業定義</span><span class="sxs-lookup"><span data-stu-id="eb4fe-114">Example 1: Create a Hive job definition</span></span>
```
PS C:\>$HiveJobDefinition = New-AzureHDInsightHiveJobDefinition -Query $QueryString
```

<span data-ttu-id="eb4fe-115">這個命令會建立一個使用預先定義的查詢字串的 Hive 作業定義，然後將它儲存在 $HiveJobDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-115">This command creates a Hive job definition that uses a pre-defined query string, and then stores it in the $HiveJobDefinition variable.</span></span>

## <span data-ttu-id="eb4fe-116">參數</span><span class="sxs-lookup"><span data-stu-id="eb4fe-116">PARAMETERS</span></span>

### <span data-ttu-id="eb4fe-117">-引數</span><span class="sxs-lookup"><span data-stu-id="eb4fe-117">-Arguments</span></span>
<span data-ttu-id="eb4fe-118">指定 Hadoop 作業的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="eb4fe-119">引數會以命令列引數的形式傳遞給每個任務。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-119">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="eb4fe-120">-定義</span><span class="sxs-lookup"><span data-stu-id="eb4fe-120">-Defines</span></span>
<span data-ttu-id="eb4fe-121">指定要在作業執行時設定的 Hadoop 配置值。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-121">Specifies Hadoop configuration values to set for when a job runs.</span></span>

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

### <span data-ttu-id="eb4fe-122">檔案</span><span class="sxs-lookup"><span data-stu-id="eb4fe-122">-File</span></span>
<span data-ttu-id="eb4fe-123">指定包含要執行之查詢之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="eb4fe-124">您可以使用這個參數，而不是 *Query* 參數。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-124">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="eb4fe-125">-檔案</span><span class="sxs-lookup"><span data-stu-id="eb4fe-125">-Files</span></span>
<span data-ttu-id="eb4fe-126">指定與 Hive 作業相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-126">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="eb4fe-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="eb4fe-127">-JobName</span></span>
<span data-ttu-id="eb4fe-128">指定要定義的 Hive 作業名稱。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-128">Specifies the name of the Hive job to define.</span></span>
<span data-ttu-id="eb4fe-129">如果您沒有指定此參數，則會使用預設名稱：「Hive：」 \<first 100 characters of query\> 。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-129">If you do not specify this parameter, the default name is used: "Hive: \<first 100 characters of query\>".</span></span>

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

### <span data-ttu-id="eb4fe-130">-設定檔</span><span class="sxs-lookup"><span data-stu-id="eb4fe-130">-Profile</span></span>
<span data-ttu-id="eb4fe-131">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eb4fe-132">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eb4fe-133">-Query</span><span class="sxs-lookup"><span data-stu-id="eb4fe-133">-Query</span></span>
<span data-ttu-id="eb4fe-134">指定 Hive 查詢。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-134">Specifies a Hive query.</span></span>

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

### <span data-ttu-id="eb4fe-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="eb4fe-135">-RunAsFileJob</span></span>
<span data-ttu-id="eb4fe-136">指示這個 Cmdlet 會在預設的 Azure 儲存空間帳戶中建立檔案，以儲存查詢。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="eb4fe-137">這個 Cmdlet 會提交參照此檔案做為腳本以執行的工作。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-137">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="eb4fe-138">您可以使用這個功能來處理特殊的字元，例如百分號 (% ) ，這些字元會在透過 Templeton 提交作業時失敗，因為 Templeton 會使用百分號符號作為 URL 參數來轉譯查詢。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb4fe-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="eb4fe-139">-StatusFolder</span></span>
<span data-ttu-id="eb4fe-140">指定包含作業之標準輸出和錯誤輸出的資料夾位置，包括其結束代碼和任務記錄。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-140">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="eb4fe-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb4fe-141">CommonParameters</span></span>
<span data-ttu-id="eb4fe-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb4fe-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eb4fe-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb4fe-144">輸入</span><span class="sxs-lookup"><span data-stu-id="eb4fe-144">INPUTS</span></span>

## <span data-ttu-id="eb4fe-145">輸出</span><span class="sxs-lookup"><span data-stu-id="eb4fe-145">OUTPUTS</span></span>

## <span data-ttu-id="eb4fe-146">筆記</span><span class="sxs-lookup"><span data-stu-id="eb4fe-146">NOTES</span></span>

## <span data-ttu-id="eb4fe-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb4fe-147">RELATED LINKS</span></span>

[<span data-ttu-id="eb4fe-148">新-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="eb4fe-148">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="eb4fe-149">新-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="eb4fe-149">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="eb4fe-150">新-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="eb4fe-150">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="eb4fe-151">新-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="eb4fe-151">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


