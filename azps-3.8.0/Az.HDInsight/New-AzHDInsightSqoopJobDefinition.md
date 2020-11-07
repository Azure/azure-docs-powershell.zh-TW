---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 2cc5acb2017a9db2bf5ed1f80ccfd1069bc1a465
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93799169"
---
# <span data-ttu-id="c8d1b-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c8d1b-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="c8d1b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d1b-103">建立 Sqoop 工作物件。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="c8d1b-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8d1b-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8d1b-105">說明</span><span class="sxs-lookup"><span data-stu-id="c8d1b-105">DESCRIPTION</span></span>
<span data-ttu-id="c8d1b-106">**新的-AzHDInsightSqoopJobDefinition** Cmdlet 定義用於 Azure HDInsight 群集的 Sqoop 工作物件。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c8d1b-107">示例</span><span class="sxs-lookup"><span data-stu-id="c8d1b-107">EXAMPLES</span></span>

### <span data-ttu-id="c8d1b-108">範例1：建立 Sqoop 作業定義</span><span class="sxs-lookup"><span data-stu-id="c8d1b-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="c8d1b-109">這個命令會建立 Sqoop 作業定義。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="c8d1b-110">參數</span><span class="sxs-lookup"><span data-stu-id="c8d1b-110">PARAMETERS</span></span>

### <span data-ttu-id="c8d1b-111">-Command</span><span class="sxs-lookup"><span data-stu-id="c8d1b-111">-Command</span></span>
<span data-ttu-id="c8d1b-112">指定 [Sqoop] 命令。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="c8d1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d1b-113">-DefaultProfile</span></span>
<span data-ttu-id="c8d1b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c8d1b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8d1b-115">檔案</span><span class="sxs-lookup"><span data-stu-id="c8d1b-115">-File</span></span>
<span data-ttu-id="c8d1b-116">指定包含要執行之查詢之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="c8d1b-117">該檔案必須在與群集相關聯的儲存空間帳戶上提供。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="c8d1b-118">您可以使用這個參數，而不是 *Query* 參數。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="c8d1b-119">-檔案</span><span class="sxs-lookup"><span data-stu-id="c8d1b-119">-Files</span></span>
<span data-ttu-id="c8d1b-120">指定與 Hive 作業相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="c8d1b-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="c8d1b-121">-LibDir</span></span>
<span data-ttu-id="c8d1b-122">指定 Sqoop 作業的文件庫目錄。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="c8d1b-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="c8d1b-123">-StatusFolder</span></span>
<span data-ttu-id="c8d1b-124">指定包含工作之標準輸出和錯誤輸出的資料夾位置。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="c8d1b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d1b-125">CommonParameters</span></span>
<span data-ttu-id="c8d1b-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d1b-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d1b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="c8d1b-128">INPUTS</span></span>

### <span data-ttu-id="c8d1b-129">所有</span><span class="sxs-lookup"><span data-stu-id="c8d1b-129">None</span></span>

## <span data-ttu-id="c8d1b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="c8d1b-130">OUTPUTS</span></span>

### <span data-ttu-id="c8d1b-131">AzureHDInsightSqoopJobDefinition （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="c8d1b-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="c8d1b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="c8d1b-132">NOTES</span></span>

## <span data-ttu-id="c8d1b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8d1b-133">RELATED LINKS</span></span>

[<span data-ttu-id="c8d1b-134">開始-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c8d1b-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


