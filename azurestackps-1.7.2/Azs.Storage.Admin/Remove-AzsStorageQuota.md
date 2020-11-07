---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b62b8ffbdcdcefff5bbb5c984a19ef0b7cb644
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793042"
---
# <span data-ttu-id="711a9-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="711a9-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="711a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="711a9-102">SYNOPSIS</span></span>
<span data-ttu-id="711a9-103">刪除現有的配額</span><span class="sxs-lookup"><span data-stu-id="711a9-103">Delete an existing quota</span></span>

## <span data-ttu-id="711a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="711a9-104">SYNTAX</span></span>

### <span data-ttu-id="711a9-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="711a9-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="711a9-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="711a9-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="711a9-107">說明</span><span class="sxs-lookup"><span data-stu-id="711a9-107">DESCRIPTION</span></span>
<span data-ttu-id="711a9-108">刪除現有的配額</span><span class="sxs-lookup"><span data-stu-id="711a9-108">Delete an existing quota</span></span>

## <span data-ttu-id="711a9-109">示例</span><span class="sxs-lookup"><span data-stu-id="711a9-109">EXAMPLES</span></span>

### <span data-ttu-id="711a9-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="711a9-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="711a9-111">依名稱移除儲存配額。</span><span class="sxs-lookup"><span data-stu-id="711a9-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="711a9-112">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="711a9-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="711a9-113">依管道移除儲存配額。</span><span class="sxs-lookup"><span data-stu-id="711a9-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="711a9-114">參數</span><span class="sxs-lookup"><span data-stu-id="711a9-114">PARAMETERS</span></span>

### <span data-ttu-id="711a9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="711a9-115">-Force</span></span>
<span data-ttu-id="711a9-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="711a9-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="711a9-117">-位置</span><span class="sxs-lookup"><span data-stu-id="711a9-117">-Location</span></span>
<span data-ttu-id="711a9-118">資源位置。</span><span class="sxs-lookup"><span data-stu-id="711a9-118">Resource location.</span></span>

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

### <span data-ttu-id="711a9-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="711a9-119">-Name</span></span>
<span data-ttu-id="711a9-120">儲存配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="711a9-120">The name of the storage quota.</span></span>

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

### <span data-ttu-id="711a9-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="711a9-121">-ResourceId</span></span>
<span data-ttu-id="711a9-122">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="711a9-122">The resource id.</span></span>

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

### <span data-ttu-id="711a9-123">-確認</span><span class="sxs-lookup"><span data-stu-id="711a9-123">-Confirm</span></span>
<span data-ttu-id="711a9-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="711a9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="711a9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="711a9-125">-WhatIf</span></span>
<span data-ttu-id="711a9-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="711a9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="711a9-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="711a9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="711a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="711a9-128">CommonParameters</span></span>
<span data-ttu-id="711a9-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="711a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="711a9-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="711a9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="711a9-131">輸入</span><span class="sxs-lookup"><span data-stu-id="711a9-131">INPUTS</span></span>

## <span data-ttu-id="711a9-132">輸出</span><span class="sxs-lookup"><span data-stu-id="711a9-132">OUTPUTS</span></span>

## <span data-ttu-id="711a9-133">筆記</span><span class="sxs-lookup"><span data-stu-id="711a9-133">NOTES</span></span>

## <span data-ttu-id="711a9-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="711a9-134">RELATED LINKS</span></span>

