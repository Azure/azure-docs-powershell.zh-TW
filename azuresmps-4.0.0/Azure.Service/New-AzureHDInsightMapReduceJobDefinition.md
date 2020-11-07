---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A8953045-3836-4C5A-96F8-461CB1DB6BBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58958a6bedd29cd55535fe879fab813a430ff20b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967362"
---
# <span data-ttu-id="e9c97-101">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e9c97-101">New-AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="e9c97-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9c97-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c97-103">定義新的 MapReduce 作業。</span><span class="sxs-lookup"><span data-stu-id="e9c97-103">Defines a new MapReduce job.</span></span>

## <span data-ttu-id="e9c97-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9c97-104">SYNTAX</span></span>

```
New-AzureHDInsightMapReduceJobDefinition [-Arguments <String[]>] -ClassName <String> [-Defines <Hashtable>]
 [-Files <String[]>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e9c97-105">說明</span><span class="sxs-lookup"><span data-stu-id="e9c97-105">DESCRIPTION</span></span>
<span data-ttu-id="e9c97-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="e9c97-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="e9c97-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="e9c97-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="e9c97-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="e9c97-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="e9c97-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="e9c97-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="e9c97-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="e9c97-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="e9c97-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="e9c97-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="e9c97-112">**新的-AzureHDInsightMapReduceJobDefinition** Cmdlet 會定義要在 Azure HDInsight 群集上執行的新 MapReduce 作業。</span><span class="sxs-lookup"><span data-stu-id="e9c97-112">The **New-AzureHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job to run on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e9c97-113">示例</span><span class="sxs-lookup"><span data-stu-id="e9c97-113">EXAMPLES</span></span>

### <span data-ttu-id="e9c97-114">範例1：定義 MapReduce 作業、執行作業及取得輸出</span><span class="sxs-lookup"><span data-stu-id="e9c97-114">Example 1: Define a MapReduce job, run the job, and get the output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "WordCount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="e9c97-115">第一個命令會取得目前訂閱的識別碼，然後將它儲存在 $SubId 變數中。</span><span class="sxs-lookup"><span data-stu-id="e9c97-115">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="e9c97-116">第二個命令會將名稱 MyCluster 指派給 $Clustername 變數。</span><span class="sxs-lookup"><span data-stu-id="e9c97-116">The second command assigns the name MyCluster to the $Clustername variable.</span></span>

<span data-ttu-id="e9c97-117">第三個命令使用 **新的 AzureHDInsightMapReduceJobDefinition** Cmdlet 來建立 MapReduce 作業定義，然後將它儲存在 $WordCountJob 變數中。</span><span class="sxs-lookup"><span data-stu-id="e9c97-117">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then store it in the $WordCountJob variable.</span></span>

<span data-ttu-id="e9c97-118">第四個命令會使用這些 Cmdlet 執行一系列的作業：</span><span class="sxs-lookup"><span data-stu-id="e9c97-118">The fourth command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="e9c97-119">[ **開始-AzureHDInsightJob** ]，在 $ClusterName 上開始作業。</span><span class="sxs-lookup"><span data-stu-id="e9c97-119">**Start-AzureHDInsightJob** to start the job on $ClusterName.</span></span> 
- <span data-ttu-id="e9c97-120">**AzureHDInsightJob** 等待工作完成，並顯示完成進度。</span><span class="sxs-lookup"><span data-stu-id="e9c97-120">**Wait-AzureHDInsightJob** to wait for the job to finish and to display the progress toward completion.</span></span>
- <span data-ttu-id="e9c97-121">**取得 AzureHDInsightJobOutput** 以取得作業輸出。</span><span class="sxs-lookup"><span data-stu-id="e9c97-121">**Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="e9c97-122">參數</span><span class="sxs-lookup"><span data-stu-id="e9c97-122">PARAMETERS</span></span>

### <span data-ttu-id="e9c97-123">-引數</span><span class="sxs-lookup"><span data-stu-id="e9c97-123">-Arguments</span></span>
<span data-ttu-id="e9c97-124">指定 Hadoop 作業的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="e9c97-124">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="e9c97-125">引數會以命令列引數的形式傳遞給每個任務。</span><span class="sxs-lookup"><span data-stu-id="e9c97-125">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="e9c97-126">-ClassName</span><span class="sxs-lookup"><span data-stu-id="e9c97-126">-ClassName</span></span>
<span data-ttu-id="e9c97-127">在 JAVA 封存 (JAR) 檔案中指定作業類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9c97-127">Specifies the name of the job class in the Java Archive (JAR) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Class

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9c97-128">-定義</span><span class="sxs-lookup"><span data-stu-id="e9c97-128">-Defines</span></span>
<span data-ttu-id="e9c97-129">指定要在作業執行時設定的 Hadoop 配置值。</span><span class="sxs-lookup"><span data-stu-id="e9c97-129">Specifies Hadoop configuration values to set when the job runs.</span></span>

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

### <span data-ttu-id="e9c97-130">-檔案</span><span class="sxs-lookup"><span data-stu-id="e9c97-130">-Files</span></span>
<span data-ttu-id="e9c97-131">指定作業所需的 WASB 檔案陣列。</span><span class="sxs-lookup"><span data-stu-id="e9c97-131">Specifies an array of WASB files that are required for a job.</span></span>

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

### <span data-ttu-id="e9c97-132">-JarFile</span><span class="sxs-lookup"><span data-stu-id="e9c97-132">-JarFile</span></span>
<span data-ttu-id="e9c97-133">指定包含 MapReduce 作業之程式碼和相依性的 JAR 檔案的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="e9c97-133">Specifies the fully qualified name of a JAR file that contains the code and dependencies of a MapReduce job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Jar

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9c97-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="e9c97-134">-JobName</span></span>
<span data-ttu-id="e9c97-135">指定 MapReduce 作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9c97-135">Specifies the name of a MapReduce job.</span></span>
<span data-ttu-id="e9c97-136">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="e9c97-136">This parameter is optional.</span></span>
<span data-ttu-id="e9c97-137">如果您沒有指定此參數，則會使用 *ClassName* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="e9c97-137">If you do not specify this parameter, the value of the *ClassName* parameter is used.</span></span>

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

### <span data-ttu-id="e9c97-138">-LibJars</span><span class="sxs-lookup"><span data-stu-id="e9c97-138">-LibJars</span></span>
<span data-ttu-id="e9c97-139">指定作業的 LibJar 參照陣列。</span><span class="sxs-lookup"><span data-stu-id="e9c97-139">Specifies an array of LibJar references of the job.</span></span>

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

### <span data-ttu-id="e9c97-140">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e9c97-140">-Profile</span></span>
<span data-ttu-id="e9c97-141">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e9c97-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e9c97-142">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e9c97-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e9c97-143">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="e9c97-143">-StatusFolder</span></span>
<span data-ttu-id="e9c97-144">指定包含作業之標準輸出和錯誤輸出的資料夾位置，包括其結束代碼和任務記錄。</span><span class="sxs-lookup"><span data-stu-id="e9c97-144">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="e9c97-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c97-145">CommonParameters</span></span>
<span data-ttu-id="e9c97-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9c97-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c97-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e9c97-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c97-148">輸入</span><span class="sxs-lookup"><span data-stu-id="e9c97-148">INPUTS</span></span>

## <span data-ttu-id="e9c97-149">輸出</span><span class="sxs-lookup"><span data-stu-id="e9c97-149">OUTPUTS</span></span>

## <span data-ttu-id="e9c97-150">筆記</span><span class="sxs-lookup"><span data-stu-id="e9c97-150">NOTES</span></span>

## <span data-ttu-id="e9c97-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9c97-151">RELATED LINKS</span></span>

[<span data-ttu-id="e9c97-152">AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="e9c97-152">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="e9c97-153">新-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e9c97-153">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="e9c97-154">新-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e9c97-154">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="e9c97-155">新-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e9c97-155">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="e9c97-156">開始-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e9c97-156">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="e9c97-157">稍候-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e9c97-157">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


