---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: c0a0f0a11b4caf18b12c21d37dd18ef153220a97
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139880"
---
# <span data-ttu-id="f31ed-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="f31ed-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="f31ed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f31ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f31ed-103">停用自動縮放文件庫。</span><span class="sxs-lookup"><span data-stu-id="f31ed-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="f31ed-104">句法</span><span class="sxs-lookup"><span data-stu-id="f31ed-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f31ed-105">說明</span><span class="sxs-lookup"><span data-stu-id="f31ed-105">DESCRIPTION</span></span>
<span data-ttu-id="f31ed-106">**Disable AzBatchAutoScale** Cmdlet 會停用指定池的自動縮放。</span><span class="sxs-lookup"><span data-stu-id="f31ed-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="f31ed-107">示例</span><span class="sxs-lookup"><span data-stu-id="f31ed-107">EXAMPLES</span></span>

### <span data-ttu-id="f31ed-108">範例1：停用自動縮放文件庫</span><span class="sxs-lookup"><span data-stu-id="f31ed-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="f31ed-109">這個命令會針對名為 MyPool 的池停用自動縮放。</span><span class="sxs-lookup"><span data-stu-id="f31ed-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="f31ed-110">參數</span><span class="sxs-lookup"><span data-stu-id="f31ed-110">PARAMETERS</span></span>

### <span data-ttu-id="f31ed-111">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="f31ed-111">-BatchContext</span></span>
<span data-ttu-id="f31ed-112">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="f31ed-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f31ed-113">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="f31ed-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f31ed-114">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="f31ed-114">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f31ed-115">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="f31ed-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f31ed-116">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="f31ed-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f31ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f31ed-117">-DefaultProfile</span></span>
<span data-ttu-id="f31ed-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f31ed-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f31ed-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="f31ed-119">-Id</span></span>
<span data-ttu-id="f31ed-120">指定該池的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="f31ed-120">Specifies the object ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f31ed-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f31ed-121">CommonParameters</span></span>
<span data-ttu-id="f31ed-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f31ed-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f31ed-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f31ed-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f31ed-124">輸入</span><span class="sxs-lookup"><span data-stu-id="f31ed-124">INPUTS</span></span>

### <span data-ttu-id="f31ed-125">System.object</span><span class="sxs-lookup"><span data-stu-id="f31ed-125">System.String</span></span>

### <span data-ttu-id="f31ed-126">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="f31ed-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f31ed-127">輸出</span><span class="sxs-lookup"><span data-stu-id="f31ed-127">OUTPUTS</span></span>

### <span data-ttu-id="f31ed-128">System.void</span><span class="sxs-lookup"><span data-stu-id="f31ed-128">System.Void</span></span>

## <span data-ttu-id="f31ed-129">筆記</span><span class="sxs-lookup"><span data-stu-id="f31ed-129">NOTES</span></span>

## <span data-ttu-id="f31ed-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="f31ed-130">RELATED LINKS</span></span>

[<span data-ttu-id="f31ed-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="f31ed-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="f31ed-132">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="f31ed-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="f31ed-133">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f31ed-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)


