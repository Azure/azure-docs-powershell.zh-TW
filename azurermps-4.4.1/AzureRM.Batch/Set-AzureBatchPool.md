---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: d18a6bdc9a2064e21507c909005692d5d21c63f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450860"
---
# <span data-ttu-id="06095-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="06095-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="06095-102">摘要</span><span class="sxs-lookup"><span data-stu-id="06095-102">SYNOPSIS</span></span>
<span data-ttu-id="06095-103">更新文件庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="06095-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06095-104">句法</span><span class="sxs-lookup"><span data-stu-id="06095-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06095-105">說明</span><span class="sxs-lookup"><span data-stu-id="06095-105">DESCRIPTION</span></span>
<span data-ttu-id="06095-106">**AzureBatchPool** Cmdlet 會更新 Azure Batch 服務中的 pool 屬性。</span><span class="sxs-lookup"><span data-stu-id="06095-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="06095-107">使用 Get-AzureBatchPool Cmdlet 來取得 **PSCloudPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="06095-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="06095-108">修改該物件的屬性，然後使用目前的 Cmdlet 來認可您對批次服務所做的變更。</span><span class="sxs-lookup"><span data-stu-id="06095-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="06095-109">示例</span><span class="sxs-lookup"><span data-stu-id="06095-109">EXAMPLES</span></span>

### <span data-ttu-id="06095-110">範例1：更新文件庫</span><span class="sxs-lookup"><span data-stu-id="06095-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="06095-111">第一個命令會使用 **AzureBatchPool** 來取得池子，然後將它儲存在 $Pool 變數中。</span><span class="sxs-lookup"><span data-stu-id="06095-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>

<span data-ttu-id="06095-112">接下來的三個命令會修改 $Pool 物件上的「開始」任務規格。</span><span class="sxs-lookup"><span data-stu-id="06095-112">The next three commands modify the start task specification on the $Pool object.</span></span>

<span data-ttu-id="06095-113">最後一個命令會更新批次服務，以符合 $Pool 中的本機物件。</span><span class="sxs-lookup"><span data-stu-id="06095-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="06095-114">參數</span><span class="sxs-lookup"><span data-stu-id="06095-114">PARAMETERS</span></span>

### <span data-ttu-id="06095-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="06095-115">-BatchContext</span></span>
<span data-ttu-id="06095-116">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="06095-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="06095-117">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06095-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="06095-118">-Pool</span><span class="sxs-lookup"><span data-stu-id="06095-118">-Pool</span></span>
<span data-ttu-id="06095-119">指定此 Cmdlet 更新批次服務的 **PSCloudPool** 。</span><span class="sxs-lookup"><span data-stu-id="06095-119">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06095-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06095-120">-DefaultProfile</span></span>
<span data-ttu-id="06095-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="06095-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06095-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06095-122">CommonParameters</span></span>
<span data-ttu-id="06095-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="06095-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06095-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="06095-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06095-125">輸入</span><span class="sxs-lookup"><span data-stu-id="06095-125">INPUTS</span></span>

### <span data-ttu-id="06095-126">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="06095-126">BatchAccountContext</span></span>
<span data-ttu-id="06095-127">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="06095-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="06095-128">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="06095-128">PSCloudPool</span></span>
<span data-ttu-id="06095-129">形參 "Pool" 接受管線中 "PSCloudPool" 類型的值</span><span class="sxs-lookup"><span data-stu-id="06095-129">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="06095-130">輸出</span><span class="sxs-lookup"><span data-stu-id="06095-130">OUTPUTS</span></span>

## <span data-ttu-id="06095-131">筆記</span><span class="sxs-lookup"><span data-stu-id="06095-131">NOTES</span></span>

## <span data-ttu-id="06095-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="06095-132">RELATED LINKS</span></span>

[<span data-ttu-id="06095-133">AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="06095-133">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="06095-134">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="06095-134">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="06095-135">新-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="06095-135">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="06095-136">移除-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="06095-136">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="06095-137">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="06095-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


