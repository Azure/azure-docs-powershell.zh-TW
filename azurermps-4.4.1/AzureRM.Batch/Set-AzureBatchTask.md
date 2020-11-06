---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: b572a7aefc3076671e78895f5fea531929858873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454908"
---
# <span data-ttu-id="8ecb0-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8ecb0-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="8ecb0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ecb0-102">SYNOPSIS</span></span>
<span data-ttu-id="8ecb0-103">更新任務的屬性。</span><span class="sxs-lookup"><span data-stu-id="8ecb0-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ecb0-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ecb0-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ecb0-105">說明</span><span class="sxs-lookup"><span data-stu-id="8ecb0-105">DESCRIPTION</span></span>
<span data-ttu-id="8ecb0-106">**AzureBatchTask** Cmdlet 會更新 Azure Batch 服務中任務的屬性。</span><span class="sxs-lookup"><span data-stu-id="8ecb0-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="8ecb0-107">使用 Get-AzureBatchTask Cmdlet 來取得 **PSCloudTask** 物件。</span><span class="sxs-lookup"><span data-stu-id="8ecb0-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="8ecb0-108">修改該物件的屬性，然後使用目前的 Cmdlet 來認可您對批次服務所做的變更。</span><span class="sxs-lookup"><span data-stu-id="8ecb0-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="8ecb0-109">示例</span><span class="sxs-lookup"><span data-stu-id="8ecb0-109">EXAMPLES</span></span>

### <span data-ttu-id="8ecb0-110">範例1：更新任務</span><span class="sxs-lookup"><span data-stu-id="8ecb0-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="8ecb0-111">第一個命令會使用 **AzureBatchTask** 來取得任務，然後將它儲存在 $Task 變數中。</span><span class="sxs-lookup"><span data-stu-id="8ecb0-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>

<span data-ttu-id="8ecb0-112">接下來的兩個命令會在 $Task 中修改任務的限制。</span><span class="sxs-lookup"><span data-stu-id="8ecb0-112">The next two commands modify the constraints of the task in $Task.</span></span>

<span data-ttu-id="8ecb0-113">最後一個命令會更新批次服務，以符合 $Task 中的本機物件。</span><span class="sxs-lookup"><span data-stu-id="8ecb0-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="8ecb0-114">參數</span><span class="sxs-lookup"><span data-stu-id="8ecb0-114">PARAMETERS</span></span>

### <span data-ttu-id="8ecb0-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="8ecb0-115">-BatchContext</span></span>
<span data-ttu-id="8ecb0-116">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="8ecb0-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8ecb0-117">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ecb0-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="8ecb0-118">-任務</span><span class="sxs-lookup"><span data-stu-id="8ecb0-118">-Task</span></span>
<span data-ttu-id="8ecb0-119">指定此 Cmdlet 更新批次服務的 **PSCloudTask** 。</span><span class="sxs-lookup"><span data-stu-id="8ecb0-119">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="8ecb0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ecb0-120">-DefaultProfile</span></span>
<span data-ttu-id="8ecb0-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ecb0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ecb0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ecb0-122">CommonParameters</span></span>
<span data-ttu-id="8ecb0-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ecb0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ecb0-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8ecb0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ecb0-125">輸入</span><span class="sxs-lookup"><span data-stu-id="8ecb0-125">INPUTS</span></span>

### <span data-ttu-id="8ecb0-126">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="8ecb0-126">BatchAccountContext</span></span>
<span data-ttu-id="8ecb0-127">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="8ecb0-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="8ecb0-128">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="8ecb0-128">PSCloudTask</span></span>
<span data-ttu-id="8ecb0-129">形參 "Task" 接受管線中 "PSCloudTask" 類型的值</span><span class="sxs-lookup"><span data-stu-id="8ecb0-129">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="8ecb0-130">輸出</span><span class="sxs-lookup"><span data-stu-id="8ecb0-130">OUTPUTS</span></span>

## <span data-ttu-id="8ecb0-131">筆記</span><span class="sxs-lookup"><span data-stu-id="8ecb0-131">NOTES</span></span>

## <span data-ttu-id="8ecb0-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ecb0-132">RELATED LINKS</span></span>

[<span data-ttu-id="8ecb0-133">AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8ecb0-133">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="8ecb0-134">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8ecb0-134">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8ecb0-135">新-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8ecb0-135">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="8ecb0-136">移除-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8ecb0-136">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="8ecb0-137">停止 AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8ecb0-137">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="8ecb0-138">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ecb0-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


