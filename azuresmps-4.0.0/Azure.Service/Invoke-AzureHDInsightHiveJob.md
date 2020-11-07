---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: BB01591D-4E1A-4C89-8B2A-5A242C29B125
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8904c5e228d181a3090b3a0d62d74d84005bd2b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967694"
---
# <span data-ttu-id="51262-101">Invoke-AzureHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="51262-101">Invoke-AzureHDInsightHiveJob</span></span>

## <span data-ttu-id="51262-102">摘要</span><span class="sxs-lookup"><span data-stu-id="51262-102">SYNOPSIS</span></span>
<span data-ttu-id="51262-103">將 Hive 查詢提交至 HDInsight 群集，顯示查詢執行的進度，並在一項操作中取得查詢結果。</span><span class="sxs-lookup"><span data-stu-id="51262-103">Submits Hive queries to an HDInsight cluster, shows progress of the query execution, and gets query results in one operation.</span></span>

## <span data-ttu-id="51262-104">句法</span><span class="sxs-lookup"><span data-stu-id="51262-104">SYNTAX</span></span>

```
Invoke-AzureHDInsightHiveJob [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="51262-105">說明</span><span class="sxs-lookup"><span data-stu-id="51262-105">DESCRIPTION</span></span>
<span data-ttu-id="51262-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="51262-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="51262-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="51262-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="51262-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="51262-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="51262-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="51262-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="51262-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="51262-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="51262-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="51262-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="51262-112">**AzureHDInsightHiveJob** Cmdlet 會將 Hive 查詢提交至 HDInsight 群集，顯示查詢執行的進度，並以一個操作取得查詢結果。</span><span class="sxs-lookup"><span data-stu-id="51262-112">The **Invoke-AzureHDInsightHiveJob** cmdlet submits Hive queries to an HDInsight cluster, displays the progress of the query execution, and gets the query results in one operation.</span></span>
<span data-ttu-id="51262-113">您必須先執行 Use-AzureHDInsightCluster Cmdlet，才能執行 **AzureHDInsightHiveJob** ，以指定要提交查詢的 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="51262-113">You must run the Use-AzureHDInsightCluster cmdlet before running **Invoke-AzureHDInsightHiveJob** to specify the HDInsight cluster to which to submit a query.</span></span>

## <span data-ttu-id="51262-114">示例</span><span class="sxs-lookup"><span data-stu-id="51262-114">EXAMPLES</span></span>

### <span data-ttu-id="51262-115">範例1：提交 Hive 查詢</span><span class="sxs-lookup"><span data-stu-id="51262-115">Example 1: Submit a Hive query</span></span>
```
PS C:\>Use-AzureHDInsightCluster "Cluster01" -Subscription (Get-AzureSubscription -Current).SubscriptionId 
PS C:\> Invoke-AzureHDInsightHiveJob "select * from hivesampletable limit 10"
```

<span data-ttu-id="51262-116">第一個命令使用 **AzureHDInsightCluster** Cmdlet 來指定目前訂閱中用來進行 Hive 查詢的群集。</span><span class="sxs-lookup"><span data-stu-id="51262-116">The first command uses the **Use-AzureHDInsightCluster** cmdlet to specify a cluster in the current subscription to use for a Hive query.</span></span>

<span data-ttu-id="51262-117">第二個命令使用 **AzureHDInsightHiveJob** Cmdlet 來提交 Hive 查詢。</span><span class="sxs-lookup"><span data-stu-id="51262-117">The second command uses the **Invoke-AzureHDInsightHiveJob** cmdlet to submit the Hive query.</span></span>

## <span data-ttu-id="51262-118">參數</span><span class="sxs-lookup"><span data-stu-id="51262-118">PARAMETERS</span></span>

### <span data-ttu-id="51262-119">-引數</span><span class="sxs-lookup"><span data-stu-id="51262-119">-Arguments</span></span>
<span data-ttu-id="51262-120">指定 Hadoop 作業的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="51262-120">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="51262-121">引數會以命令列引數的形式傳遞給每個任務。</span><span class="sxs-lookup"><span data-stu-id="51262-121">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51262-122">-定義</span><span class="sxs-lookup"><span data-stu-id="51262-122">-Defines</span></span>
<span data-ttu-id="51262-123">指定要在作業執行時設定的 Hadoop 配置值。</span><span class="sxs-lookup"><span data-stu-id="51262-123">Specifies Hadoop configuration values to set when a job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51262-124">檔案</span><span class="sxs-lookup"><span data-stu-id="51262-124">-File</span></span>
<span data-ttu-id="51262-125">指定 [Windows Azure Storage Blob] (WASB [Azure Blob 儲存體] 中包含要執行查詢的檔案) 路徑。</span><span class="sxs-lookup"><span data-stu-id="51262-125">Specifies the Windows Azure Storage Blob (WASB) path to a file in Azure blob storage that contains the query to run.</span></span>
<span data-ttu-id="51262-126">您可以使用這個參數，而不是 *Query* 參數。</span><span class="sxs-lookup"><span data-stu-id="51262-126">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51262-127">-檔案</span><span class="sxs-lookup"><span data-stu-id="51262-127">-Files</span></span>
<span data-ttu-id="51262-128">指定 Hive 作業所需的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="51262-128">Specifies a collection of files that are required for a Hive job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51262-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="51262-129">-JobName</span></span>
<span data-ttu-id="51262-130">指定 Hive 工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="51262-130">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="51262-131">如果您沒有指定此參數，這個 Cmdlet 會使用預設值：「Hive：」 \<first 100 characters of Query\> 。</span><span class="sxs-lookup"><span data-stu-id="51262-131">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51262-132">-設定檔</span><span class="sxs-lookup"><span data-stu-id="51262-132">-Profile</span></span>
<span data-ttu-id="51262-133">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="51262-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51262-134">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="51262-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51262-135">-Query</span><span class="sxs-lookup"><span data-stu-id="51262-135">-Query</span></span>
<span data-ttu-id="51262-136">指定 Hive 查詢。</span><span class="sxs-lookup"><span data-stu-id="51262-136">Specifies a Hive query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryText

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51262-137">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="51262-137">-RunAsFileJob</span></span>
<span data-ttu-id="51262-138">指示這個 Cmdlet 會在預設的 Azure 儲存空間帳戶中建立檔案，以儲存查詢。</span><span class="sxs-lookup"><span data-stu-id="51262-138">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="51262-139">這個 Cmdlet 會提交參照此檔案做為腳本以執行的工作。</span><span class="sxs-lookup"><span data-stu-id="51262-139">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="51262-140">您可以使用這個功能來處理特殊的字元，例如百分號 (% ) ，這些字元會在透過 Templeton 提交作業時失敗，因為 Templeton 會使用百分號符號作為 URL 參數來轉譯查詢。</span><span class="sxs-lookup"><span data-stu-id="51262-140">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="51262-141">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="51262-141">-StatusFolder</span></span>
<span data-ttu-id="51262-142">指定包含作業之標準輸出和錯誤輸出的資料夾位置，包括其結束代碼和任務記錄。</span><span class="sxs-lookup"><span data-stu-id="51262-142">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51262-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51262-143">CommonParameters</span></span>
<span data-ttu-id="51262-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="51262-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51262-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="51262-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51262-146">輸入</span><span class="sxs-lookup"><span data-stu-id="51262-146">INPUTS</span></span>

## <span data-ttu-id="51262-147">輸出</span><span class="sxs-lookup"><span data-stu-id="51262-147">OUTPUTS</span></span>

## <span data-ttu-id="51262-148">筆記</span><span class="sxs-lookup"><span data-stu-id="51262-148">NOTES</span></span>

## <span data-ttu-id="51262-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="51262-149">RELATED LINKS</span></span>

[<span data-ttu-id="51262-150">新-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="51262-150">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="51262-151">使用-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="51262-151">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


