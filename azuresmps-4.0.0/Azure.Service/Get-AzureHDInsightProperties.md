---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 325DE85D-B9CB-4584-8C61-DA417736ABBF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55992408c1376c9456157387456b114c292b44c2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967797"
---
# <span data-ttu-id="bcf28-101">Get-AzureHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="bcf28-101">Get-AzureHDInsightProperties</span></span>

## <span data-ttu-id="bcf28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bcf28-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf28-103">取得 HDInsight 服務的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="bcf28-103">Gets properties specific to an HDInsight service.</span></span>

## <span data-ttu-id="bcf28-104">句法</span><span class="sxs-lookup"><span data-stu-id="bcf28-104">SYNTAX</span></span>

```
Get-AzureHDInsightProperties [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Locations] [-Subscription <String>] [-Versions] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="bcf28-105">說明</span><span class="sxs-lookup"><span data-stu-id="bcf28-105">DESCRIPTION</span></span>
<span data-ttu-id="bcf28-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="bcf28-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="bcf28-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="bcf28-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="bcf28-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="bcf28-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="bcf28-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="bcf28-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="bcf28-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="bcf28-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="bcf28-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="bcf28-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="bcf28-112">**AzureHDInsightProperties** Cmdlet 會取得 Azure HDInsight 服務專用的屬性，例如可用的 Azure 區域清單、HDInsight 群集版本，以及可用的計算能力。</span><span class="sxs-lookup"><span data-stu-id="bcf28-112">The **Get-AzureHDInsightProperties** cmdlet gets properties specific to an Azure HDInsight service, such as a list of available Azure regions, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="bcf28-113">示例</span><span class="sxs-lookup"><span data-stu-id="bcf28-113">EXAMPLES</span></span>

### <span data-ttu-id="bcf28-114">範例1：取得訂閱的 HDInsight 屬性</span><span class="sxs-lookup"><span data-stu-id="bcf28-114">Example 1: Get HDInsight properties for a subscription</span></span>
```
PS C:\>$SubName = Get-AzureSubscription -Current | %{ $_.SubscriptionName }
PS C:\> Get-AzureHDInsightProperties -Subscription $SubName
```

<span data-ttu-id="bcf28-115">第一個命令會取得目前 Azure 訂閱的名稱，然後將其儲存在 $SubName 變數中。</span><span class="sxs-lookup"><span data-stu-id="bcf28-115">The first command gets the name of the current Azure subscription, and then stores it in the $SubName variable.</span></span>

<span data-ttu-id="bcf28-116">第二個命令會在 $SubName 中取得訂閱的 HDInsight 屬性。</span><span class="sxs-lookup"><span data-stu-id="bcf28-116">The second command gets the HDInsight properties for the subscription in $SubName.</span></span>

## <span data-ttu-id="bcf28-117">參數</span><span class="sxs-lookup"><span data-stu-id="bcf28-117">PARAMETERS</span></span>

### <span data-ttu-id="bcf28-118">-Certificate</span><span class="sxs-lookup"><span data-stu-id="bcf28-118">-Certificate</span></span>
<span data-ttu-id="bcf28-119">指定 Azure 訂閱的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="bcf28-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="bcf28-120">-端點</span><span class="sxs-lookup"><span data-stu-id="bcf28-120">-Endpoint</span></span>
<span data-ttu-id="bcf28-121">指定要用來連接 Azure 的端點。</span><span class="sxs-lookup"><span data-stu-id="bcf28-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="bcf28-122">如果您沒有指定此參數，此 Cmdlet 會使用預設端點。</span><span class="sxs-lookup"><span data-stu-id="bcf28-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="bcf28-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="bcf28-123">-HostedService</span></span>
<span data-ttu-id="bcf28-124">指定 HDInsight 服務的命名空間。</span><span class="sxs-lookup"><span data-stu-id="bcf28-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="bcf28-125">如果您沒有指定此參數，這個 Cmdlet 會使用預設的命名空間。</span><span class="sxs-lookup"><span data-stu-id="bcf28-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="bcf28-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="bcf28-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="bcf28-127">指出是否已忽略安全通訊端層 (SSL) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="bcf28-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="bcf28-128">-位置</span><span class="sxs-lookup"><span data-stu-id="bcf28-128">-Locations</span></span>
<span data-ttu-id="bcf28-129">表示此 Cmdlet 會取得 HDInsight 服務可用的 Azure 區域清單。</span><span class="sxs-lookup"><span data-stu-id="bcf28-129">Indicates that this cmdlet gets the list of Azure regions where the HDInsight service is available.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcf28-130">-設定檔</span><span class="sxs-lookup"><span data-stu-id="bcf28-130">-Profile</span></span>
<span data-ttu-id="bcf28-131">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="bcf28-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bcf28-132">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="bcf28-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bcf28-133">-訂閱</span><span class="sxs-lookup"><span data-stu-id="bcf28-133">-Subscription</span></span>
<span data-ttu-id="bcf28-134">指定包含要取得之 HDInsight 屬性的訂閱。</span><span class="sxs-lookup"><span data-stu-id="bcf28-134">Specifies the subscription that contains the HDInsight properties to get.</span></span>

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

### <span data-ttu-id="bcf28-135">-版本</span><span class="sxs-lookup"><span data-stu-id="bcf28-135">-Versions</span></span>
<span data-ttu-id="bcf28-136">表示此 Cmdlet 會取得訂閱服務中可用的 HDInsight 群集版本清單。</span><span class="sxs-lookup"><span data-stu-id="bcf28-136">Indicates that this cmdlet gets the list of HDInsight cluster versions that are available in the service for a subscription.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcf28-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf28-137">CommonParameters</span></span>
<span data-ttu-id="bcf28-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bcf28-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf28-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bcf28-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf28-140">輸入</span><span class="sxs-lookup"><span data-stu-id="bcf28-140">INPUTS</span></span>

## <span data-ttu-id="bcf28-141">輸出</span><span class="sxs-lookup"><span data-stu-id="bcf28-141">OUTPUTS</span></span>

## <span data-ttu-id="bcf28-142">筆記</span><span class="sxs-lookup"><span data-stu-id="bcf28-142">NOTES</span></span>

## <span data-ttu-id="bcf28-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcf28-143">RELATED LINKS</span></span>

