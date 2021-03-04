---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: be8878d338206e1355dc36082d4f9941cf141838
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916551"
---
# <span data-ttu-id="7bcd3-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7bcd3-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="7bcd3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7bcd3-102">SYNOPSIS</span></span>
<span data-ttu-id="7bcd3-103">建立一個病毒工作物件。</span><span class="sxs-lookup"><span data-stu-id="7bcd3-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="7bcd3-104">語法</span><span class="sxs-lookup"><span data-stu-id="7bcd3-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bcd3-105">描述</span><span class="sxs-lookup"><span data-stu-id="7bcd3-105">DESCRIPTION</span></span>
<span data-ttu-id="7bcd3-106">**New-AzHDInsightHiveJobDefinition** Cmdlet 定義一個與 Azure HDInsight 集區一起使用的 Hive 工作物件。</span><span class="sxs-lookup"><span data-stu-id="7bcd3-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7bcd3-107">例子</span><span class="sxs-lookup"><span data-stu-id="7bcd3-107">EXAMPLES</span></span>

### <span data-ttu-id="7bcd3-108">範例 1：建立 Hive 工作定義</span><span class="sxs-lookup"><span data-stu-id="7bcd3-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="7bcd3-109">此命令會建立一個病毒的工作定義。</span><span class="sxs-lookup"><span data-stu-id="7bcd3-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="7bcd3-110">參數</span><span class="sxs-lookup"><span data-stu-id="7bcd3-110">PARAMETERS</span></span>

### <span data-ttu-id="7bcd3-111">-引數</span><span class="sxs-lookup"><span data-stu-id="7bcd3-111">-Arguments</span></span>
<span data-ttu-id="7bcd3-112">指定工作的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="7bcd3-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="7bcd3-113">引數會以命令列引數傳遞至每個工作。</span><span class="sxs-lookup"><span data-stu-id="7bcd3-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="7bcd3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bcd3-114">-DefaultProfile</span></span>
<span data-ttu-id="7bcd3-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7bcd3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bcd3-116">-定義</span><span class="sxs-lookup"><span data-stu-id="7bcd3-116">-Defines</span></span>
<span data-ttu-id="7bcd3-117">指定在作業執行時要設定 Hadoop 設定值。</span><span class="sxs-lookup"><span data-stu-id="7bcd3-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="7bcd3-118">-檔案</span><span class="sxs-lookup"><span data-stu-id="7bcd3-118">-File</span></span>
<span data-ttu-id="7bcd3-119">指定包含要執行之查詢之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="7bcd3-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="7bcd3-120">檔案必須在與該組關聯的儲存空間帳戶上可用。</span><span class="sxs-lookup"><span data-stu-id="7bcd3-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="7bcd3-121">您可以使用此參數，而非 *查詢* 參數。</span><span class="sxs-lookup"><span data-stu-id="7bcd3-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="7bcd3-122">-檔案</span><span class="sxs-lookup"><span data-stu-id="7bcd3-122">-Files</span></span>
<span data-ttu-id="7bcd3-123">指定與病毒工作相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="7bcd3-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="7bcd3-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="7bcd3-124">-JobName</span></span>
<span data-ttu-id="7bcd3-125">指定工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bcd3-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="7bcd3-126">-查詢</span><span class="sxs-lookup"><span data-stu-id="7bcd3-126">-Query</span></span>
<span data-ttu-id="7bcd3-127">指定病毒查詢。</span><span class="sxs-lookup"><span data-stu-id="7bcd3-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="7bcd3-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="7bcd3-128">-RunAsFileJob</span></span>
<span data-ttu-id="7bcd3-129">表示此 Cmdlet 會以預設 Azure 儲存帳戶建立檔案，以儲存查詢。</span><span class="sxs-lookup"><span data-stu-id="7bcd3-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="7bcd3-130">此 Cmdlet 會提交參照此檔案的作業，做為執行腳本。</span><span class="sxs-lookup"><span data-stu-id="7bcd3-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="7bcd3-131">您可以使用此功能處理特殊字元，例如百分比符號 (%) ，這些字元會透過 Templeton 提交工作時失敗，因為 Templeton 會以百分比符號將查詢解譯為 URL 參數。</span><span class="sxs-lookup"><span data-stu-id="7bcd3-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bcd3-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="7bcd3-132">-StatusFolder</span></span>
<span data-ttu-id="7bcd3-133">指定資料夾的位置，其中包含工作的標準輸出和錯誤輸出。</span><span class="sxs-lookup"><span data-stu-id="7bcd3-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="7bcd3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bcd3-134">CommonParameters</span></span>
<span data-ttu-id="7bcd3-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7bcd3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bcd3-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bcd3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bcd3-137">輸入</span><span class="sxs-lookup"><span data-stu-id="7bcd3-137">INPUTS</span></span>

### <span data-ttu-id="7bcd3-138">沒有</span><span class="sxs-lookup"><span data-stu-id="7bcd3-138">None</span></span>

## <span data-ttu-id="7bcd3-139">輸出</span><span class="sxs-lookup"><span data-stu-id="7bcd3-139">OUTPUTS</span></span>

### <span data-ttu-id="7bcd3-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7bcd3-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="7bcd3-141">筆記</span><span class="sxs-lookup"><span data-stu-id="7bcd3-141">NOTES</span></span>

## <span data-ttu-id="7bcd3-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="7bcd3-142">RELATED LINKS</span></span>

[<span data-ttu-id="7bcd3-143">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7bcd3-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


