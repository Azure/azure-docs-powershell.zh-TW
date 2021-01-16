---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: f874432bc26ae2a579a54e4068c719b236ad4c45
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447047"
---
# <span data-ttu-id="9fe30-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9fe30-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="9fe30-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9fe30-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe30-103">停用批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="9fe30-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="9fe30-104">句法</span><span class="sxs-lookup"><span data-stu-id="9fe30-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fe30-105">說明</span><span class="sxs-lookup"><span data-stu-id="9fe30-105">DESCRIPTION</span></span>
<span data-ttu-id="9fe30-106">**Disable AzBatchJobSchedule** Cmdlet 會停用 Azure 批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="9fe30-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="9fe30-107">如果您停用排程，就不會根據該排程建立工作。</span><span class="sxs-lookup"><span data-stu-id="9fe30-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="9fe30-108">您可以稍後啟用停用的時程表。</span><span class="sxs-lookup"><span data-stu-id="9fe30-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="9fe30-109">示例</span><span class="sxs-lookup"><span data-stu-id="9fe30-109">EXAMPLES</span></span>

### <span data-ttu-id="9fe30-110">範例1：停用作業排程</span><span class="sxs-lookup"><span data-stu-id="9fe30-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="9fe30-111">這個命令會停用 ID 為 JobSchedule17 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="9fe30-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="9fe30-112">使用 **AzBatchAccountKey** Cmdlet，將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="9fe30-112">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="9fe30-113">參數</span><span class="sxs-lookup"><span data-stu-id="9fe30-113">PARAMETERS</span></span>

### <span data-ttu-id="9fe30-114">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="9fe30-114">-BatchContext</span></span>
<span data-ttu-id="9fe30-115">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="9fe30-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9fe30-116">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="9fe30-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9fe30-117">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="9fe30-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9fe30-118">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="9fe30-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9fe30-119">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="9fe30-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9fe30-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe30-120">-DefaultProfile</span></span>
<span data-ttu-id="9fe30-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9fe30-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fe30-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="9fe30-122">-Id</span></span>
<span data-ttu-id="9fe30-123">指定此 Cmdlet 停用之作業排程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9fe30-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="9fe30-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe30-124">CommonParameters</span></span>
<span data-ttu-id="9fe30-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9fe30-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe30-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9fe30-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe30-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9fe30-127">INPUTS</span></span>

### <span data-ttu-id="9fe30-128">System.object</span><span class="sxs-lookup"><span data-stu-id="9fe30-128">System.String</span></span>

### <span data-ttu-id="9fe30-129">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="9fe30-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9fe30-130">輸出</span><span class="sxs-lookup"><span data-stu-id="9fe30-130">OUTPUTS</span></span>

### <span data-ttu-id="9fe30-131">System.void</span><span class="sxs-lookup"><span data-stu-id="9fe30-131">System.Void</span></span>

## <span data-ttu-id="9fe30-132">筆記</span><span class="sxs-lookup"><span data-stu-id="9fe30-132">NOTES</span></span>

## <span data-ttu-id="9fe30-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="9fe30-133">RELATED LINKS</span></span>

[<span data-ttu-id="9fe30-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9fe30-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="9fe30-135">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9fe30-135">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9fe30-136">AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9fe30-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="9fe30-137">新-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9fe30-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="9fe30-138">移除-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9fe30-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="9fe30-139">停止 AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9fe30-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="9fe30-140">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9fe30-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
