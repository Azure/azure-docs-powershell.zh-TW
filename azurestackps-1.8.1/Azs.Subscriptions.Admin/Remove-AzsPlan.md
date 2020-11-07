---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75010b9591b4211f32c5665aa969bae28d69aaea
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793761"
---
# <span data-ttu-id="941d6-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="941d6-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="941d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="941d6-102">SYNOPSIS</span></span>
<span data-ttu-id="941d6-103">移除指定的方案</span><span class="sxs-lookup"><span data-stu-id="941d6-103">Removes the specified plan</span></span>

## <span data-ttu-id="941d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="941d6-104">SYNTAX</span></span>

### <span data-ttu-id="941d6-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="941d6-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="941d6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="941d6-106">ResourceId</span></span>
```
Remove-AzsPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="941d6-107">說明</span><span class="sxs-lookup"><span data-stu-id="941d6-107">DESCRIPTION</span></span>
<span data-ttu-id="941d6-108">移除指定的方案</span><span class="sxs-lookup"><span data-stu-id="941d6-108">Removes the specified plan</span></span>

## <span data-ttu-id="941d6-109">示例</span><span class="sxs-lookup"><span data-stu-id="941d6-109">EXAMPLES</span></span>

### <span data-ttu-id="941d6-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="941d6-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlan -Name plan1 -ResourceGroupName "rg1"
```

<span data-ttu-id="941d6-111">移除指定的方案</span><span class="sxs-lookup"><span data-stu-id="941d6-111">Removes the specified plan</span></span>

## <span data-ttu-id="941d6-112">參數</span><span class="sxs-lookup"><span data-stu-id="941d6-112">PARAMETERS</span></span>

### <span data-ttu-id="941d6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="941d6-113">-Force</span></span>
<span data-ttu-id="941d6-114">[標誌] 可移除專案而不需確認。</span><span class="sxs-lookup"><span data-stu-id="941d6-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="941d6-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="941d6-115">-Name</span></span>
<span data-ttu-id="941d6-116">方案名稱。</span><span class="sxs-lookup"><span data-stu-id="941d6-116">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941d6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="941d6-117">-ResourceGroupName</span></span>
<span data-ttu-id="941d6-118">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="941d6-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941d6-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="941d6-119">-ResourceId</span></span>
<span data-ttu-id="941d6-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="941d6-120">The resource id.</span></span>

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

### <span data-ttu-id="941d6-121">-確認</span><span class="sxs-lookup"><span data-stu-id="941d6-121">-Confirm</span></span>
<span data-ttu-id="941d6-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="941d6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="941d6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="941d6-123">-WhatIf</span></span>
<span data-ttu-id="941d6-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="941d6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="941d6-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="941d6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="941d6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="941d6-126">CommonParameters</span></span>
<span data-ttu-id="941d6-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="941d6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="941d6-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="941d6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="941d6-129">輸入</span><span class="sxs-lookup"><span data-stu-id="941d6-129">INPUTS</span></span>

## <span data-ttu-id="941d6-130">輸出</span><span class="sxs-lookup"><span data-stu-id="941d6-130">OUTPUTS</span></span>

## <span data-ttu-id="941d6-131">筆記</span><span class="sxs-lookup"><span data-stu-id="941d6-131">NOTES</span></span>

## <span data-ttu-id="941d6-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="941d6-132">RELATED LINKS</span></span>

