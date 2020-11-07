---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14885871139eaed1c901312b9540a90d385795e5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968368"
---
# <span data-ttu-id="0603d-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="0603d-101">Close-AzsAlert</span></span>

## <span data-ttu-id="0603d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0603d-102">SYNOPSIS</span></span>
<span data-ttu-id="0603d-103">關閉指定的警示。</span><span class="sxs-lookup"><span data-stu-id="0603d-103">Closes the given alert.</span></span>

## <span data-ttu-id="0603d-104">句法</span><span class="sxs-lookup"><span data-stu-id="0603d-104">SYNTAX</span></span>

### <span data-ttu-id="0603d-105">關閉 (預設) </span><span class="sxs-lookup"><span data-stu-id="0603d-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0603d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0603d-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0603d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0603d-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0603d-108">說明</span><span class="sxs-lookup"><span data-stu-id="0603d-108">DESCRIPTION</span></span>
<span data-ttu-id="0603d-109">關閉指定的警示。</span><span class="sxs-lookup"><span data-stu-id="0603d-109">Closes the given alert.</span></span>

## <span data-ttu-id="0603d-110">示例</span><span class="sxs-lookup"><span data-stu-id="0603d-110">EXAMPLES</span></span>

### <span data-ttu-id="0603d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0603d-111">EXAMPLE 1</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="0603d-112">依名稱關閉警示。</span><span class="sxs-lookup"><span data-stu-id="0603d-112">Close an alert by Name.</span></span>

### <span data-ttu-id="0603d-113">範例2</span><span class="sxs-lookup"><span data-stu-id="0603d-113">EXAMPLE 2</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="0603d-114">透過 [管道] 關閉警示。</span><span class="sxs-lookup"><span data-stu-id="0603d-114">Close an alert through piping.</span></span>

## <span data-ttu-id="0603d-115">參數</span><span class="sxs-lookup"><span data-stu-id="0603d-115">PARAMETERS</span></span>

### <span data-ttu-id="0603d-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="0603d-116">-Name</span></span>
<span data-ttu-id="0603d-117">警報識別碼。</span><span class="sxs-lookup"><span data-stu-id="0603d-117">The alert identifier.</span></span>

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

### <span data-ttu-id="0603d-118">-位置</span><span class="sxs-lookup"><span data-stu-id="0603d-118">-Location</span></span>
<span data-ttu-id="0603d-119">位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="0603d-119">Name of the location.</span></span>

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

### <span data-ttu-id="0603d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0603d-120">-ResourceGroupName</span></span>
<span data-ttu-id="0603d-121">提醒的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0603d-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="0603d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0603d-122">-InputObject</span></span>
<span data-ttu-id="0603d-123">從 [取得 AzsAlert] 傳回的警示。</span><span class="sxs-lookup"><span data-stu-id="0603d-123">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="0603d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0603d-124">-ResourceId</span></span>
<span data-ttu-id="0603d-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="0603d-125">The resource id.</span></span>

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

### <span data-ttu-id="0603d-126">-Force</span><span class="sxs-lookup"><span data-stu-id="0603d-126">-Force</span></span>
<span data-ttu-id="0603d-127">不要求確認的切換參數。</span><span class="sxs-lookup"><span data-stu-id="0603d-127">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="0603d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0603d-128">-WhatIf</span></span>
<span data-ttu-id="0603d-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0603d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0603d-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0603d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0603d-131">-確認</span><span class="sxs-lookup"><span data-stu-id="0603d-131">-Confirm</span></span>
<span data-ttu-id="0603d-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0603d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0603d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0603d-133">CommonParameters</span></span>
<span data-ttu-id="0603d-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0603d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0603d-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0603d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0603d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="0603d-136">INPUTS</span></span>

## <span data-ttu-id="0603d-137">輸出</span><span class="sxs-lookup"><span data-stu-id="0603d-137">OUTPUTS</span></span>

### <span data-ttu-id="0603d-138">AzureStack InfrastructureInsights. Alert. 警示</span><span class="sxs-lookup"><span data-stu-id="0603d-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="0603d-139">筆記</span><span class="sxs-lookup"><span data-stu-id="0603d-139">NOTES</span></span>

## <span data-ttu-id="0603d-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="0603d-140">RELATED LINKS</span></span>
