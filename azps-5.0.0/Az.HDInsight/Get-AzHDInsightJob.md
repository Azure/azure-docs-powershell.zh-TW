---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
ms.openlocfilehash: b2ba2144eccd3069453daa1ada15527539400c22
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136815"
---
# <span data-ttu-id="8fbbd-101">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8fbbd-101">Get-AzHDInsightJob</span></span>

## <span data-ttu-id="8fbbd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8fbbd-102">SYNOPSIS</span></span>
<span data-ttu-id="8fbbd-103">從群集取得作業的清單，並以逆序的時間順序列出這些作業，或檢索特定作業。</span><span class="sxs-lookup"><span data-stu-id="8fbbd-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

## <span data-ttu-id="8fbbd-104">句法</span><span class="sxs-lookup"><span data-stu-id="8fbbd-104">SYNTAX</span></span>

```
Get-AzHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8fbbd-105">說明</span><span class="sxs-lookup"><span data-stu-id="8fbbd-105">DESCRIPTION</span></span>
<span data-ttu-id="8fbbd-106">**AzHDInsightJob** Cmdlet 會以相反的時間順序，取得指定 Azure HDInsight 群集的最近作業，並在清單頂端顯示最新作業。</span><span class="sxs-lookup"><span data-stu-id="8fbbd-106">The **Get-AzHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="8fbbd-107">提供 *JobId* 參數以取得特定作業。</span><span class="sxs-lookup"><span data-stu-id="8fbbd-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="8fbbd-108">示例</span><span class="sxs-lookup"><span data-stu-id="8fbbd-108">EXAMPLES</span></span>

### <span data-ttu-id="8fbbd-109">範例1：取得指定 Azure HDInsight 群集的最近作業</span><span class="sxs-lookup"><span data-stu-id="8fbbd-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="8fbbd-110">這個命令會取得名為「hadoop-001」之群集的所有最近作業。</span><span class="sxs-lookup"><span data-stu-id="8fbbd-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="8fbbd-111">參數</span><span class="sxs-lookup"><span data-stu-id="8fbbd-111">PARAMETERS</span></span>

### <span data-ttu-id="8fbbd-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8fbbd-112">-ClusterName</span></span>
<span data-ttu-id="8fbbd-113">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fbbd-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fbbd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fbbd-114">-DefaultProfile</span></span>
<span data-ttu-id="8fbbd-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8fbbd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fbbd-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="8fbbd-116">-HttpCredential</span></span>
<span data-ttu-id="8fbbd-117">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="8fbbd-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fbbd-118">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="8fbbd-118">-JobId</span></span>
<span data-ttu-id="8fbbd-119">指定要取得之工作的作業 ID。</span><span class="sxs-lookup"><span data-stu-id="8fbbd-119">Specifies the job ID of the job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fbbd-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="8fbbd-120">-NumOfJobs</span></span>
<span data-ttu-id="8fbbd-121">指定要檢索的作業數。</span><span class="sxs-lookup"><span data-stu-id="8fbbd-121">Specifies the number of jobs to retrieve.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fbbd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fbbd-122">-ResourceGroupName</span></span>
<span data-ttu-id="8fbbd-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fbbd-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8fbbd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fbbd-124">CommonParameters</span></span>
<span data-ttu-id="8fbbd-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8fbbd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fbbd-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8fbbd-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fbbd-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8fbbd-127">INPUTS</span></span>

### <span data-ttu-id="8fbbd-128">所有</span><span class="sxs-lookup"><span data-stu-id="8fbbd-128">None</span></span>

## <span data-ttu-id="8fbbd-129">輸出</span><span class="sxs-lookup"><span data-stu-id="8fbbd-129">OUTPUTS</span></span>

### <span data-ttu-id="8fbbd-130">AzureHDInsightJob （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="8fbbd-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="8fbbd-131">筆記</span><span class="sxs-lookup"><span data-stu-id="8fbbd-131">NOTES</span></span>

## <span data-ttu-id="8fbbd-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="8fbbd-132">RELATED LINKS</span></span>

[<span data-ttu-id="8fbbd-133">新-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8fbbd-133">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="8fbbd-134">開始-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8fbbd-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="8fbbd-135">停止 AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8fbbd-135">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="8fbbd-136">稍候-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8fbbd-136">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


