---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d0dad3650338d2bba4976ce66806b714bd9e0fe
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793653"
---
# <span data-ttu-id="2406c-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="2406c-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="2406c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2406c-102">SYNOPSIS</span></span>
<span data-ttu-id="2406c-103">取得優惠指標。</span><span class="sxs-lookup"><span data-stu-id="2406c-103">Get the offer metrics.</span></span>

## <span data-ttu-id="2406c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2406c-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="2406c-105">說明</span><span class="sxs-lookup"><span data-stu-id="2406c-105">DESCRIPTION</span></span>
<span data-ttu-id="2406c-106">取得優惠指標。</span><span class="sxs-lookup"><span data-stu-id="2406c-106">Get the offer metrics.</span></span>

## <span data-ttu-id="2406c-107">示例</span><span class="sxs-lookup"><span data-stu-id="2406c-107">EXAMPLES</span></span>

### <span data-ttu-id="2406c-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2406c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="2406c-109">取得優惠指標。</span><span class="sxs-lookup"><span data-stu-id="2406c-109">Get the offer metrics.</span></span>

## <span data-ttu-id="2406c-110">參數</span><span class="sxs-lookup"><span data-stu-id="2406c-110">PARAMETERS</span></span>

### <span data-ttu-id="2406c-111">-OfferName</span><span class="sxs-lookup"><span data-stu-id="2406c-111">-OfferName</span></span>
<span data-ttu-id="2406c-112">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="2406c-112">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2406c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2406c-113">-ResourceGroupName</span></span>
<span data-ttu-id="2406c-114">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="2406c-114">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2406c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2406c-115">CommonParameters</span></span>
<span data-ttu-id="2406c-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2406c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2406c-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2406c-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2406c-118">輸入</span><span class="sxs-lookup"><span data-stu-id="2406c-118">INPUTS</span></span>

## <span data-ttu-id="2406c-119">輸出</span><span class="sxs-lookup"><span data-stu-id="2406c-119">OUTPUTS</span></span>

### <span data-ttu-id="2406c-120">AzureStack 的訂閱. 系統管理。</span><span class="sxs-lookup"><span data-stu-id="2406c-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="2406c-121">筆記</span><span class="sxs-lookup"><span data-stu-id="2406c-121">NOTES</span></span>

## <span data-ttu-id="2406c-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="2406c-122">RELATED LINKS</span></span>

