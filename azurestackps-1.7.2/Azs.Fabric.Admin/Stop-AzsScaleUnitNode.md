---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6de990526330cdd192cd99707aacc1e06ad49c5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793340"
---
# <span data-ttu-id="de672-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="de672-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="de672-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de672-102">SYNOPSIS</span></span>
<span data-ttu-id="de672-103">關閉刻度單位節點的電源。</span><span class="sxs-lookup"><span data-stu-id="de672-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="de672-104">句法</span><span class="sxs-lookup"><span data-stu-id="de672-104">SYNTAX</span></span>

### <span data-ttu-id="de672-105">停止 (預設) </span><span class="sxs-lookup"><span data-stu-id="de672-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de672-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="de672-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de672-107">說明</span><span class="sxs-lookup"><span data-stu-id="de672-107">DESCRIPTION</span></span>
<span data-ttu-id="de672-108">關閉刻度單位節點的電源。</span><span class="sxs-lookup"><span data-stu-id="de672-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="de672-109">示例</span><span class="sxs-lookup"><span data-stu-id="de672-109">EXAMPLES</span></span>

### <span data-ttu-id="de672-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="de672-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="de672-111">關閉 [縮放單位] 節點。</span><span class="sxs-lookup"><span data-stu-id="de672-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="de672-112">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="de672-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="de672-113">關閉比例單位節點的電源。</span><span class="sxs-lookup"><span data-stu-id="de672-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="de672-114">參數</span><span class="sxs-lookup"><span data-stu-id="de672-114">PARAMETERS</span></span>

### <span data-ttu-id="de672-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de672-115">-AsJob</span></span>
<span data-ttu-id="de672-116">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="de672-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="de672-117">-Force</span><span class="sxs-lookup"><span data-stu-id="de672-117">-Force</span></span>
<span data-ttu-id="de672-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="de672-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="de672-119">-位置</span><span class="sxs-lookup"><span data-stu-id="de672-119">-Location</span></span>
<span data-ttu-id="de672-120">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="de672-120">Location of the resource.</span></span>

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

### <span data-ttu-id="de672-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="de672-121">-Name</span></span>
<span data-ttu-id="de672-122">[縮放單位] 節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="de672-122">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="de672-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de672-123">-ResourceGroupName</span></span>
<span data-ttu-id="de672-124">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="de672-124">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="de672-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de672-125">-ResourceId</span></span>
<span data-ttu-id="de672-126">縮放單位節點資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="de672-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="de672-127">-關閉</span><span class="sxs-lookup"><span data-stu-id="de672-127">-Shutdown</span></span>
<span data-ttu-id="de672-128">如果設定正常關閉 [縮放單位] 節點，否則請關閉 [縮放單位] 節點的電源。</span><span class="sxs-lookup"><span data-stu-id="de672-128">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="de672-129">-確認</span><span class="sxs-lookup"><span data-stu-id="de672-129">-Confirm</span></span>
<span data-ttu-id="de672-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="de672-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de672-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de672-131">-WhatIf</span></span>
<span data-ttu-id="de672-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="de672-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de672-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de672-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de672-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de672-134">CommonParameters</span></span>
<span data-ttu-id="de672-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de672-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de672-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="de672-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de672-137">輸入</span><span class="sxs-lookup"><span data-stu-id="de672-137">INPUTS</span></span>

## <span data-ttu-id="de672-138">輸出</span><span class="sxs-lookup"><span data-stu-id="de672-138">OUTPUTS</span></span>

## <span data-ttu-id="de672-139">筆記</span><span class="sxs-lookup"><span data-stu-id="de672-139">NOTES</span></span>

## <span data-ttu-id="de672-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="de672-140">RELATED LINKS</span></span>

