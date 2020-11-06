---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 2e474462983f15c0d58f8ada60b907c100508c6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448779"
---
# <span data-ttu-id="8ab88-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8ab88-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="8ab88-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ab88-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab88-103">移除批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="8ab88-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ab88-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ab88-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ab88-105">說明</span><span class="sxs-lookup"><span data-stu-id="8ab88-105">DESCRIPTION</span></span>
<span data-ttu-id="8ab88-106">**AzureBatchJobSchedule** Cmdlet 會移除 Azure 批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="8ab88-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="8ab88-107">示例</span><span class="sxs-lookup"><span data-stu-id="8ab88-107">EXAMPLES</span></span>

## <span data-ttu-id="8ab88-108">參數</span><span class="sxs-lookup"><span data-stu-id="8ab88-108">PARAMETERS</span></span>

### <span data-ttu-id="8ab88-109">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="8ab88-109">-BatchContext</span></span>
<span data-ttu-id="8ab88-110">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="8ab88-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8ab88-111">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="8ab88-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8ab88-112">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="8ab88-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8ab88-113">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="8ab88-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8ab88-114">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="8ab88-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8ab88-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab88-115">-DefaultProfile</span></span>
<span data-ttu-id="8ab88-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ab88-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ab88-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8ab88-117">-Force</span></span>
<span data-ttu-id="8ab88-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="8ab88-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab88-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="8ab88-119">-Id</span></span>
<span data-ttu-id="8ab88-120">指定要移除之作業排程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ab88-120">Specifies the ID of the job schedule to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab88-121">-確認</span><span class="sxs-lookup"><span data-stu-id="8ab88-121">-Confirm</span></span>
<span data-ttu-id="8ab88-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8ab88-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab88-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ab88-123">-WhatIf</span></span>
<span data-ttu-id="8ab88-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8ab88-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ab88-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ab88-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab88-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab88-126">CommonParameters</span></span>
<span data-ttu-id="8ab88-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ab88-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab88-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8ab88-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab88-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8ab88-129">INPUTS</span></span>

### <span data-ttu-id="8ab88-130">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="8ab88-130">BatchAccountContext</span></span>
<span data-ttu-id="8ab88-131">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="8ab88-131">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="8ab88-132">輸出</span><span class="sxs-lookup"><span data-stu-id="8ab88-132">OUTPUTS</span></span>

## <span data-ttu-id="8ab88-133">筆記</span><span class="sxs-lookup"><span data-stu-id="8ab88-133">NOTES</span></span>

## <span data-ttu-id="8ab88-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ab88-134">RELATED LINKS</span></span>

[<span data-ttu-id="8ab88-135">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8ab88-135">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="8ab88-136">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8ab88-136">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="8ab88-137">AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8ab88-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="8ab88-138">新-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8ab88-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="8ab88-139">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8ab88-139">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="8ab88-140">停止 AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8ab88-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


