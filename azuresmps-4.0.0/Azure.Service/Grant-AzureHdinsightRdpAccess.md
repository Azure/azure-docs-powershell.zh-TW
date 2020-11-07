---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 95CCEB79-EAC4-4F56-B289-5401F976E5F5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92b2c005f855ccf99e8bae4d8db8445ba7e63dad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967708"
---
# <span data-ttu-id="b5e0f-101">Grant-AzureHDInsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="b5e0f-101">Grant-AzureHDInsightRdpAccess</span></span>

## <span data-ttu-id="b5e0f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e0f-103">授予 HDInsight 群集的 RDP 存取權。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-103">Grants RDP access to an HDInsight cluster.</span></span>

## <span data-ttu-id="b5e0f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5e0f-104">SYNTAX</span></span>

```
Grant-AzureHDInsightRdpAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -RdpCredential <PSCredential> -RdpAccessExpiry <DateTime> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b5e0f-105">說明</span><span class="sxs-lookup"><span data-stu-id="b5e0f-105">DESCRIPTION</span></span>
<span data-ttu-id="b5e0f-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="b5e0f-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="b5e0f-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="b5e0f-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="b5e0f-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="b5e0f-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="b5e0f-112">**Grant AzureHDInsightRdpAccess** Cmdlet 會授權遠端桌面通訊協定 (RDP) 存取 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-112">The **Grant-AzureHDInsightRdpAccess** cmdlet grants Remote Desktop Protocol (RDP) access to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b5e0f-113">示例</span><span class="sxs-lookup"><span data-stu-id="b5e0f-113">EXAMPLES</span></span>

## <span data-ttu-id="b5e0f-114">參數</span><span class="sxs-lookup"><span data-stu-id="b5e0f-114">PARAMETERS</span></span>

### <span data-ttu-id="b5e0f-115">-Certificate</span><span class="sxs-lookup"><span data-stu-id="b5e0f-115">-Certificate</span></span>
<span data-ttu-id="b5e0f-116">指定 Azure 訂閱的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="b5e0f-117">-端點</span><span class="sxs-lookup"><span data-stu-id="b5e0f-117">-Endpoint</span></span>
<span data-ttu-id="b5e0f-118">指定要用來連接 Azure 的端點。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="b5e0f-119">如果您沒有指定此參數，此 Cmdlet 會使用預設端點。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="b5e0f-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="b5e0f-120">-HostedService</span></span>
<span data-ttu-id="b5e0f-121">指定 HDInsight 服務的命名空間。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="b5e0f-122">如果您沒有指定此參數，這個 Cmdlet 會使用預設的命名空間。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-122">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="b5e0f-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="b5e0f-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="b5e0f-124">指出是否已忽略安全通訊端層 (SSL) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="b5e0f-125">-位置</span><span class="sxs-lookup"><span data-stu-id="b5e0f-125">-Location</span></span>
<span data-ttu-id="b5e0f-126">指定群集所在的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-126">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="b5e0f-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="b5e0f-127">-Name</span></span>
<span data-ttu-id="b5e0f-128">指定 Azure HDInsight 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-128">Specifies the name of an Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5e0f-129">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b5e0f-129">-Profile</span></span>
<span data-ttu-id="b5e0f-130">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b5e0f-131">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b5e0f-132">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="b5e0f-132">-RdpAccessExpiry</span></span>
<span data-ttu-id="b5e0f-133">指定遠端桌面通訊協定的到期日（例如 **DateTime** 物件） (RDP) 對群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-133">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e0f-134">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="b5e0f-134">-RdpCredential</span></span>
<span data-ttu-id="b5e0f-135">指定 RDP 存取群集的認證。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-135">Specifies the credentials for RDP access to a cluster.</span></span>

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

### <span data-ttu-id="b5e0f-136">-訂閱</span><span class="sxs-lookup"><span data-stu-id="b5e0f-136">-Subscription</span></span>
<span data-ttu-id="b5e0f-137">指定包含要授與存取權之 HDInsight 群集的訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-137">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="b5e0f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e0f-138">CommonParameters</span></span>
<span data-ttu-id="b5e0f-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e0f-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b5e0f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e0f-141">輸入</span><span class="sxs-lookup"><span data-stu-id="b5e0f-141">INPUTS</span></span>

## <span data-ttu-id="b5e0f-142">輸出</span><span class="sxs-lookup"><span data-stu-id="b5e0f-142">OUTPUTS</span></span>

## <span data-ttu-id="b5e0f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="b5e0f-143">NOTES</span></span>

## <span data-ttu-id="b5e0f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5e0f-144">RELATED LINKS</span></span>

[<span data-ttu-id="b5e0f-145">吊銷-AzureHdinsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="b5e0f-145">Revoke-AzureHdinsightRdpAccess</span></span>](./Revoke-AzureHdinsightRdpAccess.md)


