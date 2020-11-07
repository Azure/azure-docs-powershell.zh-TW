---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EE2ADA86-B2A3-4F6F-96EF-BB61D6DC550F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 338bef67e771bf211c063bf054e13e3844497850
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967210"
---
# <span data-ttu-id="04694-101">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="04694-101">Stop-AzureHDInsightJob</span></span>

## <span data-ttu-id="04694-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04694-102">SYNOPSIS</span></span>
<span data-ttu-id="04694-103">停止 HDInsight 作業。</span><span class="sxs-lookup"><span data-stu-id="04694-103">Stops an HDInsight job.</span></span>

## <span data-ttu-id="04694-104">句法</span><span class="sxs-lookup"><span data-stu-id="04694-104">SYNTAX</span></span>

### <span data-ttu-id="04694-105">在 HDInsight 群集上啟動 jobDetails (預設) </span><span class="sxs-lookup"><span data-stu-id="04694-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Stop-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="04694-106">在具備特定訂閱認證 (的 HDInsight 群集上啟動 jobDetails) </span><span class="sxs-lookup"><span data-stu-id="04694-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Stop-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="04694-107">說明</span><span class="sxs-lookup"><span data-stu-id="04694-107">DESCRIPTION</span></span>
<span data-ttu-id="04694-108">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="04694-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="04694-109">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="04694-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="04694-110">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="04694-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="04694-111">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="04694-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="04694-112">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="04694-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="04694-113">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="04694-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="04694-114">**AzureHDInsightJob** Cmdlet 會在指定的群集上停止 Azure HDInsight 作業。</span><span class="sxs-lookup"><span data-stu-id="04694-114">The **Stop-AzureHDInsightJob** cmdlet stops an Azure HDInsight job on the specified cluster.</span></span>

## <span data-ttu-id="04694-115">示例</span><span class="sxs-lookup"><span data-stu-id="04694-115">EXAMPLES</span></span>

## <span data-ttu-id="04694-116">參數</span><span class="sxs-lookup"><span data-stu-id="04694-116">PARAMETERS</span></span>

### <span data-ttu-id="04694-117">-Certificate</span><span class="sxs-lookup"><span data-stu-id="04694-117">-Certificate</span></span>
<span data-ttu-id="04694-118">指定 Azure 訂閱的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="04694-118">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="04694-119">-群集</span><span class="sxs-lookup"><span data-stu-id="04694-119">-Cluster</span></span>
<span data-ttu-id="04694-120">指定群集。</span><span class="sxs-lookup"><span data-stu-id="04694-120">Specifies a cluster.</span></span>
<span data-ttu-id="04694-121">這個 Cmdlet 會停止在此參數指定的群集上執行的作業。</span><span class="sxs-lookup"><span data-stu-id="04694-121">This cmdlet stops a job that runs on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04694-122">-認證</span><span class="sxs-lookup"><span data-stu-id="04694-122">-Credential</span></span>
<span data-ttu-id="04694-123">指定要用於直接 HTTP 存取群集的認證。</span><span class="sxs-lookup"><span data-stu-id="04694-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="04694-124">您可以指定此參數，而不是 *訂閱* 參數，以驗證對群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="04694-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

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

### <span data-ttu-id="04694-125">-端點</span><span class="sxs-lookup"><span data-stu-id="04694-125">-Endpoint</span></span>
<span data-ttu-id="04694-126">指定要用來連接 Azure 的端點。</span><span class="sxs-lookup"><span data-stu-id="04694-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="04694-127">如果您沒有指定此參數，此 Cmdlet 會使用預設端點。</span><span class="sxs-lookup"><span data-stu-id="04694-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="04694-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="04694-128">-HostedService</span></span>
<span data-ttu-id="04694-129">如果您不想使用預設的命名空間，請指定 HDInsight 服務的命名空間。</span><span class="sxs-lookup"><span data-stu-id="04694-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="04694-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="04694-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="04694-131">指出是否已忽略安全通訊端層 (SSL) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="04694-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="04694-132">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="04694-132">-JobId</span></span>
<span data-ttu-id="04694-133">指定要停止的 HDInsight 作業 ID。</span><span class="sxs-lookup"><span data-stu-id="04694-133">Specifies the ID of the HDInsight job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04694-134">-設定檔</span><span class="sxs-lookup"><span data-stu-id="04694-134">-Profile</span></span>
<span data-ttu-id="04694-135">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="04694-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="04694-136">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="04694-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="04694-137">-訂閱</span><span class="sxs-lookup"><span data-stu-id="04694-137">-Subscription</span></span>
<span data-ttu-id="04694-138">指定訂閱。</span><span class="sxs-lookup"><span data-stu-id="04694-138">Specifies a subscription.</span></span>
<span data-ttu-id="04694-139">這個 Cmdlet 會停止此參數指定之訂閱的作業。</span><span class="sxs-lookup"><span data-stu-id="04694-139">This cmdlet stops a job for the subscription that this parameter specifies.</span></span>

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

### <span data-ttu-id="04694-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04694-140">CommonParameters</span></span>
<span data-ttu-id="04694-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04694-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04694-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="04694-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04694-143">輸入</span><span class="sxs-lookup"><span data-stu-id="04694-143">INPUTS</span></span>

## <span data-ttu-id="04694-144">輸出</span><span class="sxs-lookup"><span data-stu-id="04694-144">OUTPUTS</span></span>

## <span data-ttu-id="04694-145">筆記</span><span class="sxs-lookup"><span data-stu-id="04694-145">NOTES</span></span>

## <span data-ttu-id="04694-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="04694-146">RELATED LINKS</span></span>

[<span data-ttu-id="04694-147">AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="04694-147">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="04694-148">開始-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="04694-148">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="04694-149">稍候-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="04694-149">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


