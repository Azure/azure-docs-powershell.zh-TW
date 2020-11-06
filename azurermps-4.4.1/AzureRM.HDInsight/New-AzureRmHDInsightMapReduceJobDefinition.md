---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 7b3bce866712565b5eeb6fc9deccc64f9da69891
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456624"
---
# <span data-ttu-id="1344d-101">New-AzureRmHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1344d-101">New-AzureRmHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="1344d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1344d-102">SYNOPSIS</span></span>
<span data-ttu-id="1344d-103">建立 MapReduce 工作物件。</span><span class="sxs-lookup"><span data-stu-id="1344d-103">Creates a MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1344d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1344d-104">SYNTAX</span></span>

```
New-AzureRmHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1344d-105">說明</span><span class="sxs-lookup"><span data-stu-id="1344d-105">DESCRIPTION</span></span>
<span data-ttu-id="1344d-106">**新的-AzureRmHDInsightMapReduceJobDefinition** Cmdlet 會定義新的 MapReduce 作業，以搭配 Azure HDInsight 群集使用。</span><span class="sxs-lookup"><span data-stu-id="1344d-106">The **New-AzureRmHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1344d-107">示例</span><span class="sxs-lookup"><span data-stu-id="1344d-107">EXAMPLES</span></span>

### <span data-ttu-id="1344d-108">範例1：建立 MapReduce 作業定義</span><span class="sxs-lookup"><span data-stu-id="1344d-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="1344d-109">這個命令會建立 MapReduce 作業定義。</span><span class="sxs-lookup"><span data-stu-id="1344d-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="1344d-110">參數</span><span class="sxs-lookup"><span data-stu-id="1344d-110">PARAMETERS</span></span>

### <span data-ttu-id="1344d-111">-引數</span><span class="sxs-lookup"><span data-stu-id="1344d-111">-Arguments</span></span>
<span data-ttu-id="1344d-112">指定作業的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="1344d-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="1344d-113">引數會以命令列引數的形式傳遞給每個任務。</span><span class="sxs-lookup"><span data-stu-id="1344d-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="1344d-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="1344d-114">-ClassName</span></span>
<span data-ttu-id="1344d-115">指定 JAR 檔案中的作業類別。</span><span class="sxs-lookup"><span data-stu-id="1344d-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="1344d-116">-定義</span><span class="sxs-lookup"><span data-stu-id="1344d-116">-Defines</span></span>
<span data-ttu-id="1344d-117">指定要在作業執行時設定的 Hadoop 配置值。</span><span class="sxs-lookup"><span data-stu-id="1344d-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="1344d-118">-檔案</span><span class="sxs-lookup"><span data-stu-id="1344d-118">-Files</span></span>
<span data-ttu-id="1344d-119">指定與 Hive 作業相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="1344d-119">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="1344d-120">-JarFile</span><span class="sxs-lookup"><span data-stu-id="1344d-120">-JarFile</span></span>
<span data-ttu-id="1344d-121">指定作業要使用的 JAR 檔案。</span><span class="sxs-lookup"><span data-stu-id="1344d-121">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="1344d-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="1344d-122">-JobName</span></span>
<span data-ttu-id="1344d-123">指定作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="1344d-123">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="1344d-124">-LibJars</span><span class="sxs-lookup"><span data-stu-id="1344d-124">-LibJars</span></span>
<span data-ttu-id="1344d-125">指定作業的 lib JAR。</span><span class="sxs-lookup"><span data-stu-id="1344d-125">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="1344d-126">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="1344d-126">-StatusFolder</span></span>
<span data-ttu-id="1344d-127">指定包含工作之標準輸出和錯誤輸出的資料夾位置。</span><span class="sxs-lookup"><span data-stu-id="1344d-127">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="1344d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1344d-128">-DefaultProfile</span></span>
<span data-ttu-id="1344d-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1344d-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1344d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1344d-130">CommonParameters</span></span>
<span data-ttu-id="1344d-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1344d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1344d-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1344d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1344d-133">輸入</span><span class="sxs-lookup"><span data-stu-id="1344d-133">INPUTS</span></span>

## <span data-ttu-id="1344d-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1344d-134">OUTPUTS</span></span>

### <span data-ttu-id="1344d-135">AzureHDInsightMapReduceJobDefinition （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="1344d-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="1344d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="1344d-136">NOTES</span></span>

## <span data-ttu-id="1344d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="1344d-137">RELATED LINKS</span></span>

[<span data-ttu-id="1344d-138">開始-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1344d-138">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

