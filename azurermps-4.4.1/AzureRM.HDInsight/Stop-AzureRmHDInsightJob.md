---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
ms.openlocfilehash: 674c8f1cb5fdf8d8c76da36a7bb6d8df06e29c8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456620"
---
# <span data-ttu-id="e4fae-101">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e4fae-101">Stop-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="e4fae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4fae-102">SYNOPSIS</span></span>
<span data-ttu-id="e4fae-103">在群集上停止指定的執行作業。</span><span class="sxs-lookup"><span data-stu-id="e4fae-103">Stops a specified running job on a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4fae-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4fae-104">SYNTAX</span></span>

```
Stop-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4fae-105">說明</span><span class="sxs-lookup"><span data-stu-id="e4fae-105">DESCRIPTION</span></span>
<span data-ttu-id="e4fae-106">**AzureRmHDInsightJob** Cmdlet 會停止 Azure HDInsight 群集上指定的執行作業。</span><span class="sxs-lookup"><span data-stu-id="e4fae-106">The **Stop-AzureRmHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e4fae-107">示例</span><span class="sxs-lookup"><span data-stu-id="e4fae-107">EXAMPLES</span></span>

### <span data-ttu-id="e4fae-108">範例1：在指定的群集上停止作業</span><span class="sxs-lookup"><span data-stu-id="e4fae-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="e4fae-109">這個命令會停止名為-hadoop-001 的群集上的工作。</span><span class="sxs-lookup"><span data-stu-id="e4fae-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="e4fae-110">參數</span><span class="sxs-lookup"><span data-stu-id="e4fae-110">PARAMETERS</span></span>

### <span data-ttu-id="e4fae-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e4fae-111">-ClusterName</span></span>
<span data-ttu-id="e4fae-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4fae-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e4fae-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="e4fae-113">-HttpCredential</span></span>
<span data-ttu-id="e4fae-114">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="e4fae-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="e4fae-115">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="e4fae-115">-JobId</span></span>
<span data-ttu-id="e4fae-116">指定作業的作業 ID。</span><span class="sxs-lookup"><span data-stu-id="e4fae-116">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="e4fae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4fae-117">-ResourceGroupName</span></span>
<span data-ttu-id="e4fae-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4fae-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e4fae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4fae-119">-DefaultProfile</span></span>
<span data-ttu-id="e4fae-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e4fae-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4fae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4fae-121">CommonParameters</span></span>
<span data-ttu-id="e4fae-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4fae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4fae-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4fae-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4fae-124">輸入</span><span class="sxs-lookup"><span data-stu-id="e4fae-124">INPUTS</span></span>

### <span data-ttu-id="e4fae-125">字串</span><span class="sxs-lookup"><span data-stu-id="e4fae-125">String</span></span>
<span data-ttu-id="e4fae-126">形參 "JobId" 接受管線中 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e4fae-126">Parameter 'JobId' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="e4fae-127">輸出</span><span class="sxs-lookup"><span data-stu-id="e4fae-127">OUTPUTS</span></span>

### <span data-ttu-id="e4fae-128">AzureHDInsightJob （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="e4fae-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="e4fae-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e4fae-129">NOTES</span></span>

## <span data-ttu-id="e4fae-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4fae-130">RELATED LINKS</span></span>

[<span data-ttu-id="e4fae-131">AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e4fae-131">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="e4fae-132">開始-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e4fae-132">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="e4fae-133">稍候-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e4fae-133">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


