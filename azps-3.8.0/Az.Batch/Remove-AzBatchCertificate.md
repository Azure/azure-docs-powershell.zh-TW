---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: f34500b72936191182c5486051a97b9e74cada16
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93968653"
---
# <span data-ttu-id="7257d-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="7257d-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="7257d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7257d-102">SYNOPSIS</span></span>
<span data-ttu-id="7257d-103">從帳戶刪除證書。</span><span class="sxs-lookup"><span data-stu-id="7257d-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="7257d-104">句法</span><span class="sxs-lookup"><span data-stu-id="7257d-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7257d-105">說明</span><span class="sxs-lookup"><span data-stu-id="7257d-105">DESCRIPTION</span></span>
<span data-ttu-id="7257d-106">**AzBatchCertificate** Cmdlet 會從指定的 Azure Batch 帳戶中移除憑證。</span><span class="sxs-lookup"><span data-stu-id="7257d-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="7257d-107">示例</span><span class="sxs-lookup"><span data-stu-id="7257d-107">EXAMPLES</span></span>

### <span data-ttu-id="7257d-108">範例1：移除憑證</span><span class="sxs-lookup"><span data-stu-id="7257d-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="7257d-109">這個命令會移除具有指定指紋的憑證。</span><span class="sxs-lookup"><span data-stu-id="7257d-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="7257d-110">範例2：移除所有使用中的憑證</span><span class="sxs-lookup"><span data-stu-id="7257d-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="7257d-111">這個命令會透過使用 Get-AzBatchCertificate Cmdlet 來取得所有作用中的憑證。</span><span class="sxs-lookup"><span data-stu-id="7257d-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="7257d-112">使用管線運算子，命令會將使用中的憑證傳到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7257d-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7257d-113">該 Cmdlet 會移除每個憑證。</span><span class="sxs-lookup"><span data-stu-id="7257d-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="7257d-114">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="7257d-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7257d-115">因此，命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7257d-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7257d-116">參數</span><span class="sxs-lookup"><span data-stu-id="7257d-116">PARAMETERS</span></span>

### <span data-ttu-id="7257d-117">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="7257d-117">-BatchContext</span></span>
<span data-ttu-id="7257d-118">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="7257d-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7257d-119">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="7257d-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7257d-120">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="7257d-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7257d-121">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="7257d-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7257d-122">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="7257d-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7257d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7257d-123">-DefaultProfile</span></span>
<span data-ttu-id="7257d-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7257d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7257d-125">-指紋</span><span class="sxs-lookup"><span data-stu-id="7257d-125">-Thumbprint</span></span>
<span data-ttu-id="7257d-126">指定此 Cmdlet 刪除的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="7257d-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="7257d-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="7257d-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="7257d-128">指定用來衍生 *指紋* 參數的演算法。</span><span class="sxs-lookup"><span data-stu-id="7257d-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="7257d-129">目前，唯一有效的值是 sha1。</span><span class="sxs-lookup"><span data-stu-id="7257d-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="7257d-130">-確認</span><span class="sxs-lookup"><span data-stu-id="7257d-130">-Confirm</span></span>
<span data-ttu-id="7257d-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7257d-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7257d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7257d-132">-WhatIf</span></span>
<span data-ttu-id="7257d-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7257d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7257d-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7257d-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7257d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7257d-135">CommonParameters</span></span>
<span data-ttu-id="7257d-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7257d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7257d-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7257d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7257d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="7257d-138">INPUTS</span></span>

### <span data-ttu-id="7257d-139">System.object</span><span class="sxs-lookup"><span data-stu-id="7257d-139">System.String</span></span>

### <span data-ttu-id="7257d-140">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="7257d-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7257d-141">輸出</span><span class="sxs-lookup"><span data-stu-id="7257d-141">OUTPUTS</span></span>

### <span data-ttu-id="7257d-142">System.void</span><span class="sxs-lookup"><span data-stu-id="7257d-142">System.Void</span></span>

## <span data-ttu-id="7257d-143">筆記</span><span class="sxs-lookup"><span data-stu-id="7257d-143">NOTES</span></span>

## <span data-ttu-id="7257d-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="7257d-144">RELATED LINKS</span></span>

[<span data-ttu-id="7257d-145">AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="7257d-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="7257d-146">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7257d-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7257d-147">新-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="7257d-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="7257d-148">停止 AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="7257d-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="7257d-149">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7257d-149">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

