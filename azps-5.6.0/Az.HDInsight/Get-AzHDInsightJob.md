---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
ms.openlocfilehash: 87a5b306619bd3d16b9a7c4e76256f2d0e74d568
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913998"
---
# <span data-ttu-id="2c824-101">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2c824-101">Get-AzHDInsightJob</span></span>

## <span data-ttu-id="2c824-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2c824-102">SYNOPSIS</span></span>
<span data-ttu-id="2c824-103">從一個工作組獲得工作清單，然後以反時間順序列出工作，或取回特定工作。</span><span class="sxs-lookup"><span data-stu-id="2c824-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

## <span data-ttu-id="2c824-104">語法</span><span class="sxs-lookup"><span data-stu-id="2c824-104">SYNTAX</span></span>

```
Get-AzHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c824-105">描述</span><span class="sxs-lookup"><span data-stu-id="2c824-105">DESCRIPTION</span></span>
<span data-ttu-id="2c824-106">**Get-AzHDInsightJob** Cmdlet 會以反時間順序取得指定 Azure HDInsight 組的最新工作，最新的工作會位於清單頂端。</span><span class="sxs-lookup"><span data-stu-id="2c824-106">The **Get-AzHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="2c824-107">提供 *JobId* 參數以取得特定工作。</span><span class="sxs-lookup"><span data-stu-id="2c824-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="2c824-108">例子</span><span class="sxs-lookup"><span data-stu-id="2c824-108">EXAMPLES</span></span>

### <span data-ttu-id="2c824-109">範例 1：取得指定 Azure HDInsight 組的最新工作</span><span class="sxs-lookup"><span data-stu-id="2c824-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
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

<span data-ttu-id="2c824-110">此命令會獲得名為 your-hadoop-001 的該組組的所有最近工作。</span><span class="sxs-lookup"><span data-stu-id="2c824-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="2c824-111">參數</span><span class="sxs-lookup"><span data-stu-id="2c824-111">PARAMETERS</span></span>

### <span data-ttu-id="2c824-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2c824-112">-ClusterName</span></span>
<span data-ttu-id="2c824-113">指定組名。</span><span class="sxs-lookup"><span data-stu-id="2c824-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2c824-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c824-114">-DefaultProfile</span></span>
<span data-ttu-id="2c824-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="2c824-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c824-116">-HTTPCredential</span><span class="sxs-lookup"><span data-stu-id="2c824-116">-HttpCredential</span></span>
<span data-ttu-id="2c824-117">指定該組 (HTTP) 組認證。</span><span class="sxs-lookup"><span data-stu-id="2c824-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="2c824-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="2c824-118">-JobId</span></span>
<span data-ttu-id="2c824-119">指定要取得的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c824-119">Specifies the job ID of the job to get.</span></span>

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

### <span data-ttu-id="2c824-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="2c824-120">-NumOfJobs</span></span>
<span data-ttu-id="2c824-121">指定要取回的工作數目。</span><span class="sxs-lookup"><span data-stu-id="2c824-121">Specifies the number of jobs to retrieve.</span></span>

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

### <span data-ttu-id="2c824-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c824-122">-ResourceGroupName</span></span>
<span data-ttu-id="2c824-123">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c824-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2c824-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c824-124">CommonParameters</span></span>
<span data-ttu-id="2c824-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2c824-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c824-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c824-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c824-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2c824-127">INPUTS</span></span>

### <span data-ttu-id="2c824-128">沒有</span><span class="sxs-lookup"><span data-stu-id="2c824-128">None</span></span>

## <span data-ttu-id="2c824-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2c824-129">OUTPUTS</span></span>

### <span data-ttu-id="2c824-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2c824-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="2c824-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2c824-131">NOTES</span></span>

## <span data-ttu-id="2c824-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c824-132">RELATED LINKS</span></span>

[<span data-ttu-id="2c824-133">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2c824-133">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="2c824-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2c824-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="2c824-135">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2c824-135">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="2c824-136">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2c824-136">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


