---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c60245b9e6b8d44d8c465427c41c69e5cd442bb0
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793866"
---
# <span data-ttu-id="5f9df-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="5f9df-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="5f9df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f9df-102">SYNOPSIS</span></span>
<span data-ttu-id="5f9df-103">啟動 [縮放單位] 節點的 [維護模式]。</span><span class="sxs-lookup"><span data-stu-id="5f9df-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="5f9df-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f9df-104">SYNTAX</span></span>

### <span data-ttu-id="5f9df-105">停用 (預設) </span><span class="sxs-lookup"><span data-stu-id="5f9df-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f9df-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f9df-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f9df-107">說明</span><span class="sxs-lookup"><span data-stu-id="5f9df-107">DESCRIPTION</span></span>
<span data-ttu-id="5f9df-108">啟動 [縮放單位] 節點的 [維護模式]。</span><span class="sxs-lookup"><span data-stu-id="5f9df-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="5f9df-109">示例</span><span class="sxs-lookup"><span data-stu-id="5f9df-109">EXAMPLES</span></span>

### <span data-ttu-id="5f9df-110">範例1</span><span class="sxs-lookup"><span data-stu-id="5f9df-110">EXAMPLE 1</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="5f9df-111">針對縮放單位節點啟用 [維護模式]。</span><span class="sxs-lookup"><span data-stu-id="5f9df-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="5f9df-112">參數</span><span class="sxs-lookup"><span data-stu-id="5f9df-112">PARAMETERS</span></span>

### <span data-ttu-id="5f9df-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="5f9df-113">-Name</span></span>
<span data-ttu-id="5f9df-114">[縮放單位] 節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f9df-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9df-115">-位置</span><span class="sxs-lookup"><span data-stu-id="5f9df-115">-Location</span></span>
<span data-ttu-id="5f9df-116">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="5f9df-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9df-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f9df-117">-ResourceGroupName</span></span>
<span data-ttu-id="5f9df-118">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5f9df-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9df-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f9df-119">-ResourceId</span></span>
<span data-ttu-id="5f9df-120">縮放單位節點資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f9df-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="5f9df-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f9df-121">-AsJob</span></span>
<span data-ttu-id="5f9df-122">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="5f9df-122">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9df-123">-Force</span><span class="sxs-lookup"><span data-stu-id="5f9df-123">-Force</span></span>
<span data-ttu-id="5f9df-124">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="5f9df-124">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9df-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f9df-125">-WhatIf</span></span>
<span data-ttu-id="5f9df-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5f9df-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f9df-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f9df-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9df-128">-確認</span><span class="sxs-lookup"><span data-stu-id="5f9df-128">-Confirm</span></span>
<span data-ttu-id="5f9df-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5f9df-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9df-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f9df-130">CommonParameters</span></span>
<span data-ttu-id="5f9df-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f9df-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f9df-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5f9df-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f9df-133">輸入</span><span class="sxs-lookup"><span data-stu-id="5f9df-133">INPUTS</span></span>

## <span data-ttu-id="5f9df-134">輸出</span><span class="sxs-lookup"><span data-stu-id="5f9df-134">OUTPUTS</span></span>

## <span data-ttu-id="5f9df-135">筆記</span><span class="sxs-lookup"><span data-stu-id="5f9df-135">NOTES</span></span>

## <span data-ttu-id="5f9df-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f9df-136">RELATED LINKS</span></span>
