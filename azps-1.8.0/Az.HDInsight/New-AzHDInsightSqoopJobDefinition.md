---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: d5841a7c612bccb760a8d755fc9a1c1364cc52a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787666"
---
# <span data-ttu-id="273c0-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="273c0-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="273c0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="273c0-102">SYNOPSIS</span></span>
<span data-ttu-id="273c0-103">建立 Sqoop 工作物件。</span><span class="sxs-lookup"><span data-stu-id="273c0-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="273c0-104">句法</span><span class="sxs-lookup"><span data-stu-id="273c0-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="273c0-105">說明</span><span class="sxs-lookup"><span data-stu-id="273c0-105">DESCRIPTION</span></span>
<span data-ttu-id="273c0-106">**新的-AzHDInsightSqoopJobDefinition** Cmdlet 定義用於 Azure HDInsight 群集的 Sqoop 工作物件。</span><span class="sxs-lookup"><span data-stu-id="273c0-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="273c0-107">示例</span><span class="sxs-lookup"><span data-stu-id="273c0-107">EXAMPLES</span></span>

### <span data-ttu-id="273c0-108">範例1：建立 Sqoop 作業定義</span><span class="sxs-lookup"><span data-stu-id="273c0-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="273c0-109">這個命令會建立 Sqoop 作業定義。</span><span class="sxs-lookup"><span data-stu-id="273c0-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="273c0-110">參數</span><span class="sxs-lookup"><span data-stu-id="273c0-110">PARAMETERS</span></span>

### <span data-ttu-id="273c0-111">-Command</span><span class="sxs-lookup"><span data-stu-id="273c0-111">-Command</span></span>
<span data-ttu-id="273c0-112">指定 [Sqoop] 命令。</span><span class="sxs-lookup"><span data-stu-id="273c0-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="273c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="273c0-113">-DefaultProfile</span></span>
<span data-ttu-id="273c0-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="273c0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="273c0-115">檔案</span><span class="sxs-lookup"><span data-stu-id="273c0-115">-File</span></span>
<span data-ttu-id="273c0-116">指定包含要執行之查詢之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="273c0-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="273c0-117">該檔案必須在與群集相關聯的儲存空間帳戶上提供。</span><span class="sxs-lookup"><span data-stu-id="273c0-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="273c0-118">您可以使用這個參數，而不是 *Query* 參數。</span><span class="sxs-lookup"><span data-stu-id="273c0-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="273c0-119">-檔案</span><span class="sxs-lookup"><span data-stu-id="273c0-119">-Files</span></span>
<span data-ttu-id="273c0-120">指定與 Hive 作業相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="273c0-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="273c0-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="273c0-121">-LibDir</span></span>
<span data-ttu-id="273c0-122">指定 Sqoop 作業的文件庫目錄。</span><span class="sxs-lookup"><span data-stu-id="273c0-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="273c0-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="273c0-123">-StatusFolder</span></span>
<span data-ttu-id="273c0-124">指定包含工作之標準輸出和錯誤輸出的資料夾位置。</span><span class="sxs-lookup"><span data-stu-id="273c0-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="273c0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="273c0-125">CommonParameters</span></span>
<span data-ttu-id="273c0-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="273c0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="273c0-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="273c0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="273c0-128">輸入</span><span class="sxs-lookup"><span data-stu-id="273c0-128">INPUTS</span></span>

### <span data-ttu-id="273c0-129">所有</span><span class="sxs-lookup"><span data-stu-id="273c0-129">None</span></span>

## <span data-ttu-id="273c0-130">輸出</span><span class="sxs-lookup"><span data-stu-id="273c0-130">OUTPUTS</span></span>

### <span data-ttu-id="273c0-131">AzureHDInsightSqoopJobDefinition （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="273c0-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="273c0-132">筆記</span><span class="sxs-lookup"><span data-stu-id="273c0-132">NOTES</span></span>

## <span data-ttu-id="273c0-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="273c0-133">RELATED LINKS</span></span>

[<span data-ttu-id="273c0-134">開始-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="273c0-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

