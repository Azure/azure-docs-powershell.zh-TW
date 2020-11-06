---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ce97fe1fc7e21f166b1bb86db52bc8ad6e29e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442784"
---
# <span data-ttu-id="4cf81-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="4cf81-101">Close-AzsAlert</span></span>

## <span data-ttu-id="4cf81-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4cf81-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf81-103">關閉指定的警示。</span><span class="sxs-lookup"><span data-stu-id="4cf81-103">Closes the given alert.</span></span>

## <span data-ttu-id="4cf81-104">句法</span><span class="sxs-lookup"><span data-stu-id="4cf81-104">SYNTAX</span></span>

### <span data-ttu-id="4cf81-105">關閉 (預設) </span><span class="sxs-lookup"><span data-stu-id="4cf81-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4cf81-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4cf81-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cf81-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cf81-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cf81-108">說明</span><span class="sxs-lookup"><span data-stu-id="4cf81-108">DESCRIPTION</span></span>
<span data-ttu-id="4cf81-109">關閉指定的警示。</span><span class="sxs-lookup"><span data-stu-id="4cf81-109">Closes the given alert.</span></span>

## <span data-ttu-id="4cf81-110">示例</span><span class="sxs-lookup"><span data-stu-id="4cf81-110">EXAMPLES</span></span>

### <span data-ttu-id="4cf81-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4cf81-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="4cf81-112">依名稱關閉警示。</span><span class="sxs-lookup"><span data-stu-id="4cf81-112">Close an alert by Name.</span></span>

### <span data-ttu-id="4cf81-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="4cf81-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="4cf81-114">透過 [管道] 關閉警示。</span><span class="sxs-lookup"><span data-stu-id="4cf81-114">Close an alert through piping.</span></span>

## <span data-ttu-id="4cf81-115">參數</span><span class="sxs-lookup"><span data-stu-id="4cf81-115">PARAMETERS</span></span>

### <span data-ttu-id="4cf81-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4cf81-116">-Force</span></span>
<span data-ttu-id="4cf81-117">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="4cf81-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4cf81-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cf81-118">-InputObject</span></span>
<span data-ttu-id="4cf81-119">從 [取得 AzsAlert] 傳回的警示。</span><span class="sxs-lookup"><span data-stu-id="4cf81-119">An alert returned from Get-AzsAlert.</span></span>

```yaml
Type: Alert
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf81-120">-位置</span><span class="sxs-lookup"><span data-stu-id="4cf81-120">-Location</span></span>
<span data-ttu-id="4cf81-121">位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cf81-121">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf81-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="4cf81-122">-Name</span></span>
<span data-ttu-id="4cf81-123">警報識別碼。</span><span class="sxs-lookup"><span data-stu-id="4cf81-123">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf81-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cf81-124">-ResourceGroupName</span></span>
<span data-ttu-id="4cf81-125">資源所駐留的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4cf81-125">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf81-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cf81-126">-ResourceId</span></span>
<span data-ttu-id="4cf81-127">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="4cf81-127">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf81-128">-確認</span><span class="sxs-lookup"><span data-stu-id="4cf81-128">-Confirm</span></span>
<span data-ttu-id="4cf81-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4cf81-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cf81-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cf81-130">-WhatIf</span></span>
<span data-ttu-id="4cf81-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4cf81-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cf81-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4cf81-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cf81-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf81-133">CommonParameters</span></span>
<span data-ttu-id="4cf81-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4cf81-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf81-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4cf81-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf81-136">輸入</span><span class="sxs-lookup"><span data-stu-id="4cf81-136">INPUTS</span></span>

## <span data-ttu-id="4cf81-137">輸出</span><span class="sxs-lookup"><span data-stu-id="4cf81-137">OUTPUTS</span></span>

### <span data-ttu-id="4cf81-138">AzureStack InfrastructureInsights. Alert. 警示</span><span class="sxs-lookup"><span data-stu-id="4cf81-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="4cf81-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4cf81-139">NOTES</span></span>

## <span data-ttu-id="4cf81-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cf81-140">RELATED LINKS</span></span>

