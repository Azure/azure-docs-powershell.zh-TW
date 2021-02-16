---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 4cf45d237d5611d5d9fb0fb1eb178d2c85807354
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139143"
---
# <span data-ttu-id="db6be-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="db6be-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="db6be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db6be-102">SYNOPSIS</span></span>
<span data-ttu-id="db6be-103">建立 Hive 工作物件。</span><span class="sxs-lookup"><span data-stu-id="db6be-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="db6be-104">句法</span><span class="sxs-lookup"><span data-stu-id="db6be-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db6be-105">說明</span><span class="sxs-lookup"><span data-stu-id="db6be-105">DESCRIPTION</span></span>
<span data-ttu-id="db6be-106">**新的-AzHDInsightHiveJobDefinition** Cmdlet 會定義用於 Azure HDInsight 群集的 Hive 工作物件。</span><span class="sxs-lookup"><span data-stu-id="db6be-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="db6be-107">示例</span><span class="sxs-lookup"><span data-stu-id="db6be-107">EXAMPLES</span></span>

### <span data-ttu-id="db6be-108">範例1：建立蜂巢作業定義</span><span class="sxs-lookup"><span data-stu-id="db6be-108">Example 1: Create a Hive job definition</span></span>
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

<span data-ttu-id="db6be-109">這個命令會建立一個蜂巢作業定義。</span><span class="sxs-lookup"><span data-stu-id="db6be-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="db6be-110">參數</span><span class="sxs-lookup"><span data-stu-id="db6be-110">PARAMETERS</span></span>

### <span data-ttu-id="db6be-111">-引數</span><span class="sxs-lookup"><span data-stu-id="db6be-111">-Arguments</span></span>
<span data-ttu-id="db6be-112">指定作業的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="db6be-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="db6be-113">引數會以命令列引數的形式傳遞給每個任務。</span><span class="sxs-lookup"><span data-stu-id="db6be-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="db6be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6be-114">-DefaultProfile</span></span>
<span data-ttu-id="db6be-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="db6be-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db6be-116">-定義</span><span class="sxs-lookup"><span data-stu-id="db6be-116">-Defines</span></span>
<span data-ttu-id="db6be-117">指定要在作業執行時設定的 Hadoop 配置值。</span><span class="sxs-lookup"><span data-stu-id="db6be-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="db6be-118">檔案</span><span class="sxs-lookup"><span data-stu-id="db6be-118">-File</span></span>
<span data-ttu-id="db6be-119">指定包含要執行之查詢之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="db6be-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="db6be-120">該檔案必須在與群集相關聯的儲存空間帳戶上提供。</span><span class="sxs-lookup"><span data-stu-id="db6be-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="db6be-121">您可以使用這個參數，而不是 *Query* 參數。</span><span class="sxs-lookup"><span data-stu-id="db6be-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="db6be-122">-檔案</span><span class="sxs-lookup"><span data-stu-id="db6be-122">-Files</span></span>
<span data-ttu-id="db6be-123">指定與 Hive 作業相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="db6be-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="db6be-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="db6be-124">-JobName</span></span>
<span data-ttu-id="db6be-125">指定作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="db6be-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="db6be-126">-Query</span><span class="sxs-lookup"><span data-stu-id="db6be-126">-Query</span></span>
<span data-ttu-id="db6be-127">指定 Hive 查詢。</span><span class="sxs-lookup"><span data-stu-id="db6be-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="db6be-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="db6be-128">-RunAsFileJob</span></span>
<span data-ttu-id="db6be-129">指示這個 Cmdlet 會在預設的 Azure 儲存空間帳戶中建立檔案，以儲存查詢。</span><span class="sxs-lookup"><span data-stu-id="db6be-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="db6be-130">這個 Cmdlet 會提交參照此檔案做為腳本以執行的工作。</span><span class="sxs-lookup"><span data-stu-id="db6be-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="db6be-131">您可以使用這個功能來處理特殊的字元，例如百分號 (% ) ，這些字元會在透過 Templeton 提交作業時失敗，因為 Templeton 會使用百分號符號作為 URL 參數來轉譯查詢。</span><span class="sxs-lookup"><span data-stu-id="db6be-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="db6be-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="db6be-132">-StatusFolder</span></span>
<span data-ttu-id="db6be-133">指定包含工作之標準輸出和錯誤輸出的資料夾位置。</span><span class="sxs-lookup"><span data-stu-id="db6be-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="db6be-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6be-134">CommonParameters</span></span>
<span data-ttu-id="db6be-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db6be-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6be-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="db6be-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6be-137">輸入</span><span class="sxs-lookup"><span data-stu-id="db6be-137">INPUTS</span></span>

### <span data-ttu-id="db6be-138">所有</span><span class="sxs-lookup"><span data-stu-id="db6be-138">None</span></span>

## <span data-ttu-id="db6be-139">輸出</span><span class="sxs-lookup"><span data-stu-id="db6be-139">OUTPUTS</span></span>

### <span data-ttu-id="db6be-140">AzureHDInsightHiveJobDefinition （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="db6be-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="db6be-141">筆記</span><span class="sxs-lookup"><span data-stu-id="db6be-141">NOTES</span></span>

## <span data-ttu-id="db6be-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="db6be-142">RELATED LINKS</span></span>

[<span data-ttu-id="db6be-143">開始-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="db6be-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


