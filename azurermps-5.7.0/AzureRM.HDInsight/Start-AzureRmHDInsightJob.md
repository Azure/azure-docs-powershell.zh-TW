---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/start-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
ms.openlocfilehash: 8c3e0f01472469be856d69c1a87f8eb5185f2012
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456223"
---
# <span data-ttu-id="b418a-101">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b418a-101">Start-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="b418a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b418a-102">SYNOPSIS</span></span>
<span data-ttu-id="b418a-103">在指定的群集上啟動已定義的 Azure HDInsight 作業。</span><span class="sxs-lookup"><span data-stu-id="b418a-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b418a-104">句法</span><span class="sxs-lookup"><span data-stu-id="b418a-104">SYNTAX</span></span>

```
Start-AzureRmHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b418a-105">說明</span><span class="sxs-lookup"><span data-stu-id="b418a-105">DESCRIPTION</span></span>
<span data-ttu-id="b418a-106">**Start-AzureRMHDInsightJob** Cmdlet 會在指定的群集上啟動已定義的 Azure HDInsight 作業。</span><span class="sxs-lookup"><span data-stu-id="b418a-106">The **Start-AzureRMHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="b418a-107">這可以是 MapReduce 作業、流式 MapReduce 作業、Hive 作業或豬作業。</span><span class="sxs-lookup"><span data-stu-id="b418a-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="b418a-108">示例</span><span class="sxs-lookup"><span data-stu-id="b418a-108">EXAMPLES</span></span>

### <span data-ttu-id="b418a-109">範例1：在指定的群集上開始作業</span><span class="sxs-lookup"><span data-stu-id="b418a-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b418a-110">這個命令會在名為 [您的-hadoop-001] 的群集上啟動作業。</span><span class="sxs-lookup"><span data-stu-id="b418a-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b418a-111">參數</span><span class="sxs-lookup"><span data-stu-id="b418a-111">PARAMETERS</span></span>

### <span data-ttu-id="b418a-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b418a-112">-ClusterName</span></span>
<span data-ttu-id="b418a-113">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="b418a-113">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b418a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b418a-114">-DefaultProfile</span></span>
<span data-ttu-id="b418a-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b418a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b418a-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="b418a-116">-HttpCredential</span></span>
<span data-ttu-id="b418a-117">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="b418a-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b418a-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="b418a-118">-JobDefinition</span></span>
<span data-ttu-id="b418a-119">指定要從 Azure HDInsight 群集上開始的工作。</span><span class="sxs-lookup"><span data-stu-id="b418a-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b418a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b418a-120">-ResourceGroupName</span></span>
<span data-ttu-id="b418a-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b418a-121">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b418a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b418a-122">CommonParameters</span></span>
<span data-ttu-id="b418a-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b418a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b418a-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b418a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b418a-125">輸入</span><span class="sxs-lookup"><span data-stu-id="b418a-125">INPUTS</span></span>

### <span data-ttu-id="b418a-126">AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b418a-126">AzureHDInsightJobDefinition</span></span>
<span data-ttu-id="b418a-127">形參 "JobDefinition" 接受管線中 "AzureHDInsightJobDefinition" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b418a-127">Parameter 'JobDefinition' accepts value of type 'AzureHDInsightJobDefinition' from the pipeline</span></span>

## <span data-ttu-id="b418a-128">輸出</span><span class="sxs-lookup"><span data-stu-id="b418a-128">OUTPUTS</span></span>

### <span data-ttu-id="b418a-129">AzureHDInsightJob （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="b418a-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="b418a-130">筆記</span><span class="sxs-lookup"><span data-stu-id="b418a-130">NOTES</span></span>

## <span data-ttu-id="b418a-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b418a-131">RELATED LINKS</span></span>

[<span data-ttu-id="b418a-132">AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b418a-132">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="b418a-133">新-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b418a-133">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="b418a-134">停止 AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b418a-134">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="b418a-135">稍候-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b418a-135">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


