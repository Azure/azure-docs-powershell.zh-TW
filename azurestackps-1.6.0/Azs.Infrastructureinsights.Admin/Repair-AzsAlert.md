---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b06ae4189b427686f4237c1a6eae841fcaba5c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443016"
---
# <span data-ttu-id="a7ace-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="a7ace-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="a7ace-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7ace-102">SYNOPSIS</span></span>
<span data-ttu-id="a7ace-103">修復指定的警示。</span><span class="sxs-lookup"><span data-stu-id="a7ace-103">Repairs the given alert.</span></span>

## <span data-ttu-id="a7ace-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7ace-104">SYNTAX</span></span>

### <span data-ttu-id="a7ace-105">修復 (預設) </span><span class="sxs-lookup"><span data-stu-id="a7ace-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7ace-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a7ace-106">InputObject</span></span>
```
Repair-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7ace-107">說明</span><span class="sxs-lookup"><span data-stu-id="a7ace-107">DESCRIPTION</span></span>
<span data-ttu-id="a7ace-108">修復指定的警示。</span><span class="sxs-lookup"><span data-stu-id="a7ace-108">Repairs the given alert.</span></span>

## <span data-ttu-id="a7ace-109">示例</span><span class="sxs-lookup"><span data-stu-id="a7ace-109">EXAMPLES</span></span>

### <span data-ttu-id="a7ace-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a7ace-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="a7ace-111">透過名稱來修復警示。</span><span class="sxs-lookup"><span data-stu-id="a7ace-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="a7ace-112">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a7ace-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="a7ace-113">透過 [管道] 修復警示。</span><span class="sxs-lookup"><span data-stu-id="a7ace-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="a7ace-114">參數</span><span class="sxs-lookup"><span data-stu-id="a7ace-114">PARAMETERS</span></span>

### <span data-ttu-id="a7ace-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a7ace-115">-Force</span></span>
<span data-ttu-id="a7ace-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="a7ace-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a7ace-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7ace-117">-InputObject</span></span>
<span data-ttu-id="a7ace-118">從 [取得 AzsAlert] 傳回的警示。</span><span class="sxs-lookup"><span data-stu-id="a7ace-118">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="a7ace-119">-位置</span><span class="sxs-lookup"><span data-stu-id="a7ace-119">-Location</span></span>
<span data-ttu-id="a7ace-120">位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7ace-120">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ace-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a7ace-121">-Name</span></span>
<span data-ttu-id="a7ace-122">警報識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7ace-122">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ace-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7ace-123">-ResourceGroupName</span></span>
<span data-ttu-id="a7ace-124">資源所駐留的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a7ace-124">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ace-125">-確認</span><span class="sxs-lookup"><span data-stu-id="a7ace-125">-Confirm</span></span>
<span data-ttu-id="a7ace-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a7ace-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7ace-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7ace-127">-WhatIf</span></span>
<span data-ttu-id="a7ace-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a7ace-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7ace-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7ace-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7ace-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7ace-130">CommonParameters</span></span>
<span data-ttu-id="a7ace-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7ace-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7ace-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a7ace-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7ace-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a7ace-133">INPUTS</span></span>

## <span data-ttu-id="a7ace-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a7ace-134">OUTPUTS</span></span>

## <span data-ttu-id="a7ace-135">筆記</span><span class="sxs-lookup"><span data-stu-id="a7ace-135">NOTES</span></span>

## <span data-ttu-id="a7ace-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7ace-136">RELATED LINKS</span></span>

