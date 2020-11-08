---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ced1207f07360c0a18674d6f8ae4170be9b87beb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968226"
---
# <span data-ttu-id="9088e-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="9088e-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="9088e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9088e-102">SYNOPSIS</span></span>
<span data-ttu-id="9088e-103">新增縮放單位。</span><span class="sxs-lookup"><span data-stu-id="9088e-103">Add a new scale unit.</span></span>

## <span data-ttu-id="9088e-104">句法</span><span class="sxs-lookup"><span data-stu-id="9088e-104">SYNTAX</span></span>

### <span data-ttu-id="9088e-105">ScaleOut (預設) </span><span class="sxs-lookup"><span data-stu-id="9088e-105">ScaleOut (Default)</span></span>
```
Add-AzsScaleUnitNode -Name <String> -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence]
 [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9088e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9088e-106">ResourceId</span></span>
```
Add-AzsScaleUnitNode -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence] -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9088e-107">說明</span><span class="sxs-lookup"><span data-stu-id="9088e-107">DESCRIPTION</span></span>
<span data-ttu-id="9088e-108">新增縮放單位。</span><span class="sxs-lookup"><span data-stu-id="9088e-108">Add a new scale unit.</span></span>

## <span data-ttu-id="9088e-109">示例</span><span class="sxs-lookup"><span data-stu-id="9088e-109">EXAMPLES</span></span>

### <span data-ttu-id="9088e-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9088e-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -ScaleUnitName "Azs-ERC03" -NodeList $nodeList
```

<span data-ttu-id="9088e-111">新增 [縮放比例單位] 節點。</span><span class="sxs-lookup"><span data-stu-id="9088e-111">Add a new scale unit node.</span></span>

## <span data-ttu-id="9088e-112">參數</span><span class="sxs-lookup"><span data-stu-id="9088e-112">PARAMETERS</span></span>

### <span data-ttu-id="9088e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9088e-113">-AsJob</span></span>
<span data-ttu-id="9088e-114">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="9088e-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="9088e-115">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="9088e-115">-AwaitStorageConvergence</span></span>
<span data-ttu-id="9088e-116">[旗標] 表示該作業是否應該等到儲存之後，才能返回。</span><span class="sxs-lookup"><span data-stu-id="9088e-116">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="9088e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9088e-117">-Force</span></span>
<span data-ttu-id="9088e-118">不要求確認</span><span class="sxs-lookup"><span data-stu-id="9088e-118">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="9088e-119">-位置</span><span class="sxs-lookup"><span data-stu-id="9088e-119">-Location</span></span>
<span data-ttu-id="9088e-120">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="9088e-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9088e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="9088e-121">-Name</span></span>
<span data-ttu-id="9088e-122">{{Fill Name Description}}</span><span class="sxs-lookup"><span data-stu-id="9088e-122">{{Fill Name Description}}</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9088e-123">-NodeList</span><span class="sxs-lookup"><span data-stu-id="9088e-123">-NodeList</span></span>
<span data-ttu-id="9088e-124">刻度單位中的節點清單。</span><span class="sxs-lookup"><span data-stu-id="9088e-124">List of nodes in the scale unit.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9088e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9088e-125">-ResourceGroupName</span></span>
<span data-ttu-id="9088e-126">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="9088e-126">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9088e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9088e-127">-ResourceId</span></span>
<span data-ttu-id="9088e-128">縮放單位節點資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9088e-128">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="9088e-129">-確認</span><span class="sxs-lookup"><span data-stu-id="9088e-129">-Confirm</span></span>
<span data-ttu-id="9088e-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9088e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9088e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9088e-131">-WhatIf</span></span>
<span data-ttu-id="9088e-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9088e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9088e-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9088e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9088e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9088e-134">CommonParameters</span></span>
<span data-ttu-id="9088e-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9088e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9088e-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9088e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9088e-137">輸入</span><span class="sxs-lookup"><span data-stu-id="9088e-137">INPUTS</span></span>

## <span data-ttu-id="9088e-138">輸出</span><span class="sxs-lookup"><span data-stu-id="9088e-138">OUTPUTS</span></span>

## <span data-ttu-id="9088e-139">筆記</span><span class="sxs-lookup"><span data-stu-id="9088e-139">NOTES</span></span>

## <span data-ttu-id="9088e-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="9088e-140">RELATED LINKS</span></span>
