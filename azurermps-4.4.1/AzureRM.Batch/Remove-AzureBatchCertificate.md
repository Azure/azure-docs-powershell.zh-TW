---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: c63caed99a10851d6172e0db5dcc33e3404be215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447157"
---
# <span data-ttu-id="5dff2-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="5dff2-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="5dff2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5dff2-102">SYNOPSIS</span></span>
<span data-ttu-id="5dff2-103">從帳戶刪除證書。</span><span class="sxs-lookup"><span data-stu-id="5dff2-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dff2-104">句法</span><span class="sxs-lookup"><span data-stu-id="5dff2-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5dff2-105">說明</span><span class="sxs-lookup"><span data-stu-id="5dff2-105">DESCRIPTION</span></span>
<span data-ttu-id="5dff2-106">**AzureBatchCertificate** Cmdlet 會從指定的 Azure Batch 帳戶中移除憑證。</span><span class="sxs-lookup"><span data-stu-id="5dff2-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="5dff2-107">示例</span><span class="sxs-lookup"><span data-stu-id="5dff2-107">EXAMPLES</span></span>

### <span data-ttu-id="5dff2-108">範例1：移除憑證</span><span class="sxs-lookup"><span data-stu-id="5dff2-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="5dff2-109">這個命令會移除具有指定指紋的憑證。</span><span class="sxs-lookup"><span data-stu-id="5dff2-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="5dff2-110">範例2：移除所有使用中的憑證</span><span class="sxs-lookup"><span data-stu-id="5dff2-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="5dff2-111">這個命令會透過使用 Get-AzureBatchCertificate Cmdlet 來取得所有作用中的憑證。</span><span class="sxs-lookup"><span data-stu-id="5dff2-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="5dff2-112">使用管線運算子，命令會將使用中的憑證傳到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5dff2-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5dff2-113">該 Cmdlet 會移除每個憑證。</span><span class="sxs-lookup"><span data-stu-id="5dff2-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="5dff2-114">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="5dff2-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="5dff2-115">因此，命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5dff2-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5dff2-116">參數</span><span class="sxs-lookup"><span data-stu-id="5dff2-116">PARAMETERS</span></span>

### <span data-ttu-id="5dff2-117">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="5dff2-117">-BatchContext</span></span>
<span data-ttu-id="5dff2-118">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="5dff2-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5dff2-119">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5dff2-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="5dff2-120">-指紋</span><span class="sxs-lookup"><span data-stu-id="5dff2-120">-Thumbprint</span></span>
<span data-ttu-id="5dff2-121">指定此 Cmdlet 刪除的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="5dff2-121">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="5dff2-122">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="5dff2-122">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="5dff2-123">指定用來衍生 *指紋* 參數的演算法。</span><span class="sxs-lookup"><span data-stu-id="5dff2-123">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="5dff2-124">目前，唯一有效的值是 sha1。</span><span class="sxs-lookup"><span data-stu-id="5dff2-124">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="5dff2-125">-確認</span><span class="sxs-lookup"><span data-stu-id="5dff2-125">-Confirm</span></span>
<span data-ttu-id="5dff2-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5dff2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dff2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dff2-127">-WhatIf</span></span>
<span data-ttu-id="5dff2-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5dff2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dff2-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5dff2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dff2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dff2-130">-DefaultProfile</span></span>
<span data-ttu-id="5dff2-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5dff2-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dff2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dff2-132">CommonParameters</span></span>
<span data-ttu-id="5dff2-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5dff2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dff2-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5dff2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dff2-135">輸入</span><span class="sxs-lookup"><span data-stu-id="5dff2-135">INPUTS</span></span>

### <span data-ttu-id="5dff2-136">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="5dff2-136">BatchAccountContext</span></span>
<span data-ttu-id="5dff2-137">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="5dff2-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="5dff2-138">輸出</span><span class="sxs-lookup"><span data-stu-id="5dff2-138">OUTPUTS</span></span>

## <span data-ttu-id="5dff2-139">筆記</span><span class="sxs-lookup"><span data-stu-id="5dff2-139">NOTES</span></span>

## <span data-ttu-id="5dff2-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="5dff2-140">RELATED LINKS</span></span>

[<span data-ttu-id="5dff2-141">AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="5dff2-141">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="5dff2-142">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5dff2-142">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5dff2-143">新-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="5dff2-143">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="5dff2-144">停止 AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="5dff2-144">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="5dff2-145">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5dff2-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


