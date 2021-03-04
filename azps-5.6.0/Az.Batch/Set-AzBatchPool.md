---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 26a280ef567ed09ff14cf143048aadceeeed29e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912117"
---
# <span data-ttu-id="f03e8-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="f03e8-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="f03e8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f03e8-102">SYNOPSIS</span></span>
<span data-ttu-id="f03e8-103">更新資料庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f03e8-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="f03e8-104">語法</span><span class="sxs-lookup"><span data-stu-id="f03e8-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f03e8-105">描述</span><span class="sxs-lookup"><span data-stu-id="f03e8-105">DESCRIPTION</span></span>
<span data-ttu-id="f03e8-106">**Set-AzBatchPool** Cmdlet 會更新 Azure Batch 服務中的集區屬性。</span><span class="sxs-lookup"><span data-stu-id="f03e8-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="f03e8-107">使用 Get-AzBatchPool Cmdlet 取得 **PSCloudPool** 物件。</span><span class="sxs-lookup"><span data-stu-id="f03e8-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="f03e8-108">修改該物件的屬性，然後使用目前的 Cmdlet 來提交您變更的批次處理服務。</span><span class="sxs-lookup"><span data-stu-id="f03e8-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="f03e8-109">例子</span><span class="sxs-lookup"><span data-stu-id="f03e8-109">EXAMPLES</span></span>

### <span data-ttu-id="f03e8-110">範例 1：更新資料庫</span><span class="sxs-lookup"><span data-stu-id="f03e8-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="f03e8-111">第一個命令會使用 **Get-AzBatchPool** 取得一個資料庫，然後將它儲存在$Pool變數中。</span><span class="sxs-lookup"><span data-stu-id="f03e8-111">The first command gets a pool by using **Get-AzBatchPool**, and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="f03e8-112">接下來三個命令會修改物件上的$Pool規格。</span><span class="sxs-lookup"><span data-stu-id="f03e8-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="f03e8-113">最後一個命令會更新 Batch 服務，以與 $Pool 中的本地$Pool。</span><span class="sxs-lookup"><span data-stu-id="f03e8-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="f03e8-114">參數</span><span class="sxs-lookup"><span data-stu-id="f03e8-114">PARAMETERS</span></span>

### <span data-ttu-id="f03e8-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="f03e8-115">-BatchContext</span></span>
<span data-ttu-id="f03e8-116">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="f03e8-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f03e8-117">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="f03e8-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f03e8-118">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="f03e8-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f03e8-119">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="f03e8-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f03e8-120">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="f03e8-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f03e8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f03e8-121">-DefaultProfile</span></span>
<span data-ttu-id="f03e8-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f03e8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f03e8-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="f03e8-123">-Pool</span></span>
<span data-ttu-id="f03e8-124">指定此 **Cmdlet** 更新批次處理服務的 PSCloudPool。</span><span class="sxs-lookup"><span data-stu-id="f03e8-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="f03e8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f03e8-125">CommonParameters</span></span>
<span data-ttu-id="f03e8-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f03e8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f03e8-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f03e8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f03e8-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f03e8-128">INPUTS</span></span>

### <span data-ttu-id="f03e8-129">Microsoft.Azure.Commands.Batch。Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="f03e8-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="f03e8-130">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="f03e8-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f03e8-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f03e8-131">OUTPUTS</span></span>

### <span data-ttu-id="f03e8-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="f03e8-132">System.Void</span></span>

## <span data-ttu-id="f03e8-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f03e8-133">NOTES</span></span>

## <span data-ttu-id="f03e8-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f03e8-134">RELATED LINKS</span></span>

[<span data-ttu-id="f03e8-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="f03e8-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="f03e8-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f03e8-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f03e8-137">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="f03e8-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="f03e8-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="f03e8-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="f03e8-139">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f03e8-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
