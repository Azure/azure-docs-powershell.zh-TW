---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/stop-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
ms.openlocfilehash: 82587d855b41a8112bac900f0efe6c4b30941eb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626162"
---
# <span data-ttu-id="0529c-101">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0529c-101">Stop-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="0529c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0529c-102">SYNOPSIS</span></span>
<span data-ttu-id="0529c-103">在群集上停止指定的執行作業。</span><span class="sxs-lookup"><span data-stu-id="0529c-103">Stops a specified running job on a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0529c-104">句法</span><span class="sxs-lookup"><span data-stu-id="0529c-104">SYNTAX</span></span>

```
Stop-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0529c-105">說明</span><span class="sxs-lookup"><span data-stu-id="0529c-105">DESCRIPTION</span></span>
<span data-ttu-id="0529c-106">**AzureRmHDInsightJob** Cmdlet 會停止 Azure HDInsight 群集上指定的執行作業。</span><span class="sxs-lookup"><span data-stu-id="0529c-106">The **Stop-AzureRmHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="0529c-107">示例</span><span class="sxs-lookup"><span data-stu-id="0529c-107">EXAMPLES</span></span>

### <span data-ttu-id="0529c-108">範例1：在指定的群集上停止作業</span><span class="sxs-lookup"><span data-stu-id="0529c-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="0529c-109">這個命令會停止名為-hadoop-001 的群集上的工作。</span><span class="sxs-lookup"><span data-stu-id="0529c-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="0529c-110">參數</span><span class="sxs-lookup"><span data-stu-id="0529c-110">PARAMETERS</span></span>

### <span data-ttu-id="0529c-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0529c-111">-ClusterName</span></span>
<span data-ttu-id="0529c-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="0529c-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="0529c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0529c-113">-DefaultProfile</span></span>
<span data-ttu-id="0529c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0529c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0529c-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="0529c-115">-HttpCredential</span></span>
<span data-ttu-id="0529c-116">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="0529c-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="0529c-117">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="0529c-117">-JobId</span></span>
<span data-ttu-id="0529c-118">指定作業的作業 ID。</span><span class="sxs-lookup"><span data-stu-id="0529c-118">Specifies the job ID of the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0529c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0529c-119">-ResourceGroupName</span></span>
<span data-ttu-id="0529c-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0529c-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0529c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0529c-121">CommonParameters</span></span>
<span data-ttu-id="0529c-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0529c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0529c-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0529c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0529c-124">輸入</span><span class="sxs-lookup"><span data-stu-id="0529c-124">INPUTS</span></span>

### <span data-ttu-id="0529c-125">字串</span><span class="sxs-lookup"><span data-stu-id="0529c-125">String</span></span>
<span data-ttu-id="0529c-126">形參 "JobId" 接受管線中 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0529c-126">Parameter 'JobId' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="0529c-127">輸出</span><span class="sxs-lookup"><span data-stu-id="0529c-127">OUTPUTS</span></span>

### <span data-ttu-id="0529c-128">AzureHDInsightJob （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="0529c-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="0529c-129">筆記</span><span class="sxs-lookup"><span data-stu-id="0529c-129">NOTES</span></span>

## <span data-ttu-id="0529c-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="0529c-130">RELATED LINKS</span></span>

[<span data-ttu-id="0529c-131">AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0529c-131">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="0529c-132">開始-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0529c-132">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="0529c-133">稍候-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0529c-133">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


