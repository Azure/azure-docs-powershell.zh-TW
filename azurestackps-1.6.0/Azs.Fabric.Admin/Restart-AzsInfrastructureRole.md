---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: da781ee77cb94e7bc442b72ad0655041cf23b546
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442572"
---
# <span data-ttu-id="b2933-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="b2933-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="b2933-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b2933-102">SYNOPSIS</span></span>
<span data-ttu-id="b2933-103">重新開機要求的基礎結構角色。</span><span class="sxs-lookup"><span data-stu-id="b2933-103">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="b2933-104">句法</span><span class="sxs-lookup"><span data-stu-id="b2933-104">SYNTAX</span></span>

### <span data-ttu-id="b2933-105">重新開機 (預設) </span><span class="sxs-lookup"><span data-stu-id="b2933-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2933-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2933-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2933-107">說明</span><span class="sxs-lookup"><span data-stu-id="b2933-107">DESCRIPTION</span></span>
<span data-ttu-id="b2933-108">重新開機要求的基礎結構角色。</span><span class="sxs-lookup"><span data-stu-id="b2933-108">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="b2933-109">示例</span><span class="sxs-lookup"><span data-stu-id="b2933-109">EXAMPLES</span></span>

### <span data-ttu-id="b2933-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b2933-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restart-AzsInfrastructureRole -Name "Compute Controller"
```

<span data-ttu-id="b2933-111">重新開機已損壞的基礎結構角色。</span><span class="sxs-lookup"><span data-stu-id="b2933-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="b2933-112">參數</span><span class="sxs-lookup"><span data-stu-id="b2933-112">PARAMETERS</span></span>

### <span data-ttu-id="b2933-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2933-113">-AsJob</span></span>
<span data-ttu-id="b2933-114">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="b2933-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="b2933-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b2933-115">-Force</span></span>
<span data-ttu-id="b2933-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="b2933-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b2933-117">-位置</span><span class="sxs-lookup"><span data-stu-id="b2933-117">-Location</span></span>
<span data-ttu-id="b2933-118">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="b2933-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2933-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="b2933-119">-Name</span></span>
<span data-ttu-id="b2933-120">結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="b2933-120">Infrastructure role name.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2933-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2933-121">-ResourceGroupName</span></span>
<span data-ttu-id="b2933-122">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b2933-122">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2933-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2933-123">-ResourceId</span></span>
<span data-ttu-id="b2933-124">結構角色資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2933-124">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="b2933-125">-確認</span><span class="sxs-lookup"><span data-stu-id="b2933-125">-Confirm</span></span>
<span data-ttu-id="b2933-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b2933-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2933-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2933-127">-WhatIf</span></span>
<span data-ttu-id="b2933-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b2933-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2933-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b2933-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2933-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2933-130">CommonParameters</span></span>
<span data-ttu-id="b2933-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b2933-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2933-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b2933-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2933-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b2933-133">INPUTS</span></span>

## <span data-ttu-id="b2933-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b2933-134">OUTPUTS</span></span>

## <span data-ttu-id="b2933-135">筆記</span><span class="sxs-lookup"><span data-stu-id="b2933-135">NOTES</span></span>

## <span data-ttu-id="b2933-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2933-136">RELATED LINKS</span></span>

