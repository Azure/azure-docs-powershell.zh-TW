---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2cb2886e84b42d499fb04693757cee333458f9b
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793650"
---
# <span data-ttu-id="76b92-101">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="76b92-101">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="76b92-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76b92-102">SYNOPSIS</span></span>
<span data-ttu-id="76b92-103">取得訂閱可存取的所有取得方案集合。</span><span class="sxs-lookup"><span data-stu-id="76b92-103">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="76b92-104">句法</span><span class="sxs-lookup"><span data-stu-id="76b92-104">SYNTAX</span></span>

### <span data-ttu-id="76b92-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="76b92-105">List (Default)</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId <Guid> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="76b92-106">獲取</span><span class="sxs-lookup"><span data-stu-id="76b92-106">Get</span></span>
```
Get-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <Guid> [<CommonParameters>]
```

### <span data-ttu-id="76b92-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="76b92-107">ResourceId</span></span>
```
Get-AzsSubscriptionPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="76b92-108">說明</span><span class="sxs-lookup"><span data-stu-id="76b92-108">DESCRIPTION</span></span>
<span data-ttu-id="76b92-109">取得訂閱可存取的所有取得方案集合。</span><span class="sxs-lookup"><span data-stu-id="76b92-109">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="76b92-110">示例</span><span class="sxs-lookup"><span data-stu-id="76b92-110">EXAMPLES</span></span>

### <span data-ttu-id="76b92-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="76b92-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="76b92-112">取得訂閱可存取的所有取得方案集合。</span><span class="sxs-lookup"><span data-stu-id="76b92-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="76b92-113">參數</span><span class="sxs-lookup"><span data-stu-id="76b92-113">PARAMETERS</span></span>

### <span data-ttu-id="76b92-114">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="76b92-114">-AcquisitionId</span></span>
<span data-ttu-id="76b92-115">方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="76b92-115">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b92-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76b92-116">-ResourceId</span></span>
<span data-ttu-id="76b92-117">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="76b92-117">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b92-118">-略過</span><span class="sxs-lookup"><span data-stu-id="76b92-118">-Skip</span></span>
<span data-ttu-id="76b92-119">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="76b92-119">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b92-120">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76b92-120">-TargetSubscriptionId</span></span>
<span data-ttu-id="76b92-121">目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="76b92-121">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b92-122">-上方</span><span class="sxs-lookup"><span data-stu-id="76b92-122">-Top</span></span>
<span data-ttu-id="76b92-123">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="76b92-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="76b92-124">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="76b92-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b92-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b92-125">CommonParameters</span></span>
<span data-ttu-id="76b92-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76b92-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b92-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="76b92-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b92-128">輸入</span><span class="sxs-lookup"><span data-stu-id="76b92-128">INPUTS</span></span>

## <span data-ttu-id="76b92-129">輸出</span><span class="sxs-lookup"><span data-stu-id="76b92-129">OUTPUTS</span></span>

### <span data-ttu-id="76b92-130">AzureStack PlanAcquisition 的訂閱。</span><span class="sxs-lookup"><span data-stu-id="76b92-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="76b92-131">筆記</span><span class="sxs-lookup"><span data-stu-id="76b92-131">NOTES</span></span>

## <span data-ttu-id="76b92-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="76b92-132">RELATED LINKS</span></span>

