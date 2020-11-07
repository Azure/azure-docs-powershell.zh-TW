---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 22ddeeffd696de260e13c1c817afedfabe1887a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625304"
---
# <span data-ttu-id="b2f0b-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b2f0b-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="b2f0b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b2f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f0b-103">建立流式處理 MapReduce 工作物件。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-103">Creates a Streaming MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2f0b-104">句法</span><span class="sxs-lookup"><span data-stu-id="b2f0b-104">SYNTAX</span></span>

```
New-AzureRmHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>]
 [-Files <String[]>] [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>]
 -InputPath <String> [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2f0b-105">說明</span><span class="sxs-lookup"><span data-stu-id="b2f0b-105">DESCRIPTION</span></span>
<span data-ttu-id="b2f0b-106">**AzureRmHDInsightStreamingMapReduceJobDefinition** Cmdlet 會定義流式處理 MapReduce 工作物件，以便與 Azure HDInsight 群集搭配使用。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-106">The **New-AzureRmHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b2f0b-107">示例</span><span class="sxs-lookup"><span data-stu-id="b2f0b-107">EXAMPLES</span></span>

### <span data-ttu-id="b2f0b-108">範例1：建立流式處理 MapReduce 作業定義</span><span class="sxs-lookup"><span data-stu-id="b2f0b-108">Example 1: Create a Streaming MapReduce job definition</span></span>
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

<span data-ttu-id="b2f0b-109">這個命令會建立流式處理 MapReduce 作業定義。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="b2f0b-110">參數</span><span class="sxs-lookup"><span data-stu-id="b2f0b-110">PARAMETERS</span></span>

### <span data-ttu-id="b2f0b-111">-引數</span><span class="sxs-lookup"><span data-stu-id="b2f0b-111">-Arguments</span></span>
<span data-ttu-id="b2f0b-112">指定作業的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="b2f0b-113">引數會以命令列引數的形式傳遞給每個任務。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="b2f0b-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="b2f0b-114">-CommandEnvironment</span></span>
<span data-ttu-id="b2f0b-115">指定當作業在輔助節點上執行時，要設定的命令列環境變數陣列。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="b2f0b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f0b-116">-DefaultProfile</span></span>
<span data-ttu-id="b2f0b-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b2f0b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2f0b-118">-定義</span><span class="sxs-lookup"><span data-stu-id="b2f0b-118">-Defines</span></span>
<span data-ttu-id="b2f0b-119">指定要在作業執行時設定的 Hadoop 配置值。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="b2f0b-120">檔案</span><span class="sxs-lookup"><span data-stu-id="b2f0b-120">-File</span></span>
<span data-ttu-id="b2f0b-121">指定包含要執行之查詢之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="b2f0b-122">您可以使用這個參數，而不是 *Query* 參數。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="b2f0b-123">-檔案</span><span class="sxs-lookup"><span data-stu-id="b2f0b-123">-Files</span></span>
<span data-ttu-id="b2f0b-124">指定與 Hive 作業相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="b2f0b-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="b2f0b-125">-InputPath</span></span>
<span data-ttu-id="b2f0b-126">指定輸入檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="b2f0b-127">-映射器</span><span class="sxs-lookup"><span data-stu-id="b2f0b-127">-Mapper</span></span>
<span data-ttu-id="b2f0b-128">指定映射器檔案名。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="b2f0b-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b2f0b-129">-OutputPath</span></span>
<span data-ttu-id="b2f0b-130">指定作業輸出的路徑。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="b2f0b-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="b2f0b-131">-Reducer</span></span>
<span data-ttu-id="b2f0b-132">指定 Reducer 檔案名。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="b2f0b-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="b2f0b-133">-StatusFolder</span></span>
<span data-ttu-id="b2f0b-134">指定包含工作之標準輸出和錯誤輸出的資料夾位置。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="b2f0b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f0b-135">CommonParameters</span></span>
<span data-ttu-id="b2f0b-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f0b-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f0b-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b2f0b-138">INPUTS</span></span>

### <span data-ttu-id="b2f0b-139">所有</span><span class="sxs-lookup"><span data-stu-id="b2f0b-139">None</span></span>

## <span data-ttu-id="b2f0b-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b2f0b-140">OUTPUTS</span></span>

### <span data-ttu-id="b2f0b-141">AzureHDInsightStreamingMapReduceJobDefinition （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="b2f0b-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="b2f0b-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b2f0b-142">NOTES</span></span>

## <span data-ttu-id="b2f0b-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2f0b-143">RELATED LINKS</span></span>

[<span data-ttu-id="b2f0b-144">開始-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b2f0b-144">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


