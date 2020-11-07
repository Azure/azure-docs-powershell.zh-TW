---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1a26c22b5714fc7db448935b31b0af685301217
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968271"
---
# <span data-ttu-id="f8ace-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="f8ace-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="f8ace-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8ace-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ace-103">關閉刻度單位節點的電源。</span><span class="sxs-lookup"><span data-stu-id="f8ace-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="f8ace-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8ace-104">SYNTAX</span></span>

### <span data-ttu-id="f8ace-105">停止 (預設) </span><span class="sxs-lookup"><span data-stu-id="f8ace-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8ace-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8ace-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8ace-107">說明</span><span class="sxs-lookup"><span data-stu-id="f8ace-107">DESCRIPTION</span></span>
<span data-ttu-id="f8ace-108">關閉刻度單位節點的電源。</span><span class="sxs-lookup"><span data-stu-id="f8ace-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="f8ace-109">示例</span><span class="sxs-lookup"><span data-stu-id="f8ace-109">EXAMPLES</span></span>

### <span data-ttu-id="f8ace-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f8ace-110">EXAMPLE 1</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="f8ace-111">關閉 [縮放單位] 節點。</span><span class="sxs-lookup"><span data-stu-id="f8ace-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="f8ace-112">範例2</span><span class="sxs-lookup"><span data-stu-id="f8ace-112">EXAMPLE 2</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="f8ace-113">關閉比例單位節點的電源。</span><span class="sxs-lookup"><span data-stu-id="f8ace-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="f8ace-114">參數</span><span class="sxs-lookup"><span data-stu-id="f8ace-114">PARAMETERS</span></span>

### <span data-ttu-id="f8ace-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f8ace-115">-Name</span></span>
<span data-ttu-id="f8ace-116">[縮放單位] 節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8ace-116">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ace-117">-位置</span><span class="sxs-lookup"><span data-stu-id="f8ace-117">-Location</span></span>
<span data-ttu-id="f8ace-118">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="f8ace-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ace-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8ace-119">-ResourceGroupName</span></span>
<span data-ttu-id="f8ace-120">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f8ace-120">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ace-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8ace-121">-ResourceId</span></span>
<span data-ttu-id="f8ace-122">縮放單位節點資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f8ace-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="f8ace-123">-關閉</span><span class="sxs-lookup"><span data-stu-id="f8ace-123">-Shutdown</span></span>
<span data-ttu-id="f8ace-124">如果設定正常關閉 [縮放單位] 節點，否則請關閉 [縮放單位] 節點的電源。</span><span class="sxs-lookup"><span data-stu-id="f8ace-124">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="f8ace-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8ace-125">-AsJob</span></span>
<span data-ttu-id="f8ace-126">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="f8ace-126">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f8ace-127">-Force</span><span class="sxs-lookup"><span data-stu-id="f8ace-127">-Force</span></span>
<span data-ttu-id="f8ace-128">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="f8ace-128">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f8ace-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8ace-129">-WhatIf</span></span>
<span data-ttu-id="f8ace-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f8ace-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8ace-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8ace-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8ace-132">-確認</span><span class="sxs-lookup"><span data-stu-id="f8ace-132">-Confirm</span></span>
<span data-ttu-id="f8ace-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f8ace-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8ace-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ace-134">CommonParameters</span></span>
<span data-ttu-id="f8ace-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8ace-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ace-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f8ace-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ace-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f8ace-137">INPUTS</span></span>

## <span data-ttu-id="f8ace-138">輸出</span><span class="sxs-lookup"><span data-stu-id="f8ace-138">OUTPUTS</span></span>

## <span data-ttu-id="f8ace-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f8ace-139">NOTES</span></span>

## <span data-ttu-id="f8ace-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8ace-140">RELATED LINKS</span></span>
