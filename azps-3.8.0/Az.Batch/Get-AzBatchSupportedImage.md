---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: 56ec7eafcea7233697089d692b2799fa6c9b744a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958944"
---
# <span data-ttu-id="0450a-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="0450a-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="0450a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0450a-102">SYNOPSIS</span></span>
<span data-ttu-id="0450a-103">取得批次帳戶支援的批次影像。</span><span class="sxs-lookup"><span data-stu-id="0450a-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="0450a-104">句法</span><span class="sxs-lookup"><span data-stu-id="0450a-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0450a-105">說明</span><span class="sxs-lookup"><span data-stu-id="0450a-105">DESCRIPTION</span></span>
<span data-ttu-id="0450a-106">**AzBatchSupportedImage** Cmdlet 會取得 Azure Batch 帳戶中提供的支援虛擬機器影像。</span><span class="sxs-lookup"><span data-stu-id="0450a-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="0450a-107">使用 *BatchCoNtext* 參數指定帳戶。</span><span class="sxs-lookup"><span data-stu-id="0450a-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="0450a-108">示例</span><span class="sxs-lookup"><span data-stu-id="0450a-108">EXAMPLES</span></span>

### <span data-ttu-id="0450a-109">範例1：取得所有可用的支援影像</span><span class="sxs-lookup"><span data-stu-id="0450a-109">Example 1: Get all available supported images</span></span>

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

<span data-ttu-id="0450a-110">第一個命令會使用 **AzBatchAccountKey** 來取得包含訂閱之便捷鍵的批次帳戶內容。</span><span class="sxs-lookup"><span data-stu-id="0450a-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="0450a-111">該命令會將內容儲存在 $CoNtext 變數中，以用於下一個命令。</span><span class="sxs-lookup"><span data-stu-id="0450a-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="0450a-112">第二個命令會取得該 Batch 帳戶的所有可用支援影像。</span><span class="sxs-lookup"><span data-stu-id="0450a-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="0450a-113">參數</span><span class="sxs-lookup"><span data-stu-id="0450a-113">PARAMETERS</span></span>

### <span data-ttu-id="0450a-114">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="0450a-114">-BatchContext</span></span>
<span data-ttu-id="0450a-115">與批次服務互動時要使用的 BatchAccountCoNtext 實例。</span><span class="sxs-lookup"><span data-stu-id="0450a-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="0450a-116">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="0450a-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="0450a-117">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="0450a-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="0450a-118">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="0450a-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="0450a-119">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="0450a-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0450a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0450a-120">-DefaultProfile</span></span>
<span data-ttu-id="0450a-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0450a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0450a-122">-篩選</span><span class="sxs-lookup"><span data-stu-id="0450a-122">-Filter</span></span>
<span data-ttu-id="0450a-123">為支援的圖像指定 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="0450a-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="0450a-124">如果您沒有指定篩選，這個 Cmdlet 會傳回批次帳戶所支援的所有影像。</span><span class="sxs-lookup"><span data-stu-id="0450a-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0450a-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0450a-125">-MaxCount</span></span>
<span data-ttu-id="0450a-126">指定要傳回的支援影像數目上限。</span><span class="sxs-lookup"><span data-stu-id="0450a-126">Specifies the maximum number of supported images to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0450a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0450a-127">CommonParameters</span></span>
<span data-ttu-id="0450a-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0450a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0450a-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0450a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0450a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="0450a-130">INPUTS</span></span>

### <span data-ttu-id="0450a-131">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="0450a-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0450a-132">輸出</span><span class="sxs-lookup"><span data-stu-id="0450a-132">OUTPUTS</span></span>

### <span data-ttu-id="0450a-133">Microsoft.Azure.Commands.Batch。PSImageInformation</span><span class="sxs-lookup"><span data-stu-id="0450a-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="0450a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="0450a-134">NOTES</span></span>

## <span data-ttu-id="0450a-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="0450a-135">RELATED LINKS</span></span>
[<span data-ttu-id="0450a-136">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0450a-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)