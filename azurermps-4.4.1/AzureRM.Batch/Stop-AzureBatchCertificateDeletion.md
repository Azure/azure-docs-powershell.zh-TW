---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: 820e94b75c19d49f4e49ee8419f7807a839f925b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450851"
---
# <span data-ttu-id="3c4ba-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="3c4ba-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="3c4ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c4ba-102">SYNOPSIS</span></span>
<span data-ttu-id="3c4ba-103">取消刪除憑證失敗。</span><span class="sxs-lookup"><span data-stu-id="3c4ba-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c4ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c4ba-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c4ba-105">說明</span><span class="sxs-lookup"><span data-stu-id="3c4ba-105">DESCRIPTION</span></span>
<span data-ttu-id="3c4ba-106">**AzureBatchCertificateDeletion** Cmdlet 會針對 Azure Batch 服務中的憑證取消刪除失敗的操作。</span><span class="sxs-lookup"><span data-stu-id="3c4ba-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="3c4ba-107">只有在證書處於 **DeleteFailed** 狀態時，才能停止刪除。</span><span class="sxs-lookup"><span data-stu-id="3c4ba-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="3c4ba-108">此 cmldet 會將憑證還原為 **使用中** 的狀態。</span><span class="sxs-lookup"><span data-stu-id="3c4ba-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="3c4ba-109">示例</span><span class="sxs-lookup"><span data-stu-id="3c4ba-109">EXAMPLES</span></span>

### <span data-ttu-id="3c4ba-110">範例1：取消刪除</span><span class="sxs-lookup"><span data-stu-id="3c4ba-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="3c4ba-111">這個命令會取消刪除具有指定指紋的憑證。</span><span class="sxs-lookup"><span data-stu-id="3c4ba-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="3c4ba-112">參數</span><span class="sxs-lookup"><span data-stu-id="3c4ba-112">PARAMETERS</span></span>

### <span data-ttu-id="3c4ba-113">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="3c4ba-113">-BatchContext</span></span>
<span data-ttu-id="3c4ba-114">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="3c4ba-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3c4ba-115">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c4ba-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="3c4ba-116">-指紋</span><span class="sxs-lookup"><span data-stu-id="3c4ba-116">-Thumbprint</span></span>
<span data-ttu-id="3c4ba-117">指定此 Cmdlet 還原 **為 [作用中]** 狀態的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="3c4ba-117">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="3c4ba-118">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="3c4ba-118">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="3c4ba-119">指定用來衍生 *指紋* 參數的演算法。</span><span class="sxs-lookup"><span data-stu-id="3c4ba-119">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="3c4ba-120">目前，唯一有效的值是 sha1。</span><span class="sxs-lookup"><span data-stu-id="3c4ba-120">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="3c4ba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c4ba-121">-DefaultProfile</span></span>
<span data-ttu-id="3c4ba-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c4ba-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c4ba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c4ba-123">CommonParameters</span></span>
<span data-ttu-id="3c4ba-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c4ba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c4ba-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3c4ba-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c4ba-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3c4ba-126">INPUTS</span></span>

### <span data-ttu-id="3c4ba-127">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="3c4ba-127">BatchAccountContext</span></span>
<span data-ttu-id="3c4ba-128">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3c4ba-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="3c4ba-129">輸出</span><span class="sxs-lookup"><span data-stu-id="3c4ba-129">OUTPUTS</span></span>

## <span data-ttu-id="3c4ba-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3c4ba-130">NOTES</span></span>

## <span data-ttu-id="3c4ba-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c4ba-131">RELATED LINKS</span></span>

[<span data-ttu-id="3c4ba-132">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3c4ba-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="3c4ba-133">移除-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="3c4ba-133">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="3c4ba-134">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3c4ba-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


