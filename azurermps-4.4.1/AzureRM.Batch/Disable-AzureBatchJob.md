---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: 2e19e6b1733ccc3dfe0a802756e2c0a517232803
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626352"
---
# <span data-ttu-id="232ad-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="232ad-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="232ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="232ad-102">SYNOPSIS</span></span>
<span data-ttu-id="232ad-103">停用批次作業。</span><span class="sxs-lookup"><span data-stu-id="232ad-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="232ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="232ad-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="232ad-105">說明</span><span class="sxs-lookup"><span data-stu-id="232ad-105">DESCRIPTION</span></span>
<span data-ttu-id="232ad-106">**Disable AzureBatchJob** Cmdlet 會停用 Azure 批次作業。</span><span class="sxs-lookup"><span data-stu-id="232ad-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="232ad-107">啟用作業之後，就可以執行新的工作。</span><span class="sxs-lookup"><span data-stu-id="232ad-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="232ad-108">[停用的作業] 不會執行新工作。</span><span class="sxs-lookup"><span data-stu-id="232ad-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="232ad-109">您可以稍後啟用停用的作業。</span><span class="sxs-lookup"><span data-stu-id="232ad-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="232ad-110">示例</span><span class="sxs-lookup"><span data-stu-id="232ad-110">EXAMPLES</span></span>

### <span data-ttu-id="232ad-111">範例1：停用批次作業</span><span class="sxs-lookup"><span data-stu-id="232ad-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="232ad-112">這個命令會停用具有識別碼作業的作業-000001。</span><span class="sxs-lookup"><span data-stu-id="232ad-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="232ad-113">此命令會終止作業的作用中工作。</span><span class="sxs-lookup"><span data-stu-id="232ad-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="232ad-114">使用 **AzureRmBatchAccountKeys** Cmdlet，將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="232ad-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="232ad-115">參數</span><span class="sxs-lookup"><span data-stu-id="232ad-115">PARAMETERS</span></span>

### <span data-ttu-id="232ad-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="232ad-116">-BatchContext</span></span>
<span data-ttu-id="232ad-117">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="232ad-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="232ad-118">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="232ad-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="232ad-119">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="232ad-119">-DisableJobOption</span></span>
<span data-ttu-id="232ad-120">指定與此 Cmdlet 所停作業相關聯的作用中工作的處理方式。</span><span class="sxs-lookup"><span data-stu-id="232ad-120">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="232ad-121">有效值為：</span><span class="sxs-lookup"><span data-stu-id="232ad-121">Valid values are:</span></span> 

- <span data-ttu-id="232ad-122">Requeue</span><span class="sxs-lookup"><span data-stu-id="232ad-122">Requeue</span></span> 
- <span data-ttu-id="232ad-123">終結</span><span class="sxs-lookup"><span data-stu-id="232ad-123">Terminate</span></span> 
- <span data-ttu-id="232ad-124">稍</span><span class="sxs-lookup"><span data-stu-id="232ad-124">Wait</span></span>

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

### <span data-ttu-id="232ad-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="232ad-125">-Id</span></span>
<span data-ttu-id="232ad-126">指定此 Cmdlet 停用作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="232ad-126">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="232ad-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="232ad-127">-DefaultProfile</span></span>
<span data-ttu-id="232ad-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="232ad-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="232ad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="232ad-129">CommonParameters</span></span>
<span data-ttu-id="232ad-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="232ad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="232ad-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="232ad-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="232ad-132">輸入</span><span class="sxs-lookup"><span data-stu-id="232ad-132">INPUTS</span></span>

### <span data-ttu-id="232ad-133">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="232ad-133">BatchAccountContext</span></span>
<span data-ttu-id="232ad-134">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="232ad-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="232ad-135">字串</span><span class="sxs-lookup"><span data-stu-id="232ad-135">String</span></span>
<span data-ttu-id="232ad-136">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="232ad-136">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="232ad-137">輸出</span><span class="sxs-lookup"><span data-stu-id="232ad-137">OUTPUTS</span></span>

## <span data-ttu-id="232ad-138">筆記</span><span class="sxs-lookup"><span data-stu-id="232ad-138">NOTES</span></span>

## <span data-ttu-id="232ad-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="232ad-139">RELATED LINKS</span></span>

[<span data-ttu-id="232ad-140">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="232ad-140">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="232ad-141">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="232ad-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="232ad-142">AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="232ad-142">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="232ad-143">新-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="232ad-143">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="232ad-144">移除-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="232ad-144">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="232ad-145">停止 AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="232ad-145">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="232ad-146">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="232ad-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


