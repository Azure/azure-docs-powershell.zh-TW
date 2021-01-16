---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: 11532648242438983ae1bc9222dbc3ac12fa05e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446983"
---
# <span data-ttu-id="edef5-101">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="edef5-101">Get-AzBatchJobStatistic</span></span>

## <span data-ttu-id="edef5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="edef5-102">SYNOPSIS</span></span>
<span data-ttu-id="edef5-103">取得批次帳戶的作業摘要統計資料。</span><span class="sxs-lookup"><span data-stu-id="edef5-103">Gets job summary statistics for a Batch account.</span></span>

## <span data-ttu-id="edef5-104">句法</span><span class="sxs-lookup"><span data-stu-id="edef5-104">SYNTAX</span></span>

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="edef5-105">說明</span><span class="sxs-lookup"><span data-stu-id="edef5-105">DESCRIPTION</span></span>
<span data-ttu-id="edef5-106">**AzBatchJobStatistic** Cmdlet 會取得 Azure Batch 帳戶中所有作業的存留期摘要統計資料。</span><span class="sxs-lookup"><span data-stu-id="edef5-106">The **Get-AzBatchJobStatistic** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="edef5-107">統計資料會匯總到帳戶中存在的所有工作，從帳戶建立到統計的最後一次更新時間。</span><span class="sxs-lookup"><span data-stu-id="edef5-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="edef5-108">示例</span><span class="sxs-lookup"><span data-stu-id="edef5-108">EXAMPLES</span></span>

### <span data-ttu-id="edef5-109">範例1：取得所有作業的摘要統計資料</span><span class="sxs-lookup"><span data-stu-id="edef5-109">Example 1: Get summary statistics for all jobs</span></span>
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

<span data-ttu-id="edef5-110">第一個命令會使用 **AzBatchAccountKey** 建立名為 ContosoBatchAccount 的 batch 帳戶的帳戶金鑰的物件參考。</span><span class="sxs-lookup"><span data-stu-id="edef5-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="edef5-111">該命令會將這個物件參照儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="edef5-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="edef5-112">第二個命令會取得所有作業的摘要統計資料。</span><span class="sxs-lookup"><span data-stu-id="edef5-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="edef5-113">此命令會使用第一個命令的 $CoNtext 值。</span><span class="sxs-lookup"><span data-stu-id="edef5-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="edef5-114">參數</span><span class="sxs-lookup"><span data-stu-id="edef5-114">PARAMETERS</span></span>

### <span data-ttu-id="edef5-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="edef5-115">-BatchContext</span></span>
<span data-ttu-id="edef5-116">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="edef5-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="edef5-117">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="edef5-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="edef5-118">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="edef5-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="edef5-119">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="edef5-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="edef5-120">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="edef5-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="edef5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edef5-121">-DefaultProfile</span></span>
<span data-ttu-id="edef5-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="edef5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edef5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edef5-123">CommonParameters</span></span>
<span data-ttu-id="edef5-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="edef5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edef5-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="edef5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edef5-126">輸入</span><span class="sxs-lookup"><span data-stu-id="edef5-126">INPUTS</span></span>

### <span data-ttu-id="edef5-127">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="edef5-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="edef5-128">輸出</span><span class="sxs-lookup"><span data-stu-id="edef5-128">OUTPUTS</span></span>

### <span data-ttu-id="edef5-129">Microsoft.Azure.Commands.Batch。PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="edef5-129">Microsoft.Azure.Commands.Batch.Models.PSJobStatistics</span></span>

## <span data-ttu-id="edef5-130">筆記</span><span class="sxs-lookup"><span data-stu-id="edef5-130">NOTES</span></span>

## <span data-ttu-id="edef5-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="edef5-131">RELATED LINKS</span></span>

[<span data-ttu-id="edef5-132">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="edef5-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="edef5-133">AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="edef5-133">Get-AzBatchPoolStatistic</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="edef5-134">AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="edef5-134">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)
