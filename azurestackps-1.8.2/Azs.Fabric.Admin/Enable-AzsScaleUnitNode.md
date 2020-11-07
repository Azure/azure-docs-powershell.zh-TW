---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d77229892da63973513dd8870a949ff296f5538
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968095"
---
# <span data-ttu-id="6f3d2-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="6f3d2-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="6f3d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f3d2-102">SYNOPSIS</span></span>
<span data-ttu-id="6f3d2-103">停止 [縮放單位] 節點的 [維護] 模式。</span><span class="sxs-lookup"><span data-stu-id="6f3d2-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="6f3d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f3d2-104">SYNTAX</span></span>

### <span data-ttu-id="6f3d2-105">啟用 (預設) </span><span class="sxs-lookup"><span data-stu-id="6f3d2-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f3d2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f3d2-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f3d2-107">說明</span><span class="sxs-lookup"><span data-stu-id="6f3d2-107">DESCRIPTION</span></span>
<span data-ttu-id="6f3d2-108">停止 [縮放單位] 節點的 [維護] 模式。</span><span class="sxs-lookup"><span data-stu-id="6f3d2-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="6f3d2-109">示例</span><span class="sxs-lookup"><span data-stu-id="6f3d2-109">EXAMPLES</span></span>

### <span data-ttu-id="6f3d2-110">範例1</span><span class="sxs-lookup"><span data-stu-id="6f3d2-110">EXAMPLE 1</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="6f3d2-111">停止 [縮放單位] 節點上的 [維護] 模式。</span><span class="sxs-lookup"><span data-stu-id="6f3d2-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="6f3d2-112">參數</span><span class="sxs-lookup"><span data-stu-id="6f3d2-112">PARAMETERS</span></span>

### <span data-ttu-id="6f3d2-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f3d2-113">-Name</span></span>
<span data-ttu-id="6f3d2-114">[縮放單位] 節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f3d2-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f3d2-115">-位置</span><span class="sxs-lookup"><span data-stu-id="6f3d2-115">-Location</span></span>
<span data-ttu-id="6f3d2-116">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="6f3d2-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f3d2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f3d2-117">-ResourceGroupName</span></span>
<span data-ttu-id="6f3d2-118">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="6f3d2-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f3d2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f3d2-119">-ResourceId</span></span>
<span data-ttu-id="6f3d2-120">縮放單位節點資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f3d2-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="6f3d2-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f3d2-121">-AsJob</span></span>
<span data-ttu-id="6f3d2-122">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="6f3d2-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="6f3d2-123">-Force</span><span class="sxs-lookup"><span data-stu-id="6f3d2-123">-Force</span></span>
<span data-ttu-id="6f3d2-124">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="6f3d2-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6f3d2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f3d2-125">-WhatIf</span></span>
<span data-ttu-id="6f3d2-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f3d2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f3d2-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f3d2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f3d2-128">-確認</span><span class="sxs-lookup"><span data-stu-id="6f3d2-128">-Confirm</span></span>
<span data-ttu-id="6f3d2-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6f3d2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f3d2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f3d2-130">CommonParameters</span></span>
<span data-ttu-id="6f3d2-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f3d2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f3d2-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f3d2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f3d2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="6f3d2-133">INPUTS</span></span>

## <span data-ttu-id="6f3d2-134">輸出</span><span class="sxs-lookup"><span data-stu-id="6f3d2-134">OUTPUTS</span></span>

## <span data-ttu-id="6f3d2-135">筆記</span><span class="sxs-lookup"><span data-stu-id="6f3d2-135">NOTES</span></span>

## <span data-ttu-id="6f3d2-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f3d2-136">RELATED LINKS</span></span>
