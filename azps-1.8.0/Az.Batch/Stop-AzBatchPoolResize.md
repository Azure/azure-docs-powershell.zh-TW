---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 9e970251671297a6fa4a0019bb663c9e34cbe4d7
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93623264"
---
# <span data-ttu-id="7be95-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="7be95-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="7be95-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7be95-102">SYNOPSIS</span></span>
<span data-ttu-id="7be95-103">停止調整池大小的操作。</span><span class="sxs-lookup"><span data-stu-id="7be95-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="7be95-104">句法</span><span class="sxs-lookup"><span data-stu-id="7be95-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7be95-105">說明</span><span class="sxs-lookup"><span data-stu-id="7be95-105">DESCRIPTION</span></span>
<span data-ttu-id="7be95-106">**AzBatchPoolResize** Cmdlet 會在池中停止 Azure 批次調整大小操作。</span><span class="sxs-lookup"><span data-stu-id="7be95-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="7be95-107">示例</span><span class="sxs-lookup"><span data-stu-id="7be95-107">EXAMPLES</span></span>

### <span data-ttu-id="7be95-108">範例1：停止調整池子的大小</span><span class="sxs-lookup"><span data-stu-id="7be95-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="7be95-109">這個命令會在具有識別碼 ContosoPool06 的池中停止調整大小操作。</span><span class="sxs-lookup"><span data-stu-id="7be95-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="7be95-110">使用 Get-AzBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="7be95-110">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="7be95-111">範例2：使用管線停止調整池的大小</span><span class="sxs-lookup"><span data-stu-id="7be95-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="7be95-112">這個命令會使用管線運算子停止調整池的大小。</span><span class="sxs-lookup"><span data-stu-id="7be95-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="7be95-113">命令會使用 Get-AzBatchPool Cmdlet 來取得具有識別碼 ContosoPool06 的 pool。</span><span class="sxs-lookup"><span data-stu-id="7be95-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="7be95-114">命令會將該 pool 物件傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7be95-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="7be95-115">該命令會停止該池子上的調整大小作業。</span><span class="sxs-lookup"><span data-stu-id="7be95-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="7be95-116">參數</span><span class="sxs-lookup"><span data-stu-id="7be95-116">PARAMETERS</span></span>

### <span data-ttu-id="7be95-117">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="7be95-117">-BatchContext</span></span>
<span data-ttu-id="7be95-118">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="7be95-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7be95-119">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="7be95-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7be95-120">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="7be95-120">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7be95-121">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="7be95-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7be95-122">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="7be95-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7be95-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7be95-123">-DefaultProfile</span></span>
<span data-ttu-id="7be95-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7be95-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7be95-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="7be95-125">-Id</span></span>
<span data-ttu-id="7be95-126">指定此 Cmdlet 停止調整大小操作的池 ID。</span><span class="sxs-lookup"><span data-stu-id="7be95-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="7be95-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be95-127">CommonParameters</span></span>
<span data-ttu-id="7be95-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7be95-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be95-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7be95-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be95-130">輸入</span><span class="sxs-lookup"><span data-stu-id="7be95-130">INPUTS</span></span>

### <span data-ttu-id="7be95-131">System.object</span><span class="sxs-lookup"><span data-stu-id="7be95-131">System.String</span></span>

### <span data-ttu-id="7be95-132">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="7be95-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7be95-133">輸出</span><span class="sxs-lookup"><span data-stu-id="7be95-133">OUTPUTS</span></span>

### <span data-ttu-id="7be95-134">System.void</span><span class="sxs-lookup"><span data-stu-id="7be95-134">System.Void</span></span>

## <span data-ttu-id="7be95-135">筆記</span><span class="sxs-lookup"><span data-stu-id="7be95-135">NOTES</span></span>

## <span data-ttu-id="7be95-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="7be95-136">RELATED LINKS</span></span>

[<span data-ttu-id="7be95-137">AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7be95-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7be95-138">AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="7be95-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="7be95-139">開始-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="7be95-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="7be95-140">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7be95-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


