---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 673d9e5034b1e7c97d3b6b7cfdd6f89e9a79a34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624216"
---
# <span data-ttu-id="93942-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="93942-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="93942-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93942-102">SYNOPSIS</span></span>
<span data-ttu-id="93942-103">移除批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="93942-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93942-104">句法</span><span class="sxs-lookup"><span data-stu-id="93942-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93942-105">說明</span><span class="sxs-lookup"><span data-stu-id="93942-105">DESCRIPTION</span></span>
<span data-ttu-id="93942-106">**AzureBatchJobSchedule** Cmdlet 會移除 Azure 批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="93942-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="93942-107">示例</span><span class="sxs-lookup"><span data-stu-id="93942-107">EXAMPLES</span></span>

## <span data-ttu-id="93942-108">參數</span><span class="sxs-lookup"><span data-stu-id="93942-108">PARAMETERS</span></span>

### <span data-ttu-id="93942-109">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="93942-109">-BatchContext</span></span>
<span data-ttu-id="93942-110">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="93942-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="93942-111">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93942-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="93942-112">-Force</span><span class="sxs-lookup"><span data-stu-id="93942-112">-Force</span></span>
<span data-ttu-id="93942-113">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="93942-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93942-114">-識別碼</span><span class="sxs-lookup"><span data-stu-id="93942-114">-Id</span></span>
<span data-ttu-id="93942-115">指定要移除之作業排程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="93942-115">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="93942-116">-確認</span><span class="sxs-lookup"><span data-stu-id="93942-116">-Confirm</span></span>
<span data-ttu-id="93942-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="93942-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93942-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93942-118">-WhatIf</span></span>
<span data-ttu-id="93942-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93942-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93942-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93942-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93942-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93942-121">-DefaultProfile</span></span>
<span data-ttu-id="93942-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="93942-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93942-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93942-123">CommonParameters</span></span>
<span data-ttu-id="93942-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93942-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93942-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="93942-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93942-126">輸入</span><span class="sxs-lookup"><span data-stu-id="93942-126">INPUTS</span></span>

### <span data-ttu-id="93942-127">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="93942-127">BatchAccountContext</span></span>
<span data-ttu-id="93942-128">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="93942-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="93942-129">輸出</span><span class="sxs-lookup"><span data-stu-id="93942-129">OUTPUTS</span></span>

## <span data-ttu-id="93942-130">筆記</span><span class="sxs-lookup"><span data-stu-id="93942-130">NOTES</span></span>

## <span data-ttu-id="93942-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="93942-131">RELATED LINKS</span></span>

[<span data-ttu-id="93942-132">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="93942-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="93942-133">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="93942-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="93942-134">AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="93942-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="93942-135">新-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="93942-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="93942-136">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="93942-136">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="93942-137">停止 AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="93942-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


