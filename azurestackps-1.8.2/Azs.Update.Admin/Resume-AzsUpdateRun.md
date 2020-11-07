---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb3b784d079d1de3cec1d4fe3ec50a2853a4b054
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968510"
---
# <span data-ttu-id="eb630-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="eb630-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="eb630-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb630-102">SYNOPSIS</span></span>
<span data-ttu-id="eb630-103">繼續先前啟動失敗的更新執行。</span><span class="sxs-lookup"><span data-stu-id="eb630-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="eb630-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb630-104">SYNTAX</span></span>

### <span data-ttu-id="eb630-105">UpdateRuns_Rerun (預設) </span><span class="sxs-lookup"><span data-stu-id="eb630-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb630-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb630-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb630-107">說明</span><span class="sxs-lookup"><span data-stu-id="eb630-107">DESCRIPTION</span></span>
<span data-ttu-id="eb630-108">繼續先前啟動失敗的更新執行。</span><span class="sxs-lookup"><span data-stu-id="eb630-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="eb630-109">Resumeed 更新執行將會在上次失敗的階段繼續進行。</span><span class="sxs-lookup"><span data-stu-id="eb630-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="eb630-110">示例</span><span class="sxs-lookup"><span data-stu-id="eb630-110">EXAMPLES</span></span>

### <span data-ttu-id="eb630-111">範例1</span><span class="sxs-lookup"><span data-stu-id="eb630-111">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="eb630-112">繼續先前啟動失敗的更新執行。</span><span class="sxs-lookup"><span data-stu-id="eb630-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="eb630-113">參數</span><span class="sxs-lookup"><span data-stu-id="eb630-113">PARAMETERS</span></span>

### <span data-ttu-id="eb630-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb630-114">-Name</span></span>
<span data-ttu-id="eb630-115">更新執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb630-115">Update run identifier.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb630-116">-位置</span><span class="sxs-lookup"><span data-stu-id="eb630-116">-Location</span></span>
<span data-ttu-id="eb630-117">更新位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb630-117">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb630-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb630-118">-ResourceGroupName</span></span>
<span data-ttu-id="eb630-119">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="eb630-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb630-120">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="eb630-120">-UpdateName</span></span>
<span data-ttu-id="eb630-121">此更新的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="eb630-121">Display name of the update.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb630-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb630-122">-AsJob</span></span>
<span data-ttu-id="eb630-123">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="eb630-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="eb630-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb630-124">-ResourceId</span></span>
<span data-ttu-id="eb630-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="eb630-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb630-126">-Force</span><span class="sxs-lookup"><span data-stu-id="eb630-126">-Force</span></span>
<span data-ttu-id="eb630-127">[標誌] 可移除專案而不需確認。</span><span class="sxs-lookup"><span data-stu-id="eb630-127">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="eb630-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb630-128">-WhatIf</span></span>
<span data-ttu-id="eb630-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb630-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb630-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb630-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb630-131">-確認</span><span class="sxs-lookup"><span data-stu-id="eb630-131">-Confirm</span></span>
<span data-ttu-id="eb630-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eb630-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb630-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb630-133">CommonParameters</span></span>
<span data-ttu-id="eb630-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb630-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb630-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eb630-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb630-136">輸入</span><span class="sxs-lookup"><span data-stu-id="eb630-136">INPUTS</span></span>

## <span data-ttu-id="eb630-137">輸出</span><span class="sxs-lookup"><span data-stu-id="eb630-137">OUTPUTS</span></span>

## <span data-ttu-id="eb630-138">筆記</span><span class="sxs-lookup"><span data-stu-id="eb630-138">NOTES</span></span>

## <span data-ttu-id="eb630-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb630-139">RELATED LINKS</span></span>
