---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
ms.openlocfilehash: 6e19594cfcd79c6be82373af6245ea2154296b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626622"
---
# <span data-ttu-id="80e40-101">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="80e40-101">Wait-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="80e40-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80e40-102">SYNOPSIS</span></span>
<span data-ttu-id="80e40-103">等待指定作業的完成或失敗。</span><span class="sxs-lookup"><span data-stu-id="80e40-103">Waits for the completion or failure of a specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80e40-104">句法</span><span class="sxs-lookup"><span data-stu-id="80e40-104">SYNTAX</span></span>

```
Wait-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80e40-105">說明</span><span class="sxs-lookup"><span data-stu-id="80e40-105">DESCRIPTION</span></span>
<span data-ttu-id="80e40-106">**AzureRmHDInsightJob** Cmdlet 會等待 Azure HDInsight 作業的完成或失敗。</span><span class="sxs-lookup"><span data-stu-id="80e40-106">The **Wait-AzureRmHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="80e40-107">示例</span><span class="sxs-lookup"><span data-stu-id="80e40-107">EXAMPLES</span></span>

### <span data-ttu-id="80e40-108">範例1：等候作業的完成或失敗</span><span class="sxs-lookup"><span data-stu-id="80e40-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="80e40-109">這個命令會等待作業的完成或失敗。</span><span class="sxs-lookup"><span data-stu-id="80e40-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="80e40-110">參數</span><span class="sxs-lookup"><span data-stu-id="80e40-110">PARAMETERS</span></span>

### <span data-ttu-id="80e40-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="80e40-111">-ClusterName</span></span>
<span data-ttu-id="80e40-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="80e40-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="80e40-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="80e40-113">-HttpCredential</span></span>
<span data-ttu-id="80e40-114">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="80e40-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="80e40-115">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="80e40-115">-JobId</span></span>
<span data-ttu-id="80e40-116">指定作業的作業 ID。</span><span class="sxs-lookup"><span data-stu-id="80e40-116">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="80e40-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80e40-117">-ResourceGroupName</span></span>
<span data-ttu-id="80e40-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="80e40-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="80e40-119">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="80e40-119">-TimeoutInSeconds</span></span>
<span data-ttu-id="80e40-120">等待工作完成所需的總時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="80e40-120">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="80e40-121">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="80e40-121">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="80e40-122">在作業狀態檢查之間等待的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="80e40-122">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="80e40-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80e40-123">-DefaultProfile</span></span>
<span data-ttu-id="80e40-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="80e40-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80e40-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80e40-125">CommonParameters</span></span>
<span data-ttu-id="80e40-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80e40-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80e40-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80e40-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80e40-128">輸入</span><span class="sxs-lookup"><span data-stu-id="80e40-128">INPUTS</span></span>

### <span data-ttu-id="80e40-129">字串</span><span class="sxs-lookup"><span data-stu-id="80e40-129">String</span></span>
<span data-ttu-id="80e40-130">形參 "JobId" 接受管線中 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="80e40-130">Parameter 'JobId' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="80e40-131">輸出</span><span class="sxs-lookup"><span data-stu-id="80e40-131">OUTPUTS</span></span>

### <span data-ttu-id="80e40-132">AzureHDInsightJob （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="80e40-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="80e40-133">筆記</span><span class="sxs-lookup"><span data-stu-id="80e40-133">NOTES</span></span>

## <span data-ttu-id="80e40-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="80e40-134">RELATED LINKS</span></span>

[<span data-ttu-id="80e40-135">AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="80e40-135">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="80e40-136">開始-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="80e40-136">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="80e40-137">停止 AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="80e40-137">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

