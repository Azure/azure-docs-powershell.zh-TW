---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 60A5ACF7-2637-4BDC-BF41-80E81B23F4CD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0308c3ff5bee358a82d74d452784f42c69bc7c32
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966870"
---
# <span data-ttu-id="6d5fb-101">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6d5fb-101">Start-AzureHDInsightJob</span></span>

## <span data-ttu-id="6d5fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6d5fb-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5fb-103">啟動 HDInsight 作業。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-103">Starts an HDInsight job.</span></span>

## <span data-ttu-id="6d5fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="6d5fb-104">SYNTAX</span></span>

### <span data-ttu-id="6d5fb-105">在 HDInsight 群集上啟動 jobDetails (預設) </span><span class="sxs-lookup"><span data-stu-id="6d5fb-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Start-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>]
 -JobDefinition <AzureHDInsightJobDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6d5fb-106">在具備特定訂閱認證 (的 HDInsight 群集上啟動 jobDetails) </span><span class="sxs-lookup"><span data-stu-id="6d5fb-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Start-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobDefinition <AzureHDInsightJobDefinition>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6d5fb-107">說明</span><span class="sxs-lookup"><span data-stu-id="6d5fb-107">DESCRIPTION</span></span>
<span data-ttu-id="6d5fb-108">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="6d5fb-109">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="6d5fb-110">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="6d5fb-111">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="6d5fb-112">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="6d5fb-113">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="6d5fb-114">**Start-AzureHDInsightJob** Cmdlet 會在指定的群集上啟動已定義的 Azure HDInsight 作業。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-114">The **Start-AzureHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="6d5fb-115">要開始的工作可以是 MapReduce 作業、流式作業、Hive 作業或豬工作。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-115">The job to start can be a MapReduce job, a streaming job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="6d5fb-116">示例</span><span class="sxs-lookup"><span data-stu-id="6d5fb-116">EXAMPLES</span></span>

### <span data-ttu-id="6d5fb-117">範例1：啟動 HDInsight 作業</span><span class="sxs-lookup"><span data-stu-id="6d5fb-117">Example 1: Start an HDInsight job</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "Cluster01" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="6d5fb-118">第一個命令會取得目前的訂閱識別碼，然後將它儲存在 $SubId 變數中。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-118">The first command gets the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="6d5fb-119">第二個命令會將名稱 Cluster01 指派給 $ClusterName 變數。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-119">The second command assigns the name Cluster01 to the $ClusterName variable.</span></span>

<span data-ttu-id="6d5fb-120">第三個命令使用 **新的 AzureHDInsightMapReduceJobDefinition** Cmdlet 來建立 MapReduce 作業定義，然後將它儲存在 $WordCountJob 變數中。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-120">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="6d5fb-121">最後一個命令會使用管線運算子，將 $WordCountJob 傳遞給 **AzureHDInsightJob** Cmdlet 以開始作業。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-121">The final command uses the pipeline operator to pass the $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="6d5fb-122">作業啟動後，會傳遞到 **AzureHDInsightJob** Cmdlet，在將作業傳遞到 **AzureHDInsightJobOutput** Cmdlet 以取得作業輸出之前，該指令會等到該作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-122">After the job starts, it is passed to the **Wait-AzureHDInsightJob** cmdlet, which waits for the job to complete before passing it to the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="6d5fb-123">參數</span><span class="sxs-lookup"><span data-stu-id="6d5fb-123">PARAMETERS</span></span>

### <span data-ttu-id="6d5fb-124">-Certificate</span><span class="sxs-lookup"><span data-stu-id="6d5fb-124">-Certificate</span></span>
<span data-ttu-id="6d5fb-125">指定 Azure 訂閱的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-125">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5fb-126">-群集</span><span class="sxs-lookup"><span data-stu-id="6d5fb-126">-Cluster</span></span>
<span data-ttu-id="6d5fb-127">指定群集。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-127">Specifies a cluster.</span></span>
<span data-ttu-id="6d5fb-128">這個 Cmdlet 會在群集上啟動此參數指定的工作。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-128">This cmdlet starts a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5fb-129">-認證</span><span class="sxs-lookup"><span data-stu-id="6d5fb-129">-Credential</span></span>
<span data-ttu-id="6d5fb-130">指定直接 HTTP 存取群集的群集認證。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-130">Specifies cluster credentials for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="6d5fb-131">您可以指定此參數，而不是 *訂閱* 參數，以驗證對群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-131">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Start jobDetails on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5fb-132">-端點</span><span class="sxs-lookup"><span data-stu-id="6d5fb-132">-Endpoint</span></span>
<span data-ttu-id="6d5fb-133">指定要用來連接 Azure 的端點。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-133">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="6d5fb-134">如果您沒有指定此參數，此 Cmdlet 會使用預設端點。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-134">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5fb-135">-HostedService</span><span class="sxs-lookup"><span data-stu-id="6d5fb-135">-HostedService</span></span>
<span data-ttu-id="6d5fb-136">如果您不想使用預設的命名空間，請指定 HDInsight 服務的命名空間。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-136">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5fb-137">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="6d5fb-137">-IgnoreSslErrors</span></span>
<span data-ttu-id="6d5fb-138">指出是否已忽略安全通訊端層 (SSL) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-138">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5fb-139">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="6d5fb-139">-JobDefinition</span></span>
<span data-ttu-id="6d5fb-140">指定連線到 Microsoft Azure 的端點（如果端點與預設值不同）。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-140">Specifies the endpoint to use when connecting to Microsoft Azure if the endpoint is different from the default.</span></span>

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: jobDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5fb-141">-設定檔</span><span class="sxs-lookup"><span data-stu-id="6d5fb-141">-Profile</span></span>
<span data-ttu-id="6d5fb-142">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6d5fb-143">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6d5fb-144">-訂閱</span><span class="sxs-lookup"><span data-stu-id="6d5fb-144">-Subscription</span></span>
<span data-ttu-id="6d5fb-145">指定訂閱。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-145">Specifies a subscription.</span></span>
<span data-ttu-id="6d5fb-146">這個 Cmdlet 會針對此參數指定的訂閱啟動作業。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-146">This cmdlet starts a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5fb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5fb-147">CommonParameters</span></span>
<span data-ttu-id="6d5fb-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5fb-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6d5fb-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5fb-150">輸入</span><span class="sxs-lookup"><span data-stu-id="6d5fb-150">INPUTS</span></span>

## <span data-ttu-id="6d5fb-151">輸出</span><span class="sxs-lookup"><span data-stu-id="6d5fb-151">OUTPUTS</span></span>

## <span data-ttu-id="6d5fb-152">筆記</span><span class="sxs-lookup"><span data-stu-id="6d5fb-152">NOTES</span></span>

## <span data-ttu-id="6d5fb-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d5fb-153">RELATED LINKS</span></span>

[<span data-ttu-id="6d5fb-154">AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6d5fb-154">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="6d5fb-155">AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="6d5fb-155">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="6d5fb-156">新-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="6d5fb-156">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="6d5fb-157">停止 AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6d5fb-157">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="6d5fb-158">稍候-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6d5fb-158">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


