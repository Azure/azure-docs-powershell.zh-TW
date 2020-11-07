---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0B194605-F6B2-4FBC-ABF8-E49876EC7CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b215cfa95c20a2e8d13cfefa9e2ef0b3794a6727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967086"
---
# <span data-ttu-id="b313e-101">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="b313e-101">Get-AzureHDInsightJobOutput</span></span>

## <span data-ttu-id="b313e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b313e-102">SYNOPSIS</span></span>
<span data-ttu-id="b313e-103">取得作業的記錄輸出。</span><span class="sxs-lookup"><span data-stu-id="b313e-103">Gets the log output for a job.</span></span>

## <span data-ttu-id="b313e-104">句法</span><span class="sxs-lookup"><span data-stu-id="b313e-104">SYNTAX</span></span>

```
Get-AzureHDInsightJobOutput [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-DownloadTaskLogs] [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-StandardError]
 [-StandardOutput] [-Subscription <String>] [-TaskLogsDirectory <String>] [-TaskSummary]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b313e-105">說明</span><span class="sxs-lookup"><span data-stu-id="b313e-105">DESCRIPTION</span></span>
<span data-ttu-id="b313e-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="b313e-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="b313e-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="b313e-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="b313e-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="b313e-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="b313e-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell 在 HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)中建立以 Linux 為基礎的群集。</span><span class="sxs-lookup"><span data-stu-id="b313e-109">For information about how to use the new HDInsight to create a cluster, see Create Linux-based clusters in [HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="b313e-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)。</span><span class="sxs-lookup"><span data-stu-id="b313e-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="b313e-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b313e-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="b313e-112">**AzureHDInsightJobOutput** Cmdlet 會從與群集相關聯的儲存空間帳戶取得作業的記錄輸出。</span><span class="sxs-lookup"><span data-stu-id="b313e-112">The **Get-AzureHDInsightJobOutput** cmdlet gets the log output for a job from the storage account associated with a cluster.</span></span>
<span data-ttu-id="b313e-113">您可以取得各種類型的作業記錄，包括標準輸出、標準錯誤、任務記錄及任務記錄摘要。</span><span class="sxs-lookup"><span data-stu-id="b313e-113">You can get various types of job logs including standard output, standard error, task logs, and a summary of the task logs.</span></span>

## <span data-ttu-id="b313e-114">示例</span><span class="sxs-lookup"><span data-stu-id="b313e-114">EXAMPLES</span></span>

### <span data-ttu-id="b313e-115">範例1：取得作業輸出</span><span class="sxs-lookup"><span data-stu-id="b313e-115">Example 1: Get job output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster"
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" $WordCountJob
    | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -StandardError
```

<span data-ttu-id="b313e-116">第一個命令會取得目前訂閱的識別碼，然後將它儲存在 $SubId 變數中。</span><span class="sxs-lookup"><span data-stu-id="b313e-116">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="b313e-117">第二個命令會將名稱 MyCluster 儲存在 $Clustername 變數中。</span><span class="sxs-lookup"><span data-stu-id="b313e-117">The second command stores the name MyCluster in the $Clustername variable.</span></span>

<span data-ttu-id="b313e-118">第三個命令會建立 MapReduce 作業定義，然後將它儲存在 $WordCountJob 變數中。</span><span class="sxs-lookup"><span data-stu-id="b313e-118">The third command creates a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>
<span data-ttu-id="b313e-119">命令會將 $WordCountJob 的工作傳遞給 **AzureHDInsightJob** Cmdlet，以啟動作業。</span><span class="sxs-lookup"><span data-stu-id="b313e-119">The command passes the job in $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="b313e-120">它也會將 $WordCountJob 傳送給 **AzureHDInsightJob** Cmdlet，以等待工作完成，然後使用 **AzureHDInsightJobOutput** 取得作業輸出。</span><span class="sxs-lookup"><span data-stu-id="b313e-120">It also passes $WordCountJob to the **Wait-AzureHDInsightJob** cmdlet to wait for the job to finish, and then it uses **Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="b313e-121">參數</span><span class="sxs-lookup"><span data-stu-id="b313e-121">PARAMETERS</span></span>

### <span data-ttu-id="b313e-122">-Certificate</span><span class="sxs-lookup"><span data-stu-id="b313e-122">-Certificate</span></span>
<span data-ttu-id="b313e-123">指定 Azure 訂閱的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="b313e-123">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b313e-124">-群集</span><span class="sxs-lookup"><span data-stu-id="b313e-124">-Cluster</span></span>
<span data-ttu-id="b313e-125">指定群集。</span><span class="sxs-lookup"><span data-stu-id="b313e-125">Specifies a cluster.</span></span>
<span data-ttu-id="b313e-126">這個 Cmdlet 會從群集中取得此參數指定的作業記錄。</span><span class="sxs-lookup"><span data-stu-id="b313e-126">This cmdlet gets job logs from the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b313e-127">-DownloadTaskLogs</span><span class="sxs-lookup"><span data-stu-id="b313e-127">-DownloadTaskLogs</span></span>
<span data-ttu-id="b313e-128">表示此 Cmdlet 會取得工作的任務記錄。</span><span class="sxs-lookup"><span data-stu-id="b313e-128">Indicates that this cmdlet gets the task logs for a job.</span></span>

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

### <span data-ttu-id="b313e-129">-端點</span><span class="sxs-lookup"><span data-stu-id="b313e-129">-Endpoint</span></span>
<span data-ttu-id="b313e-130">指定要用來連接 Azure 的端點。</span><span class="sxs-lookup"><span data-stu-id="b313e-130">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="b313e-131">如果您沒有指定此參數，此 Cmdlet 會使用預設端點。</span><span class="sxs-lookup"><span data-stu-id="b313e-131">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b313e-132">-HostedService</span><span class="sxs-lookup"><span data-stu-id="b313e-132">-HostedService</span></span>
<span data-ttu-id="b313e-133">如果您不想使用預設的命名空間，請指定 HDInsight 服務的命名空間。</span><span class="sxs-lookup"><span data-stu-id="b313e-133">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b313e-134">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="b313e-134">-IgnoreSslErrors</span></span>
<span data-ttu-id="b313e-135">指出是否已忽略安全通訊端層 (SSL) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="b313e-135">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b313e-136">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="b313e-136">-JobId</span></span>
<span data-ttu-id="b313e-137">指定要取得的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="b313e-137">Specifies the ID of the job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b313e-138">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b313e-138">-Profile</span></span>
<span data-ttu-id="b313e-139">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b313e-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b313e-140">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b313e-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b313e-141">-StandardError</span><span class="sxs-lookup"><span data-stu-id="b313e-141">-StandardError</span></span>
<span data-ttu-id="b313e-142">表示此 Cmdlet 會取得作業的 StdErr 輸出。</span><span class="sxs-lookup"><span data-stu-id="b313e-142">Indicates that this cmdlet gets the StdErr output of a job.</span></span>

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

### <span data-ttu-id="b313e-143">-StandardOutput</span><span class="sxs-lookup"><span data-stu-id="b313e-143">-StandardOutput</span></span>
<span data-ttu-id="b313e-144">表示此 Cmdlet 會取得作業的 SdtOut 輸出。</span><span class="sxs-lookup"><span data-stu-id="b313e-144">Indicates that this cmdlet gets the SdtOut output of a job.</span></span>

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

### <span data-ttu-id="b313e-145">-訂閱</span><span class="sxs-lookup"><span data-stu-id="b313e-145">-Subscription</span></span>
<span data-ttu-id="b313e-146">指定包含要取得之 HDInsight 群集的訂閱。</span><span class="sxs-lookup"><span data-stu-id="b313e-146">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b313e-147">-TaskLogsDirectory</span><span class="sxs-lookup"><span data-stu-id="b313e-147">-TaskLogsDirectory</span></span>
<span data-ttu-id="b313e-148">指定要儲存任務記錄的本機資料夾。</span><span class="sxs-lookup"><span data-stu-id="b313e-148">Specifies a local folder in which to store tasks logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LogsDir

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b313e-149">-TaskSummary</span><span class="sxs-lookup"><span data-stu-id="b313e-149">-TaskSummary</span></span>
<span data-ttu-id="b313e-150">表示此 Cmdlet 會取得任務記錄摘要。</span><span class="sxs-lookup"><span data-stu-id="b313e-150">Indicates that this cmdlets gets the task log summary.</span></span>

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

### <span data-ttu-id="b313e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b313e-151">CommonParameters</span></span>
<span data-ttu-id="b313e-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b313e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b313e-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b313e-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b313e-154">輸入</span><span class="sxs-lookup"><span data-stu-id="b313e-154">INPUTS</span></span>

## <span data-ttu-id="b313e-155">輸出</span><span class="sxs-lookup"><span data-stu-id="b313e-155">OUTPUTS</span></span>

## <span data-ttu-id="b313e-156">筆記</span><span class="sxs-lookup"><span data-stu-id="b313e-156">NOTES</span></span>

## <span data-ttu-id="b313e-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="b313e-157">RELATED LINKS</span></span>

[<span data-ttu-id="b313e-158">新-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b313e-158">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="b313e-159">開始-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b313e-159">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="b313e-160">稍候-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b313e-160">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)
