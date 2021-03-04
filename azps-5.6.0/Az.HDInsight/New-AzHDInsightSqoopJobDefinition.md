---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 3217673c01e4d77fe2643765df55ff58747b3133
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906914"
---
# <span data-ttu-id="4f63c-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4f63c-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="4f63c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4f63c-102">SYNOPSIS</span></span>
<span data-ttu-id="4f63c-103">建立 Sqoop 工作物件。</span><span class="sxs-lookup"><span data-stu-id="4f63c-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="4f63c-104">語法</span><span class="sxs-lookup"><span data-stu-id="4f63c-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f63c-105">描述</span><span class="sxs-lookup"><span data-stu-id="4f63c-105">DESCRIPTION</span></span>
<span data-ttu-id="4f63c-106">**New-AzHDInsightSqoopJobDefinition** Cmdlet 會定義 Sqoop 工作物件，以用於 Azure HDInsight 集區。</span><span class="sxs-lookup"><span data-stu-id="4f63c-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="4f63c-107">例子</span><span class="sxs-lookup"><span data-stu-id="4f63c-107">EXAMPLES</span></span>

### <span data-ttu-id="4f63c-108">範例 1：建立 Sqoop 工作定義</span><span class="sxs-lookup"><span data-stu-id="4f63c-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="4f63c-109">此命令會建立 Sqoop 工作定義。</span><span class="sxs-lookup"><span data-stu-id="4f63c-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="4f63c-110">參數</span><span class="sxs-lookup"><span data-stu-id="4f63c-110">PARAMETERS</span></span>

### <span data-ttu-id="4f63c-111">-命令</span><span class="sxs-lookup"><span data-stu-id="4f63c-111">-Command</span></span>
<span data-ttu-id="4f63c-112">指定 Sqoop 命令。</span><span class="sxs-lookup"><span data-stu-id="4f63c-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="4f63c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f63c-113">-DefaultProfile</span></span>
<span data-ttu-id="4f63c-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="4f63c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f63c-115">-檔案</span><span class="sxs-lookup"><span data-stu-id="4f63c-115">-File</span></span>
<span data-ttu-id="4f63c-116">指定包含要執行之查詢之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="4f63c-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="4f63c-117">檔案必須在與該組關聯的儲存空間帳戶上提供。</span><span class="sxs-lookup"><span data-stu-id="4f63c-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="4f63c-118">您可以使用此參數，而非 *查詢* 參數。</span><span class="sxs-lookup"><span data-stu-id="4f63c-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="4f63c-119">-檔案</span><span class="sxs-lookup"><span data-stu-id="4f63c-119">-Files</span></span>
<span data-ttu-id="4f63c-120">指定與病毒工作相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="4f63c-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="4f63c-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="4f63c-121">-LibDir</span></span>
<span data-ttu-id="4f63c-122">指定 Sqoop 工作文件庫目錄。</span><span class="sxs-lookup"><span data-stu-id="4f63c-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="4f63c-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="4f63c-123">-StatusFolder</span></span>
<span data-ttu-id="4f63c-124">指定資料夾的位置，其中包含工作的標準輸出和錯誤輸出。</span><span class="sxs-lookup"><span data-stu-id="4f63c-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="4f63c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f63c-125">CommonParameters</span></span>
<span data-ttu-id="4f63c-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4f63c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f63c-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f63c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f63c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="4f63c-128">INPUTS</span></span>

### <span data-ttu-id="4f63c-129">沒有</span><span class="sxs-lookup"><span data-stu-id="4f63c-129">None</span></span>

## <span data-ttu-id="4f63c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="4f63c-130">OUTPUTS</span></span>

### <span data-ttu-id="4f63c-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4f63c-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="4f63c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="4f63c-132">NOTES</span></span>

## <span data-ttu-id="4f63c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f63c-133">RELATED LINKS</span></span>

[<span data-ttu-id="4f63c-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4f63c-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


