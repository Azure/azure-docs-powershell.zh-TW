---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 339c3a537e84ff63a6eac0a6f1f63669ce4567ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903878"
---
# <span data-ttu-id="03626-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="03626-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="03626-102">簡介</span><span class="sxs-lookup"><span data-stu-id="03626-102">SYNOPSIS</span></span>
<span data-ttu-id="03626-103">停止調整區大小作業。</span><span class="sxs-lookup"><span data-stu-id="03626-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="03626-104">語法</span><span class="sxs-lookup"><span data-stu-id="03626-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03626-105">描述</span><span class="sxs-lookup"><span data-stu-id="03626-105">DESCRIPTION</span></span>
<span data-ttu-id="03626-106">**Stop-AzBatchPoolResize Cmdlet** 會停止在資料庫上的 Azure 批次調整大小作業。</span><span class="sxs-lookup"><span data-stu-id="03626-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="03626-107">例子</span><span class="sxs-lookup"><span data-stu-id="03626-107">EXAMPLES</span></span>

### <span data-ttu-id="03626-108">範例 1：停止調整資料庫大小</span><span class="sxs-lookup"><span data-stu-id="03626-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="03626-109">此命令會停止在具有 ID ContosoPool06 的集中執行調整大小作業。</span><span class="sxs-lookup"><span data-stu-id="03626-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="03626-110">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="03626-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="03626-111">範例 2：使用管線停止調整資料庫大小</span><span class="sxs-lookup"><span data-stu-id="03626-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="03626-112">此命令會使用管線運算子停止調整資料庫大小。</span><span class="sxs-lookup"><span data-stu-id="03626-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="03626-113">命令會使用命令 Cmdlet 來Get-AzBatchPool ContosoPool06。</span><span class="sxs-lookup"><span data-stu-id="03626-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="03626-114">該命令會將該 Pool 物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03626-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="03626-115">該命令會停止該區上的大小調整大小作業。</span><span class="sxs-lookup"><span data-stu-id="03626-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="03626-116">參數</span><span class="sxs-lookup"><span data-stu-id="03626-116">PARAMETERS</span></span>

### <span data-ttu-id="03626-117">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="03626-117">-BatchContext</span></span>
<span data-ttu-id="03626-118">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="03626-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="03626-119">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="03626-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="03626-120">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="03626-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="03626-121">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="03626-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="03626-122">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="03626-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="03626-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03626-123">-DefaultProfile</span></span>
<span data-ttu-id="03626-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="03626-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03626-125">-Id</span><span class="sxs-lookup"><span data-stu-id="03626-125">-Id</span></span>
<span data-ttu-id="03626-126">指定此 Cmdlet 停止重大小作業之資料庫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="03626-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="03626-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03626-127">CommonParameters</span></span>
<span data-ttu-id="03626-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="03626-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03626-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03626-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03626-130">輸入</span><span class="sxs-lookup"><span data-stu-id="03626-130">INPUTS</span></span>

### <span data-ttu-id="03626-131">System.String</span><span class="sxs-lookup"><span data-stu-id="03626-131">System.String</span></span>

### <span data-ttu-id="03626-132">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="03626-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="03626-133">輸出</span><span class="sxs-lookup"><span data-stu-id="03626-133">OUTPUTS</span></span>

### <span data-ttu-id="03626-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="03626-134">System.Void</span></span>

## <span data-ttu-id="03626-135">筆記</span><span class="sxs-lookup"><span data-stu-id="03626-135">NOTES</span></span>

## <span data-ttu-id="03626-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="03626-136">RELATED LINKS</span></span>

[<span data-ttu-id="03626-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="03626-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="03626-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="03626-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="03626-139">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="03626-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="03626-140">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="03626-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
