---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: e62aebd6a03f7d5a162f141eae55e3df6c9a0a88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454744"
---
# <span data-ttu-id="481cd-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="481cd-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="481cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="481cd-102">SYNOPSIS</span></span>
<span data-ttu-id="481cd-103">從帳戶刪除證書。</span><span class="sxs-lookup"><span data-stu-id="481cd-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="481cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="481cd-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="481cd-105">說明</span><span class="sxs-lookup"><span data-stu-id="481cd-105">DESCRIPTION</span></span>
<span data-ttu-id="481cd-106">**AzureBatchCertificate** Cmdlet 會從指定的 Azure Batch 帳戶中移除憑證。</span><span class="sxs-lookup"><span data-stu-id="481cd-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="481cd-107">示例</span><span class="sxs-lookup"><span data-stu-id="481cd-107">EXAMPLES</span></span>

### <span data-ttu-id="481cd-108">範例1：移除憑證</span><span class="sxs-lookup"><span data-stu-id="481cd-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="481cd-109">這個命令會移除具有指定指紋的憑證。</span><span class="sxs-lookup"><span data-stu-id="481cd-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="481cd-110">範例2：移除所有使用中的憑證</span><span class="sxs-lookup"><span data-stu-id="481cd-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="481cd-111">這個命令會透過使用 Get-AzureBatchCertificate Cmdlet 來取得所有作用中的憑證。</span><span class="sxs-lookup"><span data-stu-id="481cd-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="481cd-112">使用管線運算子，命令會將使用中的憑證傳到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="481cd-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="481cd-113">該 Cmdlet 會移除每個憑證。</span><span class="sxs-lookup"><span data-stu-id="481cd-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="481cd-114">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="481cd-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="481cd-115">因此，命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="481cd-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="481cd-116">參數</span><span class="sxs-lookup"><span data-stu-id="481cd-116">PARAMETERS</span></span>

### <span data-ttu-id="481cd-117">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="481cd-117">-BatchContext</span></span>
<span data-ttu-id="481cd-118">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="481cd-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="481cd-119">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="481cd-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="481cd-120">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="481cd-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="481cd-121">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="481cd-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="481cd-122">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="481cd-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="481cd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="481cd-123">-DefaultProfile</span></span>
<span data-ttu-id="481cd-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="481cd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="481cd-125">-指紋</span><span class="sxs-lookup"><span data-stu-id="481cd-125">-Thumbprint</span></span>
<span data-ttu-id="481cd-126">指定此 Cmdlet 刪除的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="481cd-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481cd-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="481cd-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="481cd-128">指定用來衍生 *指紋* 參數的演算法。</span><span class="sxs-lookup"><span data-stu-id="481cd-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="481cd-129">目前，唯一有效的值是 sha1。</span><span class="sxs-lookup"><span data-stu-id="481cd-129">Currently, the only valid value is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481cd-130">-確認</span><span class="sxs-lookup"><span data-stu-id="481cd-130">-Confirm</span></span>
<span data-ttu-id="481cd-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="481cd-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481cd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="481cd-132">-WhatIf</span></span>
<span data-ttu-id="481cd-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="481cd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="481cd-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="481cd-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481cd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="481cd-135">CommonParameters</span></span>
<span data-ttu-id="481cd-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="481cd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="481cd-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="481cd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="481cd-138">輸入</span><span class="sxs-lookup"><span data-stu-id="481cd-138">INPUTS</span></span>

### <span data-ttu-id="481cd-139">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="481cd-139">BatchAccountContext</span></span>
<span data-ttu-id="481cd-140">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="481cd-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="481cd-141">輸出</span><span class="sxs-lookup"><span data-stu-id="481cd-141">OUTPUTS</span></span>

## <span data-ttu-id="481cd-142">筆記</span><span class="sxs-lookup"><span data-stu-id="481cd-142">NOTES</span></span>

## <span data-ttu-id="481cd-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="481cd-143">RELATED LINKS</span></span>

[<span data-ttu-id="481cd-144">AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="481cd-144">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="481cd-145">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="481cd-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="481cd-146">新-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="481cd-146">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="481cd-147">停止 AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="481cd-147">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="481cd-148">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="481cd-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


