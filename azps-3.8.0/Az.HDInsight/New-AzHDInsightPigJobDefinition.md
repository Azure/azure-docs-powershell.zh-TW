---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: d9ea9152844db82d345ba1f6f50305b33975ced4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93799173"
---
# <span data-ttu-id="74d4f-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="74d4f-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="74d4f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="74d4f-103">建立豬工作物件。</span><span class="sxs-lookup"><span data-stu-id="74d4f-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="74d4f-104">句法</span><span class="sxs-lookup"><span data-stu-id="74d4f-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74d4f-105">說明</span><span class="sxs-lookup"><span data-stu-id="74d4f-105">DESCRIPTION</span></span>
<span data-ttu-id="74d4f-106">**新的-AzHDInsightPigJobDefinition** Cmdlet 定義用於 Azure HDInsight 群集的豬工作物件。</span><span class="sxs-lookup"><span data-stu-id="74d4f-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="74d4f-107">示例</span><span class="sxs-lookup"><span data-stu-id="74d4f-107">EXAMPLES</span></span>

### <span data-ttu-id="74d4f-108">範例1：建立豬作業定義</span><span class="sxs-lookup"><span data-stu-id="74d4f-108">Example 1: Create a Pig job definition</span></span>
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

<span data-ttu-id="74d4f-109">這個命令會建立豬作業定義。</span><span class="sxs-lookup"><span data-stu-id="74d4f-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="74d4f-110">參數</span><span class="sxs-lookup"><span data-stu-id="74d4f-110">PARAMETERS</span></span>

### <span data-ttu-id="74d4f-111">-引數</span><span class="sxs-lookup"><span data-stu-id="74d4f-111">-Arguments</span></span>
<span data-ttu-id="74d4f-112">指定作業的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="74d4f-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="74d4f-113">引數會以命令列引數的形式傳遞給每個任務。</span><span class="sxs-lookup"><span data-stu-id="74d4f-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="74d4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d4f-114">-DefaultProfile</span></span>
<span data-ttu-id="74d4f-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="74d4f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74d4f-116">檔案</span><span class="sxs-lookup"><span data-stu-id="74d4f-116">-File</span></span>
<span data-ttu-id="74d4f-117">指定包含要執行之查詢之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="74d4f-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="74d4f-118">該檔案必須在與群集相關聯的儲存空間帳戶上提供。</span><span class="sxs-lookup"><span data-stu-id="74d4f-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="74d4f-119">您可以使用這個參數，而不是 *Query* 參數。</span><span class="sxs-lookup"><span data-stu-id="74d4f-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="74d4f-120">-檔案</span><span class="sxs-lookup"><span data-stu-id="74d4f-120">-Files</span></span>
<span data-ttu-id="74d4f-121">指定與 Hive 作業相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="74d4f-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="74d4f-122">-Query</span><span class="sxs-lookup"><span data-stu-id="74d4f-122">-Query</span></span>
<span data-ttu-id="74d4f-123">指定豬查詢。</span><span class="sxs-lookup"><span data-stu-id="74d4f-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="74d4f-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="74d4f-124">-StatusFolder</span></span>
<span data-ttu-id="74d4f-125">指定包含工作之標準輸出和錯誤輸出的資料夾位置。</span><span class="sxs-lookup"><span data-stu-id="74d4f-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="74d4f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d4f-126">CommonParameters</span></span>
<span data-ttu-id="74d4f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74d4f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d4f-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74d4f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d4f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="74d4f-129">INPUTS</span></span>

### <span data-ttu-id="74d4f-130">所有</span><span class="sxs-lookup"><span data-stu-id="74d4f-130">None</span></span>

## <span data-ttu-id="74d4f-131">輸出</span><span class="sxs-lookup"><span data-stu-id="74d4f-131">OUTPUTS</span></span>

### <span data-ttu-id="74d4f-132">AzureHDInsightPigJobDefinition （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="74d4f-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="74d4f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="74d4f-133">NOTES</span></span>

## <span data-ttu-id="74d4f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="74d4f-134">RELATED LINKS</span></span>

[<span data-ttu-id="74d4f-135">開始-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="74d4f-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

