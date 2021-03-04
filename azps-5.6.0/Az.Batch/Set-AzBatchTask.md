---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: 80fc0c530904717561aa34ca98844fede75e747e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912466"
---
# <span data-ttu-id="49bf3-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="49bf3-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="49bf3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="49bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="49bf3-103">更新工作的屬性。</span><span class="sxs-lookup"><span data-stu-id="49bf3-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="49bf3-104">語法</span><span class="sxs-lookup"><span data-stu-id="49bf3-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49bf3-105">描述</span><span class="sxs-lookup"><span data-stu-id="49bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="49bf3-106">**Set-AzBatchTask** Cmdlet 會更新 Azure Batch 服務中工作的屬性。</span><span class="sxs-lookup"><span data-stu-id="49bf3-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="49bf3-107">使用 Get-AzBatchTask Cmdlet 取得 **PSCloudTask** 物件。</span><span class="sxs-lookup"><span data-stu-id="49bf3-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="49bf3-108">修改該物件的屬性，然後使用目前的 Cmdlet 來提交您變更的批次處理服務。</span><span class="sxs-lookup"><span data-stu-id="49bf3-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="49bf3-109">例子</span><span class="sxs-lookup"><span data-stu-id="49bf3-109">EXAMPLES</span></span>

### <span data-ttu-id="49bf3-110">範例 1：更新工作</span><span class="sxs-lookup"><span data-stu-id="49bf3-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="49bf3-111">第一個命令會使用 **Get-AzBatchTask** 取得工作，然後將它儲存在$Task變數中。</span><span class="sxs-lookup"><span data-stu-id="49bf3-111">The first command gets a task by using **Get-AzBatchTask**, and then stores it in the $Task variable.</span></span>
<span data-ttu-id="49bf3-112">接下來兩個命令會修改工作的限制$Task。</span><span class="sxs-lookup"><span data-stu-id="49bf3-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="49bf3-113">最後一個命令會更新 Batch 服務，以配合 $Task。</span><span class="sxs-lookup"><span data-stu-id="49bf3-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="49bf3-114">參數</span><span class="sxs-lookup"><span data-stu-id="49bf3-114">PARAMETERS</span></span>

### <span data-ttu-id="49bf3-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="49bf3-115">-BatchContext</span></span>
<span data-ttu-id="49bf3-116">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="49bf3-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="49bf3-117">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="49bf3-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="49bf3-118">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="49bf3-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="49bf3-119">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="49bf3-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="49bf3-120">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="49bf3-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="49bf3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49bf3-121">-DefaultProfile</span></span>
<span data-ttu-id="49bf3-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="49bf3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49bf3-123">-工作</span><span class="sxs-lookup"><span data-stu-id="49bf3-123">-Task</span></span>
<span data-ttu-id="49bf3-124">指定此 Cmdlet 更新批次處理服務的 **PSCloudTask。**</span><span class="sxs-lookup"><span data-stu-id="49bf3-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49bf3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49bf3-125">CommonParameters</span></span>
<span data-ttu-id="49bf3-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="49bf3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49bf3-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49bf3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49bf3-128">輸入</span><span class="sxs-lookup"><span data-stu-id="49bf3-128">INPUTS</span></span>

### <span data-ttu-id="49bf3-129">Microsoft.Azure.Commands.Batch。Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="49bf3-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="49bf3-130">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="49bf3-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="49bf3-131">輸出</span><span class="sxs-lookup"><span data-stu-id="49bf3-131">OUTPUTS</span></span>

### <span data-ttu-id="49bf3-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="49bf3-132">System.Void</span></span>

## <span data-ttu-id="49bf3-133">筆記</span><span class="sxs-lookup"><span data-stu-id="49bf3-133">NOTES</span></span>

## <span data-ttu-id="49bf3-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="49bf3-134">RELATED LINKS</span></span>

[<span data-ttu-id="49bf3-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="49bf3-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="49bf3-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="49bf3-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="49bf3-137">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="49bf3-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="49bf3-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="49bf3-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="49bf3-139">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="49bf3-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="49bf3-140">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="49bf3-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
