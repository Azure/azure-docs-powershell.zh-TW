---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: ac63bbdb95551ff5ff08661a92f0924d5853ade5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451748"
---
# <span data-ttu-id="92f7f-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="92f7f-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="92f7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="92f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="92f7f-103">停止批次任務。</span><span class="sxs-lookup"><span data-stu-id="92f7f-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92f7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="92f7f-104">SYNTAX</span></span>

### <span data-ttu-id="92f7f-105">標識號</span><span class="sxs-lookup"><span data-stu-id="92f7f-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92f7f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="92f7f-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92f7f-107">說明</span><span class="sxs-lookup"><span data-stu-id="92f7f-107">DESCRIPTION</span></span>
<span data-ttu-id="92f7f-108">**AzureBatchTask** Cmdlet 會停止 Azure Batch 工作。</span><span class="sxs-lookup"><span data-stu-id="92f7f-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="92f7f-109">示例</span><span class="sxs-lookup"><span data-stu-id="92f7f-109">EXAMPLES</span></span>

### <span data-ttu-id="92f7f-110">範例1：依識別碼刪除批次任務</span><span class="sxs-lookup"><span data-stu-id="92f7f-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="92f7f-111">這個命令會停止在具有 ID 作業的作業下具有識別碼 Task23 的工作-000001。</span><span class="sxs-lookup"><span data-stu-id="92f7f-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="92f7f-112">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="92f7f-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="92f7f-113">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="92f7f-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="92f7f-114">範例2：使用管線停止批次工作</span><span class="sxs-lookup"><span data-stu-id="92f7f-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="92f7f-115">這個命令會透過使用 Get-AzureBatchTask Cmdlet 來取得作業中具有 id 作業000001之識別碼 Task26 的批次任務。</span><span class="sxs-lookup"><span data-stu-id="92f7f-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="92f7f-116">透過使用管線運算子，命令會將該工作傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92f7f-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="92f7f-117">命令會停止該任務。</span><span class="sxs-lookup"><span data-stu-id="92f7f-117">The command stops that task.</span></span>

## <span data-ttu-id="92f7f-118">參數</span><span class="sxs-lookup"><span data-stu-id="92f7f-118">PARAMETERS</span></span>

### <span data-ttu-id="92f7f-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="92f7f-119">-BatchContext</span></span>
<span data-ttu-id="92f7f-120">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="92f7f-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="92f7f-121">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92f7f-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="92f7f-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="92f7f-122">-Id</span></span>
<span data-ttu-id="92f7f-123">指定此 Cmdlet 停止的任務識別碼。</span><span class="sxs-lookup"><span data-stu-id="92f7f-123">Specifies the ID of the task that this cmdlet stops.</span></span>

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

### <span data-ttu-id="92f7f-124">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="92f7f-124">-JobId</span></span>
<span data-ttu-id="92f7f-125">指定包含該任務的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="92f7f-125">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="92f7f-126">-任務</span><span class="sxs-lookup"><span data-stu-id="92f7f-126">-Task</span></span>
<span data-ttu-id="92f7f-127">指定此 Cmdlet 停止的工作。</span><span class="sxs-lookup"><span data-stu-id="92f7f-127">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="92f7f-128">若要取得 **PSCloudTask** 物件，請使用 Get-AzureBatchTask Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92f7f-128">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="92f7f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f7f-129">-DefaultProfile</span></span>
<span data-ttu-id="92f7f-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="92f7f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92f7f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f7f-131">CommonParameters</span></span>
<span data-ttu-id="92f7f-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="92f7f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f7f-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="92f7f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f7f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="92f7f-134">INPUTS</span></span>

### <span data-ttu-id="92f7f-135">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="92f7f-135">BatchAccountContext</span></span>
<span data-ttu-id="92f7f-136">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="92f7f-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="92f7f-137">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="92f7f-137">PSCloudTask</span></span>
<span data-ttu-id="92f7f-138">形參 "Task" 接受管線中 "PSCloudTask" 類型的值</span><span class="sxs-lookup"><span data-stu-id="92f7f-138">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="92f7f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="92f7f-139">OUTPUTS</span></span>

## <span data-ttu-id="92f7f-140">筆記</span><span class="sxs-lookup"><span data-stu-id="92f7f-140">NOTES</span></span>

## <span data-ttu-id="92f7f-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="92f7f-141">RELATED LINKS</span></span>

[<span data-ttu-id="92f7f-142">AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="92f7f-142">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="92f7f-143">新-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="92f7f-143">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="92f7f-144">移除-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="92f7f-144">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="92f7f-145">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="92f7f-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


