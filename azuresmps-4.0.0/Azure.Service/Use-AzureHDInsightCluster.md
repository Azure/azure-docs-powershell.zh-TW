---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0BF58D9C-814E-4276-823F-D566DC99391C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 773af58d0ae9b4ca940240875b5cf9a8d3a0ffe7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967283"
---
# <span data-ttu-id="74513-101">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="74513-101">Use-AzureHDInsightCluster</span></span>

## <span data-ttu-id="74513-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74513-102">SYNOPSIS</span></span>
<span data-ttu-id="74513-103">選取要用來提交作業的 Invoke-AzureHDInsightHiveJob Cmdlet 的 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="74513-103">Selects an HDInsight cluster for the Invoke-AzureHDInsightHiveJob cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="74513-104">句法</span><span class="sxs-lookup"><span data-stu-id="74513-104">SYNTAX</span></span>

```
Use-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="74513-105">說明</span><span class="sxs-lookup"><span data-stu-id="74513-105">DESCRIPTION</span></span>
<span data-ttu-id="74513-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="74513-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="74513-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="74513-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="74513-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="74513-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="74513-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="74513-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="74513-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="74513-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="74513-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="74513-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="74513-112">**AzureHDInsightCluster** Cmdlet 會選取 Azure HDInsight 群集，以取得用於提交作業的 **Invoke AzureHDInsightHiveJob** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74513-112">The **Use-AzureHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the **Invoke-AzureHDInsightHiveJob** cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="74513-113">示例</span><span class="sxs-lookup"><span data-stu-id="74513-113">EXAMPLES</span></span>

## <span data-ttu-id="74513-114">參數</span><span class="sxs-lookup"><span data-stu-id="74513-114">PARAMETERS</span></span>

### <span data-ttu-id="74513-115">-Certificate</span><span class="sxs-lookup"><span data-stu-id="74513-115">-Certificate</span></span>
<span data-ttu-id="74513-116">指定 Azure 訂閱的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="74513-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="74513-117">-端點</span><span class="sxs-lookup"><span data-stu-id="74513-117">-Endpoint</span></span>
<span data-ttu-id="74513-118">指定要用來連接 Azure 的端點。</span><span class="sxs-lookup"><span data-stu-id="74513-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="74513-119">如果您沒有指定此參數，此 Cmdlet 會使用預設端點。</span><span class="sxs-lookup"><span data-stu-id="74513-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="74513-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="74513-120">-HostedService</span></span>
<span data-ttu-id="74513-121">指定 HDInsight 服務的命名空間。</span><span class="sxs-lookup"><span data-stu-id="74513-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="74513-122">如果您沒有指定此參數，則會使用預設的命名空間。</span><span class="sxs-lookup"><span data-stu-id="74513-122">If you do not specify this parameter, the default namespace is used.</span></span>

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

### <span data-ttu-id="74513-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="74513-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="74513-124">指出是否已忽略安全通訊端層 (SSL) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="74513-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="74513-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="74513-125">-Name</span></span>
<span data-ttu-id="74513-126">指定 **AzureHDInsightHiveJob** Cmdlet 所使用之群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="74513-126">Specifies the name of the cluster that is used by the **Invoke-AzureHDInsightHiveJob** cmdlet.</span></span>

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

### <span data-ttu-id="74513-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="74513-127">-Profile</span></span>
<span data-ttu-id="74513-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="74513-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="74513-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="74513-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="74513-130">-訂閱</span><span class="sxs-lookup"><span data-stu-id="74513-130">-Subscription</span></span>
<span data-ttu-id="74513-131">指定包含要使用之 HDInsight 群集的訂閱。</span><span class="sxs-lookup"><span data-stu-id="74513-131">Specifies the subscription that contains the HDInsight clusters to use.</span></span>

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

### <span data-ttu-id="74513-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74513-132">CommonParameters</span></span>
<span data-ttu-id="74513-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74513-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74513-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74513-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74513-135">輸入</span><span class="sxs-lookup"><span data-stu-id="74513-135">INPUTS</span></span>

## <span data-ttu-id="74513-136">輸出</span><span class="sxs-lookup"><span data-stu-id="74513-136">OUTPUTS</span></span>

## <span data-ttu-id="74513-137">筆記</span><span class="sxs-lookup"><span data-stu-id="74513-137">NOTES</span></span>

## <span data-ttu-id="74513-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="74513-138">RELATED LINKS</span></span>

[<span data-ttu-id="74513-139">AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="74513-139">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="74513-140">新-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="74513-140">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="74513-141">移除-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="74513-141">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)


