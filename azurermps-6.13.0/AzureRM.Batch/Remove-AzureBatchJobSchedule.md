---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 59a906420e2326564e779c9358e07a5003946b28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623764"
---
# <span data-ttu-id="f5fd1-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f5fd1-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="f5fd1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="f5fd1-103">移除批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="f5fd1-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5fd1-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5fd1-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5fd1-105">說明</span><span class="sxs-lookup"><span data-stu-id="f5fd1-105">DESCRIPTION</span></span>
<span data-ttu-id="f5fd1-106">**AzureBatchJobSchedule** Cmdlet 會移除 Azure 批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="f5fd1-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="f5fd1-107">示例</span><span class="sxs-lookup"><span data-stu-id="f5fd1-107">EXAMPLES</span></span>

## <span data-ttu-id="f5fd1-108">參數</span><span class="sxs-lookup"><span data-stu-id="f5fd1-108">PARAMETERS</span></span>

### <span data-ttu-id="f5fd1-109">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="f5fd1-109">-BatchContext</span></span>
<span data-ttu-id="f5fd1-110">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="f5fd1-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f5fd1-111">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="f5fd1-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f5fd1-112">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="f5fd1-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f5fd1-113">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="f5fd1-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f5fd1-114">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="f5fd1-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f5fd1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5fd1-115">-DefaultProfile</span></span>
<span data-ttu-id="f5fd1-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5fd1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5fd1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f5fd1-117">-Force</span></span>
<span data-ttu-id="f5fd1-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f5fd1-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fd1-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="f5fd1-119">-Id</span></span>
<span data-ttu-id="f5fd1-120">指定要移除之作業排程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f5fd1-120">Specifies the ID of the job schedule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5fd1-121">-確認</span><span class="sxs-lookup"><span data-stu-id="f5fd1-121">-Confirm</span></span>
<span data-ttu-id="f5fd1-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f5fd1-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fd1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5fd1-123">-WhatIf</span></span>
<span data-ttu-id="f5fd1-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f5fd1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5fd1-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5fd1-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fd1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5fd1-126">CommonParameters</span></span>
<span data-ttu-id="f5fd1-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5fd1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5fd1-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f5fd1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5fd1-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f5fd1-129">INPUTS</span></span>

### <span data-ttu-id="f5fd1-130">System.object</span><span class="sxs-lookup"><span data-stu-id="f5fd1-130">System.String</span></span>

### <span data-ttu-id="f5fd1-131">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="f5fd1-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="f5fd1-132">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="f5fd1-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="f5fd1-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f5fd1-133">OUTPUTS</span></span>

### <span data-ttu-id="f5fd1-134">System.void</span><span class="sxs-lookup"><span data-stu-id="f5fd1-134">System.Void</span></span>

## <span data-ttu-id="f5fd1-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f5fd1-135">NOTES</span></span>

## <span data-ttu-id="f5fd1-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5fd1-136">RELATED LINKS</span></span>

[<span data-ttu-id="f5fd1-137">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f5fd1-137">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="f5fd1-138">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f5fd1-138">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="f5fd1-139">AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f5fd1-139">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="f5fd1-140">新-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f5fd1-140">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="f5fd1-141">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f5fd1-141">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="f5fd1-142">停止 AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f5fd1-142">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


