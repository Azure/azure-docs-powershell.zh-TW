---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 1a53e72cd31d3ca43cf5c9a4e6a66de4bc2bd59d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457455"
---
# <span data-ttu-id="0d202-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="0d202-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="0d202-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d202-102">SYNOPSIS</span></span>
<span data-ttu-id="0d202-103">停用自動縮放文件庫。</span><span class="sxs-lookup"><span data-stu-id="0d202-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d202-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d202-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d202-105">說明</span><span class="sxs-lookup"><span data-stu-id="0d202-105">DESCRIPTION</span></span>
<span data-ttu-id="0d202-106">**Disable AzureBatchAutoScale** Cmdlet 會停用指定池的自動縮放。</span><span class="sxs-lookup"><span data-stu-id="0d202-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="0d202-107">示例</span><span class="sxs-lookup"><span data-stu-id="0d202-107">EXAMPLES</span></span>

### <span data-ttu-id="0d202-108">範例1：停用自動縮放文件庫</span><span class="sxs-lookup"><span data-stu-id="0d202-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="0d202-109">這個命令會針對名為 MyPool 的池停用自動縮放。</span><span class="sxs-lookup"><span data-stu-id="0d202-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="0d202-110">參數</span><span class="sxs-lookup"><span data-stu-id="0d202-110">PARAMETERS</span></span>

### <span data-ttu-id="0d202-111">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="0d202-111">-BatchContext</span></span>
<span data-ttu-id="0d202-112">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="0d202-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0d202-113">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="0d202-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0d202-114">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="0d202-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0d202-115">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="0d202-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0d202-116">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="0d202-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0d202-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d202-117">-DefaultProfile</span></span>
<span data-ttu-id="0d202-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d202-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d202-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="0d202-119">-Id</span></span>
<span data-ttu-id="0d202-120">指定該池的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d202-120">Specifies the object ID of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d202-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d202-121">CommonParameters</span></span>
<span data-ttu-id="0d202-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d202-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d202-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0d202-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d202-124">輸入</span><span class="sxs-lookup"><span data-stu-id="0d202-124">INPUTS</span></span>

### <span data-ttu-id="0d202-125">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="0d202-125">BatchAccountContext</span></span>
<span data-ttu-id="0d202-126">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0d202-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="0d202-127">字串</span><span class="sxs-lookup"><span data-stu-id="0d202-127">String</span></span>
<span data-ttu-id="0d202-128">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="0d202-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="0d202-129">輸出</span><span class="sxs-lookup"><span data-stu-id="0d202-129">OUTPUTS</span></span>

## <span data-ttu-id="0d202-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0d202-130">NOTES</span></span>

## <span data-ttu-id="0d202-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d202-131">RELATED LINKS</span></span>

[<span data-ttu-id="0d202-132">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="0d202-132">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="0d202-133">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="0d202-133">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="0d202-134">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0d202-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

