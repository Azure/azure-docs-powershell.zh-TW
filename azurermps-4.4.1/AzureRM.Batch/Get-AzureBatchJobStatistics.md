---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
ms.openlocfilehash: 03b7e3999fbc482223365b59867c02c75e9d5ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449646"
---
# <span data-ttu-id="de7d1-101">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="de7d1-101">Get-AzureBatchJobStatistics</span></span>

## <span data-ttu-id="de7d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de7d1-102">SYNOPSIS</span></span>
<span data-ttu-id="de7d1-103">取得批次帳戶的作業摘要統計資料。</span><span class="sxs-lookup"><span data-stu-id="de7d1-103">Gets job summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de7d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="de7d1-104">SYNTAX</span></span>

```
Get-AzureBatchJobStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de7d1-105">說明</span><span class="sxs-lookup"><span data-stu-id="de7d1-105">DESCRIPTION</span></span>
<span data-ttu-id="de7d1-106">**AzureBatchJobStatistics** Cmdlet 會取得 Azure Batch 帳戶中所有作業的存留期摘要統計資料。</span><span class="sxs-lookup"><span data-stu-id="de7d1-106">The **Get-AzureBatchJobStatistics** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="de7d1-107">統計資料會匯總到帳戶中存在的所有工作，從帳戶建立到統計的最後一次更新時間。</span><span class="sxs-lookup"><span data-stu-id="de7d1-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="de7d1-108">示例</span><span class="sxs-lookup"><span data-stu-id="de7d1-108">EXAMPLES</span></span>

### <span data-ttu-id="de7d1-109">範例1：取得所有作業的摘要統計資料</span><span class="sxs-lookup"><span data-stu-id="de7d1-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzureBatchJobStatistics -BatchContext $Context
FailedTaskCount    : 330
KernelCpuTime      : 00:24:31.8440000
LastUpdateTime     : 5/16/2016 6:00:00 PM
ReadIOGiB          : 38.1271341182292
ReadIOps           : 26546054
StartTime          : 11/3/2015 9:47:14 PM
SucceededTaskCount : 766
TaskRetryCount     : 0
Url                : https://accountname.westus.batch.azure.com/lifetimejobstats
UserCpuTime        : 20:55:50.3200000
WaitTime           : 03:54:49.8530000
WallClockTime      : 20:55:50.3200000
WriteIOGiB         : 0.159623090177774
WriteIOps          : 146946
```

<span data-ttu-id="de7d1-110">第一個命令會使用 **AzureRmBatchAccountKeys** 建立名為 ContosoBatchAccount 的 batch 帳戶的帳戶金鑰的物件參考。</span><span class="sxs-lookup"><span data-stu-id="de7d1-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="de7d1-111">該命令會將這個物件參照儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="de7d1-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="de7d1-112">第二個命令會取得所有作業的摘要統計資料。</span><span class="sxs-lookup"><span data-stu-id="de7d1-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="de7d1-113">此命令會使用第一個命令的 $CoNtext 值。</span><span class="sxs-lookup"><span data-stu-id="de7d1-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="de7d1-114">參數</span><span class="sxs-lookup"><span data-stu-id="de7d1-114">PARAMETERS</span></span>

### <span data-ttu-id="de7d1-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="de7d1-115">-BatchContext</span></span>
<span data-ttu-id="de7d1-116">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="de7d1-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="de7d1-117">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de7d1-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de7d1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de7d1-118">-DefaultProfile</span></span>
<span data-ttu-id="de7d1-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="de7d1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de7d1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de7d1-120">CommonParameters</span></span>
<span data-ttu-id="de7d1-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de7d1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de7d1-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="de7d1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de7d1-123">輸入</span><span class="sxs-lookup"><span data-stu-id="de7d1-123">INPUTS</span></span>

### <span data-ttu-id="de7d1-124">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="de7d1-124">BatchAccountContext</span></span>
<span data-ttu-id="de7d1-125">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="de7d1-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="de7d1-126">輸出</span><span class="sxs-lookup"><span data-stu-id="de7d1-126">OUTPUTS</span></span>

### <span data-ttu-id="de7d1-127">PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="de7d1-127">PSJobStatistics</span></span>

## <span data-ttu-id="de7d1-128">筆記</span><span class="sxs-lookup"><span data-stu-id="de7d1-128">NOTES</span></span>

## <span data-ttu-id="de7d1-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="de7d1-129">RELATED LINKS</span></span>

[<span data-ttu-id="de7d1-130">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="de7d1-130">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="de7d1-131">AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="de7d1-131">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="de7d1-132">AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="de7d1-132">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)


