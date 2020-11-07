---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 57d7037f6deb669531bb03c3bf4f2e504586f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791613"
---
# <span data-ttu-id="5f4dd-101">New-AzsAddonPlanDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="5f4dd-101">New-AzsAddonPlanDefinitionObject</span></span>

## <span data-ttu-id="5f4dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f4dd-102">SYNOPSIS</span></span>
<span data-ttu-id="5f4dd-103">包含要連結或取消連結至優惠的所需方案名稱。</span><span class="sxs-lookup"><span data-stu-id="5f4dd-103">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="5f4dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f4dd-104">SYNTAX</span></span>

```
New-AzsAddonPlanDefinitionObject [[-PlanId] <String>] [[-MaxAcquisitionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="5f4dd-105">說明</span><span class="sxs-lookup"><span data-stu-id="5f4dd-105">DESCRIPTION</span></span>
<span data-ttu-id="5f4dd-106">包含要連結或取消連結至優惠的所需方案名稱。</span><span class="sxs-lookup"><span data-stu-id="5f4dd-106">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="5f4dd-107">示例</span><span class="sxs-lookup"><span data-stu-id="5f4dd-107">EXAMPLES</span></span>

### <span data-ttu-id="5f4dd-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5f4dd-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsAddonPlanDefinitionObject -PlanId $planIdentifier -MaxAcquisitionCount 500
```

<span data-ttu-id="5f4dd-109">針對含500購置限制的指定方案，建立新的方案定義物件。</span><span class="sxs-lookup"><span data-stu-id="5f4dd-109">Create a new plan definition object for the specified plan with the acquisition limit of 500.</span></span>

## <span data-ttu-id="5f4dd-110">參數</span><span class="sxs-lookup"><span data-stu-id="5f4dd-110">PARAMETERS</span></span>

### <span data-ttu-id="5f4dd-111">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="5f4dd-111">-MaxAcquisitionCount</span></span>
<span data-ttu-id="5f4dd-112">單一訂閱可以取得的最大實例數。</span><span class="sxs-lookup"><span data-stu-id="5f4dd-112">Maximum number of instances that can be acquired by a single subscription.</span></span>
<span data-ttu-id="5f4dd-113">如果未指定，則假設值為1。</span><span class="sxs-lookup"><span data-stu-id="5f4dd-113">If not specified, the assumed value is 1.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4dd-114">-PlanId</span><span class="sxs-lookup"><span data-stu-id="5f4dd-114">-PlanId</span></span>
<span data-ttu-id="5f4dd-115">方案識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f4dd-115">Plan identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4dd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f4dd-116">CommonParameters</span></span>
<span data-ttu-id="5f4dd-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f4dd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f4dd-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5f4dd-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f4dd-119">輸入</span><span class="sxs-lookup"><span data-stu-id="5f4dd-119">INPUTS</span></span>

## <span data-ttu-id="5f4dd-120">輸出</span><span class="sxs-lookup"><span data-stu-id="5f4dd-120">OUTPUTS</span></span>

## <span data-ttu-id="5f4dd-121">筆記</span><span class="sxs-lookup"><span data-stu-id="5f4dd-121">NOTES</span></span>

## <span data-ttu-id="5f4dd-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f4dd-122">RELATED LINKS</span></span>

