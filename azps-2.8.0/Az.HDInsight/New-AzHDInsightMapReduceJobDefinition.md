---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: c1dab20f44edfd4e3714e4465a0bf295e8e78fb5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612289"
---
# <span data-ttu-id="d76b1-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d76b1-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="d76b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d76b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d76b1-103">建立 MapReduce 工作物件。</span><span class="sxs-lookup"><span data-stu-id="d76b1-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="d76b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="d76b1-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d76b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="d76b1-105">DESCRIPTION</span></span>
<span data-ttu-id="d76b1-106">**新的-AzHDInsightMapReduceJobDefinition** Cmdlet 會定義新的 MapReduce 作業，以搭配 Azure HDInsight 群集使用。</span><span class="sxs-lookup"><span data-stu-id="d76b1-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="d76b1-107">示例</span><span class="sxs-lookup"><span data-stu-id="d76b1-107">EXAMPLES</span></span>

### <span data-ttu-id="d76b1-108">範例1：建立 MapReduce 作業定義</span><span class="sxs-lookup"><span data-stu-id="d76b1-108">Example 1: Create a MapReduce job definition</span></span>
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

<span data-ttu-id="d76b1-109">這個命令會建立 MapReduce 作業定義。</span><span class="sxs-lookup"><span data-stu-id="d76b1-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="d76b1-110">參數</span><span class="sxs-lookup"><span data-stu-id="d76b1-110">PARAMETERS</span></span>

### <span data-ttu-id="d76b1-111">-引數</span><span class="sxs-lookup"><span data-stu-id="d76b1-111">-Arguments</span></span>
<span data-ttu-id="d76b1-112">指定作業的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="d76b1-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="d76b1-113">引數會以命令列引數的形式傳遞給每個任務。</span><span class="sxs-lookup"><span data-stu-id="d76b1-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="d76b1-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="d76b1-114">-ClassName</span></span>
<span data-ttu-id="d76b1-115">指定 JAR 檔案中的作業類別。</span><span class="sxs-lookup"><span data-stu-id="d76b1-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="d76b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d76b1-116">-DefaultProfile</span></span>
<span data-ttu-id="d76b1-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d76b1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d76b1-118">-定義</span><span class="sxs-lookup"><span data-stu-id="d76b1-118">-Defines</span></span>
<span data-ttu-id="d76b1-119">指定要在作業執行時設定的 Hadoop 配置值。</span><span class="sxs-lookup"><span data-stu-id="d76b1-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="d76b1-120">-檔案</span><span class="sxs-lookup"><span data-stu-id="d76b1-120">-Files</span></span>
<span data-ttu-id="d76b1-121">指定與 Hive 作業相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="d76b1-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="d76b1-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="d76b1-122">-JarFile</span></span>
<span data-ttu-id="d76b1-123">指定作業要使用的 JAR 檔案。</span><span class="sxs-lookup"><span data-stu-id="d76b1-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="d76b1-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="d76b1-124">-JobName</span></span>
<span data-ttu-id="d76b1-125">指定作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="d76b1-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="d76b1-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="d76b1-126">-LibJars</span></span>
<span data-ttu-id="d76b1-127">指定作業的 lib JAR。</span><span class="sxs-lookup"><span data-stu-id="d76b1-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="d76b1-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="d76b1-128">-StatusFolder</span></span>
<span data-ttu-id="d76b1-129">指定包含工作之標準輸出和錯誤輸出的資料夾位置。</span><span class="sxs-lookup"><span data-stu-id="d76b1-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="d76b1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d76b1-130">CommonParameters</span></span>
<span data-ttu-id="d76b1-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d76b1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d76b1-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d76b1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d76b1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="d76b1-133">INPUTS</span></span>

### <span data-ttu-id="d76b1-134">所有</span><span class="sxs-lookup"><span data-stu-id="d76b1-134">None</span></span>

## <span data-ttu-id="d76b1-135">輸出</span><span class="sxs-lookup"><span data-stu-id="d76b1-135">OUTPUTS</span></span>

### <span data-ttu-id="d76b1-136">AzureHDInsightMapReduceJobDefinition （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="d76b1-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="d76b1-137">筆記</span><span class="sxs-lookup"><span data-stu-id="d76b1-137">NOTES</span></span>

## <span data-ttu-id="d76b1-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="d76b1-138">RELATED LINKS</span></span>

[<span data-ttu-id="d76b1-139">開始-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d76b1-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

