---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3E3C9626-7AED-4B15-93D0-0B79AD17A834
online version: ''
schema: 2.0.0
ms.openlocfilehash: de4b768dbc6c97e84bccd4c8e0ef42f6f81a5b31
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967796"
---
# <span data-ttu-id="8443b-101">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8443b-101">Get-AzureHDInsightJob</span></span>

## <span data-ttu-id="8443b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8443b-102">SYNOPSIS</span></span>
<span data-ttu-id="8443b-103">取得 HDInsight 作業。</span><span class="sxs-lookup"><span data-stu-id="8443b-103">Gets HDInsight jobs.</span></span>

## <span data-ttu-id="8443b-104">句法</span><span class="sxs-lookup"><span data-stu-id="8443b-104">SYNTAX</span></span>

### <span data-ttu-id="8443b-105"> (預設) 取得 HDInsight 群集的 jobDetails 歷程記錄</span><span class="sxs-lookup"><span data-stu-id="8443b-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Get-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] [-IgnoreSslErrors <Boolean>]
 [-JobId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8443b-106">使用特定的訂閱認證來取得 HDInsight 群集 (的 jobDetails 歷程記錄) </span><span class="sxs-lookup"><span data-stu-id="8443b-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Get-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] [-JobId <String>] [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8443b-107">說明</span><span class="sxs-lookup"><span data-stu-id="8443b-107">DESCRIPTION</span></span>
<span data-ttu-id="8443b-108">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="8443b-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="8443b-109">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="8443b-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="8443b-110">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="8443b-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="8443b-111">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="8443b-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="8443b-112">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="8443b-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="8443b-113">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="8443b-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="8443b-114">**AzureHDInsightJob** Cmdlet 會取得指定群集的最近 Azure HDInsight 作業，並以相反的時間順序顯示它們。</span><span class="sxs-lookup"><span data-stu-id="8443b-114">The **Get-AzureHDInsightJob** cmdlet gets recent Azure HDInsight jobs for a specified cluster and displays them in reverse chronological order.</span></span>

## <span data-ttu-id="8443b-115">示例</span><span class="sxs-lookup"><span data-stu-id="8443b-115">EXAMPLES</span></span>

## <span data-ttu-id="8443b-116">參數</span><span class="sxs-lookup"><span data-stu-id="8443b-116">PARAMETERS</span></span>

### <span data-ttu-id="8443b-117">-Certificate</span><span class="sxs-lookup"><span data-stu-id="8443b-117">-Certificate</span></span>
<span data-ttu-id="8443b-118">指定 Azure 訂閱的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="8443b-118">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="8443b-119">-群集</span><span class="sxs-lookup"><span data-stu-id="8443b-119">-Cluster</span></span>
<span data-ttu-id="8443b-120">指定群集。</span><span class="sxs-lookup"><span data-stu-id="8443b-120">Specifies a cluster.</span></span>
<span data-ttu-id="8443b-121">這個 Cmdlet 會取得在此參數指定的群集上執行的 HDInsight 作業。</span><span class="sxs-lookup"><span data-stu-id="8443b-121">This cmdlet gets HDInsight jobs that run on the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="8443b-122">-認證</span><span class="sxs-lookup"><span data-stu-id="8443b-122">-Credential</span></span>
<span data-ttu-id="8443b-123">指定要用於直接 HTTP 存取群集的認證。</span><span class="sxs-lookup"><span data-stu-id="8443b-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="8443b-124">您可以指定此參數，而不是 *訂閱* 參數，以驗證對群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="8443b-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8443b-125">-端點</span><span class="sxs-lookup"><span data-stu-id="8443b-125">-Endpoint</span></span>
<span data-ttu-id="8443b-126">指定要用來連接 Azure 的端點。</span><span class="sxs-lookup"><span data-stu-id="8443b-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="8443b-127">如果您沒有指定此參數，此 Cmdlet 會使用預設端點。</span><span class="sxs-lookup"><span data-stu-id="8443b-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="8443b-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="8443b-128">-HostedService</span></span>
<span data-ttu-id="8443b-129">如果您不想使用預設的命名空間，請指定 HDInsight 服務的命名空間。</span><span class="sxs-lookup"><span data-stu-id="8443b-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="8443b-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="8443b-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="8443b-131">指出是否已忽略安全通訊端層 (SSL) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="8443b-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="8443b-132">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="8443b-132">-JobId</span></span>
<span data-ttu-id="8443b-133">指定要取得作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8443b-133">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8443b-134">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8443b-134">-Profile</span></span>
<span data-ttu-id="8443b-135">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8443b-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8443b-136">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8443b-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8443b-137">-訂閱</span><span class="sxs-lookup"><span data-stu-id="8443b-137">-Subscription</span></span>
<span data-ttu-id="8443b-138">指定包含要取得之 HDInsight 作業的訂閱。</span><span class="sxs-lookup"><span data-stu-id="8443b-138">Specifies the subscription that contains the HDInsight jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8443b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8443b-139">CommonParameters</span></span>
<span data-ttu-id="8443b-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8443b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8443b-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8443b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8443b-142">輸入</span><span class="sxs-lookup"><span data-stu-id="8443b-142">INPUTS</span></span>

## <span data-ttu-id="8443b-143">輸出</span><span class="sxs-lookup"><span data-stu-id="8443b-143">OUTPUTS</span></span>

## <span data-ttu-id="8443b-144">筆記</span><span class="sxs-lookup"><span data-stu-id="8443b-144">NOTES</span></span>

## <span data-ttu-id="8443b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="8443b-145">RELATED LINKS</span></span>

[<span data-ttu-id="8443b-146">開始-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8443b-146">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="8443b-147">停止 AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8443b-147">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="8443b-148">稍候-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8443b-148">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


