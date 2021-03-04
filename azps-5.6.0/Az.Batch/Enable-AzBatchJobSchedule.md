---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 01e34258d7c3e94975032d0e77087b05acf3f264
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904749"
---
# <span data-ttu-id="5506b-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5506b-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="5506b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5506b-102">SYNOPSIS</span></span>
<span data-ttu-id="5506b-103">啟用批次工作排程。</span><span class="sxs-lookup"><span data-stu-id="5506b-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="5506b-104">語法</span><span class="sxs-lookup"><span data-stu-id="5506b-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5506b-105">描述</span><span class="sxs-lookup"><span data-stu-id="5506b-105">DESCRIPTION</span></span>
<span data-ttu-id="5506b-106">**Enable-AzBatchJobSchedule** Cmdlet 可啟用 Azure 批次工作排程。</span><span class="sxs-lookup"><span data-stu-id="5506b-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="5506b-107">啟用工作排程之後，就可以根據該排程建立工作。</span><span class="sxs-lookup"><span data-stu-id="5506b-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="5506b-108">例子</span><span class="sxs-lookup"><span data-stu-id="5506b-108">EXAMPLES</span></span>

### <span data-ttu-id="5506b-109">範例 1：啟用工作排程</span><span class="sxs-lookup"><span data-stu-id="5506b-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="5506b-110">此命令會啟用具有 ID JobSchedule17 的工作排程。</span><span class="sxs-lookup"><span data-stu-id="5506b-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="5506b-111">使用 **Get-AzBatchAccountKey** Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="5506b-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="5506b-112">參數</span><span class="sxs-lookup"><span data-stu-id="5506b-112">PARAMETERS</span></span>

### <span data-ttu-id="5506b-113">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="5506b-113">-BatchContext</span></span>
<span data-ttu-id="5506b-114">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="5506b-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5506b-115">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="5506b-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5506b-116">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="5506b-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5506b-117">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="5506b-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5506b-118">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="5506b-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5506b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5506b-119">-DefaultProfile</span></span>
<span data-ttu-id="5506b-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5506b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5506b-121">-Id</span><span class="sxs-lookup"><span data-stu-id="5506b-121">-Id</span></span>
<span data-ttu-id="5506b-122">指定此 Cmdlet 啟用的工作排程識別碼。</span><span class="sxs-lookup"><span data-stu-id="5506b-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="5506b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5506b-123">CommonParameters</span></span>
<span data-ttu-id="5506b-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5506b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5506b-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5506b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5506b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="5506b-126">INPUTS</span></span>

### <span data-ttu-id="5506b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5506b-127">System.String</span></span>

### <span data-ttu-id="5506b-128">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="5506b-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5506b-129">輸出</span><span class="sxs-lookup"><span data-stu-id="5506b-129">OUTPUTS</span></span>

### <span data-ttu-id="5506b-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="5506b-130">System.Void</span></span>

## <span data-ttu-id="5506b-131">筆記</span><span class="sxs-lookup"><span data-stu-id="5506b-131">NOTES</span></span>

## <span data-ttu-id="5506b-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="5506b-132">RELATED LINKS</span></span>

[<span data-ttu-id="5506b-133">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5506b-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="5506b-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5506b-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5506b-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5506b-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="5506b-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5506b-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="5506b-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5506b-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="5506b-138">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5506b-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="5506b-139">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5506b-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
