---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: ec52f8b48433e52e86551a8346f4ec9a61b5727d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910773"
---
# <span data-ttu-id="383e8-101">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="383e8-101">Get-AzBatchJobStatistic</span></span>

## <span data-ttu-id="383e8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="383e8-102">SYNOPSIS</span></span>
<span data-ttu-id="383e8-103">獲得批次帳戶的工作摘要統計資料。</span><span class="sxs-lookup"><span data-stu-id="383e8-103">Gets job summary statistics for a Batch account.</span></span>

## <span data-ttu-id="383e8-104">語法</span><span class="sxs-lookup"><span data-stu-id="383e8-104">SYNTAX</span></span>

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="383e8-105">描述</span><span class="sxs-lookup"><span data-stu-id="383e8-105">DESCRIPTION</span></span>
<span data-ttu-id="383e8-106">**Get-AzBatchJobStatistic** Cmdlet 會取得 Azure Batch 帳戶中所有工作的生命週期摘要統計資料。</span><span class="sxs-lookup"><span data-stu-id="383e8-106">The **Get-AzBatchJobStatistic** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="383e8-107">統計資料會匯總到帳戶內曾經存在的所有工作，從帳戶建立到統計資料的上次更新時間。</span><span class="sxs-lookup"><span data-stu-id="383e8-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="383e8-108">例子</span><span class="sxs-lookup"><span data-stu-id="383e8-108">EXAMPLES</span></span>

### <span data-ttu-id="383e8-109">範例 1：取得所有工作的摘要統計資料</span><span class="sxs-lookup"><span data-stu-id="383e8-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzBatchJobStatistic -BatchContext $Context
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

<span data-ttu-id="383e8-110">第一個命令會使用 **Get-AzBatchAccountKey，為名為 ContosoBatchAccount** 的批次帳戶建立帳戶金鑰的物件參照。</span><span class="sxs-lookup"><span data-stu-id="383e8-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="383e8-111">命令會在此變數中儲存$CoNtext參照。</span><span class="sxs-lookup"><span data-stu-id="383e8-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="383e8-112">第二個命令會獲得所有工作的摘要統計資料。</span><span class="sxs-lookup"><span data-stu-id="383e8-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="383e8-113">命令會使用$CoNtext命令中的值。</span><span class="sxs-lookup"><span data-stu-id="383e8-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="383e8-114">參數</span><span class="sxs-lookup"><span data-stu-id="383e8-114">PARAMETERS</span></span>

### <span data-ttu-id="383e8-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="383e8-115">-BatchContext</span></span>
<span data-ttu-id="383e8-116">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="383e8-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="383e8-117">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="383e8-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="383e8-118">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="383e8-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="383e8-119">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="383e8-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="383e8-120">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="383e8-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="383e8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="383e8-121">-DefaultProfile</span></span>
<span data-ttu-id="383e8-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="383e8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="383e8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="383e8-123">CommonParameters</span></span>
<span data-ttu-id="383e8-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="383e8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="383e8-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="383e8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="383e8-126">輸入</span><span class="sxs-lookup"><span data-stu-id="383e8-126">INPUTS</span></span>

### <span data-ttu-id="383e8-127">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="383e8-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="383e8-128">輸出</span><span class="sxs-lookup"><span data-stu-id="383e8-128">OUTPUTS</span></span>

### <span data-ttu-id="383e8-129">Microsoft.Azure.Commands.Batch。Models.PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="383e8-129">Microsoft.Azure.Commands.Batch.Models.PSJobStatistics</span></span>

## <span data-ttu-id="383e8-130">筆記</span><span class="sxs-lookup"><span data-stu-id="383e8-130">NOTES</span></span>

## <span data-ttu-id="383e8-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="383e8-131">RELATED LINKS</span></span>

[<span data-ttu-id="383e8-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="383e8-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="383e8-133">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="383e8-133">Get-AzBatchPoolStatistic</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="383e8-134">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="383e8-134">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)
