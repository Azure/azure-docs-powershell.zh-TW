---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0983e05a36de72148571ccbbc7f1454343ad393a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968080"
---
# <span data-ttu-id="decad-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="decad-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="decad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="decad-102">SYNOPSIS</span></span>
<span data-ttu-id="decad-103">刪除現有的配額</span><span class="sxs-lookup"><span data-stu-id="decad-103">Delete an existing quota</span></span>

## <span data-ttu-id="decad-104">句法</span><span class="sxs-lookup"><span data-stu-id="decad-104">SYNTAX</span></span>

### <span data-ttu-id="decad-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="decad-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="decad-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="decad-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="decad-107">說明</span><span class="sxs-lookup"><span data-stu-id="decad-107">DESCRIPTION</span></span>
<span data-ttu-id="decad-108">刪除現有的配額</span><span class="sxs-lookup"><span data-stu-id="decad-108">Delete an existing quota</span></span>

## <span data-ttu-id="decad-109">示例</span><span class="sxs-lookup"><span data-stu-id="decad-109">EXAMPLES</span></span>

### <span data-ttu-id="decad-110">範例1</span><span class="sxs-lookup"><span data-stu-id="decad-110">EXAMPLE 1</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="decad-111">依名稱移除儲存配額。</span><span class="sxs-lookup"><span data-stu-id="decad-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="decad-112">範例2</span><span class="sxs-lookup"><span data-stu-id="decad-112">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="decad-113">依管道移除儲存配額。</span><span class="sxs-lookup"><span data-stu-id="decad-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="decad-114">參數</span><span class="sxs-lookup"><span data-stu-id="decad-114">PARAMETERS</span></span>

### <span data-ttu-id="decad-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="decad-115">-Name</span></span>
<span data-ttu-id="decad-116">儲存配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="decad-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="decad-117">-位置</span><span class="sxs-lookup"><span data-stu-id="decad-117">-Location</span></span>
<span data-ttu-id="decad-118">資源位置。</span><span class="sxs-lookup"><span data-stu-id="decad-118">Resource location.</span></span>

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

### <span data-ttu-id="decad-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="decad-119">-ResourceId</span></span>
<span data-ttu-id="decad-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="decad-120">The resource id.</span></span>

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

### <span data-ttu-id="decad-121">-Force</span><span class="sxs-lookup"><span data-stu-id="decad-121">-Force</span></span>
<span data-ttu-id="decad-122">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="decad-122">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="decad-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="decad-123">-WhatIf</span></span>
<span data-ttu-id="decad-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="decad-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="decad-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="decad-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="decad-126">-確認</span><span class="sxs-lookup"><span data-stu-id="decad-126">-Confirm</span></span>
<span data-ttu-id="decad-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="decad-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="decad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="decad-128">CommonParameters</span></span>
<span data-ttu-id="decad-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="decad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="decad-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="decad-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="decad-131">輸入</span><span class="sxs-lookup"><span data-stu-id="decad-131">INPUTS</span></span>

## <span data-ttu-id="decad-132">輸出</span><span class="sxs-lookup"><span data-stu-id="decad-132">OUTPUTS</span></span>

## <span data-ttu-id="decad-133">筆記</span><span class="sxs-lookup"><span data-stu-id="decad-133">NOTES</span></span>

## <span data-ttu-id="decad-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="decad-134">RELATED LINKS</span></span>
