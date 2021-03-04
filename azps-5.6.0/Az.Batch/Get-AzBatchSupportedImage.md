---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: e5d177776e288a855c35def8d45310a6f6849c27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911757"
---
# <span data-ttu-id="e6d22-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="e6d22-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="e6d22-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e6d22-102">SYNOPSIS</span></span>
<span data-ttu-id="e6d22-103">為批次帳戶獲得批次支援的圖像。</span><span class="sxs-lookup"><span data-stu-id="e6d22-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="e6d22-104">語法</span><span class="sxs-lookup"><span data-stu-id="e6d22-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6d22-105">描述</span><span class="sxs-lookup"><span data-stu-id="e6d22-105">DESCRIPTION</span></span>
<span data-ttu-id="e6d22-106">**Get-AzBatchSupportedImdlet** 取得 Azure Batch 帳戶中可用的支援虛擬機器圖像。</span><span class="sxs-lookup"><span data-stu-id="e6d22-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="e6d22-107">使用 *BatchCoNtext* 參數指定帳戶。</span><span class="sxs-lookup"><span data-stu-id="e6d22-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="e6d22-108">例子</span><span class="sxs-lookup"><span data-stu-id="e6d22-108">EXAMPLES</span></span>

### <span data-ttu-id="e6d22-109">範例 1：取得所有可用的支援影像</span><span class="sxs-lookup"><span data-stu-id="e6d22-109">Example 1: Get all available supported images</span></span>

```powershell
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchSupportedImage -BatchContext $Context
BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:16.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 16.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:18.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 18.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : credativ:debian:8:latest
NodeAgentSkuId        : batch.node.debian 8
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : microsoftwindowsserver:windowsserver:2016-datacenter:latest
NodeAgentSkuId        : batch.node.windows amd64
OSType                : Windows
VerificationType      : Verified

...
```

<span data-ttu-id="e6d22-110">第一個命令會使用 **Get-AzBatchAccountKey** 取得包含您訂閱便捷鍵的批次處理帳戶上下文。</span><span class="sxs-lookup"><span data-stu-id="e6d22-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="e6d22-111">該命令會儲存上下文$CoNtext變數中，以用於下一個命令。</span><span class="sxs-lookup"><span data-stu-id="e6d22-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="e6d22-112">第二個命令會針對該 Batch 帳戶獲得所有可用的支援影像。</span><span class="sxs-lookup"><span data-stu-id="e6d22-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="e6d22-113">參數</span><span class="sxs-lookup"><span data-stu-id="e6d22-113">PARAMETERS</span></span>

### <span data-ttu-id="e6d22-114">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="e6d22-114">-BatchContext</span></span>
<span data-ttu-id="e6d22-115">BatchAccountCoNtext 實例，用於與批次處理服務互動。</span><span class="sxs-lookup"><span data-stu-id="e6d22-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="e6d22-116">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="e6d22-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="e6d22-117">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="e6d22-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="e6d22-118">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="e6d22-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="e6d22-119">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="e6d22-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e6d22-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6d22-120">-DefaultProfile</span></span>
<span data-ttu-id="e6d22-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6d22-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6d22-122">-篩選</span><span class="sxs-lookup"><span data-stu-id="e6d22-122">-Filter</span></span>
<span data-ttu-id="e6d22-123">指定支援影像的 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="e6d22-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="e6d22-124">如果您未指定篩選，此 Cmdlet 會返回 Batch 帳戶支援的所有影像。</span><span class="sxs-lookup"><span data-stu-id="e6d22-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6d22-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e6d22-125">-MaxCount</span></span>
<span data-ttu-id="e6d22-126">指定要退回的最大支援影像數目。</span><span class="sxs-lookup"><span data-stu-id="e6d22-126">Specifies the maximum number of supported images to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6d22-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6d22-127">CommonParameters</span></span>
<span data-ttu-id="e6d22-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e6d22-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6d22-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6d22-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6d22-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e6d22-130">INPUTS</span></span>

### <span data-ttu-id="e6d22-131">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="e6d22-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e6d22-132">輸出</span><span class="sxs-lookup"><span data-stu-id="e6d22-132">OUTPUTS</span></span>

### <span data-ttu-id="e6d22-133">Microsoft.Azure.Commands.Batch。Models.PSImageInformation</span><span class="sxs-lookup"><span data-stu-id="e6d22-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="e6d22-134">筆記</span><span class="sxs-lookup"><span data-stu-id="e6d22-134">NOTES</span></span>

## <span data-ttu-id="e6d22-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6d22-135">RELATED LINKS</span></span>

[<span data-ttu-id="e6d22-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e6d22-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)