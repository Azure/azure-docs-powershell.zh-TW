---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 1470f02570462a3a7bb922c88504e3c8a20eb8fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906813"
---
# <span data-ttu-id="04007-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="04007-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="04007-102">簡介</span><span class="sxs-lookup"><span data-stu-id="04007-102">SYNOPSIS</span></span>
<span data-ttu-id="04007-103">啟用批次工作。</span><span class="sxs-lookup"><span data-stu-id="04007-103">Enables a Batch job.</span></span>

## <span data-ttu-id="04007-104">語法</span><span class="sxs-lookup"><span data-stu-id="04007-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04007-105">描述</span><span class="sxs-lookup"><span data-stu-id="04007-105">DESCRIPTION</span></span>
<span data-ttu-id="04007-106">**Enable-AzBatchJob** Cmdlet 可啟用 Azure Batch 工作。</span><span class="sxs-lookup"><span data-stu-id="04007-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="04007-107">啟用工作之後，就可以執行新的工作。</span><span class="sxs-lookup"><span data-stu-id="04007-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="04007-108">例子</span><span class="sxs-lookup"><span data-stu-id="04007-108">EXAMPLES</span></span>

### <span data-ttu-id="04007-109">範例 1：啟用批次處理工作</span><span class="sxs-lookup"><span data-stu-id="04007-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="04007-110">此命令會啟用具有識別碼 Job-000001 的工作。</span><span class="sxs-lookup"><span data-stu-id="04007-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="04007-111">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="04007-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="04007-112">參數</span><span class="sxs-lookup"><span data-stu-id="04007-112">PARAMETERS</span></span>

### <span data-ttu-id="04007-113">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="04007-113">-BatchContext</span></span>
<span data-ttu-id="04007-114">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="04007-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="04007-115">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="04007-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="04007-116">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="04007-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="04007-117">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="04007-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="04007-118">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="04007-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="04007-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04007-119">-DefaultProfile</span></span>
<span data-ttu-id="04007-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="04007-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04007-121">-Id</span><span class="sxs-lookup"><span data-stu-id="04007-121">-Id</span></span>
<span data-ttu-id="04007-122">指定此 Cmdlet 啟用的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="04007-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="04007-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04007-123">CommonParameters</span></span>
<span data-ttu-id="04007-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="04007-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04007-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04007-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04007-126">輸入</span><span class="sxs-lookup"><span data-stu-id="04007-126">INPUTS</span></span>

### <span data-ttu-id="04007-127">System.String</span><span class="sxs-lookup"><span data-stu-id="04007-127">System.String</span></span>

### <span data-ttu-id="04007-128">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="04007-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="04007-129">輸出</span><span class="sxs-lookup"><span data-stu-id="04007-129">OUTPUTS</span></span>

### <span data-ttu-id="04007-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="04007-130">System.Void</span></span>

## <span data-ttu-id="04007-131">筆記</span><span class="sxs-lookup"><span data-stu-id="04007-131">NOTES</span></span>

## <span data-ttu-id="04007-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="04007-132">RELATED LINKS</span></span>

[<span data-ttu-id="04007-133">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="04007-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="04007-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="04007-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="04007-135">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="04007-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="04007-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="04007-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="04007-137">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="04007-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="04007-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="04007-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
