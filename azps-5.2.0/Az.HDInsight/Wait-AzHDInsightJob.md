---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 6b87b7f6e3482aad974c5f7d334724f5d2f99e7c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274711"
---
# <span data-ttu-id="09888-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="09888-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="09888-102">摘要</span><span class="sxs-lookup"><span data-stu-id="09888-102">SYNOPSIS</span></span>
<span data-ttu-id="09888-103">等待指定作業的完成或失敗。</span><span class="sxs-lookup"><span data-stu-id="09888-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="09888-104">句法</span><span class="sxs-lookup"><span data-stu-id="09888-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09888-105">說明</span><span class="sxs-lookup"><span data-stu-id="09888-105">DESCRIPTION</span></span>
<span data-ttu-id="09888-106">**AzHDInsightJob** Cmdlet 會等待 Azure HDInsight 作業的完成或失敗。</span><span class="sxs-lookup"><span data-stu-id="09888-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="09888-107">示例</span><span class="sxs-lookup"><span data-stu-id="09888-107">EXAMPLES</span></span>

### <span data-ttu-id="09888-108">範例1：等候作業的完成或失敗</span><span class="sxs-lookup"><span data-stu-id="09888-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="09888-109">這個命令會等待作業的完成或失敗。</span><span class="sxs-lookup"><span data-stu-id="09888-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="09888-110">參數</span><span class="sxs-lookup"><span data-stu-id="09888-110">PARAMETERS</span></span>

### <span data-ttu-id="09888-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="09888-111">-ClusterName</span></span>
<span data-ttu-id="09888-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="09888-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="09888-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09888-113">-DefaultProfile</span></span>
<span data-ttu-id="09888-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="09888-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09888-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="09888-115">-HttpCredential</span></span>
<span data-ttu-id="09888-116">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="09888-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09888-117">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="09888-117">-JobId</span></span>
<span data-ttu-id="09888-118">指定作業的作業 ID。</span><span class="sxs-lookup"><span data-stu-id="09888-118">Specifies the job ID of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09888-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09888-119">-ResourceGroupName</span></span>
<span data-ttu-id="09888-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="09888-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="09888-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="09888-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="09888-122">等待工作完成所需的總時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="09888-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="09888-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="09888-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="09888-124">在作業狀態檢查之間等待的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="09888-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="09888-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09888-125">CommonParameters</span></span>
<span data-ttu-id="09888-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="09888-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09888-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="09888-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09888-128">輸入</span><span class="sxs-lookup"><span data-stu-id="09888-128">INPUTS</span></span>

### <span data-ttu-id="09888-129">System.object</span><span class="sxs-lookup"><span data-stu-id="09888-129">System.String</span></span>

## <span data-ttu-id="09888-130">輸出</span><span class="sxs-lookup"><span data-stu-id="09888-130">OUTPUTS</span></span>

### <span data-ttu-id="09888-131">AzureHDInsightJob （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="09888-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="09888-132">筆記</span><span class="sxs-lookup"><span data-stu-id="09888-132">NOTES</span></span>

## <span data-ttu-id="09888-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="09888-133">RELATED LINKS</span></span>

[<span data-ttu-id="09888-134">AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="09888-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="09888-135">開始-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="09888-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="09888-136">停止 AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="09888-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


