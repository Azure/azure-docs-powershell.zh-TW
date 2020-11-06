---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: d8ce1ec138decb5769aebba431db2accd671f100
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451752"
---
# <span data-ttu-id="aecad-101">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="aecad-101">Stop-AzureBatchPoolResize</span></span>

## <span data-ttu-id="aecad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aecad-102">SYNOPSIS</span></span>
<span data-ttu-id="aecad-103">停止調整池大小的操作。</span><span class="sxs-lookup"><span data-stu-id="aecad-103">Stops a pool resize operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aecad-104">句法</span><span class="sxs-lookup"><span data-stu-id="aecad-104">SYNTAX</span></span>

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aecad-105">說明</span><span class="sxs-lookup"><span data-stu-id="aecad-105">DESCRIPTION</span></span>
<span data-ttu-id="aecad-106">**AzureBatchPoolResize** Cmdlet 會在池中停止 Azure 批次調整大小操作。</span><span class="sxs-lookup"><span data-stu-id="aecad-106">The **Stop-AzureBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="aecad-107">示例</span><span class="sxs-lookup"><span data-stu-id="aecad-107">EXAMPLES</span></span>

### <span data-ttu-id="aecad-108">範例1：停止調整池子的大小</span><span class="sxs-lookup"><span data-stu-id="aecad-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="aecad-109">這個命令會在具有識別碼 ContosoPool06 的池中停止調整大小操作。</span><span class="sxs-lookup"><span data-stu-id="aecad-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="aecad-110">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="aecad-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="aecad-111">範例2：使用管線停止調整池的大小</span><span class="sxs-lookup"><span data-stu-id="aecad-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="aecad-112">這個命令會使用管線運算子停止調整池的大小。</span><span class="sxs-lookup"><span data-stu-id="aecad-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="aecad-113">命令會使用 Get-AzureBatchPool Cmdlet 來取得具有識別碼 ContosoPool06 的 pool。</span><span class="sxs-lookup"><span data-stu-id="aecad-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="aecad-114">命令會將該 pool 物件傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aecad-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="aecad-115">該命令會停止該池子上的調整大小作業。</span><span class="sxs-lookup"><span data-stu-id="aecad-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="aecad-116">參數</span><span class="sxs-lookup"><span data-stu-id="aecad-116">PARAMETERS</span></span>

### <span data-ttu-id="aecad-117">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="aecad-117">-BatchContext</span></span>
<span data-ttu-id="aecad-118">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="aecad-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="aecad-119">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aecad-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="aecad-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="aecad-120">-Id</span></span>
<span data-ttu-id="aecad-121">指定此 Cmdlet 停止調整大小操作的池 ID。</span><span class="sxs-lookup"><span data-stu-id="aecad-121">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="aecad-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aecad-122">-DefaultProfile</span></span>
<span data-ttu-id="aecad-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aecad-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aecad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aecad-124">CommonParameters</span></span>
<span data-ttu-id="aecad-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aecad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aecad-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aecad-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aecad-127">輸入</span><span class="sxs-lookup"><span data-stu-id="aecad-127">INPUTS</span></span>

### <span data-ttu-id="aecad-128">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="aecad-128">BatchAccountContext</span></span>
<span data-ttu-id="aecad-129">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="aecad-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="aecad-130">字串</span><span class="sxs-lookup"><span data-stu-id="aecad-130">String</span></span>
<span data-ttu-id="aecad-131">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="aecad-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="aecad-132">輸出</span><span class="sxs-lookup"><span data-stu-id="aecad-132">OUTPUTS</span></span>

## <span data-ttu-id="aecad-133">筆記</span><span class="sxs-lookup"><span data-stu-id="aecad-133">NOTES</span></span>

## <span data-ttu-id="aecad-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="aecad-134">RELATED LINKS</span></span>

[<span data-ttu-id="aecad-135">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="aecad-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="aecad-136">AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="aecad-136">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="aecad-137">開始-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="aecad-137">Start-AzureBatchPoolResize</span></span>](./Start-AzureBatchPoolResize.md)

[<span data-ttu-id="aecad-138">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="aecad-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


