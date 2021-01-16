---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: d6ab15fffd71776188291c58f2e21bbee5f27423
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438292"
---
# <span data-ttu-id="27f07-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="27f07-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="27f07-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27f07-102">SYNOPSIS</span></span>
<span data-ttu-id="27f07-103">建立 MapReduce 工作物件。</span><span class="sxs-lookup"><span data-stu-id="27f07-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="27f07-104">句法</span><span class="sxs-lookup"><span data-stu-id="27f07-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27f07-105">說明</span><span class="sxs-lookup"><span data-stu-id="27f07-105">DESCRIPTION</span></span>
<span data-ttu-id="27f07-106">**新的-AzHDInsightMapReduceJobDefinition** Cmdlet 會定義新的 MapReduce 作業，以搭配 Azure HDInsight 群集使用。</span><span class="sxs-lookup"><span data-stu-id="27f07-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="27f07-107">示例</span><span class="sxs-lookup"><span data-stu-id="27f07-107">EXAMPLES</span></span>

### <span data-ttu-id="27f07-108">範例1：建立 MapReduce 作業定義</span><span class="sxs-lookup"><span data-stu-id="27f07-108">Example 1: Create a MapReduce job definition</span></span>
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

<span data-ttu-id="27f07-109">這個命令會建立 MapReduce 作業定義。</span><span class="sxs-lookup"><span data-stu-id="27f07-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="27f07-110">參數</span><span class="sxs-lookup"><span data-stu-id="27f07-110">PARAMETERS</span></span>

### <span data-ttu-id="27f07-111">-引數</span><span class="sxs-lookup"><span data-stu-id="27f07-111">-Arguments</span></span>
<span data-ttu-id="27f07-112">指定作業的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="27f07-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="27f07-113">引數會以命令列引數的形式傳遞給每個任務。</span><span class="sxs-lookup"><span data-stu-id="27f07-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="27f07-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="27f07-114">-ClassName</span></span>
<span data-ttu-id="27f07-115">指定 JAR 檔案中的作業類別。</span><span class="sxs-lookup"><span data-stu-id="27f07-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="27f07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27f07-116">-DefaultProfile</span></span>
<span data-ttu-id="27f07-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="27f07-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27f07-118">-定義</span><span class="sxs-lookup"><span data-stu-id="27f07-118">-Defines</span></span>
<span data-ttu-id="27f07-119">指定要在作業執行時設定的 Hadoop 配置值。</span><span class="sxs-lookup"><span data-stu-id="27f07-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="27f07-120">-檔案</span><span class="sxs-lookup"><span data-stu-id="27f07-120">-Files</span></span>
<span data-ttu-id="27f07-121">指定與 Hive 作業相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="27f07-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="27f07-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="27f07-122">-JarFile</span></span>
<span data-ttu-id="27f07-123">指定作業要使用的 JAR 檔案。</span><span class="sxs-lookup"><span data-stu-id="27f07-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="27f07-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="27f07-124">-JobName</span></span>
<span data-ttu-id="27f07-125">指定作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="27f07-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="27f07-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="27f07-126">-LibJars</span></span>
<span data-ttu-id="27f07-127">指定作業的 lib JAR。</span><span class="sxs-lookup"><span data-stu-id="27f07-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="27f07-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="27f07-128">-StatusFolder</span></span>
<span data-ttu-id="27f07-129">指定包含工作之標準輸出和錯誤輸出的資料夾位置。</span><span class="sxs-lookup"><span data-stu-id="27f07-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="27f07-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27f07-130">CommonParameters</span></span>
<span data-ttu-id="27f07-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27f07-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27f07-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="27f07-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27f07-133">輸入</span><span class="sxs-lookup"><span data-stu-id="27f07-133">INPUTS</span></span>

### <span data-ttu-id="27f07-134">所有</span><span class="sxs-lookup"><span data-stu-id="27f07-134">None</span></span>

## <span data-ttu-id="27f07-135">輸出</span><span class="sxs-lookup"><span data-stu-id="27f07-135">OUTPUTS</span></span>

### <span data-ttu-id="27f07-136">AzureHDInsightMapReduceJobDefinition （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="27f07-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="27f07-137">筆記</span><span class="sxs-lookup"><span data-stu-id="27f07-137">NOTES</span></span>

## <span data-ttu-id="27f07-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="27f07-138">RELATED LINKS</span></span>

[<span data-ttu-id="27f07-139">開始-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="27f07-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


