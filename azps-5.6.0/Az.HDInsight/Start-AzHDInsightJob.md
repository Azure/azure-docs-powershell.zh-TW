---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 316ac2671fe60271ad0d994855189071e3da2b95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905101"
---
# <span data-ttu-id="2da54-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2da54-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="2da54-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2da54-102">SYNOPSIS</span></span>
<span data-ttu-id="2da54-103">在指定的組集中開始已定義的 Azure HDInsight 工作。</span><span class="sxs-lookup"><span data-stu-id="2da54-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="2da54-104">語法</span><span class="sxs-lookup"><span data-stu-id="2da54-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2da54-105">描述</span><span class="sxs-lookup"><span data-stu-id="2da54-105">DESCRIPTION</span></span>
<span data-ttu-id="2da54-106">**Start-AzHDInsightJob** Cmdlet 會啟動指定組上的已定義 Azure HDInsight 工作。</span><span class="sxs-lookup"><span data-stu-id="2da54-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="2da54-107">這可以是 MapReduce 工作、串流 MapReduce 工作、一項病毒工作，或一份小豬工作。</span><span class="sxs-lookup"><span data-stu-id="2da54-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="2da54-108">例子</span><span class="sxs-lookup"><span data-stu-id="2da54-108">EXAMPLES</span></span>

### <span data-ttu-id="2da54-109">範例 1：在指定的組群上開始工作</span><span class="sxs-lookup"><span data-stu-id="2da54-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="2da54-110">此命令會啟動名為 your-hadoop-001 的組組工作。</span><span class="sxs-lookup"><span data-stu-id="2da54-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="2da54-111">參數</span><span class="sxs-lookup"><span data-stu-id="2da54-111">PARAMETERS</span></span>

### <span data-ttu-id="2da54-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2da54-112">-ClusterName</span></span>
<span data-ttu-id="2da54-113">指定組名。</span><span class="sxs-lookup"><span data-stu-id="2da54-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2da54-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2da54-114">-DefaultProfile</span></span>
<span data-ttu-id="2da54-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="2da54-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2da54-116">-HTTPCredential</span><span class="sxs-lookup"><span data-stu-id="2da54-116">-HttpCredential</span></span>
<span data-ttu-id="2da54-117">指定該組 (HTTP) 組認證。</span><span class="sxs-lookup"><span data-stu-id="2da54-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="2da54-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="2da54-118">-JobDefinition</span></span>
<span data-ttu-id="2da54-119">指定從 Azure HDInsight 集區開始的工作。</span><span class="sxs-lookup"><span data-stu-id="2da54-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2da54-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2da54-120">-ResourceGroupName</span></span>
<span data-ttu-id="2da54-121">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2da54-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2da54-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da54-122">CommonParameters</span></span>
<span data-ttu-id="2da54-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2da54-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da54-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2da54-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da54-125">輸入</span><span class="sxs-lookup"><span data-stu-id="2da54-125">INPUTS</span></span>

### <span data-ttu-id="2da54-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2da54-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="2da54-127">輸出</span><span class="sxs-lookup"><span data-stu-id="2da54-127">OUTPUTS</span></span>

### <span data-ttu-id="2da54-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2da54-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="2da54-129">筆記</span><span class="sxs-lookup"><span data-stu-id="2da54-129">NOTES</span></span>

## <span data-ttu-id="2da54-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="2da54-130">RELATED LINKS</span></span>

[<span data-ttu-id="2da54-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2da54-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="2da54-132">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2da54-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="2da54-133">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2da54-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="2da54-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2da54-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


