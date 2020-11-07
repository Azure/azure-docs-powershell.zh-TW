---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 2EA36090-1A45-4F77-9222-9C0E9C07656C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea1247fd2b91f173b8125ad61c0bf2b57f408d18
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967278"
---
# <span data-ttu-id="06196-101">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="06196-101">Wait-AzureHDInsightJob</span></span>

## <span data-ttu-id="06196-102">摘要</span><span class="sxs-lookup"><span data-stu-id="06196-102">SYNOPSIS</span></span>
<span data-ttu-id="06196-103">等待 HDInsight 作業的完成或失敗，並顯示工作進度。</span><span class="sxs-lookup"><span data-stu-id="06196-103">Awaits the completion or failure of an HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="06196-104">句法</span><span class="sxs-lookup"><span data-stu-id="06196-104">SYNTAX</span></span>

### <span data-ttu-id="06196-105"> (預設) 取得 HDInsight 群集的 jobDetails 歷程記錄</span><span class="sxs-lookup"><span data-stu-id="06196-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="06196-106">使用特定的訂閱認證來取得 HDInsight 群集 (的 jobDetails 歷程記錄) </span><span class="sxs-lookup"><span data-stu-id="06196-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Wait-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Job <AzureHDInsightJob> -Subscription <String> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="06196-107">在 HDInsight 群集上具有作業 Id 的等待作業</span><span class="sxs-lookup"><span data-stu-id="06196-107">Wait Job with JobId on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-WaitTimeoutInSeconds <Double>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="06196-108">在 HDInsight 群集上使用 [等候作業] 作業</span><span class="sxs-lookup"><span data-stu-id="06196-108">Wait Job with Job on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] -Job <AzureHDInsightJob> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="06196-109">說明</span><span class="sxs-lookup"><span data-stu-id="06196-109">DESCRIPTION</span></span>
<span data-ttu-id="06196-110">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="06196-110">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="06196-111">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="06196-111">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="06196-112">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="06196-112">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="06196-113">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="06196-113">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="06196-114">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="06196-114">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="06196-115">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="06196-115">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="06196-116">**AzureHDInsightJob** Cmdlet 會等待 Azure HDInsight 作業的完成或失敗，並顯示工作的進度。</span><span class="sxs-lookup"><span data-stu-id="06196-116">The **Wait-AzureHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="06196-117">示例</span><span class="sxs-lookup"><span data-stu-id="06196-117">EXAMPLES</span></span>

### <span data-ttu-id="06196-118">範例1：執行工作並等待其完成</span><span class="sxs-lookup"><span data-stu-id="06196-118">Example 1: Run a job and wait for it to complete</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:>\ $ClusterName = "MyCluster"
PS C:>\ $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:>\ $WordCountJob | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="06196-119">第一個命令會取得目前的 Azure 訂閱識別碼，然後將它儲存在 $SubId 變數中。</span><span class="sxs-lookup"><span data-stu-id="06196-119">The first command gets the current Azure subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="06196-120">第二個命令會取得指定的群集，然後將它儲存在 $ClusterName 變數中。</span><span class="sxs-lookup"><span data-stu-id="06196-120">The second command gets the specified cluster, and then stores it in the $ClusterName variable.</span></span>

<span data-ttu-id="06196-121">第三個命令使用 **新的 AzureHDInsightMapReduceJobDefinition** Cmdlet 來建立 MapReduce 作業定義，然後將它儲存在 $WordCountJob 變數中。</span><span class="sxs-lookup"><span data-stu-id="06196-121">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="06196-122">第四個命令順序使用數個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="06196-122">The fourth command uses several cmdlets in sequence:</span></span> 

- <span data-ttu-id="06196-123">它會使用管線運算子，將 $WordCountJob 傳送到 **AzureHDInsightJob** Cmdlet 來啟動作業。</span><span class="sxs-lookup"><span data-stu-id="06196-123">It uses the pipeline operator to pass $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span> 
- <span data-ttu-id="06196-124">作業會傳送到 **AzureHDInsightJob** Cmdlet，以在3600秒後完成作業。</span><span class="sxs-lookup"><span data-stu-id="06196-124">The job is passed to the **Wait-AzureHDInsightJob** cmdlet to wait 3600 seconds for the job to complete.</span></span> 
- <span data-ttu-id="06196-125">如果作業完成，命令會使用 **AzureHDInsightJobOutput** Cmdlet 來取得作業輸出。</span><span class="sxs-lookup"><span data-stu-id="06196-125">If the job completes, the command uses the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="06196-126">參數</span><span class="sxs-lookup"><span data-stu-id="06196-126">PARAMETERS</span></span>

### <span data-ttu-id="06196-127">-Certificate</span><span class="sxs-lookup"><span data-stu-id="06196-127">-Certificate</span></span>
<span data-ttu-id="06196-128">指定 Azure 訂閱的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="06196-128">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06196-129">-群集</span><span class="sxs-lookup"><span data-stu-id="06196-129">-Cluster</span></span>
<span data-ttu-id="06196-130">指定群集。</span><span class="sxs-lookup"><span data-stu-id="06196-130">Specifies a cluster.</span></span>
<span data-ttu-id="06196-131">這個 Cmdlet 會在群集上等待此參數指定的工作。</span><span class="sxs-lookup"><span data-stu-id="06196-131">This cmdlet waits for a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06196-132">-認證</span><span class="sxs-lookup"><span data-stu-id="06196-132">-Credential</span></span>
<span data-ttu-id="06196-133">指定要用於直接 HTTP 存取群集的認證。</span><span class="sxs-lookup"><span data-stu-id="06196-133">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="06196-134">您可以指定此參數，而不是 *訂閱* 參數，以驗證對群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="06196-134">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster, Wait Job with JobId on an HDInsight Cluster, Wait Job with Job on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06196-135">-端點</span><span class="sxs-lookup"><span data-stu-id="06196-135">-Endpoint</span></span>
<span data-ttu-id="06196-136">指定要用來連接 Azure 的端點。</span><span class="sxs-lookup"><span data-stu-id="06196-136">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="06196-137">如果您沒有指定此參數，此 Cmdlet 會使用預設端點。</span><span class="sxs-lookup"><span data-stu-id="06196-137">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06196-138">-HostedService</span><span class="sxs-lookup"><span data-stu-id="06196-138">-HostedService</span></span>
<span data-ttu-id="06196-139">指定 HDInsight 服務的命名空間。</span><span class="sxs-lookup"><span data-stu-id="06196-139">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="06196-140">如果您沒有指定此參數，則會使用預設的命名空間。</span><span class="sxs-lookup"><span data-stu-id="06196-140">If you do not specify this parameter, the default namespace is used.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06196-141">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="06196-141">-IgnoreSslErrors</span></span>
<span data-ttu-id="06196-142">指出是否已忽略安全通訊端層 (SSL) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="06196-142">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06196-143">-工作</span><span class="sxs-lookup"><span data-stu-id="06196-143">-Job</span></span>
<span data-ttu-id="06196-144">指定 Azure HDInsight 作業。</span><span class="sxs-lookup"><span data-stu-id="06196-144">Specifies an Azure HDInsight job.</span></span>

```yaml
Type: AzureHDInsightJob
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential), Wait Job with Job on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06196-145">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="06196-145">-JobId</span></span>
<span data-ttu-id="06196-146">指定要等候之作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="06196-146">Specifies the ID of the job to wait for.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06196-147">-設定檔</span><span class="sxs-lookup"><span data-stu-id="06196-147">-Profile</span></span>
<span data-ttu-id="06196-148">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="06196-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="06196-149">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="06196-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="06196-150">-訂閱</span><span class="sxs-lookup"><span data-stu-id="06196-150">-Subscription</span></span>
<span data-ttu-id="06196-151">指定訂閱。</span><span class="sxs-lookup"><span data-stu-id="06196-151">Specifies a subscription.</span></span>
<span data-ttu-id="06196-152">這個 Cmdlet 會等待此參數指定之訂閱的作業。</span><span class="sxs-lookup"><span data-stu-id="06196-152">This cmdlet waits for a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06196-153">-WaitTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="06196-153">-WaitTimeoutInSeconds</span></span>
<span data-ttu-id="06196-154">指定等待作業的超時時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="06196-154">Specifies the time-out, in seconds, for the wait operation.</span></span>
<span data-ttu-id="06196-155">如果超時在作業完成之前到期，該 Cmdlet 就會停止執行。</span><span class="sxs-lookup"><span data-stu-id="06196-155">If the time-out expires before the job completes, the cmdlet ceases to run.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06196-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06196-156">CommonParameters</span></span>
<span data-ttu-id="06196-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="06196-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06196-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="06196-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06196-159">輸入</span><span class="sxs-lookup"><span data-stu-id="06196-159">INPUTS</span></span>

## <span data-ttu-id="06196-160">輸出</span><span class="sxs-lookup"><span data-stu-id="06196-160">OUTPUTS</span></span>

## <span data-ttu-id="06196-161">筆記</span><span class="sxs-lookup"><span data-stu-id="06196-161">NOTES</span></span>

## <span data-ttu-id="06196-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="06196-162">RELATED LINKS</span></span>

[<span data-ttu-id="06196-163">AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="06196-163">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="06196-164">AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="06196-164">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="06196-165">開始-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="06196-165">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="06196-166">停止 AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="06196-166">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)


