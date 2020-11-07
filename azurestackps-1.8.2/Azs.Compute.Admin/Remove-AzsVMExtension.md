---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0aa30655a7fa73b6cb53de12f8906ebb59ea5a17
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968231"
---
# <span data-ttu-id="269fd-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="269fd-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="269fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="269fd-102">SYNOPSIS</span></span>
<span data-ttu-id="269fd-103">刪除虛擬機器延伸影像。</span><span class="sxs-lookup"><span data-stu-id="269fd-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="269fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="269fd-104">SYNTAX</span></span>

### <span data-ttu-id="269fd-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="269fd-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="269fd-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="269fd-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="269fd-107">說明</span><span class="sxs-lookup"><span data-stu-id="269fd-107">DESCRIPTION</span></span>
<span data-ttu-id="269fd-108">刪除指定的虛擬電腦延伸影像。</span><span class="sxs-lookup"><span data-stu-id="269fd-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="269fd-109">示例</span><span class="sxs-lookup"><span data-stu-id="269fd-109">EXAMPLES</span></span>

### <span data-ttu-id="269fd-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="269fd-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="269fd-111">移除平臺影像延伸。</span><span class="sxs-lookup"><span data-stu-id="269fd-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="269fd-112">參數</span><span class="sxs-lookup"><span data-stu-id="269fd-112">PARAMETERS</span></span>

### <span data-ttu-id="269fd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="269fd-113">-Force</span></span>
<span data-ttu-id="269fd-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="269fd-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="269fd-115">-位置</span><span class="sxs-lookup"><span data-stu-id="269fd-115">-Location</span></span>
<span data-ttu-id="269fd-116">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="269fd-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="269fd-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="269fd-117">-Publisher</span></span>
<span data-ttu-id="269fd-118">發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="269fd-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="269fd-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="269fd-119">-ResourceId</span></span>
<span data-ttu-id="269fd-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="269fd-120">The resource id.</span></span>

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

### <span data-ttu-id="269fd-121">-類型</span><span class="sxs-lookup"><span data-stu-id="269fd-121">-Type</span></span>
<span data-ttu-id="269fd-122">延伸類型。</span><span class="sxs-lookup"><span data-stu-id="269fd-122">Type of extension.</span></span>

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

### <span data-ttu-id="269fd-123">-版本</span><span class="sxs-lookup"><span data-stu-id="269fd-123">-Version</span></span>
<span data-ttu-id="269fd-124">虛擬機器擴充影像的版本。</span><span class="sxs-lookup"><span data-stu-id="269fd-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="269fd-125">-確認</span><span class="sxs-lookup"><span data-stu-id="269fd-125">-Confirm</span></span>
<span data-ttu-id="269fd-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="269fd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="269fd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="269fd-127">-WhatIf</span></span>
<span data-ttu-id="269fd-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="269fd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="269fd-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="269fd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="269fd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="269fd-130">CommonParameters</span></span>
<span data-ttu-id="269fd-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="269fd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="269fd-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="269fd-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="269fd-133">輸入</span><span class="sxs-lookup"><span data-stu-id="269fd-133">INPUTS</span></span>

## <span data-ttu-id="269fd-134">輸出</span><span class="sxs-lookup"><span data-stu-id="269fd-134">OUTPUTS</span></span>

## <span data-ttu-id="269fd-135">筆記</span><span class="sxs-lookup"><span data-stu-id="269fd-135">NOTES</span></span>

## <span data-ttu-id="269fd-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="269fd-136">RELATED LINKS</span></span>

