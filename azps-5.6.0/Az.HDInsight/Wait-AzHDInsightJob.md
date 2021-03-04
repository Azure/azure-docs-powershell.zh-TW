---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 4d4b3ff71142540ff5c5635938d31a16e3fd9603
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907870"
---
# <span data-ttu-id="eb45e-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="eb45e-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="eb45e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eb45e-102">SYNOPSIS</span></span>
<span data-ttu-id="eb45e-103">等待指定工作的完成或失敗。</span><span class="sxs-lookup"><span data-stu-id="eb45e-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="eb45e-104">語法</span><span class="sxs-lookup"><span data-stu-id="eb45e-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb45e-105">描述</span><span class="sxs-lookup"><span data-stu-id="eb45e-105">DESCRIPTION</span></span>
<span data-ttu-id="eb45e-106">**Wait-AzHDInsightJob** Cmdlet 正在等待 Azure HDInsight 工作的完成或失敗。</span><span class="sxs-lookup"><span data-stu-id="eb45e-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="eb45e-107">例子</span><span class="sxs-lookup"><span data-stu-id="eb45e-107">EXAMPLES</span></span>

### <span data-ttu-id="eb45e-108">範例 1：等待工作的完成或失敗</span><span class="sxs-lookup"><span data-stu-id="eb45e-108">Example 1: Wait for the completion or failure of a job</span></span>
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

<span data-ttu-id="eb45e-109">此命令會等待工作的完成或失敗。</span><span class="sxs-lookup"><span data-stu-id="eb45e-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="eb45e-110">參數</span><span class="sxs-lookup"><span data-stu-id="eb45e-110">PARAMETERS</span></span>

### <span data-ttu-id="eb45e-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="eb45e-111">-ClusterName</span></span>
<span data-ttu-id="eb45e-112">指定組名。</span><span class="sxs-lookup"><span data-stu-id="eb45e-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="eb45e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb45e-113">-DefaultProfile</span></span>
<span data-ttu-id="eb45e-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="eb45e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb45e-115">-HTTPCredential</span><span class="sxs-lookup"><span data-stu-id="eb45e-115">-HttpCredential</span></span>
<span data-ttu-id="eb45e-116">指定該組 (HTTP) 組認證。</span><span class="sxs-lookup"><span data-stu-id="eb45e-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="eb45e-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="eb45e-117">-JobId</span></span>
<span data-ttu-id="eb45e-118">指定工作的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb45e-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="eb45e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb45e-119">-ResourceGroupName</span></span>
<span data-ttu-id="eb45e-120">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb45e-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="eb45e-121">-TimeoutIn TimeoutIn Timeouts</span><span class="sxs-lookup"><span data-stu-id="eb45e-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="eb45e-122">等待工作完成的總時間 ，以碼錶示。</span><span class="sxs-lookup"><span data-stu-id="eb45e-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="eb45e-123">-WaitIntervalIn用秒</span><span class="sxs-lookup"><span data-stu-id="eb45e-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="eb45e-124">在工作狀態檢查之間等候的時間 ，以碼錶示。</span><span class="sxs-lookup"><span data-stu-id="eb45e-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="eb45e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb45e-125">CommonParameters</span></span>
<span data-ttu-id="eb45e-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eb45e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb45e-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb45e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb45e-128">輸入</span><span class="sxs-lookup"><span data-stu-id="eb45e-128">INPUTS</span></span>

### <span data-ttu-id="eb45e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="eb45e-129">System.String</span></span>

## <span data-ttu-id="eb45e-130">輸出</span><span class="sxs-lookup"><span data-stu-id="eb45e-130">OUTPUTS</span></span>

### <span data-ttu-id="eb45e-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="eb45e-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="eb45e-132">筆記</span><span class="sxs-lookup"><span data-stu-id="eb45e-132">NOTES</span></span>

## <span data-ttu-id="eb45e-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb45e-133">RELATED LINKS</span></span>

[<span data-ttu-id="eb45e-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="eb45e-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="eb45e-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="eb45e-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="eb45e-136">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="eb45e-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


