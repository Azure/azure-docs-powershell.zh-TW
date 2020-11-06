---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: 979c136f1bdbd216cebe367060ebdc5d8360ea24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446479"
---
# <span data-ttu-id="007de-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="007de-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="007de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="007de-102">SYNOPSIS</span></span>
<span data-ttu-id="007de-103">停止批次任務。</span><span class="sxs-lookup"><span data-stu-id="007de-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="007de-104">句法</span><span class="sxs-lookup"><span data-stu-id="007de-104">SYNTAX</span></span>

### <span data-ttu-id="007de-105">標識號</span><span class="sxs-lookup"><span data-stu-id="007de-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="007de-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="007de-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="007de-107">說明</span><span class="sxs-lookup"><span data-stu-id="007de-107">DESCRIPTION</span></span>
<span data-ttu-id="007de-108">**AzureBatchTask** Cmdlet 會停止 Azure Batch 工作。</span><span class="sxs-lookup"><span data-stu-id="007de-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="007de-109">示例</span><span class="sxs-lookup"><span data-stu-id="007de-109">EXAMPLES</span></span>

### <span data-ttu-id="007de-110">範例1：依識別碼刪除批次任務</span><span class="sxs-lookup"><span data-stu-id="007de-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="007de-111">這個命令會停止在具有 ID 作業的作業下具有識別碼 Task23 的工作-000001。</span><span class="sxs-lookup"><span data-stu-id="007de-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="007de-112">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="007de-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="007de-113">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="007de-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="007de-114">範例2：使用管線停止批次工作</span><span class="sxs-lookup"><span data-stu-id="007de-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="007de-115">這個命令會透過使用 Get-AzureBatchTask Cmdlet 來取得作業中具有 id 作業000001之識別碼 Task26 的批次任務。</span><span class="sxs-lookup"><span data-stu-id="007de-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="007de-116">透過使用管線運算子，命令會將該工作傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="007de-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="007de-117">命令會停止該任務。</span><span class="sxs-lookup"><span data-stu-id="007de-117">The command stops that task.</span></span>

## <span data-ttu-id="007de-118">參數</span><span class="sxs-lookup"><span data-stu-id="007de-118">PARAMETERS</span></span>

### <span data-ttu-id="007de-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="007de-119">-BatchContext</span></span>
<span data-ttu-id="007de-120">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="007de-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="007de-121">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="007de-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="007de-122">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="007de-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="007de-123">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="007de-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="007de-124">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="007de-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="007de-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="007de-125">-DefaultProfile</span></span>
<span data-ttu-id="007de-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="007de-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="007de-127">-識別碼</span><span class="sxs-lookup"><span data-stu-id="007de-127">-Id</span></span>
<span data-ttu-id="007de-128">指定此 Cmdlet 停止的任務識別碼。</span><span class="sxs-lookup"><span data-stu-id="007de-128">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="007de-129">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="007de-129">-JobId</span></span>
<span data-ttu-id="007de-130">指定包含該任務的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="007de-130">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="007de-131">-任務</span><span class="sxs-lookup"><span data-stu-id="007de-131">-Task</span></span>
<span data-ttu-id="007de-132">指定此 Cmdlet 停止的工作。</span><span class="sxs-lookup"><span data-stu-id="007de-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="007de-133">若要取得 **PSCloudTask** 物件，請使用 Get-AzureBatchTask Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="007de-133">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="007de-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="007de-134">CommonParameters</span></span>
<span data-ttu-id="007de-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="007de-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="007de-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="007de-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="007de-137">輸入</span><span class="sxs-lookup"><span data-stu-id="007de-137">INPUTS</span></span>

### <span data-ttu-id="007de-138">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="007de-138">BatchAccountContext</span></span>
<span data-ttu-id="007de-139">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="007de-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="007de-140">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="007de-140">PSCloudTask</span></span>
<span data-ttu-id="007de-141">形參 "Task" 接受管線中 "PSCloudTask" 類型的值</span><span class="sxs-lookup"><span data-stu-id="007de-141">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="007de-142">輸出</span><span class="sxs-lookup"><span data-stu-id="007de-142">OUTPUTS</span></span>

## <span data-ttu-id="007de-143">筆記</span><span class="sxs-lookup"><span data-stu-id="007de-143">NOTES</span></span>

## <span data-ttu-id="007de-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="007de-144">RELATED LINKS</span></span>

[<span data-ttu-id="007de-145">AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="007de-145">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="007de-146">新-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="007de-146">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="007de-147">移除-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="007de-147">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="007de-148">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="007de-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


