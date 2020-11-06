---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: 73d80d3547ea895e5cbd35b2d514d9a757164bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456919"
---
# <span data-ttu-id="ee371-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ee371-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="ee371-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ee371-102">SYNOPSIS</span></span>
<span data-ttu-id="ee371-103">停用批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="ee371-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee371-104">句法</span><span class="sxs-lookup"><span data-stu-id="ee371-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee371-105">說明</span><span class="sxs-lookup"><span data-stu-id="ee371-105">DESCRIPTION</span></span>
<span data-ttu-id="ee371-106">**Disable AzureBatchJobSchedule** Cmdlet 會停用 Azure 批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="ee371-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="ee371-107">如果您停用排程，就不會根據該排程建立工作。</span><span class="sxs-lookup"><span data-stu-id="ee371-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="ee371-108">您可以稍後啟用停用的時程表。</span><span class="sxs-lookup"><span data-stu-id="ee371-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="ee371-109">示例</span><span class="sxs-lookup"><span data-stu-id="ee371-109">EXAMPLES</span></span>

### <span data-ttu-id="ee371-110">範例1：停用作業排程</span><span class="sxs-lookup"><span data-stu-id="ee371-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="ee371-111">這個命令會停用 ID 為 JobSchedule17 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="ee371-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="ee371-112">使用 **AzureRmBatchAccountKeys** Cmdlet，將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="ee371-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="ee371-113">參數</span><span class="sxs-lookup"><span data-stu-id="ee371-113">PARAMETERS</span></span>

### <span data-ttu-id="ee371-114">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="ee371-114">-BatchContext</span></span>
<span data-ttu-id="ee371-115">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="ee371-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ee371-116">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee371-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="ee371-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="ee371-117">-Id</span></span>
<span data-ttu-id="ee371-118">指定此 Cmdlet 停用之作業排程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee371-118">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="ee371-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee371-119">-DefaultProfile</span></span>
<span data-ttu-id="ee371-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee371-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee371-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee371-121">CommonParameters</span></span>
<span data-ttu-id="ee371-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ee371-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee371-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ee371-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee371-124">輸入</span><span class="sxs-lookup"><span data-stu-id="ee371-124">INPUTS</span></span>

### <span data-ttu-id="ee371-125">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="ee371-125">BatchAccountContext</span></span>
<span data-ttu-id="ee371-126">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ee371-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ee371-127">字串</span><span class="sxs-lookup"><span data-stu-id="ee371-127">String</span></span>
<span data-ttu-id="ee371-128">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="ee371-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ee371-129">輸出</span><span class="sxs-lookup"><span data-stu-id="ee371-129">OUTPUTS</span></span>

## <span data-ttu-id="ee371-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ee371-130">NOTES</span></span>

## <span data-ttu-id="ee371-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee371-131">RELATED LINKS</span></span>

[<span data-ttu-id="ee371-132">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ee371-132">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="ee371-133">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ee371-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ee371-134">AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ee371-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="ee371-135">新-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ee371-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="ee371-136">移除-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ee371-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="ee371-137">停止 AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ee371-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="ee371-138">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ee371-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


