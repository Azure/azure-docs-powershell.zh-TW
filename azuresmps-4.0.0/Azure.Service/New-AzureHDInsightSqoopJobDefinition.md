---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E11AAB11-0CBF-4746-91D7-4D5E64801C29
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6dba4c331a69093f49c95728c028eaaf5d0bdb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967361"
---
# <span data-ttu-id="f618d-101">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f618d-101">New-AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="f618d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f618d-102">SYNOPSIS</span></span>
<span data-ttu-id="f618d-103">定義新的 Sqoop 工作。</span><span class="sxs-lookup"><span data-stu-id="f618d-103">Defines a new Sqoop job.</span></span>

## <span data-ttu-id="f618d-104">句法</span><span class="sxs-lookup"><span data-stu-id="f618d-104">SYNTAX</span></span>

```
New-AzureHDInsightSqoopJobDefinition [-Command <String>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f618d-105">說明</span><span class="sxs-lookup"><span data-stu-id="f618d-105">DESCRIPTION</span></span>
<span data-ttu-id="f618d-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="f618d-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="f618d-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="f618d-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="f618d-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="f618d-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="f618d-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="f618d-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="f618d-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="f618d-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="f618d-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="f618d-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="f618d-112">**新的-AzureHDInsightSqoopJobDefinition** Cmdlet 會建立要在 Azure HDInsight 群集上執行的 Sqoop 作業。</span><span class="sxs-lookup"><span data-stu-id="f618d-112">The **New-AzureHDInsightSqoopJobDefinition** cmdlet creates a Sqoop job to run on an Azure HDInsight cluster.</span></span>

<span data-ttu-id="f618d-113">Sqoop 是一種在 Hadoop 群集與關聯式資料庫之間傳輸資料的工具。</span><span class="sxs-lookup"><span data-stu-id="f618d-113">Sqoop is a tool to transfer data between Hadoop clusters and relational databases.</span></span>
<span data-ttu-id="f618d-114">您可以使用 Sqoop，將資料從 SQL Server 資料庫匯入到 Hadoop 分散式檔案系統 (HDFS) 、使用 Hadoop MapReduce 轉換資料，然後再將資料從 HDFS 匯出回 SQL Server 資料庫。</span><span class="sxs-lookup"><span data-stu-id="f618d-114">You can use Sqoop to import data from a SQL Server database to a Hadoop Distributed File System (HDFS), transform the data with Hadoop MapReduce, and then export the data from the HDFS back to the SQL Server database.</span></span>

## <span data-ttu-id="f618d-115">示例</span><span class="sxs-lookup"><span data-stu-id="f618d-115">EXAMPLES</span></span>

### <span data-ttu-id="f618d-116">範例1：匯入資料</span><span class="sxs-lookup"><span data-stu-id="f618d-116">Example 1: Import data</span></span>
```
PS C:\>$SqoopJobDef = New-AzureHDInsightSqoopJobDefinition -Command "import --connect jdbc:sqlserver://<SQLDatabaseServerName>.database.windows.net:1433;username=<SQLDatabasUsername>@<SQLDatabaseServerName>; password=<SQLDatabasePassword>; database=<SQLDatabaseDatabaseName> --table <TableName> --target-dir wasb://<ContainerName>@<WindowsAzureStorageAccountName>.blob.core.windows.net/<Path>"
```

<span data-ttu-id="f618d-117">這個命令會定義一個 Sqoop 作業，將資料表中的所有列從 AzureSQL 伺服器資料庫匯入到 HDInsight 群集，然後將作業定義儲存在 $SqoopJobDef 變數中。</span><span class="sxs-lookup"><span data-stu-id="f618d-117">This command defines a Sqoop job that imports all of the rows in a table from an AzureSQL Server database to an HDInsight cluster, and then stores the job definition in the $SqoopJobDef variable.</span></span>

## <span data-ttu-id="f618d-118">參數</span><span class="sxs-lookup"><span data-stu-id="f618d-118">PARAMETERS</span></span>

### <span data-ttu-id="f618d-119">-Command</span><span class="sxs-lookup"><span data-stu-id="f618d-119">-Command</span></span>
<span data-ttu-id="f618d-120">指定 Sqoop 命令及其引數。</span><span class="sxs-lookup"><span data-stu-id="f618d-120">Specifies a Sqoop command and its arguments.</span></span>

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

### <span data-ttu-id="f618d-121">檔案</span><span class="sxs-lookup"><span data-stu-id="f618d-121">-File</span></span>
<span data-ttu-id="f618d-122">指定包含要執行命令的腳本檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="f618d-122">Specifies the path to a script file that contains the commands to run.</span></span>
<span data-ttu-id="f618d-123">腳本檔案必須位於 WASB 上。</span><span class="sxs-lookup"><span data-stu-id="f618d-123">The script file must be located on WASB.</span></span>

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

### <span data-ttu-id="f618d-124">-檔案</span><span class="sxs-lookup"><span data-stu-id="f618d-124">-Files</span></span>
<span data-ttu-id="f618d-125">指定作業所需的 WASB 檔案集合。</span><span class="sxs-lookup"><span data-stu-id="f618d-125">Specifies the collection of WASB files that are required for a job.</span></span>

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

### <span data-ttu-id="f618d-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f618d-126">-Profile</span></span>
<span data-ttu-id="f618d-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f618d-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f618d-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f618d-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f618d-129">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="f618d-129">-StatusFolder</span></span>
<span data-ttu-id="f618d-130">指定包含作業之標準輸出和錯誤輸出的資料夾位置，包括其結束代碼和任務記錄。</span><span class="sxs-lookup"><span data-stu-id="f618d-130">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="f618d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f618d-131">CommonParameters</span></span>
<span data-ttu-id="f618d-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f618d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f618d-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f618d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f618d-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f618d-134">INPUTS</span></span>

## <span data-ttu-id="f618d-135">輸出</span><span class="sxs-lookup"><span data-stu-id="f618d-135">OUTPUTS</span></span>

## <span data-ttu-id="f618d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f618d-136">NOTES</span></span>

## <span data-ttu-id="f618d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="f618d-137">RELATED LINKS</span></span>

[<span data-ttu-id="f618d-138">新-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f618d-138">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="f618d-139">新-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f618d-139">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="f618d-140">新-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f618d-140">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="f618d-141">新-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f618d-141">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


