---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 60e0f8e6799a89d673b3c9ca7de7827b197440fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903830"
---
# <span data-ttu-id="4c238-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4c238-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="4c238-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4c238-102">SYNOPSIS</span></span>
<span data-ttu-id="4c238-103">建立串流 MapReduce 工作物件。</span><span class="sxs-lookup"><span data-stu-id="4c238-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="4c238-104">語法</span><span class="sxs-lookup"><span data-stu-id="4c238-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c238-105">描述</span><span class="sxs-lookup"><span data-stu-id="4c238-105">DESCRIPTION</span></span>
<span data-ttu-id="4c238-106">**New-AzHDInsightStreamingMapReduceJobDefinition** Cmdlet 會定義串流 MapReduce 工作物件，以用於 Azure HDInsight 集區。</span><span class="sxs-lookup"><span data-stu-id="4c238-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="4c238-107">例子</span><span class="sxs-lookup"><span data-stu-id="4c238-107">EXAMPLES</span></span>

### <span data-ttu-id="4c238-108">範例 1：建立串流 MapReduce 工作定義</span><span class="sxs-lookup"><span data-stu-id="4c238-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="4c238-109">此命令會建立串流 MapReduce 工作定義。</span><span class="sxs-lookup"><span data-stu-id="4c238-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="4c238-110">參數</span><span class="sxs-lookup"><span data-stu-id="4c238-110">PARAMETERS</span></span>

### <span data-ttu-id="4c238-111">-引數</span><span class="sxs-lookup"><span data-stu-id="4c238-111">-Arguments</span></span>
<span data-ttu-id="4c238-112">指定工作的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="4c238-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="4c238-113">引數會以命令列引數傳遞至每個工作。</span><span class="sxs-lookup"><span data-stu-id="4c238-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="4c238-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="4c238-114">-CommandEnvironment</span></span>
<span data-ttu-id="4c238-115">指定工作在員工節點上執行時要設定之命令列環境變數的陣列。</span><span class="sxs-lookup"><span data-stu-id="4c238-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="4c238-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c238-116">-DefaultProfile</span></span>
<span data-ttu-id="4c238-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="4c238-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c238-118">-定義</span><span class="sxs-lookup"><span data-stu-id="4c238-118">-Defines</span></span>
<span data-ttu-id="4c238-119">指定在作業執行時要設定 Hadoop 設定值。</span><span class="sxs-lookup"><span data-stu-id="4c238-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="4c238-120">-檔案</span><span class="sxs-lookup"><span data-stu-id="4c238-120">-File</span></span>
<span data-ttu-id="4c238-121">指定要執行之查詢之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="4c238-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="4c238-122">您可以使用此參數，而非 *查詢* 參數。</span><span class="sxs-lookup"><span data-stu-id="4c238-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="4c238-123">-檔案</span><span class="sxs-lookup"><span data-stu-id="4c238-123">-Files</span></span>
<span data-ttu-id="4c238-124">指定與病毒工作相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="4c238-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="4c238-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="4c238-125">-InputPath</span></span>
<span data-ttu-id="4c238-126">指定輸入檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="4c238-126">Specifies the path to the input files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c238-127">-對應器</span><span class="sxs-lookup"><span data-stu-id="4c238-127">-Mapper</span></span>
<span data-ttu-id="4c238-128">指定對應程式檔案名。</span><span class="sxs-lookup"><span data-stu-id="4c238-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="4c238-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="4c238-129">-OutputPath</span></span>
<span data-ttu-id="4c238-130">指定工作輸出的路徑。</span><span class="sxs-lookup"><span data-stu-id="4c238-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="4c238-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="4c238-131">-Reducer</span></span>
<span data-ttu-id="4c238-132">指定 Reducer 檔案名。</span><span class="sxs-lookup"><span data-stu-id="4c238-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="4c238-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="4c238-133">-StatusFolder</span></span>
<span data-ttu-id="4c238-134">指定資料夾的位置，其中包含工作的標準輸出和錯誤輸出。</span><span class="sxs-lookup"><span data-stu-id="4c238-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="4c238-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c238-135">CommonParameters</span></span>
<span data-ttu-id="4c238-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4c238-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c238-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c238-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c238-138">輸入</span><span class="sxs-lookup"><span data-stu-id="4c238-138">INPUTS</span></span>

### <span data-ttu-id="4c238-139">沒有</span><span class="sxs-lookup"><span data-stu-id="4c238-139">None</span></span>

## <span data-ttu-id="4c238-140">輸出</span><span class="sxs-lookup"><span data-stu-id="4c238-140">OUTPUTS</span></span>

### <span data-ttu-id="4c238-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4c238-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="4c238-142">筆記</span><span class="sxs-lookup"><span data-stu-id="4c238-142">NOTES</span></span>

## <span data-ttu-id="4c238-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c238-143">RELATED LINKS</span></span>

[<span data-ttu-id="4c238-144">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4c238-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


