---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/stop-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
ms.openlocfilehash: 26572b942671bcfca9fc52d2a93da29d55405b18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908553"
---
# <span data-ttu-id="3ed43-101">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="3ed43-101">Stop-AzHDInsightJob</span></span>

## <span data-ttu-id="3ed43-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3ed43-102">SYNOPSIS</span></span>
<span data-ttu-id="3ed43-103">停止在一個組上指定的執行中工作。</span><span class="sxs-lookup"><span data-stu-id="3ed43-103">Stops a specified running job on a cluster.</span></span>

## <span data-ttu-id="3ed43-104">語法</span><span class="sxs-lookup"><span data-stu-id="3ed43-104">SYNTAX</span></span>

```
Stop-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ed43-105">描述</span><span class="sxs-lookup"><span data-stu-id="3ed43-105">DESCRIPTION</span></span>
<span data-ttu-id="3ed43-106">**Stop-AzHDInsightJob** Cmdlet 會停止 Azure HDInsight 集區上指定的執行中工作。</span><span class="sxs-lookup"><span data-stu-id="3ed43-106">The **Stop-AzHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="3ed43-107">例子</span><span class="sxs-lookup"><span data-stu-id="3ed43-107">EXAMPLES</span></span>

### <span data-ttu-id="3ed43-108">範例 1：停止指定組集中的工作</span><span class="sxs-lookup"><span data-stu-id="3ed43-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="3ed43-109">此命令會停止名為 your-hadoop-001 的組組工作。</span><span class="sxs-lookup"><span data-stu-id="3ed43-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="3ed43-110">參數</span><span class="sxs-lookup"><span data-stu-id="3ed43-110">PARAMETERS</span></span>

### <span data-ttu-id="3ed43-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3ed43-111">-ClusterName</span></span>
<span data-ttu-id="3ed43-112">指定組名。</span><span class="sxs-lookup"><span data-stu-id="3ed43-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="3ed43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ed43-113">-DefaultProfile</span></span>
<span data-ttu-id="3ed43-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="3ed43-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ed43-115">-HTTPCredential</span><span class="sxs-lookup"><span data-stu-id="3ed43-115">-HttpCredential</span></span>
<span data-ttu-id="3ed43-116">指定該組 (HTTP) 組認證。</span><span class="sxs-lookup"><span data-stu-id="3ed43-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="3ed43-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="3ed43-117">-JobId</span></span>
<span data-ttu-id="3ed43-118">指定工作的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="3ed43-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="3ed43-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ed43-119">-ResourceGroupName</span></span>
<span data-ttu-id="3ed43-120">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ed43-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3ed43-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ed43-121">CommonParameters</span></span>
<span data-ttu-id="3ed43-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3ed43-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ed43-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ed43-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ed43-124">輸入</span><span class="sxs-lookup"><span data-stu-id="3ed43-124">INPUTS</span></span>

### <span data-ttu-id="3ed43-125">System.String</span><span class="sxs-lookup"><span data-stu-id="3ed43-125">System.String</span></span>

## <span data-ttu-id="3ed43-126">輸出</span><span class="sxs-lookup"><span data-stu-id="3ed43-126">OUTPUTS</span></span>

### <span data-ttu-id="3ed43-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="3ed43-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="3ed43-128">筆記</span><span class="sxs-lookup"><span data-stu-id="3ed43-128">NOTES</span></span>

## <span data-ttu-id="3ed43-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ed43-129">RELATED LINKS</span></span>

[<span data-ttu-id="3ed43-130">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="3ed43-130">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="3ed43-131">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="3ed43-131">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="3ed43-132">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="3ed43-132">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


