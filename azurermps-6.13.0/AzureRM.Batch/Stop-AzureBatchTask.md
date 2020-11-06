---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: 18a96a72cc965f5e93a035ba6ed7b91ba5419edf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451919"
---
# <span data-ttu-id="38d85-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="38d85-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="38d85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38d85-102">SYNOPSIS</span></span>
<span data-ttu-id="38d85-103">停止批次任務。</span><span class="sxs-lookup"><span data-stu-id="38d85-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38d85-104">句法</span><span class="sxs-lookup"><span data-stu-id="38d85-104">SYNTAX</span></span>

### <span data-ttu-id="38d85-105">標識號</span><span class="sxs-lookup"><span data-stu-id="38d85-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38d85-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="38d85-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38d85-107">說明</span><span class="sxs-lookup"><span data-stu-id="38d85-107">DESCRIPTION</span></span>
<span data-ttu-id="38d85-108">**AzureBatchTask** Cmdlet 會停止 Azure Batch 工作。</span><span class="sxs-lookup"><span data-stu-id="38d85-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="38d85-109">示例</span><span class="sxs-lookup"><span data-stu-id="38d85-109">EXAMPLES</span></span>

### <span data-ttu-id="38d85-110">範例1：依識別碼刪除批次任務</span><span class="sxs-lookup"><span data-stu-id="38d85-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="38d85-111">這個命令會停止在具有 ID 作業的作業下具有識別碼 Task23 的工作-000001。</span><span class="sxs-lookup"><span data-stu-id="38d85-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="38d85-112">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="38d85-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="38d85-113">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="38d85-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="38d85-114">範例2：使用管線停止批次工作</span><span class="sxs-lookup"><span data-stu-id="38d85-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="38d85-115">這個命令會透過使用 Get-AzureBatchTask Cmdlet 來取得作業中具有 id 作業000001之識別碼 Task26 的批次任務。</span><span class="sxs-lookup"><span data-stu-id="38d85-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="38d85-116">透過使用管線運算子，命令會將該工作傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38d85-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="38d85-117">命令會停止該任務。</span><span class="sxs-lookup"><span data-stu-id="38d85-117">The command stops that task.</span></span>

## <span data-ttu-id="38d85-118">參數</span><span class="sxs-lookup"><span data-stu-id="38d85-118">PARAMETERS</span></span>

### <span data-ttu-id="38d85-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="38d85-119">-BatchContext</span></span>
<span data-ttu-id="38d85-120">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="38d85-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="38d85-121">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="38d85-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="38d85-122">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="38d85-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="38d85-123">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="38d85-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="38d85-124">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="38d85-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="38d85-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d85-125">-DefaultProfile</span></span>
<span data-ttu-id="38d85-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38d85-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38d85-127">-識別碼</span><span class="sxs-lookup"><span data-stu-id="38d85-127">-Id</span></span>
<span data-ttu-id="38d85-128">指定此 Cmdlet 停止的任務識別碼。</span><span class="sxs-lookup"><span data-stu-id="38d85-128">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d85-129">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="38d85-129">-JobId</span></span>
<span data-ttu-id="38d85-130">指定包含該任務的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="38d85-130">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d85-131">-任務</span><span class="sxs-lookup"><span data-stu-id="38d85-131">-Task</span></span>
<span data-ttu-id="38d85-132">指定此 Cmdlet 停止的工作。</span><span class="sxs-lookup"><span data-stu-id="38d85-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="38d85-133">若要取得 **PSCloudTask** 物件，請使用 Get-AzureBatchTask Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38d85-133">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38d85-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d85-134">CommonParameters</span></span>
<span data-ttu-id="38d85-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38d85-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d85-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="38d85-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d85-137">輸入</span><span class="sxs-lookup"><span data-stu-id="38d85-137">INPUTS</span></span>

### <span data-ttu-id="38d85-138">System.object</span><span class="sxs-lookup"><span data-stu-id="38d85-138">System.String</span></span>

### <span data-ttu-id="38d85-139">Microsoft.Azure.Commands.Batch。PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="38d85-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="38d85-140">參數： Task (ByValue) </span><span class="sxs-lookup"><span data-stu-id="38d85-140">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="38d85-141">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="38d85-141">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="38d85-142">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="38d85-142">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="38d85-143">輸出</span><span class="sxs-lookup"><span data-stu-id="38d85-143">OUTPUTS</span></span>

### <span data-ttu-id="38d85-144">System.void</span><span class="sxs-lookup"><span data-stu-id="38d85-144">System.Void</span></span>

## <span data-ttu-id="38d85-145">筆記</span><span class="sxs-lookup"><span data-stu-id="38d85-145">NOTES</span></span>

## <span data-ttu-id="38d85-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="38d85-146">RELATED LINKS</span></span>

[<span data-ttu-id="38d85-147">AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="38d85-147">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="38d85-148">新-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="38d85-148">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="38d85-149">移除-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="38d85-149">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="38d85-150">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="38d85-150">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


