---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2cb2886e84b42d499fb04693757cee333458f9b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968319"
---
# <span data-ttu-id="2e773-101">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="2e773-101">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="2e773-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e773-102">SYNOPSIS</span></span>
<span data-ttu-id="2e773-103">取得訂閱可存取的所有取得方案集合。</span><span class="sxs-lookup"><span data-stu-id="2e773-103">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="2e773-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e773-104">SYNTAX</span></span>

### <span data-ttu-id="2e773-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="2e773-105">List (Default)</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId <Guid> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2e773-106">獲取</span><span class="sxs-lookup"><span data-stu-id="2e773-106">Get</span></span>
```
Get-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <Guid> [<CommonParameters>]
```

### <span data-ttu-id="2e773-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e773-107">ResourceId</span></span>
```
Get-AzsSubscriptionPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2e773-108">說明</span><span class="sxs-lookup"><span data-stu-id="2e773-108">DESCRIPTION</span></span>
<span data-ttu-id="2e773-109">取得訂閱可存取的所有取得方案集合。</span><span class="sxs-lookup"><span data-stu-id="2e773-109">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="2e773-110">示例</span><span class="sxs-lookup"><span data-stu-id="2e773-110">EXAMPLES</span></span>

### <span data-ttu-id="2e773-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2e773-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="2e773-112">取得訂閱可存取的所有取得方案集合。</span><span class="sxs-lookup"><span data-stu-id="2e773-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="2e773-113">參數</span><span class="sxs-lookup"><span data-stu-id="2e773-113">PARAMETERS</span></span>

### <span data-ttu-id="2e773-114">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="2e773-114">-AcquisitionId</span></span>
<span data-ttu-id="2e773-115">方案採集識別碼</span><span class="sxs-lookup"><span data-stu-id="2e773-115">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="2e773-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e773-116">-ResourceId</span></span>
<span data-ttu-id="2e773-117">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="2e773-117">The resource id.</span></span>

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

### <span data-ttu-id="2e773-118">-略過</span><span class="sxs-lookup"><span data-stu-id="2e773-118">-Skip</span></span>
<span data-ttu-id="2e773-119">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="2e773-119">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="2e773-120">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e773-120">-TargetSubscriptionId</span></span>
<span data-ttu-id="2e773-121">目標訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="2e773-121">The target subscription ID.</span></span>

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

### <span data-ttu-id="2e773-122">-上方</span><span class="sxs-lookup"><span data-stu-id="2e773-122">-Top</span></span>
<span data-ttu-id="2e773-123">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="2e773-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2e773-124">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="2e773-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="2e773-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e773-125">CommonParameters</span></span>
<span data-ttu-id="2e773-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e773-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e773-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e773-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e773-128">輸入</span><span class="sxs-lookup"><span data-stu-id="2e773-128">INPUTS</span></span>

## <span data-ttu-id="2e773-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2e773-129">OUTPUTS</span></span>

### <span data-ttu-id="2e773-130">AzureStack PlanAcquisition 的訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e773-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="2e773-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2e773-131">NOTES</span></span>

## <span data-ttu-id="2e773-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e773-132">RELATED LINKS</span></span>

