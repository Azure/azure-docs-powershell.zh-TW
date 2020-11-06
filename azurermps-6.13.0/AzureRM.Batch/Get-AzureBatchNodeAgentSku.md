---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodeagentsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
ms.openlocfilehash: 86451c1ac7ba52c9b013b3724d9c706caaa961ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444003"
---
# <span data-ttu-id="8696f-101">Get-AzureBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="8696f-101">Get-AzureBatchNodeAgentSku</span></span>

## <span data-ttu-id="8696f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8696f-102">SYNOPSIS</span></span>
<span data-ttu-id="8696f-103">取得批次帳戶中可用的批節點代理程式 Sku。</span><span class="sxs-lookup"><span data-stu-id="8696f-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8696f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8696f-104">SYNTAX</span></span>

```
Get-AzureBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8696f-105">說明</span><span class="sxs-lookup"><span data-stu-id="8696f-105">DESCRIPTION</span></span>
<span data-ttu-id="8696f-106">**AzureBatchNodeAgentSku** Cmdlet 會取得 Azure Batch 帳戶中提供的節點代理 sku。</span><span class="sxs-lookup"><span data-stu-id="8696f-106">The **Get-AzureBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="8696f-107">使用 *BatchCoNtext* 參數指定帳戶。</span><span class="sxs-lookup"><span data-stu-id="8696f-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="8696f-108">您可以將搜尋範圍縮小到與開放式資料通訊協定 (OData) 篩選器相符的 Sku。</span><span class="sxs-lookup"><span data-stu-id="8696f-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="8696f-109">示例</span><span class="sxs-lookup"><span data-stu-id="8696f-109">EXAMPLES</span></span>

### <span data-ttu-id="8696f-110">範例1：取得所有可用的節點代理程式 Sku</span><span class="sxs-lookup"><span data-stu-id="8696f-110">Example 1: Get all available node agent SKUs</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

<span data-ttu-id="8696f-111">第一個命令會使用 **AzureRmBatchAccountKeys** 來取得包含訂閱之便捷鍵的批次帳戶內容。</span><span class="sxs-lookup"><span data-stu-id="8696f-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="8696f-112">該命令會將內容儲存在 $CoNtext 變數中，以用於下一個命令。</span><span class="sxs-lookup"><span data-stu-id="8696f-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="8696f-113">第二個命令會取得批次支援的所有可用節點代理程式 Sku。</span><span class="sxs-lookup"><span data-stu-id="8696f-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="8696f-114">參數</span><span class="sxs-lookup"><span data-stu-id="8696f-114">PARAMETERS</span></span>

### <span data-ttu-id="8696f-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="8696f-115">-BatchContext</span></span>
<span data-ttu-id="8696f-116">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="8696f-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8696f-117">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="8696f-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8696f-118">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="8696f-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8696f-119">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="8696f-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8696f-120">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="8696f-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8696f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8696f-121">-DefaultProfile</span></span>
<span data-ttu-id="8696f-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8696f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8696f-123">-篩選</span><span class="sxs-lookup"><span data-stu-id="8696f-123">-Filter</span></span>
<span data-ttu-id="8696f-124">為節點代理程式 Sku 指定 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="8696f-124">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="8696f-125">如果您沒有指定篩選，這個 Cmdlet 會傳回 Batch 支援的所有節點代理程式 Sku。</span><span class="sxs-lookup"><span data-stu-id="8696f-125">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

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

### <span data-ttu-id="8696f-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8696f-126">-MaxCount</span></span>
<span data-ttu-id="8696f-127">指定要傳回的節點代理 Sku 數目上限。</span><span class="sxs-lookup"><span data-stu-id="8696f-127">Specifies the maximum number of node agent SKUs to return.</span></span>

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

### <span data-ttu-id="8696f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8696f-128">CommonParameters</span></span>
<span data-ttu-id="8696f-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8696f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8696f-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8696f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8696f-131">輸入</span><span class="sxs-lookup"><span data-stu-id="8696f-131">INPUTS</span></span>

### <span data-ttu-id="8696f-132">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="8696f-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="8696f-133">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="8696f-133">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="8696f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="8696f-134">OUTPUTS</span></span>

### <span data-ttu-id="8696f-135">Microsoft.Azure.Commands.Batch。PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="8696f-135">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="8696f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8696f-136">NOTES</span></span>

## <span data-ttu-id="8696f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8696f-137">RELATED LINKS</span></span>

[<span data-ttu-id="8696f-138">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8696f-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


