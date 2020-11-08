---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: 7c3e976e85e6754702f8288f5bb257086837fc36
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970610"
---
# <span data-ttu-id="5b1bc-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5b1bc-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="5b1bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b1bc-102">SYNOPSIS</span></span>
<span data-ttu-id="5b1bc-103">更新任務的屬性。</span><span class="sxs-lookup"><span data-stu-id="5b1bc-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="5b1bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b1bc-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b1bc-105">說明</span><span class="sxs-lookup"><span data-stu-id="5b1bc-105">DESCRIPTION</span></span>
<span data-ttu-id="5b1bc-106">**AzBatchTask** Cmdlet 會更新 Azure Batch 服務中任務的屬性。</span><span class="sxs-lookup"><span data-stu-id="5b1bc-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="5b1bc-107">使用 Get-AzBatchTask Cmdlet 來取得 **PSCloudTask** 物件。</span><span class="sxs-lookup"><span data-stu-id="5b1bc-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="5b1bc-108">修改該物件的屬性，然後使用目前的 Cmdlet 來認可您對批次服務所做的變更。</span><span class="sxs-lookup"><span data-stu-id="5b1bc-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="5b1bc-109">示例</span><span class="sxs-lookup"><span data-stu-id="5b1bc-109">EXAMPLES</span></span>

### <span data-ttu-id="5b1bc-110">範例1：更新任務</span><span class="sxs-lookup"><span data-stu-id="5b1bc-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="5b1bc-111">第一個命令會使用 **AzBatchTask** 來取得任務，然後將它儲存在 $Task 變數中。</span><span class="sxs-lookup"><span data-stu-id="5b1bc-111">The first command gets a task by using **Get-AzBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="5b1bc-112">接下來的兩個命令會在 $Task 中修改任務的限制。</span><span class="sxs-lookup"><span data-stu-id="5b1bc-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="5b1bc-113">最後一個命令會更新批次服務，以符合 $Task 中的本機物件。</span><span class="sxs-lookup"><span data-stu-id="5b1bc-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="5b1bc-114">參數</span><span class="sxs-lookup"><span data-stu-id="5b1bc-114">PARAMETERS</span></span>

### <span data-ttu-id="5b1bc-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="5b1bc-115">-BatchContext</span></span>
<span data-ttu-id="5b1bc-116">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="5b1bc-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5b1bc-117">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="5b1bc-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5b1bc-118">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="5b1bc-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5b1bc-119">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="5b1bc-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5b1bc-120">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="5b1bc-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5b1bc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b1bc-121">-DefaultProfile</span></span>
<span data-ttu-id="5b1bc-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b1bc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b1bc-123">-任務</span><span class="sxs-lookup"><span data-stu-id="5b1bc-123">-Task</span></span>
<span data-ttu-id="5b1bc-124">指定此 Cmdlet 更新批次服務的 **PSCloudTask** 。</span><span class="sxs-lookup"><span data-stu-id="5b1bc-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="5b1bc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b1bc-125">CommonParameters</span></span>
<span data-ttu-id="5b1bc-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b1bc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b1bc-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5b1bc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b1bc-128">輸入</span><span class="sxs-lookup"><span data-stu-id="5b1bc-128">INPUTS</span></span>

### <span data-ttu-id="5b1bc-129">Microsoft.Azure.Commands.Batch。PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="5b1bc-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="5b1bc-130">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="5b1bc-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5b1bc-131">輸出</span><span class="sxs-lookup"><span data-stu-id="5b1bc-131">OUTPUTS</span></span>

### <span data-ttu-id="5b1bc-132">System.void</span><span class="sxs-lookup"><span data-stu-id="5b1bc-132">System.Void</span></span>

## <span data-ttu-id="5b1bc-133">筆記</span><span class="sxs-lookup"><span data-stu-id="5b1bc-133">NOTES</span></span>

## <span data-ttu-id="5b1bc-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b1bc-134">RELATED LINKS</span></span>

[<span data-ttu-id="5b1bc-135">AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5b1bc-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="5b1bc-136">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5b1bc-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5b1bc-137">新-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5b1bc-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="5b1bc-138">移除-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5b1bc-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="5b1bc-139">停止 AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5b1bc-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="5b1bc-140">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b1bc-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
