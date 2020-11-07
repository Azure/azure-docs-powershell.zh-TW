---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: cdddb11071bb7e4c4d57bd44fb2bbe5193b4153f
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93799445"
---
# <span data-ttu-id="5f4a5-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="5f4a5-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="5f4a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f4a5-102">SYNOPSIS</span></span>
<span data-ttu-id="5f4a5-103">取消刪除憑證失敗。</span><span class="sxs-lookup"><span data-stu-id="5f4a5-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="5f4a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f4a5-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f4a5-105">說明</span><span class="sxs-lookup"><span data-stu-id="5f4a5-105">DESCRIPTION</span></span>
<span data-ttu-id="5f4a5-106">**AzBatchCertificateDeletion** Cmdlet 會針對 Azure Batch 服務中的憑證取消刪除失敗的操作。</span><span class="sxs-lookup"><span data-stu-id="5f4a5-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="5f4a5-107">只有在證書處於 **DeleteFailed** 狀態時，才能停止刪除。</span><span class="sxs-lookup"><span data-stu-id="5f4a5-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="5f4a5-108">這個 Cmdlet 會將憑證還原到作用 **中狀態。**</span><span class="sxs-lookup"><span data-stu-id="5f4a5-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="5f4a5-109">示例</span><span class="sxs-lookup"><span data-stu-id="5f4a5-109">EXAMPLES</span></span>

### <span data-ttu-id="5f4a5-110">範例1：取消刪除</span><span class="sxs-lookup"><span data-stu-id="5f4a5-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="5f4a5-111">這個命令會取消刪除具有指定指紋的憑證。</span><span class="sxs-lookup"><span data-stu-id="5f4a5-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="5f4a5-112">參數</span><span class="sxs-lookup"><span data-stu-id="5f4a5-112">PARAMETERS</span></span>

### <span data-ttu-id="5f4a5-113">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="5f4a5-113">-BatchContext</span></span>
<span data-ttu-id="5f4a5-114">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="5f4a5-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5f4a5-115">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="5f4a5-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5f4a5-116">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="5f4a5-116">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5f4a5-117">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="5f4a5-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5f4a5-118">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="5f4a5-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5f4a5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f4a5-119">-DefaultProfile</span></span>
<span data-ttu-id="5f4a5-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f4a5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f4a5-121">-指紋</span><span class="sxs-lookup"><span data-stu-id="5f4a5-121">-Thumbprint</span></span>
<span data-ttu-id="5f4a5-122">指定此 Cmdlet 還原 **為 [作用中]** 狀態的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="5f4a5-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="5f4a5-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="5f4a5-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="5f4a5-124">指定用來衍生 *指紋* 參數的演算法。</span><span class="sxs-lookup"><span data-stu-id="5f4a5-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="5f4a5-125">目前，唯一有效的值是 sha1。</span><span class="sxs-lookup"><span data-stu-id="5f4a5-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="5f4a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f4a5-126">CommonParameters</span></span>
<span data-ttu-id="5f4a5-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f4a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f4a5-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5f4a5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f4a5-129">輸入</span><span class="sxs-lookup"><span data-stu-id="5f4a5-129">INPUTS</span></span>

### <span data-ttu-id="5f4a5-130">System.object</span><span class="sxs-lookup"><span data-stu-id="5f4a5-130">System.String</span></span>

### <span data-ttu-id="5f4a5-131">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="5f4a5-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5f4a5-132">輸出</span><span class="sxs-lookup"><span data-stu-id="5f4a5-132">OUTPUTS</span></span>

### <span data-ttu-id="5f4a5-133">System.void</span><span class="sxs-lookup"><span data-stu-id="5f4a5-133">System.Void</span></span>

## <span data-ttu-id="5f4a5-134">筆記</span><span class="sxs-lookup"><span data-stu-id="5f4a5-134">NOTES</span></span>

## <span data-ttu-id="5f4a5-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f4a5-135">RELATED LINKS</span></span>

[<span data-ttu-id="5f4a5-136">AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5f4a5-136">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5f4a5-137">移除-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="5f4a5-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="5f4a5-138">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5f4a5-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


