---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 771B7CB2-88F6-4FC5-9DB0-E623D231E51A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdbf7778ca2d7498d7f33586f7e9e50e0955c521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967408"
---
# <span data-ttu-id="91935-101">Set-AzureHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="91935-101">Set-AzureHDInsightClusterSize</span></span>

## <span data-ttu-id="91935-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91935-102">SYNOPSIS</span></span>
<span data-ttu-id="91935-103">設定 HDInsight 群集的資料節點數。</span><span class="sxs-lookup"><span data-stu-id="91935-103">Sets the number of data nodes for an HDInsight cluster.</span></span>

## <span data-ttu-id="91935-104">句法</span><span class="sxs-lookup"><span data-stu-id="91935-104">SYNTAX</span></span>

### <span data-ttu-id="91935-105">在具有名稱的節點中設定群集大小。</span><span class="sxs-lookup"><span data-stu-id="91935-105">Set cluster size in nodes with name.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> -Name <String> [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="91935-106">在具有 [從管線的群集的節點] 中設定群集大小。</span><span class="sxs-lookup"><span data-stu-id="91935-106">Set cluster size in nodes with cluster from pipeline.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> [-Force] -Cluster <AzureHDInsightCluster>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="91935-107">群集依名稱 (與特定的訂閱認證) </span><span class="sxs-lookup"><span data-stu-id="91935-107">Cluster By Name (with Specific Subscription Credential)</span></span>
```
Set-AzureHDInsightClusterSize [-Certificate <X509Certificate2>] [-Subscription <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="91935-108">說明</span><span class="sxs-lookup"><span data-stu-id="91935-108">DESCRIPTION</span></span>
<span data-ttu-id="91935-109">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="91935-109">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="91935-110">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="91935-110">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="91935-111">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="91935-111">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="91935-112">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="91935-112">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="91935-113">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="91935-113">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="91935-114">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="91935-114">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="91935-115">**AzureHDInsightClusterSize** Cmdlet 會設定 Azure HDInsight 群集的資料節點數。</span><span class="sxs-lookup"><span data-stu-id="91935-115">The **Set-AzureHDInsightClusterSize** cmdlet sets the number of data nodes for an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="91935-116">示例</span><span class="sxs-lookup"><span data-stu-id="91935-116">EXAMPLES</span></span>

## <span data-ttu-id="91935-117">參數</span><span class="sxs-lookup"><span data-stu-id="91935-117">PARAMETERS</span></span>

### <span data-ttu-id="91935-118">-Certificate</span><span class="sxs-lookup"><span data-stu-id="91935-118">-Certificate</span></span>
<span data-ttu-id="91935-119">指定 Azure 訂閱的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="91935-119">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91935-120">-群集</span><span class="sxs-lookup"><span data-stu-id="91935-120">-Cluster</span></span>
<span data-ttu-id="91935-121">指定要調整大小的群集。</span><span class="sxs-lookup"><span data-stu-id="91935-121">Specifies the cluster to resize.</span></span>

```yaml
Type: AzureHDInsightCluster
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91935-122">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="91935-122">-ClusterSizeInNodes</span></span>
<span data-ttu-id="91935-123">指定要為群集建立的資料節點數。</span><span class="sxs-lookup"><span data-stu-id="91935-123">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with name.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91935-124">-端點</span><span class="sxs-lookup"><span data-stu-id="91935-124">-Endpoint</span></span>
<span data-ttu-id="91935-125">指定要用來連接 Azure 的端點。</span><span class="sxs-lookup"><span data-stu-id="91935-125">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="91935-126">如果您沒有指定此參數，此 Cmdlet 會使用預設端點。</span><span class="sxs-lookup"><span data-stu-id="91935-126">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91935-127">-Force</span><span class="sxs-lookup"><span data-stu-id="91935-127">-Force</span></span>
<span data-ttu-id="91935-128">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="91935-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Set cluster size in nodes with name., Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91935-129">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="91935-129">-IgnoreSslErrors</span></span>
<span data-ttu-id="91935-130">指出是否已忽略安全通訊端層 (SSL) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="91935-130">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91935-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="91935-131">-Name</span></span>
<span data-ttu-id="91935-132">指定要調整大小的 HDInsight 群集名稱。</span><span class="sxs-lookup"><span data-stu-id="91935-132">Specifies the name of the HDInsight cluster to resize.</span></span>

```yaml
Type: String
Parameter Sets: Set cluster size in nodes with name.
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91935-133">-設定檔</span><span class="sxs-lookup"><span data-stu-id="91935-133">-Profile</span></span>
<span data-ttu-id="91935-134">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="91935-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="91935-135">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="91935-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="91935-136">-訂閱</span><span class="sxs-lookup"><span data-stu-id="91935-136">-Subscription</span></span>
<span data-ttu-id="91935-137">指定訂閱。</span><span class="sxs-lookup"><span data-stu-id="91935-137">Specifies a subscription.</span></span>
<span data-ttu-id="91935-138">這個 Cmdlet 會設定此參數指定之訂閱的群集大小。</span><span class="sxs-lookup"><span data-stu-id="91935-138">This cmdlet sets the cluster size for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91935-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91935-139">CommonParameters</span></span>
<span data-ttu-id="91935-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91935-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91935-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91935-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91935-142">輸入</span><span class="sxs-lookup"><span data-stu-id="91935-142">INPUTS</span></span>

## <span data-ttu-id="91935-143">輸出</span><span class="sxs-lookup"><span data-stu-id="91935-143">OUTPUTS</span></span>

## <span data-ttu-id="91935-144">筆記</span><span class="sxs-lookup"><span data-stu-id="91935-144">NOTES</span></span>

## <span data-ttu-id="91935-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="91935-145">RELATED LINKS</span></span>

