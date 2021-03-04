---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: abe1a0eaa03d498e151a58d5970f85be088e489e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910093"
---
# <span data-ttu-id="95bf8-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="95bf8-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="95bf8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="95bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="95bf8-103">建立一個小豬工作物件。</span><span class="sxs-lookup"><span data-stu-id="95bf8-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="95bf8-104">語法</span><span class="sxs-lookup"><span data-stu-id="95bf8-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95bf8-105">描述</span><span class="sxs-lookup"><span data-stu-id="95bf8-105">DESCRIPTION</span></span>
<span data-ttu-id="95bf8-106">**New-AzHDInsightPigJobDefinition** Cmdlet 定義一個與 Azure HDInsight 集區一起使用的一個 Pig 工作物件。</span><span class="sxs-lookup"><span data-stu-id="95bf8-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="95bf8-107">例子</span><span class="sxs-lookup"><span data-stu-id="95bf8-107">EXAMPLES</span></span>

### <span data-ttu-id="95bf8-108">範例 1：建立小豬工作定義</span><span class="sxs-lookup"><span data-stu-id="95bf8-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="95bf8-109">此命令會建立一個資料元工作定義。</span><span class="sxs-lookup"><span data-stu-id="95bf8-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="95bf8-110">參數</span><span class="sxs-lookup"><span data-stu-id="95bf8-110">PARAMETERS</span></span>

### <span data-ttu-id="95bf8-111">-引數</span><span class="sxs-lookup"><span data-stu-id="95bf8-111">-Arguments</span></span>
<span data-ttu-id="95bf8-112">指定工作的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="95bf8-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="95bf8-113">引數會以命令列引數傳遞至每個工作。</span><span class="sxs-lookup"><span data-stu-id="95bf8-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="95bf8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95bf8-114">-DefaultProfile</span></span>
<span data-ttu-id="95bf8-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="95bf8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95bf8-116">-檔案</span><span class="sxs-lookup"><span data-stu-id="95bf8-116">-File</span></span>
<span data-ttu-id="95bf8-117">指定包含要執行之查詢之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="95bf8-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="95bf8-118">檔案必須在與該組關聯的儲存空間帳戶上可用。</span><span class="sxs-lookup"><span data-stu-id="95bf8-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="95bf8-119">您可以使用此參數，而非 *查詢* 參數。</span><span class="sxs-lookup"><span data-stu-id="95bf8-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="95bf8-120">-檔案</span><span class="sxs-lookup"><span data-stu-id="95bf8-120">-Files</span></span>
<span data-ttu-id="95bf8-121">指定與病毒工作相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="95bf8-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="95bf8-122">-查詢</span><span class="sxs-lookup"><span data-stu-id="95bf8-122">-Query</span></span>
<span data-ttu-id="95bf8-123">指定資料表查詢。</span><span class="sxs-lookup"><span data-stu-id="95bf8-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="95bf8-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="95bf8-124">-StatusFolder</span></span>
<span data-ttu-id="95bf8-125">指定資料夾的位置，其中包含工作的標準輸出和錯誤輸出。</span><span class="sxs-lookup"><span data-stu-id="95bf8-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="95bf8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95bf8-126">CommonParameters</span></span>
<span data-ttu-id="95bf8-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="95bf8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95bf8-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95bf8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95bf8-129">輸入</span><span class="sxs-lookup"><span data-stu-id="95bf8-129">INPUTS</span></span>

### <span data-ttu-id="95bf8-130">沒有</span><span class="sxs-lookup"><span data-stu-id="95bf8-130">None</span></span>

## <span data-ttu-id="95bf8-131">輸出</span><span class="sxs-lookup"><span data-stu-id="95bf8-131">OUTPUTS</span></span>

### <span data-ttu-id="95bf8-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="95bf8-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="95bf8-133">筆記</span><span class="sxs-lookup"><span data-stu-id="95bf8-133">NOTES</span></span>

## <span data-ttu-id="95bf8-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="95bf8-134">RELATED LINKS</span></span>

[<span data-ttu-id="95bf8-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="95bf8-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


