---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: 8db1f11cfd434beb52eb32e4b175b2dab67ecbdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624621"
---
# <span data-ttu-id="c0f04-101">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="c0f04-101">Stop-AzureBatchPoolResize</span></span>

## <span data-ttu-id="c0f04-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0f04-102">SYNOPSIS</span></span>
<span data-ttu-id="c0f04-103">停止調整池大小的操作。</span><span class="sxs-lookup"><span data-stu-id="c0f04-103">Stops a pool resize operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0f04-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0f04-104">SYNTAX</span></span>

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0f04-105">說明</span><span class="sxs-lookup"><span data-stu-id="c0f04-105">DESCRIPTION</span></span>
<span data-ttu-id="c0f04-106">**AzureBatchPoolResize** Cmdlet 會在池中停止 Azure 批次調整大小操作。</span><span class="sxs-lookup"><span data-stu-id="c0f04-106">The **Stop-AzureBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="c0f04-107">示例</span><span class="sxs-lookup"><span data-stu-id="c0f04-107">EXAMPLES</span></span>

### <span data-ttu-id="c0f04-108">範例1：停止調整池子的大小</span><span class="sxs-lookup"><span data-stu-id="c0f04-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="c0f04-109">這個命令會在具有識別碼 ContosoPool06 的池中停止調整大小操作。</span><span class="sxs-lookup"><span data-stu-id="c0f04-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="c0f04-110">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="c0f04-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c0f04-111">範例2：使用管線停止調整池的大小</span><span class="sxs-lookup"><span data-stu-id="c0f04-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="c0f04-112">這個命令會使用管線運算子停止調整池的大小。</span><span class="sxs-lookup"><span data-stu-id="c0f04-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="c0f04-113">命令會使用 Get-AzureBatchPool Cmdlet 來取得具有識別碼 ContosoPool06 的 pool。</span><span class="sxs-lookup"><span data-stu-id="c0f04-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="c0f04-114">命令會將該 pool 物件傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0f04-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="c0f04-115">該命令會停止該池子上的調整大小作業。</span><span class="sxs-lookup"><span data-stu-id="c0f04-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="c0f04-116">參數</span><span class="sxs-lookup"><span data-stu-id="c0f04-116">PARAMETERS</span></span>

### <span data-ttu-id="c0f04-117">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="c0f04-117">-BatchContext</span></span>
<span data-ttu-id="c0f04-118">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="c0f04-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c0f04-119">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="c0f04-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c0f04-120">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="c0f04-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c0f04-121">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="c0f04-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c0f04-122">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="c0f04-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c0f04-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0f04-123">-DefaultProfile</span></span>
<span data-ttu-id="c0f04-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0f04-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0f04-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="c0f04-125">-Id</span></span>
<span data-ttu-id="c0f04-126">指定此 Cmdlet 停止調整大小操作的池 ID。</span><span class="sxs-lookup"><span data-stu-id="c0f04-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0f04-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0f04-127">CommonParameters</span></span>
<span data-ttu-id="c0f04-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0f04-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0f04-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c0f04-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0f04-130">輸入</span><span class="sxs-lookup"><span data-stu-id="c0f04-130">INPUTS</span></span>

### <span data-ttu-id="c0f04-131">System.object</span><span class="sxs-lookup"><span data-stu-id="c0f04-131">System.String</span></span>

### <span data-ttu-id="c0f04-132">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="c0f04-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="c0f04-133">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c0f04-133">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="c0f04-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c0f04-134">OUTPUTS</span></span>

### <span data-ttu-id="c0f04-135">System.void</span><span class="sxs-lookup"><span data-stu-id="c0f04-135">System.Void</span></span>

## <span data-ttu-id="c0f04-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c0f04-136">NOTES</span></span>

## <span data-ttu-id="c0f04-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0f04-137">RELATED LINKS</span></span>

[<span data-ttu-id="c0f04-138">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c0f04-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c0f04-139">AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c0f04-139">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="c0f04-140">開始-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="c0f04-140">Start-AzureBatchPoolResize</span></span>](./Start-AzureBatchPoolResize.md)

[<span data-ttu-id="c0f04-141">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c0f04-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


