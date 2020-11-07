---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 7D73D37B-17EE-4FF8-9A21-D2014D5417D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: fa779907648ca8e8e1288394d562c86b6102d9ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967922"
---
# <span data-ttu-id="66a45-101">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="66a45-101">Remove-AzureHDInsightCluster</span></span>

## <span data-ttu-id="66a45-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66a45-102">SYNOPSIS</span></span>
<span data-ttu-id="66a45-103">從訂閱中刪除 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="66a45-103">Deletes an HDInsight cluster from a subscription.</span></span>

## <span data-ttu-id="66a45-104">句法</span><span class="sxs-lookup"><span data-stu-id="66a45-104">SYNTAX</span></span>

```
Remove-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="66a45-105">說明</span><span class="sxs-lookup"><span data-stu-id="66a45-105">DESCRIPTION</span></span>
<span data-ttu-id="66a45-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="66a45-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="66a45-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="66a45-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="66a45-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="66a45-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="66a45-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="66a45-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="66a45-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="66a45-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="66a45-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="66a45-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="66a45-112">**AzureHDInsightCluster** Cmdlet 會從訂閱中刪除指定的 HDInsight 服務群集。</span><span class="sxs-lookup"><span data-stu-id="66a45-112">The **Remove-AzureHDInsightCluster** cmdlet deletes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="66a45-113">這個作業也會刪除任何儲存在 Hadoop 分散式檔案系統)  (在群集上的資料。</span><span class="sxs-lookup"><span data-stu-id="66a45-113">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="66a45-114">儲存在關聯之 Azure 儲存空間帳戶中的資料不會被刪除。</span><span class="sxs-lookup"><span data-stu-id="66a45-114">Data stored in the associated Azure Storage account is not deleted.</span></span>

## <span data-ttu-id="66a45-115">示例</span><span class="sxs-lookup"><span data-stu-id="66a45-115">EXAMPLES</span></span>

### <span data-ttu-id="66a45-116">範例1：移除群集</span><span class="sxs-lookup"><span data-stu-id="66a45-116">Example 1: Remove a cluster</span></span>
```
PS C:\>Remove-AzureHDInsightCluster -Name "HDICluster"
```

<span data-ttu-id="66a45-117">這個命令會刪除名為 HDICluster 的 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="66a45-117">This command deletes the HDInsight cluster named HDICluster.</span></span>

## <span data-ttu-id="66a45-118">參數</span><span class="sxs-lookup"><span data-stu-id="66a45-118">PARAMETERS</span></span>

### <span data-ttu-id="66a45-119">-Certificate</span><span class="sxs-lookup"><span data-stu-id="66a45-119">-Certificate</span></span>
<span data-ttu-id="66a45-120">指定 Azure 訂閱的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="66a45-120">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="66a45-121">-端點</span><span class="sxs-lookup"><span data-stu-id="66a45-121">-Endpoint</span></span>
<span data-ttu-id="66a45-122">指定要用來連接 Azure 的端點。</span><span class="sxs-lookup"><span data-stu-id="66a45-122">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="66a45-123">如果您沒有指定此參數，此 Cmdlet 會使用預設端點。</span><span class="sxs-lookup"><span data-stu-id="66a45-123">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="66a45-124">-HostedService</span><span class="sxs-lookup"><span data-stu-id="66a45-124">-HostedService</span></span>
<span data-ttu-id="66a45-125">如果您不想使用預設的命名空間，請指定 HDInsight 服務的命名空間。</span><span class="sxs-lookup"><span data-stu-id="66a45-125">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="66a45-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="66a45-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="66a45-127">指出是否已忽略安全通訊端層 (SSL) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="66a45-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="66a45-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="66a45-128">-Name</span></span>
<span data-ttu-id="66a45-129">指定要移除的 HDInsight 群集名稱。</span><span class="sxs-lookup"><span data-stu-id="66a45-129">Specifies the name of the HDInsight cluster to remove.</span></span>

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

### <span data-ttu-id="66a45-130">-設定檔</span><span class="sxs-lookup"><span data-stu-id="66a45-130">-Profile</span></span>
<span data-ttu-id="66a45-131">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="66a45-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="66a45-132">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="66a45-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="66a45-133">-訂閱</span><span class="sxs-lookup"><span data-stu-id="66a45-133">-Subscription</span></span>
<span data-ttu-id="66a45-134">指定包含要移除之 HDInsight 群集的訂閱帳戶。</span><span class="sxs-lookup"><span data-stu-id="66a45-134">Specifies the subscription account that contains the HDInsight cluster to remove.</span></span>

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

### <span data-ttu-id="66a45-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a45-135">CommonParameters</span></span>
<span data-ttu-id="66a45-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66a45-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a45-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66a45-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a45-138">輸入</span><span class="sxs-lookup"><span data-stu-id="66a45-138">INPUTS</span></span>

## <span data-ttu-id="66a45-139">輸出</span><span class="sxs-lookup"><span data-stu-id="66a45-139">OUTPUTS</span></span>

## <span data-ttu-id="66a45-140">筆記</span><span class="sxs-lookup"><span data-stu-id="66a45-140">NOTES</span></span>

## <span data-ttu-id="66a45-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="66a45-141">RELATED LINKS</span></span>

[<span data-ttu-id="66a45-142">AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="66a45-142">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="66a45-143">新-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="66a45-143">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="66a45-144">使用-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="66a45-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


