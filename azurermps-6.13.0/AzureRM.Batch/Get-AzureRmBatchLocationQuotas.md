---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchlocationquotas
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
ms.openlocfilehash: dea724c77b0574e8235c58a2a696987c94ca586d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625356"
---
# <span data-ttu-id="00eb4-101">Get-AzureRmBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="00eb4-101">Get-AzureRmBatchLocationQuotas</span></span>

## <span data-ttu-id="00eb4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="00eb4-103">取得訂閱在指定位置的批次服務配額。</span><span class="sxs-lookup"><span data-stu-id="00eb4-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00eb4-104">句法</span><span class="sxs-lookup"><span data-stu-id="00eb4-104">SYNTAX</span></span>

```
Get-AzureRmBatchLocationQuotas [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00eb4-105">說明</span><span class="sxs-lookup"><span data-stu-id="00eb4-105">DESCRIPTION</span></span>
<span data-ttu-id="00eb4-106">在指定位置取得指定訂閱的批次服務配額。</span><span class="sxs-lookup"><span data-stu-id="00eb4-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="00eb4-107">示例</span><span class="sxs-lookup"><span data-stu-id="00eb4-107">EXAMPLES</span></span>

### <span data-ttu-id="00eb4-108">範例1：取得美國西部地區訂閱的批次服務配額</span><span class="sxs-lookup"><span data-stu-id="00eb4-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzureRmBatchLocationQuotas -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="00eb4-109">這個命令會取得目前訂閱在美國西部地區的配額。</span><span class="sxs-lookup"><span data-stu-id="00eb4-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="00eb4-110">傳回值表示此訂閱只能在該區域中建立一個 Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="00eb4-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="00eb4-111">參數</span><span class="sxs-lookup"><span data-stu-id="00eb4-111">PARAMETERS</span></span>

### <span data-ttu-id="00eb4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00eb4-112">-DefaultProfile</span></span>
<span data-ttu-id="00eb4-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="00eb4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00eb4-114">-位置</span><span class="sxs-lookup"><span data-stu-id="00eb4-114">-Location</span></span>
<span data-ttu-id="00eb4-115">指定此 Cmdlet 檢查配額的區域。</span><span class="sxs-lookup"><span data-stu-id="00eb4-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="00eb4-116">如需詳細資訊，請參閱 Azure 地區 (https://azure.microsoft.com/regions) 。</span><span class="sxs-lookup"><span data-stu-id="00eb4-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="00eb4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00eb4-117">CommonParameters</span></span>
<span data-ttu-id="00eb4-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00eb4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00eb4-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="00eb4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00eb4-120">輸入</span><span class="sxs-lookup"><span data-stu-id="00eb4-120">INPUTS</span></span>

### <span data-ttu-id="00eb4-121">System.object</span><span class="sxs-lookup"><span data-stu-id="00eb4-121">System.String</span></span>

## <span data-ttu-id="00eb4-122">輸出</span><span class="sxs-lookup"><span data-stu-id="00eb4-122">OUTPUTS</span></span>

### <span data-ttu-id="00eb4-123">Microsoft.Azure.Commands.Batch。PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="00eb4-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="00eb4-124">筆記</span><span class="sxs-lookup"><span data-stu-id="00eb4-124">NOTES</span></span>

## <span data-ttu-id="00eb4-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="00eb4-125">RELATED LINKS</span></span>
