---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: f74d0e56265e5b976de9cf289f3b6a4900b76d6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449365"
---
# <span data-ttu-id="78554-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="78554-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="78554-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78554-102">SYNOPSIS</span></span>
<span data-ttu-id="78554-103">建立流式處理 MapReduce 工作物件。</span><span class="sxs-lookup"><span data-stu-id="78554-103">Creates a Streaming MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78554-104">句法</span><span class="sxs-lookup"><span data-stu-id="78554-104">SYNTAX</span></span>

```
New-AzureRmHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>]
 [-Files <String[]>] [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>]
 -InputPath <String> [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78554-105">說明</span><span class="sxs-lookup"><span data-stu-id="78554-105">DESCRIPTION</span></span>
<span data-ttu-id="78554-106">**AzureRmHDInsightStreamingMapReduceJobDefinition** Cmdlet 會定義流式處理 MapReduce 工作物件，以便與 Azure HDInsight 群集搭配使用。</span><span class="sxs-lookup"><span data-stu-id="78554-106">The **New-AzureRmHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="78554-107">示例</span><span class="sxs-lookup"><span data-stu-id="78554-107">EXAMPLES</span></span>

### <span data-ttu-id="78554-108">範例1：建立流式處理 MapReduce 作業定義</span><span class="sxs-lookup"><span data-stu-id="78554-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="78554-109">這個命令會建立流式處理 MapReduce 作業定義。</span><span class="sxs-lookup"><span data-stu-id="78554-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="78554-110">參數</span><span class="sxs-lookup"><span data-stu-id="78554-110">PARAMETERS</span></span>

### <span data-ttu-id="78554-111">-引數</span><span class="sxs-lookup"><span data-stu-id="78554-111">-Arguments</span></span>
<span data-ttu-id="78554-112">指定作業的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="78554-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="78554-113">引數會以命令列引數的形式傳遞給每個任務。</span><span class="sxs-lookup"><span data-stu-id="78554-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="78554-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="78554-114">-CommandEnvironment</span></span>
<span data-ttu-id="78554-115">指定當作業在輔助節點上執行時，要設定的命令列環境變數陣列。</span><span class="sxs-lookup"><span data-stu-id="78554-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78554-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78554-116">-DefaultProfile</span></span>
<span data-ttu-id="78554-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="78554-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78554-118">-定義</span><span class="sxs-lookup"><span data-stu-id="78554-118">-Defines</span></span>
<span data-ttu-id="78554-119">指定要在作業執行時設定的 Hadoop 配置值。</span><span class="sxs-lookup"><span data-stu-id="78554-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78554-120">檔案</span><span class="sxs-lookup"><span data-stu-id="78554-120">-File</span></span>
<span data-ttu-id="78554-121">指定包含要執行之查詢之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="78554-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="78554-122">您可以使用這個參數，而不是 *Query* 參數。</span><span class="sxs-lookup"><span data-stu-id="78554-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="78554-123">-檔案</span><span class="sxs-lookup"><span data-stu-id="78554-123">-Files</span></span>
<span data-ttu-id="78554-124">指定與 Hive 作業相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="78554-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="78554-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="78554-125">-InputPath</span></span>
<span data-ttu-id="78554-126">指定輸入檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="78554-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="78554-127">-映射器</span><span class="sxs-lookup"><span data-stu-id="78554-127">-Mapper</span></span>
<span data-ttu-id="78554-128">指定映射器檔案名。</span><span class="sxs-lookup"><span data-stu-id="78554-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="78554-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="78554-129">-OutputPath</span></span>
<span data-ttu-id="78554-130">指定作業輸出的路徑。</span><span class="sxs-lookup"><span data-stu-id="78554-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="78554-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="78554-131">-Reducer</span></span>
<span data-ttu-id="78554-132">指定 Reducer 檔案名。</span><span class="sxs-lookup"><span data-stu-id="78554-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="78554-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="78554-133">-StatusFolder</span></span>
<span data-ttu-id="78554-134">指定包含工作之標準輸出和錯誤輸出的資料夾位置。</span><span class="sxs-lookup"><span data-stu-id="78554-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="78554-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78554-135">CommonParameters</span></span>
<span data-ttu-id="78554-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78554-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78554-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78554-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78554-138">輸入</span><span class="sxs-lookup"><span data-stu-id="78554-138">INPUTS</span></span>

### <span data-ttu-id="78554-139">所有</span><span class="sxs-lookup"><span data-stu-id="78554-139">None</span></span>
<span data-ttu-id="78554-140">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="78554-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="78554-141">輸出</span><span class="sxs-lookup"><span data-stu-id="78554-141">OUTPUTS</span></span>

### <span data-ttu-id="78554-142">AzureHDInsightStreamingMapReduceJobDefinition （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="78554-142">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="78554-143">筆記</span><span class="sxs-lookup"><span data-stu-id="78554-143">NOTES</span></span>

## <span data-ttu-id="78554-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="78554-144">RELATED LINKS</span></span>

[<span data-ttu-id="78554-145">開始-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="78554-145">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


