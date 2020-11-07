---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968285"
---
# <span data-ttu-id="b72bf-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="b72bf-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="b72bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b72bf-102">SYNOPSIS</span></span>
<span data-ttu-id="b72bf-103">開啟 [縮放單元] 節點。</span><span class="sxs-lookup"><span data-stu-id="b72bf-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="b72bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="b72bf-104">SYNTAX</span></span>

### <span data-ttu-id="b72bf-105">PowerOn (預設) </span><span class="sxs-lookup"><span data-stu-id="b72bf-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b72bf-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b72bf-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b72bf-107">說明</span><span class="sxs-lookup"><span data-stu-id="b72bf-107">DESCRIPTION</span></span>
<span data-ttu-id="b72bf-108">開啟 [縮放單元] 節點。</span><span class="sxs-lookup"><span data-stu-id="b72bf-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="b72bf-109">示例</span><span class="sxs-lookup"><span data-stu-id="b72bf-109">EXAMPLES</span></span>

### <span data-ttu-id="b72bf-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b72bf-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="b72bf-111">ProvisioningState：成功</span><span class="sxs-lookup"><span data-stu-id="b72bf-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="b72bf-112">開啟 [縮放單元] 節點。</span><span class="sxs-lookup"><span data-stu-id="b72bf-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="b72bf-113">參數</span><span class="sxs-lookup"><span data-stu-id="b72bf-113">PARAMETERS</span></span>

### <span data-ttu-id="b72bf-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="b72bf-114">-Name</span></span>
<span data-ttu-id="b72bf-115">[縮放單位] 節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="b72bf-115">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="b72bf-116">-位置</span><span class="sxs-lookup"><span data-stu-id="b72bf-116">-Location</span></span>
<span data-ttu-id="b72bf-117">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="b72bf-117">Location of the resource.</span></span>

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

### <span data-ttu-id="b72bf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b72bf-118">-ResourceGroupName</span></span>
<span data-ttu-id="b72bf-119">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b72bf-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b72bf-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b72bf-120">-ResourceId</span></span>
<span data-ttu-id="b72bf-121">縮放單位節點資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b72bf-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="b72bf-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b72bf-122">-AsJob</span></span>
<span data-ttu-id="b72bf-123">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="b72bf-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="b72bf-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b72bf-124">-Force</span></span>
<span data-ttu-id="b72bf-125">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="b72bf-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b72bf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b72bf-126">-WhatIf</span></span>
<span data-ttu-id="b72bf-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b72bf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b72bf-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b72bf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b72bf-129">-確認</span><span class="sxs-lookup"><span data-stu-id="b72bf-129">-Confirm</span></span>
<span data-ttu-id="b72bf-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b72bf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b72bf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b72bf-131">CommonParameters</span></span>
<span data-ttu-id="b72bf-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b72bf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b72bf-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b72bf-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b72bf-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b72bf-134">INPUTS</span></span>

## <span data-ttu-id="b72bf-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b72bf-135">OUTPUTS</span></span>

## <span data-ttu-id="b72bf-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b72bf-136">NOTES</span></span>

## <span data-ttu-id="b72bf-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b72bf-137">RELATED LINKS</span></span>
