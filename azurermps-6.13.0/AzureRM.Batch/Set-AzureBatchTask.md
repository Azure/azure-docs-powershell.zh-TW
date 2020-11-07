---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: bae5f2b075f8d4f2fa579b38bdccf160cd46caad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623568"
---
# <span data-ttu-id="2b004-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2b004-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="2b004-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b004-102">SYNOPSIS</span></span>
<span data-ttu-id="2b004-103">更新任務的屬性。</span><span class="sxs-lookup"><span data-stu-id="2b004-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b004-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b004-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b004-105">說明</span><span class="sxs-lookup"><span data-stu-id="2b004-105">DESCRIPTION</span></span>
<span data-ttu-id="2b004-106">**AzureBatchTask** Cmdlet 會更新 Azure Batch 服務中任務的屬性。</span><span class="sxs-lookup"><span data-stu-id="2b004-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="2b004-107">使用 Get-AzureBatchTask Cmdlet 來取得 **PSCloudTask** 物件。</span><span class="sxs-lookup"><span data-stu-id="2b004-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="2b004-108">修改該物件的屬性，然後使用目前的 Cmdlet 來認可您對批次服務所做的變更。</span><span class="sxs-lookup"><span data-stu-id="2b004-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="2b004-109">示例</span><span class="sxs-lookup"><span data-stu-id="2b004-109">EXAMPLES</span></span>

### <span data-ttu-id="2b004-110">範例1：更新任務</span><span class="sxs-lookup"><span data-stu-id="2b004-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="2b004-111">第一個命令會使用 **AzureBatchTask** 來取得任務，然後將它儲存在 $Task 變數中。</span><span class="sxs-lookup"><span data-stu-id="2b004-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="2b004-112">接下來的兩個命令會在 $Task 中修改任務的限制。</span><span class="sxs-lookup"><span data-stu-id="2b004-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="2b004-113">最後一個命令會更新批次服務，以符合 $Task 中的本機物件。</span><span class="sxs-lookup"><span data-stu-id="2b004-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="2b004-114">參數</span><span class="sxs-lookup"><span data-stu-id="2b004-114">PARAMETERS</span></span>

### <span data-ttu-id="2b004-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="2b004-115">-BatchContext</span></span>
<span data-ttu-id="2b004-116">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="2b004-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2b004-117">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="2b004-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2b004-118">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="2b004-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2b004-119">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="2b004-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2b004-120">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="2b004-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2b004-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b004-121">-DefaultProfile</span></span>
<span data-ttu-id="2b004-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b004-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b004-123">-任務</span><span class="sxs-lookup"><span data-stu-id="2b004-123">-Task</span></span>
<span data-ttu-id="2b004-124">指定此 Cmdlet 更新批次服務的 **PSCloudTask** 。</span><span class="sxs-lookup"><span data-stu-id="2b004-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="2b004-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b004-125">CommonParameters</span></span>
<span data-ttu-id="2b004-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b004-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b004-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2b004-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b004-128">輸入</span><span class="sxs-lookup"><span data-stu-id="2b004-128">INPUTS</span></span>

### <span data-ttu-id="2b004-129">Microsoft.Azure.Commands.Batch。PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="2b004-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="2b004-130">參數： Task (ByValue) </span><span class="sxs-lookup"><span data-stu-id="2b004-130">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="2b004-131">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="2b004-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="2b004-132">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="2b004-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="2b004-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2b004-133">OUTPUTS</span></span>

### <span data-ttu-id="2b004-134">System.void</span><span class="sxs-lookup"><span data-stu-id="2b004-134">System.Void</span></span>

## <span data-ttu-id="2b004-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2b004-135">NOTES</span></span>

## <span data-ttu-id="2b004-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b004-136">RELATED LINKS</span></span>

[<span data-ttu-id="2b004-137">AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2b004-137">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="2b004-138">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2b004-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="2b004-139">新-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2b004-139">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="2b004-140">移除-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2b004-140">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="2b004-141">停止 AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="2b004-141">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="2b004-142">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2b004-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


