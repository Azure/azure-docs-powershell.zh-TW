---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 7d1b3b05f3432a5fc512c7dff03eb51c4223701d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93968676"
---
# <span data-ttu-id="af315-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="af315-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="af315-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af315-102">SYNOPSIS</span></span>
<span data-ttu-id="af315-103">停止批次任務。</span><span class="sxs-lookup"><span data-stu-id="af315-103">Stops a Batch task.</span></span>

## <span data-ttu-id="af315-104">句法</span><span class="sxs-lookup"><span data-stu-id="af315-104">SYNTAX</span></span>

### <span data-ttu-id="af315-105">標識號</span><span class="sxs-lookup"><span data-stu-id="af315-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af315-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="af315-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af315-107">說明</span><span class="sxs-lookup"><span data-stu-id="af315-107">DESCRIPTION</span></span>
<span data-ttu-id="af315-108">**AzBatchTask** Cmdlet 會停止 Azure Batch 工作。</span><span class="sxs-lookup"><span data-stu-id="af315-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="af315-109">示例</span><span class="sxs-lookup"><span data-stu-id="af315-109">EXAMPLES</span></span>

### <span data-ttu-id="af315-110">範例1：依識別碼刪除批次任務</span><span class="sxs-lookup"><span data-stu-id="af315-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="af315-111">這個命令會停止在具有 ID 作業的作業下具有識別碼 Task23 的工作-000001。</span><span class="sxs-lookup"><span data-stu-id="af315-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="af315-112">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="af315-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="af315-113">使用 Get-AzBatchAccountKey Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="af315-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="af315-114">範例2：使用管線停止批次工作</span><span class="sxs-lookup"><span data-stu-id="af315-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="af315-115">這個命令會透過使用 Get-AzBatchTask Cmdlet 來取得作業中具有 id 作業000001之識別碼 Task26 的批次任務。</span><span class="sxs-lookup"><span data-stu-id="af315-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="af315-116">透過使用管線運算子，命令會將該工作傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af315-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="af315-117">命令會停止該任務。</span><span class="sxs-lookup"><span data-stu-id="af315-117">The command stops that task.</span></span>

## <span data-ttu-id="af315-118">參數</span><span class="sxs-lookup"><span data-stu-id="af315-118">PARAMETERS</span></span>

### <span data-ttu-id="af315-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="af315-119">-BatchContext</span></span>
<span data-ttu-id="af315-120">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="af315-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="af315-121">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="af315-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="af315-122">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="af315-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="af315-123">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="af315-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="af315-124">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="af315-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="af315-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af315-125">-DefaultProfile</span></span>
<span data-ttu-id="af315-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="af315-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af315-127">-識別碼</span><span class="sxs-lookup"><span data-stu-id="af315-127">-Id</span></span>
<span data-ttu-id="af315-128">指定此 Cmdlet 停止的任務識別碼。</span><span class="sxs-lookup"><span data-stu-id="af315-128">Specifies the ID of the task that this cmdlet stops.</span></span>

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

### <span data-ttu-id="af315-129">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="af315-129">-JobId</span></span>
<span data-ttu-id="af315-130">指定包含該任務的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="af315-130">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="af315-131">-任務</span><span class="sxs-lookup"><span data-stu-id="af315-131">-Task</span></span>
<span data-ttu-id="af315-132">指定此 Cmdlet 停止的工作。</span><span class="sxs-lookup"><span data-stu-id="af315-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="af315-133">若要取得 **PSCloudTask** 物件，請使用 Get-AzBatchTask Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af315-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="af315-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af315-134">CommonParameters</span></span>
<span data-ttu-id="af315-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af315-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af315-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="af315-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af315-137">輸入</span><span class="sxs-lookup"><span data-stu-id="af315-137">INPUTS</span></span>

### <span data-ttu-id="af315-138">System.object</span><span class="sxs-lookup"><span data-stu-id="af315-138">System.String</span></span>

### <span data-ttu-id="af315-139">Microsoft.Azure.Commands.Batch。PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="af315-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="af315-140">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="af315-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="af315-141">輸出</span><span class="sxs-lookup"><span data-stu-id="af315-141">OUTPUTS</span></span>

### <span data-ttu-id="af315-142">System.void</span><span class="sxs-lookup"><span data-stu-id="af315-142">System.Void</span></span>

## <span data-ttu-id="af315-143">筆記</span><span class="sxs-lookup"><span data-stu-id="af315-143">NOTES</span></span>

## <span data-ttu-id="af315-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="af315-144">RELATED LINKS</span></span>

[<span data-ttu-id="af315-145">AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="af315-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="af315-146">新-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="af315-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="af315-147">移除-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="af315-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="af315-148">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="af315-148">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


