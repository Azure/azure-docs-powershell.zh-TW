---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6818F49E-0A51-4D99-BC3D-5A90F1F30C33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78caed4ac43f21a1afe21a8901bdcd77ba29e482
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966922"
---
# <span data-ttu-id="f2067-101">Revoke-AzureHDInsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="f2067-101">Revoke-AzureHDInsightRdpAccess</span></span>

## <span data-ttu-id="f2067-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2067-102">SYNOPSIS</span></span>
<span data-ttu-id="f2067-103">停用 RDP 對 HDInsight 群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="f2067-103">Disables RDP access to an HDInsight cluster.</span></span>

## <span data-ttu-id="f2067-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2067-104">SYNTAX</span></span>

```
Revoke-AzureHDInsightRdpAccess [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f2067-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2067-105">DESCRIPTION</span></span>
<span data-ttu-id="f2067-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="f2067-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="f2067-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="f2067-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="f2067-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="f2067-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="f2067-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="f2067-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="f2067-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="f2067-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="f2067-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="f2067-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="f2067-112">**Revoke AzureHDInsightRdpAccess** Cmdlet 會停用遠端桌面通訊協定 (RDP) 存取 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="f2067-112">The **Revoke-AzureHDInsightRdpAccess** cmdlet disables Remote Desktop Protocol (RDP) access to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f2067-113">示例</span><span class="sxs-lookup"><span data-stu-id="f2067-113">EXAMPLES</span></span>

## <span data-ttu-id="f2067-114">參數</span><span class="sxs-lookup"><span data-stu-id="f2067-114">PARAMETERS</span></span>

### <span data-ttu-id="f2067-115">-Certificate</span><span class="sxs-lookup"><span data-stu-id="f2067-115">-Certificate</span></span>
<span data-ttu-id="f2067-116">指定 Azure 訂閱的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="f2067-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="f2067-117">-端點</span><span class="sxs-lookup"><span data-stu-id="f2067-117">-Endpoint</span></span>
<span data-ttu-id="f2067-118">指定要用來連接 Azure 的端點。</span><span class="sxs-lookup"><span data-stu-id="f2067-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="f2067-119">如果您沒有指定此參數，此 Cmdlet 會使用預設端點。</span><span class="sxs-lookup"><span data-stu-id="f2067-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="f2067-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="f2067-120">-HostedService</span></span>
<span data-ttu-id="f2067-121">指定 HDInsight 服務的命名空間。</span><span class="sxs-lookup"><span data-stu-id="f2067-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="f2067-122">如果您沒有指定此參數，這個 Cmdlet 會使用預設的命名空間。</span><span class="sxs-lookup"><span data-stu-id="f2067-122">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="f2067-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="f2067-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="f2067-124">指出是否已忽略安全通訊端層 (SSL) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="f2067-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="f2067-125">-位置</span><span class="sxs-lookup"><span data-stu-id="f2067-125">-Location</span></span>
<span data-ttu-id="f2067-126">指定群集所在的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="f2067-126">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="f2067-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2067-127">-Name</span></span>
<span data-ttu-id="f2067-128">指定 Azure HDInsight 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2067-128">Specifies the name of an Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="f2067-129">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f2067-129">-Profile</span></span>
<span data-ttu-id="f2067-130">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f2067-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f2067-131">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f2067-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f2067-132">-訂閱</span><span class="sxs-lookup"><span data-stu-id="f2067-132">-Subscription</span></span>
<span data-ttu-id="f2067-133">指定訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2067-133">Specifies a subscription.</span></span>
<span data-ttu-id="f2067-134">這個 Cmdlet 會吊銷遠端桌面通訊協定 (RDP) 此參數指定之訂閱的存取權。</span><span class="sxs-lookup"><span data-stu-id="f2067-134">This cmdlet revokes Remote Desktop Protocol (RDP) access for the subscription that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2067-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2067-135">CommonParameters</span></span>
<span data-ttu-id="f2067-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2067-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2067-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f2067-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2067-138">輸入</span><span class="sxs-lookup"><span data-stu-id="f2067-138">INPUTS</span></span>

## <span data-ttu-id="f2067-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f2067-139">OUTPUTS</span></span>

## <span data-ttu-id="f2067-140">筆記</span><span class="sxs-lookup"><span data-stu-id="f2067-140">NOTES</span></span>

## <span data-ttu-id="f2067-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2067-141">RELATED LINKS</span></span>

[<span data-ttu-id="f2067-142">授與 AzureHdinsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="f2067-142">Grant-AzureHdinsightRdpAccess</span></span>](./Grant-AzureHdinsightRdpAccess.md)


