---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 545979c621a807c2a866fc5cf1d29aa0b659dc82
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447024"
---
# <span data-ttu-id="17f0a-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="17f0a-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="17f0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="17f0a-103">啟用批次作業。</span><span class="sxs-lookup"><span data-stu-id="17f0a-103">Enables a Batch job.</span></span>

## <span data-ttu-id="17f0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="17f0a-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17f0a-105">說明</span><span class="sxs-lookup"><span data-stu-id="17f0a-105">DESCRIPTION</span></span>
<span data-ttu-id="17f0a-106">**AzBatchJob** Cmdlet 可啟用 Azure Batch 作業。</span><span class="sxs-lookup"><span data-stu-id="17f0a-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="17f0a-107">啟用作業之後，就可以執行新的工作。</span><span class="sxs-lookup"><span data-stu-id="17f0a-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="17f0a-108">示例</span><span class="sxs-lookup"><span data-stu-id="17f0a-108">EXAMPLES</span></span>

### <span data-ttu-id="17f0a-109">範例1：啟用批次作業</span><span class="sxs-lookup"><span data-stu-id="17f0a-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="17f0a-110">這個命令會啟用具有識別碼作業的作業-000001。</span><span class="sxs-lookup"><span data-stu-id="17f0a-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="17f0a-111">使用 Get-AzBatchAccountKey Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="17f0a-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="17f0a-112">參數</span><span class="sxs-lookup"><span data-stu-id="17f0a-112">PARAMETERS</span></span>

### <span data-ttu-id="17f0a-113">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="17f0a-113">-BatchContext</span></span>
<span data-ttu-id="17f0a-114">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="17f0a-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="17f0a-115">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="17f0a-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="17f0a-116">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="17f0a-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="17f0a-117">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="17f0a-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="17f0a-118">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="17f0a-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="17f0a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f0a-119">-DefaultProfile</span></span>
<span data-ttu-id="17f0a-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="17f0a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17f0a-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="17f0a-121">-Id</span></span>
<span data-ttu-id="17f0a-122">指定此 Cmdlet 啟用之作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="17f0a-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="17f0a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f0a-123">CommonParameters</span></span>
<span data-ttu-id="17f0a-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17f0a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f0a-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="17f0a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f0a-126">輸入</span><span class="sxs-lookup"><span data-stu-id="17f0a-126">INPUTS</span></span>

### <span data-ttu-id="17f0a-127">System.object</span><span class="sxs-lookup"><span data-stu-id="17f0a-127">System.String</span></span>

### <span data-ttu-id="17f0a-128">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="17f0a-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="17f0a-129">輸出</span><span class="sxs-lookup"><span data-stu-id="17f0a-129">OUTPUTS</span></span>

### <span data-ttu-id="17f0a-130">System.void</span><span class="sxs-lookup"><span data-stu-id="17f0a-130">System.Void</span></span>

## <span data-ttu-id="17f0a-131">筆記</span><span class="sxs-lookup"><span data-stu-id="17f0a-131">NOTES</span></span>

## <span data-ttu-id="17f0a-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="17f0a-132">RELATED LINKS</span></span>

[<span data-ttu-id="17f0a-133">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="17f0a-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="17f0a-134">AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="17f0a-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="17f0a-135">新-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="17f0a-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="17f0a-136">移除-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="17f0a-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="17f0a-137">停止 AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="17f0a-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="17f0a-138">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="17f0a-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
