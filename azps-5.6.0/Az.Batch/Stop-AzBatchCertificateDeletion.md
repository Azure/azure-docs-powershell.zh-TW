---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: 099f6a1ea19e9810745715dbc90ea0e0b1962285
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912910"
---
# <span data-ttu-id="8691f-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="8691f-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="8691f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8691f-102">SYNOPSIS</span></span>
<span data-ttu-id="8691f-103">取消憑證的刪除失敗。</span><span class="sxs-lookup"><span data-stu-id="8691f-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="8691f-104">語法</span><span class="sxs-lookup"><span data-stu-id="8691f-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8691f-105">描述</span><span class="sxs-lookup"><span data-stu-id="8691f-105">DESCRIPTION</span></span>
<span data-ttu-id="8691f-106">**Stop-AzBatchCertificateDeletion Cmdlet** 會取消 Azure Batch Service 中憑證的失敗刪除。</span><span class="sxs-lookup"><span data-stu-id="8691f-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="8691f-107">只有當憑證位於 **DeleteFailed** 狀態時，才能停止刪除。</span><span class="sxs-lookup"><span data-stu-id="8691f-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="8691f-108">此 Cmdlet 會將憑證還原為 **使用中** 狀態。</span><span class="sxs-lookup"><span data-stu-id="8691f-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="8691f-109">例子</span><span class="sxs-lookup"><span data-stu-id="8691f-109">EXAMPLES</span></span>

### <span data-ttu-id="8691f-110">範例 1：取消刪除</span><span class="sxs-lookup"><span data-stu-id="8691f-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="8691f-111">此命令會取消刪除具有指定指紋的憑證。</span><span class="sxs-lookup"><span data-stu-id="8691f-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="8691f-112">參數</span><span class="sxs-lookup"><span data-stu-id="8691f-112">PARAMETERS</span></span>

### <span data-ttu-id="8691f-113">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="8691f-113">-BatchContext</span></span>
<span data-ttu-id="8691f-114">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="8691f-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8691f-115">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="8691f-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8691f-116">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="8691f-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8691f-117">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="8691f-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8691f-118">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="8691f-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8691f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8691f-119">-DefaultProfile</span></span>
<span data-ttu-id="8691f-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8691f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8691f-121">-拇指列印</span><span class="sxs-lookup"><span data-stu-id="8691f-121">-Thumbprint</span></span>
<span data-ttu-id="8691f-122">指定此 Cmdlet 還原到使用中狀態之 **憑證的指紋** 。</span><span class="sxs-lookup"><span data-stu-id="8691f-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="8691f-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="8691f-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="8691f-124">指定用來推匯出 *Thumbprint 參數的* 演算法。</span><span class="sxs-lookup"><span data-stu-id="8691f-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="8691f-125">目前，唯一有效的值是 sha1。</span><span class="sxs-lookup"><span data-stu-id="8691f-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="8691f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8691f-126">CommonParameters</span></span>
<span data-ttu-id="8691f-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8691f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8691f-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8691f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8691f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8691f-129">INPUTS</span></span>

### <span data-ttu-id="8691f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8691f-130">System.String</span></span>

### <span data-ttu-id="8691f-131">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="8691f-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8691f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="8691f-132">OUTPUTS</span></span>

### <span data-ttu-id="8691f-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="8691f-133">System.Void</span></span>

## <span data-ttu-id="8691f-134">筆記</span><span class="sxs-lookup"><span data-stu-id="8691f-134">NOTES</span></span>

## <span data-ttu-id="8691f-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="8691f-135">RELATED LINKS</span></span>

[<span data-ttu-id="8691f-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8691f-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8691f-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="8691f-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="8691f-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8691f-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
