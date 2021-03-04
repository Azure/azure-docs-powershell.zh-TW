---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/invoke-azhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
ms.openlocfilehash: 2846848394cf6f376bd6b4064e193640806f81b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903833"
---
# <span data-ttu-id="0cfe1-101">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="0cfe1-101">Invoke-AzHDInsightHiveJob</span></span>

## <span data-ttu-id="0cfe1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0cfe1-102">SYNOPSIS</span></span>
<span data-ttu-id="0cfe1-103">將病毒查詢提交至 HDInsight 集區，並一次作業中取得查詢結果。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

## <span data-ttu-id="0cfe1-104">語法</span><span class="sxs-lookup"><span data-stu-id="0cfe1-104">SYNTAX</span></span>

```
Invoke-AzHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cfe1-105">描述</span><span class="sxs-lookup"><span data-stu-id="0cfe1-105">DESCRIPTION</span></span>
<span data-ttu-id="0cfe1-106">**Invoke-AzHDInsightHiveJob** Cmdlet 會提交一個 Hive 查詢至 Azure HDInsight 集區，並可在一個作業中取得查詢結果。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-106">The **Invoke-AzHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="0cfe1-107">在呼叫 **Invoke-AzHDInsightHiveJob** 之前，使用 Use-AzHDInsightCluster Cmdlet 來指定要用於查詢的組組。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-107">Use the Use-AzHDInsightCluster cmdlet before calling **Invoke-AzHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="0cfe1-108">例子</span><span class="sxs-lookup"><span data-stu-id="0cfe1-108">EXAMPLES</span></span>

### <span data-ttu-id="0cfe1-109">範例 1：將病毒查詢提交至 Azure HDInsight 集區</span><span class="sxs-lookup"><span data-stu-id="0cfe1-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="0cfe1-110">此命令將查詢 SHOW TABLES 提交到名為 your-hadoop-001 的組。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="0cfe1-111">參數</span><span class="sxs-lookup"><span data-stu-id="0cfe1-111">PARAMETERS</span></span>

### <span data-ttu-id="0cfe1-112">-引數</span><span class="sxs-lookup"><span data-stu-id="0cfe1-112">-Arguments</span></span>
<span data-ttu-id="0cfe1-113">指定工作的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="0cfe1-114">引數會以命令列引數傳遞至每個工作。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-114">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfe1-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="0cfe1-115">-DefaultContainer</span></span>
<span data-ttu-id="0cfe1-116">指定 HDInsight 集區使用之預設 Azure 儲存體帳戶中預設容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfe1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cfe1-117">-DefaultProfile</span></span>
<span data-ttu-id="0cfe1-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0cfe1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfe1-119">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0cfe1-119">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="0cfe1-120">指定 HDInsight 組使用之預設儲存空間帳戶的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-120">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfe1-121">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0cfe1-121">-DefaultStorageAccountName</span></span>
<span data-ttu-id="0cfe1-122">指定 HDInsight 集區使用的預設儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-122">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfe1-123">-定義</span><span class="sxs-lookup"><span data-stu-id="0cfe1-123">-Defines</span></span>
<span data-ttu-id="0cfe1-124">指定執行作業時要設定 Hadoop 設定值。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-124">Specifies Hadoop configuration values to set when a job runs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfe1-125">-檔案</span><span class="sxs-lookup"><span data-stu-id="0cfe1-125">-File</span></span>
<span data-ttu-id="0cfe1-126">指定 Azure 儲存體中包含要執行之查詢之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-126">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="0cfe1-127">您可以使用此參數，而非 *查詢* 參數。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-127">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfe1-128">-檔案</span><span class="sxs-lookup"><span data-stu-id="0cfe1-128">-Files</span></span>
<span data-ttu-id="0cfe1-129">指定一組要執行一項病毒的工作所需的檔案。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-129">Specifies a collection of files that are required for a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfe1-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="0cfe1-130">-JobName</span></span>
<span data-ttu-id="0cfe1-131">指定一個病毒的工作名稱。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-131">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="0cfe1-132">如果您未指定此參數，此 Cmdlet 會使用預設值：「Hive： \<first 100 characters of Query\> "。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-132">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfe1-133">-查詢</span><span class="sxs-lookup"><span data-stu-id="0cfe1-133">-Query</span></span>
<span data-ttu-id="0cfe1-134">指定病毒查詢。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-134">Specifies the Hive query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfe1-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="0cfe1-135">-RunAsFileJob</span></span>
<span data-ttu-id="0cfe1-136">表示此 Cmdlet 會以預設 Azure 儲存帳戶建立檔案，以儲存查詢。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="0cfe1-137">此 Cmdlet 會提交參照此檔案的作業，做為執行腳本。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-137">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="0cfe1-138">您可以使用此功能處理特殊字元，例如百分比符號 (%) ，這些字元會透過 Templeton 提交工作時失敗，因為 Templeton 會以百分比符號將查詢解譯為 URL 參數。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfe1-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="0cfe1-139">-StatusFolder</span></span>
<span data-ttu-id="0cfe1-140">指定資料夾的位置，其中包含工作的標準輸出和錯誤輸出。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-140">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cfe1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cfe1-141">CommonParameters</span></span>
<span data-ttu-id="0cfe1-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0cfe1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cfe1-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0cfe1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cfe1-144">輸入</span><span class="sxs-lookup"><span data-stu-id="0cfe1-144">INPUTS</span></span>

### <span data-ttu-id="0cfe1-145">沒有</span><span class="sxs-lookup"><span data-stu-id="0cfe1-145">None</span></span>

## <span data-ttu-id="0cfe1-146">輸出</span><span class="sxs-lookup"><span data-stu-id="0cfe1-146">OUTPUTS</span></span>

### <span data-ttu-id="0cfe1-147">System.String</span><span class="sxs-lookup"><span data-stu-id="0cfe1-147">System.String</span></span>

## <span data-ttu-id="0cfe1-148">筆記</span><span class="sxs-lookup"><span data-stu-id="0cfe1-148">NOTES</span></span>

## <span data-ttu-id="0cfe1-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="0cfe1-149">RELATED LINKS</span></span>

[<span data-ttu-id="0cfe1-150">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0cfe1-150">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


