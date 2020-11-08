---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 03decd5b1d32defb25692220c63ffe768445697e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137714"
---
# <span data-ttu-id="f7f44-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7f44-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="f7f44-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7f44-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f44-103">啟用批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="f7f44-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="f7f44-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7f44-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7f44-105">說明</span><span class="sxs-lookup"><span data-stu-id="f7f44-105">DESCRIPTION</span></span>
<span data-ttu-id="f7f44-106">**Enable-AzBatchJobSchedule** Cmdlet 可啟用 Azure 批次作業排程。</span><span class="sxs-lookup"><span data-stu-id="f7f44-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="f7f44-107">啟用作業排程後，就可以根據該排程來建立工作。</span><span class="sxs-lookup"><span data-stu-id="f7f44-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="f7f44-108">示例</span><span class="sxs-lookup"><span data-stu-id="f7f44-108">EXAMPLES</span></span>

### <span data-ttu-id="f7f44-109">範例1：啟用作業排程</span><span class="sxs-lookup"><span data-stu-id="f7f44-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="f7f44-110">這個命令會啟用 ID 為 JobSchedule17 的作業排程。</span><span class="sxs-lookup"><span data-stu-id="f7f44-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="f7f44-111">使用 **AzBatchAccountKey** Cmdlet，將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="f7f44-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="f7f44-112">參數</span><span class="sxs-lookup"><span data-stu-id="f7f44-112">PARAMETERS</span></span>

### <span data-ttu-id="f7f44-113">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="f7f44-113">-BatchContext</span></span>
<span data-ttu-id="f7f44-114">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="f7f44-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f7f44-115">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="f7f44-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f7f44-116">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="f7f44-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f7f44-117">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="f7f44-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f7f44-118">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="f7f44-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f7f44-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f44-119">-DefaultProfile</span></span>
<span data-ttu-id="f7f44-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7f44-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7f44-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="f7f44-121">-Id</span></span>
<span data-ttu-id="f7f44-122">指定此 Cmdlet 啟用之作業排程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f7f44-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="f7f44-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f44-123">CommonParameters</span></span>
<span data-ttu-id="f7f44-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7f44-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f44-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f7f44-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f44-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f7f44-126">INPUTS</span></span>

### <span data-ttu-id="f7f44-127">System.object</span><span class="sxs-lookup"><span data-stu-id="f7f44-127">System.String</span></span>

### <span data-ttu-id="f7f44-128">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="f7f44-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f7f44-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f7f44-129">OUTPUTS</span></span>

### <span data-ttu-id="f7f44-130">System.void</span><span class="sxs-lookup"><span data-stu-id="f7f44-130">System.Void</span></span>

## <span data-ttu-id="f7f44-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f7f44-131">NOTES</span></span>

## <span data-ttu-id="f7f44-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7f44-132">RELATED LINKS</span></span>

[<span data-ttu-id="f7f44-133">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7f44-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="f7f44-134">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f7f44-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f7f44-135">AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7f44-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="f7f44-136">新-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7f44-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="f7f44-137">移除-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7f44-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="f7f44-138">停止 AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7f44-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="f7f44-139">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f7f44-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
