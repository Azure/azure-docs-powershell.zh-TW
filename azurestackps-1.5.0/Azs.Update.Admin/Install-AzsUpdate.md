---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4406dc4cadecd1945e82b8a90e9937df2183b4da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443196"
---
# <span data-ttu-id="304c4-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="304c4-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="304c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="304c4-102">SYNOPSIS</span></span>
<span data-ttu-id="304c4-103">在更新位置套用特定更新。</span><span class="sxs-lookup"><span data-stu-id="304c4-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="304c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="304c4-104">SYNTAX</span></span>

### <span data-ttu-id="304c4-105">套用 (預設) </span><span class="sxs-lookup"><span data-stu-id="304c4-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="304c4-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="304c4-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="304c4-107">說明</span><span class="sxs-lookup"><span data-stu-id="304c4-107">DESCRIPTION</span></span>
<span data-ttu-id="304c4-108">在更新位置套用特定更新。</span><span class="sxs-lookup"><span data-stu-id="304c4-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="304c4-109">呼叫後，可能會使用 Get-AzsUpdateRun 來修改更新的進度。</span><span class="sxs-lookup"><span data-stu-id="304c4-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="304c4-110">示例</span><span class="sxs-lookup"><span data-stu-id="304c4-110">EXAMPLES</span></span>

### <span data-ttu-id="304c4-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="304c4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="304c4-112">在更新位置套用特定更新。</span><span class="sxs-lookup"><span data-stu-id="304c4-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="304c4-113">參數</span><span class="sxs-lookup"><span data-stu-id="304c4-113">PARAMETERS</span></span>

### <span data-ttu-id="304c4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="304c4-114">-AsJob</span></span>
<span data-ttu-id="304c4-115">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="304c4-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="304c4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="304c4-116">-Force</span></span>
<span data-ttu-id="304c4-117">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="304c4-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="304c4-118">-位置</span><span class="sxs-lookup"><span data-stu-id="304c4-118">-Location</span></span>
<span data-ttu-id="304c4-119">更新位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="304c4-119">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304c4-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="304c4-120">-Name</span></span>
<span data-ttu-id="304c4-121">更新的名稱。</span><span class="sxs-lookup"><span data-stu-id="304c4-121">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304c4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="304c4-122">-ResourceGroupName</span></span>
<span data-ttu-id="304c4-123">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="304c4-123">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304c4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="304c4-124">-ResourceId</span></span>
<span data-ttu-id="304c4-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="304c4-125">The resource id.</span></span>

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

### <span data-ttu-id="304c4-126">-確認</span><span class="sxs-lookup"><span data-stu-id="304c4-126">-Confirm</span></span>
<span data-ttu-id="304c4-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="304c4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="304c4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="304c4-128">-WhatIf</span></span>
<span data-ttu-id="304c4-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="304c4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="304c4-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="304c4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="304c4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="304c4-131">CommonParameters</span></span>
<span data-ttu-id="304c4-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="304c4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="304c4-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="304c4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="304c4-134">輸入</span><span class="sxs-lookup"><span data-stu-id="304c4-134">INPUTS</span></span>

## <span data-ttu-id="304c4-135">輸出</span><span class="sxs-lookup"><span data-stu-id="304c4-135">OUTPUTS</span></span>

### <span data-ttu-id="304c4-136">AzureStack 更新. 系統管理模型。</span><span class="sxs-lookup"><span data-stu-id="304c4-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="304c4-137">筆記</span><span class="sxs-lookup"><span data-stu-id="304c4-137">NOTES</span></span>

## <span data-ttu-id="304c4-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="304c4-138">RELATED LINKS</span></span>

