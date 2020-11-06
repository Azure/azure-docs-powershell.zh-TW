---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: d43754e1b04dadc447de3d727769902f5454f79a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450279"
---
# <span data-ttu-id="953e3-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="953e3-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="953e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="953e3-102">SYNOPSIS</span></span>
<span data-ttu-id="953e3-103">取消刪除憑證失敗。</span><span class="sxs-lookup"><span data-stu-id="953e3-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="953e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="953e3-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="953e3-105">說明</span><span class="sxs-lookup"><span data-stu-id="953e3-105">DESCRIPTION</span></span>
<span data-ttu-id="953e3-106">**AzureBatchCertificateDeletion** Cmdlet 會針對 Azure Batch 服務中的憑證取消刪除失敗的操作。</span><span class="sxs-lookup"><span data-stu-id="953e3-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="953e3-107">只有在證書處於 **DeleteFailed** 狀態時，才能停止刪除。</span><span class="sxs-lookup"><span data-stu-id="953e3-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="953e3-108">此 cmldet 會將憑證還原為 **使用中** 的狀態。</span><span class="sxs-lookup"><span data-stu-id="953e3-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="953e3-109">示例</span><span class="sxs-lookup"><span data-stu-id="953e3-109">EXAMPLES</span></span>

### <span data-ttu-id="953e3-110">範例1：取消刪除</span><span class="sxs-lookup"><span data-stu-id="953e3-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="953e3-111">這個命令會取消刪除具有指定指紋的憑證。</span><span class="sxs-lookup"><span data-stu-id="953e3-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="953e3-112">參數</span><span class="sxs-lookup"><span data-stu-id="953e3-112">PARAMETERS</span></span>

### <span data-ttu-id="953e3-113">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="953e3-113">-BatchContext</span></span>
<span data-ttu-id="953e3-114">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="953e3-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="953e3-115">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="953e3-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="953e3-116">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="953e3-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="953e3-117">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="953e3-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="953e3-118">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="953e3-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="953e3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="953e3-119">-DefaultProfile</span></span>
<span data-ttu-id="953e3-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="953e3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="953e3-121">-指紋</span><span class="sxs-lookup"><span data-stu-id="953e3-121">-Thumbprint</span></span>
<span data-ttu-id="953e3-122">指定此 Cmdlet 還原 **為 [作用中]** 狀態的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="953e3-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953e3-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="953e3-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="953e3-124">指定用來衍生 *指紋* 參數的演算法。</span><span class="sxs-lookup"><span data-stu-id="953e3-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="953e3-125">目前，唯一有效的值是 sha1。</span><span class="sxs-lookup"><span data-stu-id="953e3-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="953e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="953e3-126">CommonParameters</span></span>
<span data-ttu-id="953e3-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="953e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="953e3-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="953e3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="953e3-129">輸入</span><span class="sxs-lookup"><span data-stu-id="953e3-129">INPUTS</span></span>

### <span data-ttu-id="953e3-130">System.object</span><span class="sxs-lookup"><span data-stu-id="953e3-130">System.String</span></span>

### <span data-ttu-id="953e3-131">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="953e3-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="953e3-132">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="953e3-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="953e3-133">輸出</span><span class="sxs-lookup"><span data-stu-id="953e3-133">OUTPUTS</span></span>

### <span data-ttu-id="953e3-134">System.void</span><span class="sxs-lookup"><span data-stu-id="953e3-134">System.Void</span></span>

## <span data-ttu-id="953e3-135">筆記</span><span class="sxs-lookup"><span data-stu-id="953e3-135">NOTES</span></span>

## <span data-ttu-id="953e3-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="953e3-136">RELATED LINKS</span></span>

[<span data-ttu-id="953e3-137">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="953e3-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="953e3-138">移除-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="953e3-138">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="953e3-139">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="953e3-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


