---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 932d0b77fc6df9a88a2ee13ad92856727db82f06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442375"
---
# <span data-ttu-id="464ff-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="464ff-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="464ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="464ff-102">SYNOPSIS</span></span>
<span data-ttu-id="464ff-103">停止 [縮放單位] 節點的 [維護] 模式。</span><span class="sxs-lookup"><span data-stu-id="464ff-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="464ff-104">句法</span><span class="sxs-lookup"><span data-stu-id="464ff-104">SYNTAX</span></span>

### <span data-ttu-id="464ff-105">啟用 (預設) </span><span class="sxs-lookup"><span data-stu-id="464ff-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="464ff-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="464ff-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="464ff-107">說明</span><span class="sxs-lookup"><span data-stu-id="464ff-107">DESCRIPTION</span></span>
<span data-ttu-id="464ff-108">停止 [縮放單位] 節點的 [維護] 模式。</span><span class="sxs-lookup"><span data-stu-id="464ff-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="464ff-109">示例</span><span class="sxs-lookup"><span data-stu-id="464ff-109">EXAMPLES</span></span>

### <span data-ttu-id="464ff-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="464ff-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="464ff-111">停止 [縮放單位] 節點上的 [維護] 模式。</span><span class="sxs-lookup"><span data-stu-id="464ff-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="464ff-112">參數</span><span class="sxs-lookup"><span data-stu-id="464ff-112">PARAMETERS</span></span>

### <span data-ttu-id="464ff-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="464ff-113">-AsJob</span></span>
<span data-ttu-id="464ff-114">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="464ff-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="464ff-115">-Force</span><span class="sxs-lookup"><span data-stu-id="464ff-115">-Force</span></span>
<span data-ttu-id="464ff-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="464ff-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="464ff-117">-位置</span><span class="sxs-lookup"><span data-stu-id="464ff-117">-Location</span></span>
<span data-ttu-id="464ff-118">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="464ff-118">Location of the resource.</span></span>

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

### <span data-ttu-id="464ff-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="464ff-119">-Name</span></span>
<span data-ttu-id="464ff-120">[縮放單位] 節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="464ff-120">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="464ff-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="464ff-121">-ResourceGroupName</span></span>
<span data-ttu-id="464ff-122">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="464ff-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="464ff-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="464ff-123">-ResourceId</span></span>
<span data-ttu-id="464ff-124">縮放單位節點資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="464ff-124">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="464ff-125">-確認</span><span class="sxs-lookup"><span data-stu-id="464ff-125">-Confirm</span></span>
<span data-ttu-id="464ff-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="464ff-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="464ff-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="464ff-127">-WhatIf</span></span>
<span data-ttu-id="464ff-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="464ff-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="464ff-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="464ff-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="464ff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="464ff-130">CommonParameters</span></span>
<span data-ttu-id="464ff-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="464ff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="464ff-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="464ff-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="464ff-133">輸入</span><span class="sxs-lookup"><span data-stu-id="464ff-133">INPUTS</span></span>

## <span data-ttu-id="464ff-134">輸出</span><span class="sxs-lookup"><span data-stu-id="464ff-134">OUTPUTS</span></span>

## <span data-ttu-id="464ff-135">筆記</span><span class="sxs-lookup"><span data-stu-id="464ff-135">NOTES</span></span>

## <span data-ttu-id="464ff-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="464ff-136">RELATED LINKS</span></span>

