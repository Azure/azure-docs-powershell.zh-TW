---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 5550603bc4204937e8568b50b739ef8b8fadba14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903874"
---
# <span data-ttu-id="3ebb5-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3ebb5-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="3ebb5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3ebb5-102">SYNOPSIS</span></span>
<span data-ttu-id="3ebb5-103">停止批次處理工作。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-103">Stops a Batch task.</span></span>

## <span data-ttu-id="3ebb5-104">語法</span><span class="sxs-lookup"><span data-stu-id="3ebb5-104">SYNTAX</span></span>

### <span data-ttu-id="3ebb5-105">Id</span><span class="sxs-lookup"><span data-stu-id="3ebb5-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ebb5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3ebb5-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ebb5-107">描述</span><span class="sxs-lookup"><span data-stu-id="3ebb5-107">DESCRIPTION</span></span>
<span data-ttu-id="3ebb5-108">**Stop-AzBatchTask** Cmdlet 會停止 Azure 批次處理工作。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="3ebb5-109">例子</span><span class="sxs-lookup"><span data-stu-id="3ebb5-109">EXAMPLES</span></span>

### <span data-ttu-id="3ebb5-110">範例 1：刪除批次工作</span><span class="sxs-lookup"><span data-stu-id="3ebb5-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="3ebb5-111">此命令會停止在具有識別碼 Job-000001 的工作下具有識別碼工作 23 的工作。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="3ebb5-112">命令會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="3ebb5-113">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="3ebb5-114">範例 2：使用管線停止批次處理工作</span><span class="sxs-lookup"><span data-stu-id="3ebb5-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="3ebb5-115">此命令會使用識別碼 Job-000001，在具有識別碼 Job-000001 的Get-AzBatchTask工作。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="3ebb5-116">該命令會使用管線運算子，將工作傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3ebb5-117">命令會停止該工作。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-117">The command stops that task.</span></span>

## <span data-ttu-id="3ebb5-118">參數</span><span class="sxs-lookup"><span data-stu-id="3ebb5-118">PARAMETERS</span></span>

### <span data-ttu-id="3ebb5-119">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="3ebb5-119">-BatchContext</span></span>
<span data-ttu-id="3ebb5-120">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3ebb5-121">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3ebb5-122">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3ebb5-123">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3ebb5-124">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3ebb5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ebb5-125">-DefaultProfile</span></span>
<span data-ttu-id="3ebb5-126">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ebb5-127">-Id</span><span class="sxs-lookup"><span data-stu-id="3ebb5-127">-Id</span></span>
<span data-ttu-id="3ebb5-128">指定此 Cmdlet 停止的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-128">Specifies the ID of the task that this cmdlet stops.</span></span>

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

### <span data-ttu-id="3ebb5-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="3ebb5-129">-JobId</span></span>
<span data-ttu-id="3ebb5-130">指定包含該工作的工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-130">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="3ebb5-131">-工作</span><span class="sxs-lookup"><span data-stu-id="3ebb5-131">-Task</span></span>
<span data-ttu-id="3ebb5-132">指定此 Cmdlet 停止的工作。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="3ebb5-133">若要取得 **PSCloudTask** 物件，請使用 Get-AzBatchTask Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="3ebb5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ebb5-134">CommonParameters</span></span>
<span data-ttu-id="3ebb5-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3ebb5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ebb5-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ebb5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ebb5-137">輸入</span><span class="sxs-lookup"><span data-stu-id="3ebb5-137">INPUTS</span></span>

### <span data-ttu-id="3ebb5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3ebb5-138">System.String</span></span>

### <span data-ttu-id="3ebb5-139">Microsoft.Azure.Commands.Batch。Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="3ebb5-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="3ebb5-140">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="3ebb5-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3ebb5-141">輸出</span><span class="sxs-lookup"><span data-stu-id="3ebb5-141">OUTPUTS</span></span>

### <span data-ttu-id="3ebb5-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="3ebb5-142">System.Void</span></span>

## <span data-ttu-id="3ebb5-143">筆記</span><span class="sxs-lookup"><span data-stu-id="3ebb5-143">NOTES</span></span>

## <span data-ttu-id="3ebb5-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ebb5-144">RELATED LINKS</span></span>

[<span data-ttu-id="3ebb5-145">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3ebb5-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="3ebb5-146">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3ebb5-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="3ebb5-147">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3ebb5-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="3ebb5-148">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3ebb5-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
