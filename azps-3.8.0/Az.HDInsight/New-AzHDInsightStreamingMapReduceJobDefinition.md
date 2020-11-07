---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: adfa71fb251950f1946b3a43f030ff32b656ec50
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93799185"
---
# <span data-ttu-id="15fc4-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="15fc4-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="15fc4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="15fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="15fc4-103">建立流式處理 MapReduce 工作物件。</span><span class="sxs-lookup"><span data-stu-id="15fc4-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="15fc4-104">句法</span><span class="sxs-lookup"><span data-stu-id="15fc4-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15fc4-105">說明</span><span class="sxs-lookup"><span data-stu-id="15fc4-105">DESCRIPTION</span></span>
<span data-ttu-id="15fc4-106">**AzHDInsightStreamingMapReduceJobDefinition** Cmdlet 會定義流式處理 MapReduce 工作物件，以便與 Azure HDInsight 群集搭配使用。</span><span class="sxs-lookup"><span data-stu-id="15fc4-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="15fc4-107">示例</span><span class="sxs-lookup"><span data-stu-id="15fc4-107">EXAMPLES</span></span>

### <span data-ttu-id="15fc4-108">範例1：建立流式處理 MapReduce 作業定義</span><span class="sxs-lookup"><span data-stu-id="15fc4-108">Example 1: Create a Streaming MapReduce job definition</span></span>
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

<span data-ttu-id="15fc4-109">這個命令會建立流式處理 MapReduce 作業定義。</span><span class="sxs-lookup"><span data-stu-id="15fc4-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="15fc4-110">參數</span><span class="sxs-lookup"><span data-stu-id="15fc4-110">PARAMETERS</span></span>

### <span data-ttu-id="15fc4-111">-引數</span><span class="sxs-lookup"><span data-stu-id="15fc4-111">-Arguments</span></span>
<span data-ttu-id="15fc4-112">指定作業的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="15fc4-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="15fc4-113">引數會以命令列引數的形式傳遞給每個任務。</span><span class="sxs-lookup"><span data-stu-id="15fc4-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="15fc4-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="15fc4-114">-CommandEnvironment</span></span>
<span data-ttu-id="15fc4-115">指定當作業在輔助節點上執行時，要設定的命令列環境變數陣列。</span><span class="sxs-lookup"><span data-stu-id="15fc4-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="15fc4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15fc4-116">-DefaultProfile</span></span>
<span data-ttu-id="15fc4-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="15fc4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15fc4-118">-定義</span><span class="sxs-lookup"><span data-stu-id="15fc4-118">-Defines</span></span>
<span data-ttu-id="15fc4-119">指定要在作業執行時設定的 Hadoop 配置值。</span><span class="sxs-lookup"><span data-stu-id="15fc4-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="15fc4-120">檔案</span><span class="sxs-lookup"><span data-stu-id="15fc4-120">-File</span></span>
<span data-ttu-id="15fc4-121">指定包含要執行之查詢之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="15fc4-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="15fc4-122">您可以使用這個參數，而不是 *Query* 參數。</span><span class="sxs-lookup"><span data-stu-id="15fc4-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="15fc4-123">-檔案</span><span class="sxs-lookup"><span data-stu-id="15fc4-123">-Files</span></span>
<span data-ttu-id="15fc4-124">指定與 Hive 作業相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="15fc4-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="15fc4-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="15fc4-125">-InputPath</span></span>
<span data-ttu-id="15fc4-126">指定輸入檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="15fc4-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="15fc4-127">-映射器</span><span class="sxs-lookup"><span data-stu-id="15fc4-127">-Mapper</span></span>
<span data-ttu-id="15fc4-128">指定映射器檔案名。</span><span class="sxs-lookup"><span data-stu-id="15fc4-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="15fc4-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="15fc4-129">-OutputPath</span></span>
<span data-ttu-id="15fc4-130">指定作業輸出的路徑。</span><span class="sxs-lookup"><span data-stu-id="15fc4-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="15fc4-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="15fc4-131">-Reducer</span></span>
<span data-ttu-id="15fc4-132">指定 Reducer 檔案名。</span><span class="sxs-lookup"><span data-stu-id="15fc4-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="15fc4-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="15fc4-133">-StatusFolder</span></span>
<span data-ttu-id="15fc4-134">指定包含工作之標準輸出和錯誤輸出的資料夾位置。</span><span class="sxs-lookup"><span data-stu-id="15fc4-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="15fc4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15fc4-135">CommonParameters</span></span>
<span data-ttu-id="15fc4-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="15fc4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15fc4-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="15fc4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15fc4-138">輸入</span><span class="sxs-lookup"><span data-stu-id="15fc4-138">INPUTS</span></span>

### <span data-ttu-id="15fc4-139">所有</span><span class="sxs-lookup"><span data-stu-id="15fc4-139">None</span></span>

## <span data-ttu-id="15fc4-140">輸出</span><span class="sxs-lookup"><span data-stu-id="15fc4-140">OUTPUTS</span></span>

### <span data-ttu-id="15fc4-141">AzureHDInsightStreamingMapReduceJobDefinition （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="15fc4-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="15fc4-142">筆記</span><span class="sxs-lookup"><span data-stu-id="15fc4-142">NOTES</span></span>

## <span data-ttu-id="15fc4-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="15fc4-143">RELATED LINKS</span></span>

[<span data-ttu-id="15fc4-144">開始-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="15fc4-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


