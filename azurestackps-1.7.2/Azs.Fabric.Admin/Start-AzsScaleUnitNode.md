---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c5de84b66283d683d121c99c0cf2e0ea27a4a66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793342"
---
# <span data-ttu-id="c2ebb-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="c2ebb-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="c2ebb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ebb-103">開啟 [縮放單元] 節點。</span><span class="sxs-lookup"><span data-stu-id="c2ebb-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="c2ebb-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2ebb-104">SYNTAX</span></span>

### <span data-ttu-id="c2ebb-105">PowerOn (預設) </span><span class="sxs-lookup"><span data-stu-id="c2ebb-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2ebb-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2ebb-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2ebb-107">說明</span><span class="sxs-lookup"><span data-stu-id="c2ebb-107">DESCRIPTION</span></span>
<span data-ttu-id="c2ebb-108">開啟 [縮放單元] 節點。</span><span class="sxs-lookup"><span data-stu-id="c2ebb-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="c2ebb-109">示例</span><span class="sxs-lookup"><span data-stu-id="c2ebb-109">EXAMPLES</span></span>

### <span data-ttu-id="c2ebb-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c2ebb-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="c2ebb-111">ProvisioningState：成功</span><span class="sxs-lookup"><span data-stu-id="c2ebb-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="c2ebb-112">開啟 [縮放單元] 節點。</span><span class="sxs-lookup"><span data-stu-id="c2ebb-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="c2ebb-113">參數</span><span class="sxs-lookup"><span data-stu-id="c2ebb-113">PARAMETERS</span></span>

### <span data-ttu-id="c2ebb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2ebb-114">-AsJob</span></span>
<span data-ttu-id="c2ebb-115">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="c2ebb-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c2ebb-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c2ebb-116">-Force</span></span>
<span data-ttu-id="c2ebb-117">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="c2ebb-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c2ebb-118">-位置</span><span class="sxs-lookup"><span data-stu-id="c2ebb-118">-Location</span></span>
<span data-ttu-id="c2ebb-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="c2ebb-119">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2ebb-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2ebb-120">-Name</span></span>
<span data-ttu-id="c2ebb-121">[縮放單位] 節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2ebb-121">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2ebb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2ebb-122">-ResourceGroupName</span></span>
<span data-ttu-id="c2ebb-123">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c2ebb-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2ebb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2ebb-124">-ResourceId</span></span>
<span data-ttu-id="c2ebb-125">縮放單位節點資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c2ebb-125">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="c2ebb-126">-確認</span><span class="sxs-lookup"><span data-stu-id="c2ebb-126">-Confirm</span></span>
<span data-ttu-id="c2ebb-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2ebb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2ebb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2ebb-128">-WhatIf</span></span>
<span data-ttu-id="c2ebb-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2ebb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2ebb-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2ebb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2ebb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ebb-131">CommonParameters</span></span>
<span data-ttu-id="c2ebb-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2ebb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ebb-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2ebb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ebb-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c2ebb-134">INPUTS</span></span>

## <span data-ttu-id="c2ebb-135">輸出</span><span class="sxs-lookup"><span data-stu-id="c2ebb-135">OUTPUTS</span></span>

## <span data-ttu-id="c2ebb-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c2ebb-136">NOTES</span></span>

## <span data-ttu-id="c2ebb-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2ebb-137">RELATED LINKS</span></span>

