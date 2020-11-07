---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab432625ab6af4a8fbd23895cb82e1d9f83954c8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968377"
---
# <span data-ttu-id="5f767-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="5f767-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="5f767-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f767-102">SYNOPSIS</span></span>
<span data-ttu-id="5f767-103">在更新位置套用特定更新。</span><span class="sxs-lookup"><span data-stu-id="5f767-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="5f767-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f767-104">SYNTAX</span></span>

### <span data-ttu-id="5f767-105">套用 (預設) </span><span class="sxs-lookup"><span data-stu-id="5f767-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f767-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f767-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f767-107">說明</span><span class="sxs-lookup"><span data-stu-id="5f767-107">DESCRIPTION</span></span>
<span data-ttu-id="5f767-108">在更新位置套用特定更新。</span><span class="sxs-lookup"><span data-stu-id="5f767-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="5f767-109">呼叫後，可能會使用 Get-AzsUpdateRun 來修改更新的進度。</span><span class="sxs-lookup"><span data-stu-id="5f767-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="5f767-110">示例</span><span class="sxs-lookup"><span data-stu-id="5f767-110">EXAMPLES</span></span>

### <span data-ttu-id="5f767-111">範例1</span><span class="sxs-lookup"><span data-stu-id="5f767-111">EXAMPLE 1</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="5f767-112">在更新位置套用特定更新。</span><span class="sxs-lookup"><span data-stu-id="5f767-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="5f767-113">參數</span><span class="sxs-lookup"><span data-stu-id="5f767-113">PARAMETERS</span></span>

### <span data-ttu-id="5f767-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="5f767-114">-Name</span></span>
<span data-ttu-id="5f767-115">更新的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f767-115">Name of the update.</span></span>

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

### <span data-ttu-id="5f767-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f767-116">-ResourceGroupName</span></span>
<span data-ttu-id="5f767-117">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5f767-117">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="5f767-118">-位置</span><span class="sxs-lookup"><span data-stu-id="5f767-118">-Location</span></span>
<span data-ttu-id="5f767-119">更新位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f767-119">The name of the update location.</span></span>

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

### <span data-ttu-id="5f767-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f767-120">-AsJob</span></span>
<span data-ttu-id="5f767-121">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="5f767-121">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="5f767-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f767-122">-ResourceId</span></span>
<span data-ttu-id="5f767-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="5f767-123">The resource id.</span></span>

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

### <span data-ttu-id="5f767-124">-Force</span><span class="sxs-lookup"><span data-stu-id="5f767-124">-Force</span></span>
<span data-ttu-id="5f767-125">[標誌] 可移除專案而不需確認。</span><span class="sxs-lookup"><span data-stu-id="5f767-125">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="5f767-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f767-126">-WhatIf</span></span>
<span data-ttu-id="5f767-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5f767-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f767-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f767-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f767-129">-確認</span><span class="sxs-lookup"><span data-stu-id="5f767-129">-Confirm</span></span>
<span data-ttu-id="5f767-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5f767-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f767-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f767-131">CommonParameters</span></span>
<span data-ttu-id="5f767-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f767-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f767-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5f767-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f767-134">輸入</span><span class="sxs-lookup"><span data-stu-id="5f767-134">INPUTS</span></span>

## <span data-ttu-id="5f767-135">輸出</span><span class="sxs-lookup"><span data-stu-id="5f767-135">OUTPUTS</span></span>

### <span data-ttu-id="5f767-136">AzureStack 更新. 系統管理模型。</span><span class="sxs-lookup"><span data-stu-id="5f767-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="5f767-137">筆記</span><span class="sxs-lookup"><span data-stu-id="5f767-137">NOTES</span></span>

## <span data-ttu-id="5f767-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f767-138">RELATED LINKS</span></span>
