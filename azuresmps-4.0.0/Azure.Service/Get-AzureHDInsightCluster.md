---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3B39F43D-E74A-441D-91BC-26C324C1EDF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d0ea12e873604360114b02bb89d9bde12c9e70e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967090"
---
# <span data-ttu-id="9db48-101">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9db48-101">Get-AzureHDInsightCluster</span></span>

## <span data-ttu-id="9db48-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9db48-102">SYNOPSIS</span></span>
<span data-ttu-id="9db48-103">取得 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="9db48-103">Gets an HDInsight cluster.</span></span>

## <span data-ttu-id="9db48-104">句法</span><span class="sxs-lookup"><span data-stu-id="9db48-104">SYNTAX</span></span>

```
Get-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9db48-105">說明</span><span class="sxs-lookup"><span data-stu-id="9db48-105">DESCRIPTION</span></span>
<span data-ttu-id="9db48-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="9db48-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="9db48-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="9db48-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="9db48-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="9db48-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="9db48-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="9db48-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="9db48-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="9db48-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="9db48-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="9db48-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="9db48-112">**AzureHDInsightCluster** Cmdlet 會取得目前訂閱的 Azure HDInsight 服務群集。</span><span class="sxs-lookup"><span data-stu-id="9db48-112">The **Get-AzureHDInsightCluster** cmdlet gets the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="9db48-113">您可以使用 *Name* 參數來取得特定的群集。</span><span class="sxs-lookup"><span data-stu-id="9db48-113">You can use the *Name* parameter to get a specific cluster.</span></span>

## <span data-ttu-id="9db48-114">示例</span><span class="sxs-lookup"><span data-stu-id="9db48-114">EXAMPLES</span></span>

### <span data-ttu-id="9db48-115">範例1：取得訂閱中的群集</span><span class="sxs-lookup"><span data-stu-id="9db48-115">Example 1: Get the clusters in a subscription</span></span>
```
PS C:\> Get-AzureHDInsightCluster
```

<span data-ttu-id="9db48-116">這個命令會取得目前訂閱中 HDInsight 群集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9db48-116">This command gets information about the HDInsight clusters in the current subscription.</span></span>

## <span data-ttu-id="9db48-117">參數</span><span class="sxs-lookup"><span data-stu-id="9db48-117">PARAMETERS</span></span>

### <span data-ttu-id="9db48-118">-Certificate</span><span class="sxs-lookup"><span data-stu-id="9db48-118">-Certificate</span></span>
<span data-ttu-id="9db48-119">指定 Azure 訂閱的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="9db48-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="9db48-120">-端點</span><span class="sxs-lookup"><span data-stu-id="9db48-120">-Endpoint</span></span>
<span data-ttu-id="9db48-121">指定要用來連接 Azure 的端點。</span><span class="sxs-lookup"><span data-stu-id="9db48-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="9db48-122">如果您沒有指定此參數，此 Cmdlet 會使用預設端點。</span><span class="sxs-lookup"><span data-stu-id="9db48-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="9db48-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="9db48-123">-HostedService</span></span>
<span data-ttu-id="9db48-124">指定 HDInsight 服務的命名空間。</span><span class="sxs-lookup"><span data-stu-id="9db48-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="9db48-125">如果您沒有指定此參數，這個 Cmdlet 會使用預設的命名空間。</span><span class="sxs-lookup"><span data-stu-id="9db48-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="9db48-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="9db48-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="9db48-127">指出是否已忽略安全通訊端層 (SSL) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="9db48-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="9db48-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="9db48-128">-Name</span></span>
<span data-ttu-id="9db48-129">指定要取得的 HDInsight 群集名稱。</span><span class="sxs-lookup"><span data-stu-id="9db48-129">Specifies the name of an HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9db48-130">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9db48-130">-Profile</span></span>
<span data-ttu-id="9db48-131">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9db48-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9db48-132">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="9db48-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9db48-133">-訂閱</span><span class="sxs-lookup"><span data-stu-id="9db48-133">-Subscription</span></span>
<span data-ttu-id="9db48-134">指定包含要取得之 HDInsight 群集的訂閱。</span><span class="sxs-lookup"><span data-stu-id="9db48-134">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

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

### <span data-ttu-id="9db48-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db48-135">CommonParameters</span></span>
<span data-ttu-id="9db48-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9db48-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db48-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9db48-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db48-138">輸入</span><span class="sxs-lookup"><span data-stu-id="9db48-138">INPUTS</span></span>

## <span data-ttu-id="9db48-139">輸出</span><span class="sxs-lookup"><span data-stu-id="9db48-139">OUTPUTS</span></span>

## <span data-ttu-id="9db48-140">筆記</span><span class="sxs-lookup"><span data-stu-id="9db48-140">NOTES</span></span>

## <span data-ttu-id="9db48-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="9db48-141">RELATED LINKS</span></span>

[<span data-ttu-id="9db48-142">新-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9db48-142">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="9db48-143">移除-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9db48-143">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="9db48-144">使用-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9db48-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


