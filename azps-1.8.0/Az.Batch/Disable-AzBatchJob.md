---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: c560964308fe3bb2195f601f2e4138e022aa41e0
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93623358"
---
# <span data-ttu-id="e4eca-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4eca-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="e4eca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4eca-102">SYNOPSIS</span></span>
<span data-ttu-id="e4eca-103">停用批次作業。</span><span class="sxs-lookup"><span data-stu-id="e4eca-103">Disables a Batch job.</span></span>

## <span data-ttu-id="e4eca-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4eca-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4eca-105">說明</span><span class="sxs-lookup"><span data-stu-id="e4eca-105">DESCRIPTION</span></span>
<span data-ttu-id="e4eca-106">**Disable AzBatchJob** Cmdlet 會停用 Azure 批次作業。</span><span class="sxs-lookup"><span data-stu-id="e4eca-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="e4eca-107">啟用作業之後，就可以執行新的工作。</span><span class="sxs-lookup"><span data-stu-id="e4eca-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="e4eca-108">[停用的作業] 不會執行新工作。</span><span class="sxs-lookup"><span data-stu-id="e4eca-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="e4eca-109">您可以稍後啟用停用的作業。</span><span class="sxs-lookup"><span data-stu-id="e4eca-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="e4eca-110">示例</span><span class="sxs-lookup"><span data-stu-id="e4eca-110">EXAMPLES</span></span>

### <span data-ttu-id="e4eca-111">範例1：停用批次作業</span><span class="sxs-lookup"><span data-stu-id="e4eca-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="e4eca-112">這個命令會停用具有識別碼作業的作業-000001。</span><span class="sxs-lookup"><span data-stu-id="e4eca-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="e4eca-113">此命令會終止作業的作用中工作。</span><span class="sxs-lookup"><span data-stu-id="e4eca-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="e4eca-114">使用 **AzBatchAccountKeys** Cmdlet，將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="e4eca-114">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="e4eca-115">參數</span><span class="sxs-lookup"><span data-stu-id="e4eca-115">PARAMETERS</span></span>

### <span data-ttu-id="e4eca-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="e4eca-116">-BatchContext</span></span>
<span data-ttu-id="e4eca-117">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="e4eca-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e4eca-118">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="e4eca-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e4eca-119">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="e4eca-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e4eca-120">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="e4eca-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e4eca-121">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="e4eca-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e4eca-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4eca-122">-DefaultProfile</span></span>
<span data-ttu-id="e4eca-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e4eca-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4eca-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="e4eca-124">-DisableJobOption</span></span>
<span data-ttu-id="e4eca-125">指定與此 Cmdlet 所停作業相關聯的作用中工作的處理方式。</span><span class="sxs-lookup"><span data-stu-id="e4eca-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="e4eca-126">有效值為：</span><span class="sxs-lookup"><span data-stu-id="e4eca-126">Valid values are:</span></span> 
- <span data-ttu-id="e4eca-127">Requeue</span><span class="sxs-lookup"><span data-stu-id="e4eca-127">Requeue</span></span> 
- <span data-ttu-id="e4eca-128">終結</span><span class="sxs-lookup"><span data-stu-id="e4eca-128">Terminate</span></span> 
- <span data-ttu-id="e4eca-129">稍</span><span class="sxs-lookup"><span data-stu-id="e4eca-129">Wait</span></span>

```yaml
Type: Microsoft.Azure.Batch.Common.DisableJobOption
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4eca-130">-識別碼</span><span class="sxs-lookup"><span data-stu-id="e4eca-130">-Id</span></span>
<span data-ttu-id="e4eca-131">指定此 Cmdlet 停用作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e4eca-131">Specifies the ID of the job that this cmdlet disables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4eca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4eca-132">CommonParameters</span></span>
<span data-ttu-id="e4eca-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4eca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4eca-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4eca-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4eca-135">輸入</span><span class="sxs-lookup"><span data-stu-id="e4eca-135">INPUTS</span></span>

### <span data-ttu-id="e4eca-136">System.object</span><span class="sxs-lookup"><span data-stu-id="e4eca-136">System.String</span></span>

### <span data-ttu-id="e4eca-137">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="e4eca-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e4eca-138">輸出</span><span class="sxs-lookup"><span data-stu-id="e4eca-138">OUTPUTS</span></span>

### <span data-ttu-id="e4eca-139">System.void</span><span class="sxs-lookup"><span data-stu-id="e4eca-139">System.Void</span></span>

## <span data-ttu-id="e4eca-140">筆記</span><span class="sxs-lookup"><span data-stu-id="e4eca-140">NOTES</span></span>

## <span data-ttu-id="e4eca-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4eca-141">RELATED LINKS</span></span>

[<span data-ttu-id="e4eca-142">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4eca-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="e4eca-143">AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e4eca-143">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e4eca-144">AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4eca-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="e4eca-145">新-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4eca-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="e4eca-146">移除-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4eca-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="e4eca-147">停止 AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e4eca-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="e4eca-148">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e4eca-148">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


