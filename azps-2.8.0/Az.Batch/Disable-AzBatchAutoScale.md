---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: d20a52c3e907bd981bc0a692ebb4aa44495d0960
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93799542"
---
# <span data-ttu-id="3d63e-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="3d63e-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="3d63e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d63e-102">SYNOPSIS</span></span>
<span data-ttu-id="3d63e-103">停用自動縮放文件庫。</span><span class="sxs-lookup"><span data-stu-id="3d63e-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="3d63e-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d63e-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d63e-105">說明</span><span class="sxs-lookup"><span data-stu-id="3d63e-105">DESCRIPTION</span></span>
<span data-ttu-id="3d63e-106">**Disable AzBatchAutoScale** Cmdlet 會停用指定池的自動縮放。</span><span class="sxs-lookup"><span data-stu-id="3d63e-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="3d63e-107">示例</span><span class="sxs-lookup"><span data-stu-id="3d63e-107">EXAMPLES</span></span>

### <span data-ttu-id="3d63e-108">範例1：停用自動縮放文件庫</span><span class="sxs-lookup"><span data-stu-id="3d63e-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="3d63e-109">這個命令會針對名為 MyPool 的池停用自動縮放。</span><span class="sxs-lookup"><span data-stu-id="3d63e-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="3d63e-110">參數</span><span class="sxs-lookup"><span data-stu-id="3d63e-110">PARAMETERS</span></span>

### <span data-ttu-id="3d63e-111">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="3d63e-111">-BatchContext</span></span>
<span data-ttu-id="3d63e-112">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="3d63e-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3d63e-113">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="3d63e-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3d63e-114">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="3d63e-114">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3d63e-115">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="3d63e-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3d63e-116">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="3d63e-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3d63e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d63e-117">-DefaultProfile</span></span>
<span data-ttu-id="3d63e-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d63e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d63e-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="3d63e-119">-Id</span></span>
<span data-ttu-id="3d63e-120">指定該池的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d63e-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="3d63e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d63e-121">CommonParameters</span></span>
<span data-ttu-id="3d63e-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d63e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d63e-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3d63e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d63e-124">輸入</span><span class="sxs-lookup"><span data-stu-id="3d63e-124">INPUTS</span></span>

### <span data-ttu-id="3d63e-125">System.object</span><span class="sxs-lookup"><span data-stu-id="3d63e-125">System.String</span></span>

### <span data-ttu-id="3d63e-126">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="3d63e-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3d63e-127">輸出</span><span class="sxs-lookup"><span data-stu-id="3d63e-127">OUTPUTS</span></span>

### <span data-ttu-id="3d63e-128">System.void</span><span class="sxs-lookup"><span data-stu-id="3d63e-128">System.Void</span></span>

## <span data-ttu-id="3d63e-129">筆記</span><span class="sxs-lookup"><span data-stu-id="3d63e-129">NOTES</span></span>

## <span data-ttu-id="3d63e-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d63e-130">RELATED LINKS</span></span>

[<span data-ttu-id="3d63e-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="3d63e-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="3d63e-132">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="3d63e-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="3d63e-133">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d63e-133">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

