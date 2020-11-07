---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcomputeresourcesku
schema: 2.0.0
ms.openlocfilehash: e7ebc6a8e6b59679757f559ff2d09ebaa8c5475f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802594"
---
# <span data-ttu-id="865e5-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="865e5-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="865e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="865e5-102">SYNOPSIS</span></span>
<span data-ttu-id="865e5-103">列出所有計算資源 Sku</span><span class="sxs-lookup"><span data-stu-id="865e5-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="865e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="865e5-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="865e5-105">說明</span><span class="sxs-lookup"><span data-stu-id="865e5-105">DESCRIPTION</span></span>
<span data-ttu-id="865e5-106">列出所有計算資源 Sku</span><span class="sxs-lookup"><span data-stu-id="865e5-106">List all compute resource Skus</span></span>

## <span data-ttu-id="865e5-107">示例</span><span class="sxs-lookup"><span data-stu-id="865e5-107">EXAMPLES</span></span>

### <span data-ttu-id="865e5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="865e5-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="865e5-109">列出西部美國地區的所有計算資源 sku</span><span class="sxs-lookup"><span data-stu-id="865e5-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="865e5-110">參數</span><span class="sxs-lookup"><span data-stu-id="865e5-110">PARAMETERS</span></span>

### <span data-ttu-id="865e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="865e5-111">-DefaultProfile</span></span>
<span data-ttu-id="865e5-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="865e5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="865e5-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="865e5-113">CommonParameters</span></span>
<span data-ttu-id="865e5-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="865e5-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="865e5-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="865e5-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="865e5-116">輸入</span><span class="sxs-lookup"><span data-stu-id="865e5-116">INPUTS</span></span>

### <span data-ttu-id="865e5-117">所有</span><span class="sxs-lookup"><span data-stu-id="865e5-117">None</span></span>

## <span data-ttu-id="865e5-118">輸出</span><span class="sxs-lookup"><span data-stu-id="865e5-118">OUTPUTS</span></span>

### <span data-ttu-id="865e5-119">System.object</span><span class="sxs-lookup"><span data-stu-id="865e5-119">System.Object</span></span>

## <span data-ttu-id="865e5-120">筆記</span><span class="sxs-lookup"><span data-stu-id="865e5-120">NOTES</span></span>

## <span data-ttu-id="865e5-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="865e5-121">RELATED LINKS</span></span>

