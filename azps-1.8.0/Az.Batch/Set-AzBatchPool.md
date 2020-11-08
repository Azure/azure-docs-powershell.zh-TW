---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 7ab0d9f64b14f6fbdd572f69ecb081114d78891d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93799410"
---
# <span data-ttu-id="ac1a5-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="ac1a5-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="ac1a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac1a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ac1a5-103">更新文件庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ac1a5-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="ac1a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac1a5-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac1a5-105">說明</span><span class="sxs-lookup"><span data-stu-id="ac1a5-105">DESCRIPTION</span></span>
<span data-ttu-id="ac1a5-106">**AzBatchPool** Cmdlet 會更新 Azure Batch 服務中的 pool 屬性。</span><span class="sxs-lookup"><span data-stu-id="ac1a5-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="ac1a5-107">使用 Get-AzBatchPool Cmdlet 來取得 **PSCloudPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="ac1a5-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="ac1a5-108">修改該物件的屬性，然後使用目前的 Cmdlet 來認可您對批次服務所做的變更。</span><span class="sxs-lookup"><span data-stu-id="ac1a5-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="ac1a5-109">示例</span><span class="sxs-lookup"><span data-stu-id="ac1a5-109">EXAMPLES</span></span>

### <span data-ttu-id="ac1a5-110">範例1：更新文件庫</span><span class="sxs-lookup"><span data-stu-id="ac1a5-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="ac1a5-111">第一個命令會使用 **AzBatchPool** 來取得池子，然後將它儲存在 $Pool 變數中。</span><span class="sxs-lookup"><span data-stu-id="ac1a5-111">The first command gets a pool by using **Get-AzBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="ac1a5-112">接下來的三個命令會修改 $Pool 物件上的「開始」任務規格。</span><span class="sxs-lookup"><span data-stu-id="ac1a5-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="ac1a5-113">最後一個命令會更新批次服務，以符合 $Pool 中的本機物件。</span><span class="sxs-lookup"><span data-stu-id="ac1a5-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="ac1a5-114">參數</span><span class="sxs-lookup"><span data-stu-id="ac1a5-114">PARAMETERS</span></span>

### <span data-ttu-id="ac1a5-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="ac1a5-115">-BatchContext</span></span>
<span data-ttu-id="ac1a5-116">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="ac1a5-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ac1a5-117">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="ac1a5-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ac1a5-118">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="ac1a5-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ac1a5-119">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="ac1a5-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ac1a5-120">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="ac1a5-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ac1a5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac1a5-121">-DefaultProfile</span></span>
<span data-ttu-id="ac1a5-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac1a5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac1a5-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="ac1a5-123">-Pool</span></span>
<span data-ttu-id="ac1a5-124">指定此 Cmdlet 更新批次服務的 **PSCloudPool** 。</span><span class="sxs-lookup"><span data-stu-id="ac1a5-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="ac1a5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac1a5-125">CommonParameters</span></span>
<span data-ttu-id="ac1a5-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac1a5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac1a5-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ac1a5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac1a5-128">輸入</span><span class="sxs-lookup"><span data-stu-id="ac1a5-128">INPUTS</span></span>

### <span data-ttu-id="ac1a5-129">Microsoft.Azure.Commands.Batch。PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="ac1a5-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="ac1a5-130">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="ac1a5-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ac1a5-131">輸出</span><span class="sxs-lookup"><span data-stu-id="ac1a5-131">OUTPUTS</span></span>

### <span data-ttu-id="ac1a5-132">System.void</span><span class="sxs-lookup"><span data-stu-id="ac1a5-132">System.Void</span></span>

## <span data-ttu-id="ac1a5-133">筆記</span><span class="sxs-lookup"><span data-stu-id="ac1a5-133">NOTES</span></span>

## <span data-ttu-id="ac1a5-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac1a5-134">RELATED LINKS</span></span>

[<span data-ttu-id="ac1a5-135">AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="ac1a5-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="ac1a5-136">AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ac1a5-136">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ac1a5-137">新-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="ac1a5-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="ac1a5-138">移除-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="ac1a5-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="ac1a5-139">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ac1a5-139">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

