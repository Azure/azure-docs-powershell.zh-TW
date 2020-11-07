---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 781b920bf955a84554b9152f54c9847a00a8b160
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793830"
---
# <span data-ttu-id="44743-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="44743-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="44743-102">摘要</span><span class="sxs-lookup"><span data-stu-id="44743-102">SYNOPSIS</span></span>
<span data-ttu-id="44743-103">重新開機 requestd 基礎結構角色。</span><span class="sxs-lookup"><span data-stu-id="44743-103">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="44743-104">句法</span><span class="sxs-lookup"><span data-stu-id="44743-104">SYNTAX</span></span>

### <span data-ttu-id="44743-105">重新開機 (預設) </span><span class="sxs-lookup"><span data-stu-id="44743-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44743-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="44743-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44743-107">說明</span><span class="sxs-lookup"><span data-stu-id="44743-107">DESCRIPTION</span></span>
<span data-ttu-id="44743-108">重新開機 requestd 基礎結構角色。</span><span class="sxs-lookup"><span data-stu-id="44743-108">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="44743-109">示例</span><span class="sxs-lookup"><span data-stu-id="44743-109">EXAMPLES</span></span>

### <span data-ttu-id="44743-110">範例1</span><span class="sxs-lookup"><span data-stu-id="44743-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="44743-111">重新開機已損壞的基礎結構角色。</span><span class="sxs-lookup"><span data-stu-id="44743-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="44743-112">參數</span><span class="sxs-lookup"><span data-stu-id="44743-112">PARAMETERS</span></span>

### <span data-ttu-id="44743-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="44743-113">-Name</span></span>
<span data-ttu-id="44743-114">結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="44743-114">Infrastructure role name.</span></span>

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

### <span data-ttu-id="44743-115">-位置</span><span class="sxs-lookup"><span data-stu-id="44743-115">-Location</span></span>
<span data-ttu-id="44743-116">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="44743-116">Location of the resource.</span></span>

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

### <span data-ttu-id="44743-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44743-117">-ResourceGroupName</span></span>
<span data-ttu-id="44743-118">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="44743-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="44743-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44743-119">-ResourceId</span></span>
<span data-ttu-id="44743-120">結構角色資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="44743-120">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="44743-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44743-121">-AsJob</span></span>
<span data-ttu-id="44743-122">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="44743-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="44743-123">-Force</span><span class="sxs-lookup"><span data-stu-id="44743-123">-Force</span></span>
<span data-ttu-id="44743-124">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="44743-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="44743-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44743-125">-WhatIf</span></span>
<span data-ttu-id="44743-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="44743-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44743-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="44743-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44743-128">-確認</span><span class="sxs-lookup"><span data-stu-id="44743-128">-Confirm</span></span>
<span data-ttu-id="44743-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="44743-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44743-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44743-130">CommonParameters</span></span>
<span data-ttu-id="44743-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="44743-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44743-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="44743-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44743-133">輸入</span><span class="sxs-lookup"><span data-stu-id="44743-133">INPUTS</span></span>

## <span data-ttu-id="44743-134">輸出</span><span class="sxs-lookup"><span data-stu-id="44743-134">OUTPUTS</span></span>

## <span data-ttu-id="44743-135">筆記</span><span class="sxs-lookup"><span data-stu-id="44743-135">NOTES</span></span>

## <span data-ttu-id="44743-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="44743-136">RELATED LINKS</span></span>