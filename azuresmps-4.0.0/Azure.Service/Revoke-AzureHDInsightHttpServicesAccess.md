---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A1DFA523-B532-4902-838D-74C8CA97A335
online version: ''
schema: 2.0.0
ms.openlocfilehash: f85d12100eb5b2b093eea252ac308e8a45cf1c53
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967880"
---
# <span data-ttu-id="e3012-101">Revoke-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e3012-101">Revoke-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="e3012-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3012-102">SYNOPSIS</span></span>
<span data-ttu-id="e3012-103">停用 HTTP 對群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="e3012-103">Disables HTTP access to a cluster.</span></span>

## <span data-ttu-id="e3012-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3012-104">SYNTAX</span></span>

```
Revoke-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 [-IgnoreSslErrors <Boolean>] [-Endpoint <Uri>] -Location <String> -Name <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e3012-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3012-105">DESCRIPTION</span></span>
<span data-ttu-id="e3012-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="e3012-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="e3012-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="e3012-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="e3012-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="e3012-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="e3012-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="e3012-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="e3012-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="e3012-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="e3012-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="e3012-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="e3012-112">**Revoke AzureHDInsightHttpServicesAccess** Cmdlet 會針對 ODBC、Ambari、Oozie 和 WebHCatalog web 服務停用 HTTP 存取權至群集。</span><span class="sxs-lookup"><span data-stu-id="e3012-112">The **Revoke-AzureHDInsightHttpServicesAccess** cmdlet disables HTTP access to a cluster for ODBC, Ambari, Oozie and WebHCatalog web services.</span></span>

## <span data-ttu-id="e3012-113">示例</span><span class="sxs-lookup"><span data-stu-id="e3012-113">EXAMPLES</span></span>

## <span data-ttu-id="e3012-114">參數</span><span class="sxs-lookup"><span data-stu-id="e3012-114">PARAMETERS</span></span>

### <span data-ttu-id="e3012-115">-Certificate</span><span class="sxs-lookup"><span data-stu-id="e3012-115">-Certificate</span></span>
<span data-ttu-id="e3012-116">指定 Azure 訂閱的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="e3012-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="e3012-117">-端點</span><span class="sxs-lookup"><span data-stu-id="e3012-117">-Endpoint</span></span>
<span data-ttu-id="e3012-118">指定要用來連接 Azure 的端點。</span><span class="sxs-lookup"><span data-stu-id="e3012-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="e3012-119">如果您沒有指定此參數，此 Cmdlet 會使用預設端點。</span><span class="sxs-lookup"><span data-stu-id="e3012-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="e3012-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="e3012-120">-HostedService</span></span>
<span data-ttu-id="e3012-121">如果您不想使用預設的命名空間，請指定 HDInsight 服務的命名空間。</span><span class="sxs-lookup"><span data-stu-id="e3012-121">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="e3012-122">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="e3012-122">-IgnoreSslErrors</span></span>
<span data-ttu-id="e3012-123">指出是否已忽略安全通訊端層 (SSL) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="e3012-123">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="e3012-124">-位置</span><span class="sxs-lookup"><span data-stu-id="e3012-124">-Location</span></span>
<span data-ttu-id="e3012-125">指定 HDInsight 群集所在的地區。</span><span class="sxs-lookup"><span data-stu-id="e3012-125">Specifies the region in which an HDInsight cluster is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3012-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3012-126">-Name</span></span>
<span data-ttu-id="e3012-127">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3012-127">Specifies the name of a cluster.</span></span>
<span data-ttu-id="e3012-128">這個 Cmdlet 會停用此參數指定之群集的 HTTP 存取權。</span><span class="sxs-lookup"><span data-stu-id="e3012-128">This cmdlet disables HTTP access to the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3012-129">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e3012-129">-Profile</span></span>
<span data-ttu-id="e3012-130">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e3012-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e3012-131">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e3012-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e3012-132">-訂閱</span><span class="sxs-lookup"><span data-stu-id="e3012-132">-Subscription</span></span>
<span data-ttu-id="e3012-133">指定包含要吊銷之 HDInsight 群集的訂閱帳戶。</span><span class="sxs-lookup"><span data-stu-id="e3012-133">Specifies the subscription account that contains the HDInsight cluster to revoke.</span></span>

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

### <span data-ttu-id="e3012-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3012-134">CommonParameters</span></span>
<span data-ttu-id="e3012-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3012-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3012-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3012-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3012-137">輸入</span><span class="sxs-lookup"><span data-stu-id="e3012-137">INPUTS</span></span>

## <span data-ttu-id="e3012-138">輸出</span><span class="sxs-lookup"><span data-stu-id="e3012-138">OUTPUTS</span></span>

## <span data-ttu-id="e3012-139">筆記</span><span class="sxs-lookup"><span data-stu-id="e3012-139">NOTES</span></span>

## <span data-ttu-id="e3012-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3012-140">RELATED LINKS</span></span>

[<span data-ttu-id="e3012-141">授與 AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e3012-141">Grant-AzureHDInsightHttpServicesAccess</span></span>](./Grant-AzureHDInsightHttpServicesAccess.md)


