---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: 62858f37a7444e052c3d0a192a346a2284f232c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906969"
---
# <span data-ttu-id="dcce9-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="dcce9-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="dcce9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dcce9-102">SYNOPSIS</span></span>
<span data-ttu-id="dcce9-103">從帳戶刪除憑證。</span><span class="sxs-lookup"><span data-stu-id="dcce9-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="dcce9-104">語法</span><span class="sxs-lookup"><span data-stu-id="dcce9-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dcce9-105">描述</span><span class="sxs-lookup"><span data-stu-id="dcce9-105">DESCRIPTION</span></span>
<span data-ttu-id="dcce9-106">**Remove-AzBatchCertificate** Cmdlet 會從指定的 Azure Batch 帳戶移除憑證。</span><span class="sxs-lookup"><span data-stu-id="dcce9-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="dcce9-107">例子</span><span class="sxs-lookup"><span data-stu-id="dcce9-107">EXAMPLES</span></span>

### <span data-ttu-id="dcce9-108">範例 1：移除憑證</span><span class="sxs-lookup"><span data-stu-id="dcce9-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="dcce9-109">此命令會移除具有指定指紋的憑證。</span><span class="sxs-lookup"><span data-stu-id="dcce9-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="dcce9-110">範例 2：移除所有使用中憑證</span><span class="sxs-lookup"><span data-stu-id="dcce9-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="dcce9-111">此命令會使用 Cmdlet 的所有使用中Get-AzBatchCertificate憑證。</span><span class="sxs-lookup"><span data-stu-id="dcce9-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="dcce9-112">該命令會使用管線運算子，將活動憑證傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dcce9-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dcce9-113">該 Cmdlet 會移除每個憑證。</span><span class="sxs-lookup"><span data-stu-id="dcce9-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="dcce9-114">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="dcce9-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="dcce9-115">因此，命令不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="dcce9-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="dcce9-116">參數</span><span class="sxs-lookup"><span data-stu-id="dcce9-116">PARAMETERS</span></span>

### <span data-ttu-id="dcce9-117">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="dcce9-117">-BatchContext</span></span>
<span data-ttu-id="dcce9-118">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="dcce9-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dcce9-119">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="dcce9-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="dcce9-120">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="dcce9-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="dcce9-121">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="dcce9-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="dcce9-122">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="dcce9-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="dcce9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcce9-123">-DefaultProfile</span></span>
<span data-ttu-id="dcce9-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dcce9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcce9-125">-拇指列印</span><span class="sxs-lookup"><span data-stu-id="dcce9-125">-Thumbprint</span></span>
<span data-ttu-id="dcce9-126">指定此 Cmdlet 刪除之憑證的指紋。</span><span class="sxs-lookup"><span data-stu-id="dcce9-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="dcce9-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="dcce9-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="dcce9-128">指定用來推匯出 *Thumbprint 參數的* 演算法。</span><span class="sxs-lookup"><span data-stu-id="dcce9-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="dcce9-129">目前，唯一有效的值是 sha1。</span><span class="sxs-lookup"><span data-stu-id="dcce9-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="dcce9-130">-確認</span><span class="sxs-lookup"><span data-stu-id="dcce9-130">-Confirm</span></span>
<span data-ttu-id="dcce9-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="dcce9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcce9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcce9-132">-WhatIf</span></span>
<span data-ttu-id="dcce9-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dcce9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcce9-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dcce9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcce9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcce9-135">CommonParameters</span></span>
<span data-ttu-id="dcce9-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dcce9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcce9-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dcce9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcce9-138">輸入</span><span class="sxs-lookup"><span data-stu-id="dcce9-138">INPUTS</span></span>

### <span data-ttu-id="dcce9-139">System.String</span><span class="sxs-lookup"><span data-stu-id="dcce9-139">System.String</span></span>

### <span data-ttu-id="dcce9-140">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="dcce9-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="dcce9-141">輸出</span><span class="sxs-lookup"><span data-stu-id="dcce9-141">OUTPUTS</span></span>

### <span data-ttu-id="dcce9-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="dcce9-142">System.Void</span></span>

## <span data-ttu-id="dcce9-143">筆記</span><span class="sxs-lookup"><span data-stu-id="dcce9-143">NOTES</span></span>

## <span data-ttu-id="dcce9-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="dcce9-144">RELATED LINKS</span></span>

[<span data-ttu-id="dcce9-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="dcce9-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="dcce9-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="dcce9-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="dcce9-147">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="dcce9-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="dcce9-148">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="dcce9-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="dcce9-149">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dcce9-149">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
