---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 7ea8831b3fdb9f6d5b11f5419f05dd34313d100f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917321"
---
# <span data-ttu-id="e7c2f-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e7c2f-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="e7c2f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e7c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="e7c2f-103">建立 MapReduce 工作物件。</span><span class="sxs-lookup"><span data-stu-id="e7c2f-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="e7c2f-104">語法</span><span class="sxs-lookup"><span data-stu-id="e7c2f-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7c2f-105">描述</span><span class="sxs-lookup"><span data-stu-id="e7c2f-105">DESCRIPTION</span></span>
<span data-ttu-id="e7c2f-106">**New-AzHDInsightMapReduceJobDefinition** Cmdlet 定義新的 MapReduce 工作，以用於 Azure HDInsight 集區。</span><span class="sxs-lookup"><span data-stu-id="e7c2f-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e7c2f-107">例子</span><span class="sxs-lookup"><span data-stu-id="e7c2f-107">EXAMPLES</span></span>

### <span data-ttu-id="e7c2f-108">範例 1：建立 MapReduce 工作定義</span><span class="sxs-lookup"><span data-stu-id="e7c2f-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="e7c2f-109">此命令會建立 MapReduce 工作定義。</span><span class="sxs-lookup"><span data-stu-id="e7c2f-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="e7c2f-110">參數</span><span class="sxs-lookup"><span data-stu-id="e7c2f-110">PARAMETERS</span></span>

### <span data-ttu-id="e7c2f-111">-引數</span><span class="sxs-lookup"><span data-stu-id="e7c2f-111">-Arguments</span></span>
<span data-ttu-id="e7c2f-112">指定工作的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="e7c2f-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="e7c2f-113">引數會以命令列引數傳遞至每個工作。</span><span class="sxs-lookup"><span data-stu-id="e7c2f-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="e7c2f-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="e7c2f-114">-ClassName</span></span>
<span data-ttu-id="e7c2f-115">指定 JAR 檔案中的工作類別。</span><span class="sxs-lookup"><span data-stu-id="e7c2f-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="e7c2f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7c2f-116">-DefaultProfile</span></span>
<span data-ttu-id="e7c2f-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e7c2f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7c2f-118">-定義</span><span class="sxs-lookup"><span data-stu-id="e7c2f-118">-Defines</span></span>
<span data-ttu-id="e7c2f-119">指定在作業執行時要設定 Hadoop 設定值。</span><span class="sxs-lookup"><span data-stu-id="e7c2f-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="e7c2f-120">-檔案</span><span class="sxs-lookup"><span data-stu-id="e7c2f-120">-Files</span></span>
<span data-ttu-id="e7c2f-121">指定與病毒工作相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="e7c2f-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="e7c2f-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="e7c2f-122">-JarFile</span></span>
<span data-ttu-id="e7c2f-123">指定要用於工作的 JAR 檔案。</span><span class="sxs-lookup"><span data-stu-id="e7c2f-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="e7c2f-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="e7c2f-124">-JobName</span></span>
<span data-ttu-id="e7c2f-125">指定工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7c2f-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="e7c2f-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="e7c2f-126">-LibJars</span></span>
<span data-ttu-id="e7c2f-127">指定工作的 lib JARS。</span><span class="sxs-lookup"><span data-stu-id="e7c2f-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="e7c2f-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="e7c2f-128">-StatusFolder</span></span>
<span data-ttu-id="e7c2f-129">指定資料夾的位置，其中包含工作的標準輸出和錯誤輸出。</span><span class="sxs-lookup"><span data-stu-id="e7c2f-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="e7c2f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7c2f-130">CommonParameters</span></span>
<span data-ttu-id="e7c2f-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e7c2f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7c2f-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7c2f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7c2f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e7c2f-133">INPUTS</span></span>

### <span data-ttu-id="e7c2f-134">沒有</span><span class="sxs-lookup"><span data-stu-id="e7c2f-134">None</span></span>

## <span data-ttu-id="e7c2f-135">輸出</span><span class="sxs-lookup"><span data-stu-id="e7c2f-135">OUTPUTS</span></span>

### <span data-ttu-id="e7c2f-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e7c2f-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="e7c2f-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e7c2f-137">NOTES</span></span>

## <span data-ttu-id="e7c2f-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7c2f-138">RELATED LINKS</span></span>

[<span data-ttu-id="e7c2f-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e7c2f-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


