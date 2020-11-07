---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E3D22B03-2997-4F2C-895E-AE0993FD7C92
online version: ''
schema: 2.0.0
ms.openlocfilehash: bfd3e1f2bb5d057dec8a7bee5929ba5c67c8d53d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967944"
---
# <span data-ttu-id="4a513-101">Grant-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4a513-101">Grant-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="4a513-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a513-102">SYNOPSIS</span></span>
<span data-ttu-id="4a513-103">授予群集的 HTTP 存取權。</span><span class="sxs-lookup"><span data-stu-id="4a513-103">Grants HTTP access to a cluster.</span></span>

## <span data-ttu-id="4a513-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a513-104">SYNTAX</span></span>

```
Grant-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Credential <PSCredential> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4a513-105">說明</span><span class="sxs-lookup"><span data-stu-id="4a513-105">DESCRIPTION</span></span>
<span data-ttu-id="4a513-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="4a513-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="4a513-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="4a513-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="4a513-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="4a513-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="4a513-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="4a513-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="4a513-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="4a513-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="4a513-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="4a513-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="4a513-112">**授與 AzureHDInsightHttpServicesAccess** Cmdlet 會使用 ODBC、Ambari、Oozie 和 web 服務，將 HTTP 存取權授予 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="4a513-112">The **Grant-AzureHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie, and web services.</span></span>

## <span data-ttu-id="4a513-113">示例</span><span class="sxs-lookup"><span data-stu-id="4a513-113">EXAMPLES</span></span>

## <span data-ttu-id="4a513-114">參數</span><span class="sxs-lookup"><span data-stu-id="4a513-114">PARAMETERS</span></span>

### <span data-ttu-id="4a513-115">-Certificate</span><span class="sxs-lookup"><span data-stu-id="4a513-115">-Certificate</span></span>
<span data-ttu-id="4a513-116">指定 Azure 訂閱的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="4a513-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="4a513-117">-認證</span><span class="sxs-lookup"><span data-stu-id="4a513-117">-Credential</span></span>
<span data-ttu-id="4a513-118">指定 HTTP 存取的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="4a513-118">Specifies a user name and password for HTTP access.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a513-119">-端點</span><span class="sxs-lookup"><span data-stu-id="4a513-119">-Endpoint</span></span>
<span data-ttu-id="4a513-120">指定要用來連接 Azure 的端點。</span><span class="sxs-lookup"><span data-stu-id="4a513-120">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="4a513-121">如果您沒有指定此參數，此 Cmdlet 會使用預設端點。</span><span class="sxs-lookup"><span data-stu-id="4a513-121">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="4a513-122">-HostedService</span><span class="sxs-lookup"><span data-stu-id="4a513-122">-HostedService</span></span>
<span data-ttu-id="4a513-123">指定 HDInsight 服務的命名空間。</span><span class="sxs-lookup"><span data-stu-id="4a513-123">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="4a513-124">如果您沒有指定此參數，這個 Cmdlet 會使用預設的命名空間。</span><span class="sxs-lookup"><span data-stu-id="4a513-124">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="4a513-125">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="4a513-125">-IgnoreSslErrors</span></span>
<span data-ttu-id="4a513-126">指出是否已忽略安全通訊端層 (SSL) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a513-126">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="4a513-127">-位置</span><span class="sxs-lookup"><span data-stu-id="4a513-127">-Location</span></span>
<span data-ttu-id="4a513-128">指定群集所在的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="4a513-128">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="4a513-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="4a513-129">-Name</span></span>
<span data-ttu-id="4a513-130">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a513-130">Specifies the name of a cluster.</span></span>
<span data-ttu-id="4a513-131">這個 Cmdlet 會將 HTTP 存取權授予此參數指定的群集。</span><span class="sxs-lookup"><span data-stu-id="4a513-131">This cmdlet grants HTTP access to the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="4a513-132">-設定檔</span><span class="sxs-lookup"><span data-stu-id="4a513-132">-Profile</span></span>
<span data-ttu-id="4a513-133">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4a513-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4a513-134">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="4a513-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4a513-135">-訂閱</span><span class="sxs-lookup"><span data-stu-id="4a513-135">-Subscription</span></span>
<span data-ttu-id="4a513-136">指定包含要授與存取權之 HDInsight 群集的訂閱。</span><span class="sxs-lookup"><span data-stu-id="4a513-136">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="4a513-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a513-137">CommonParameters</span></span>
<span data-ttu-id="4a513-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a513-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a513-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4a513-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a513-140">輸入</span><span class="sxs-lookup"><span data-stu-id="4a513-140">INPUTS</span></span>

## <span data-ttu-id="4a513-141">輸出</span><span class="sxs-lookup"><span data-stu-id="4a513-141">OUTPUTS</span></span>

## <span data-ttu-id="4a513-142">筆記</span><span class="sxs-lookup"><span data-stu-id="4a513-142">NOTES</span></span>

## <span data-ttu-id="4a513-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a513-143">RELATED LINKS</span></span>

[<span data-ttu-id="4a513-144">吊銷-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4a513-144">Revoke-AzureHDInsightHttpServicesAccess</span></span>](./Revoke-AzureHDInsightHttpServicesAccess.md)


