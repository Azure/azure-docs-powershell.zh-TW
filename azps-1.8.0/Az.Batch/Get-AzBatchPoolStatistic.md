---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
ms.openlocfilehash: d75efbd2ef369444fb655d1a011d7a1dbfab9100
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93623322"
---
# <span data-ttu-id="bb54c-101">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="bb54c-101">Get-AzBatchPoolStatistic</span></span>

## <span data-ttu-id="bb54c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb54c-102">SYNOPSIS</span></span>
<span data-ttu-id="bb54c-103">取得批次帳戶的 [池摘要統計資料]。</span><span class="sxs-lookup"><span data-stu-id="bb54c-103">Gets pool summary statistics for a Batch account.</span></span>

## <span data-ttu-id="bb54c-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb54c-104">SYNTAX</span></span>

```
Get-AzBatchPoolStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb54c-105">說明</span><span class="sxs-lookup"><span data-stu-id="bb54c-105">DESCRIPTION</span></span>
<span data-ttu-id="bb54c-106">**AzBatchPoolStatistic** Cmdlet 會取得指定帳戶中所有池的存留期統計資料。</span><span class="sxs-lookup"><span data-stu-id="bb54c-106">The **Get-AzBatchPoolStatistic** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="bb54c-107">每個已存在於帳戶中的所有池都會匯總統計資料，從帳戶建立到統計的最後一次更新時間。</span><span class="sxs-lookup"><span data-stu-id="bb54c-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="bb54c-108">示例</span><span class="sxs-lookup"><span data-stu-id="bb54c-108">EXAMPLES</span></span>

### <span data-ttu-id="bb54c-109">範例1：取得帳戶中所有池的資源統計資料</span><span class="sxs-lookup"><span data-stu-id="bb54c-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzBatchPoolStatistic -BatchContext $Context
PS C:\> $PoolStatistics.ResourceStatistics 
AverageCpuPercentage : 0.351232518750755
AverageDiskGiB       : 55.2569014701165
AverageMemoryGiB     : 2.87273772318252
DiskReadGiB          : 45.1326256990433
DiskReadIOps         : 878278
DiskWriteGiB         : 1230.72120628133
DiskWriteIOps        : 176832212
LastUpdateTime       : 5/16/2016 4:30:00 PM
NetworkReadGiB       : 29.3502839952707
NetworkWriteGiB      : 25.5208827350289
PeakDiskGiB          : 21.9638671875
PeakMemoryGiB        : 1.11184692382813
StartTime            : 2/10/2016 7:07:24 PM
```

<span data-ttu-id="bb54c-110">第一個命令會使用 **AzBatchAccountKeys** 建立名為 ContosoBatchAccount 的 batch 帳戶的帳戶金鑰的物件參考。</span><span class="sxs-lookup"><span data-stu-id="bb54c-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="bb54c-111">該命令會將這個物件參照儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="bb54c-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="bb54c-112">第二個命令會取得指定帳戶中所有池的統計資料，然後將它們儲存在 $PoolStatistics 中。</span><span class="sxs-lookup"><span data-stu-id="bb54c-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>
<span data-ttu-id="bb54c-113">最後一個命令會顯示 $PoolStatistics 的 **ResourceStatistics** 屬性。</span><span class="sxs-lookup"><span data-stu-id="bb54c-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="bb54c-114">參數</span><span class="sxs-lookup"><span data-stu-id="bb54c-114">PARAMETERS</span></span>

### <span data-ttu-id="bb54c-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="bb54c-115">-BatchContext</span></span>
<span data-ttu-id="bb54c-116">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="bb54c-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bb54c-117">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="bb54c-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bb54c-118">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="bb54c-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bb54c-119">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="bb54c-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bb54c-120">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="bb54c-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bb54c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb54c-121">-DefaultProfile</span></span>
<span data-ttu-id="bb54c-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb54c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb54c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb54c-123">CommonParameters</span></span>
<span data-ttu-id="bb54c-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb54c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb54c-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bb54c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb54c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="bb54c-126">INPUTS</span></span>

### <span data-ttu-id="bb54c-127">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="bb54c-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bb54c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="bb54c-128">OUTPUTS</span></span>

### <span data-ttu-id="bb54c-129">Microsoft.Azure.Commands.Batch。PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="bb54c-129">Microsoft.Azure.Commands.Batch.Models.PSPoolStatistics</span></span>

## <span data-ttu-id="bb54c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="bb54c-130">NOTES</span></span>

## <span data-ttu-id="bb54c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb54c-131">RELATED LINKS</span></span>

[<span data-ttu-id="bb54c-132">AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bb54c-132">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="bb54c-133">AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="bb54c-133">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)

[<span data-ttu-id="bb54c-134">AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="bb54c-134">Get-AzBatchJobStatistic</span></span>](./Get-AzBatchJobStatistic.md)


