---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f7f40982a4c7d24e02e7e365163cc6250ff8791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443315"
---
# <span data-ttu-id="10c82-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="10c82-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="10c82-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10c82-102">SYNOPSIS</span></span>
<span data-ttu-id="10c82-103">依名稱刪除配額。</span><span class="sxs-lookup"><span data-stu-id="10c82-103">Delete a quota by name.</span></span>

## <span data-ttu-id="10c82-104">句法</span><span class="sxs-lookup"><span data-stu-id="10c82-104">SYNTAX</span></span>

### <span data-ttu-id="10c82-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="10c82-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10c82-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="10c82-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10c82-107">說明</span><span class="sxs-lookup"><span data-stu-id="10c82-107">DESCRIPTION</span></span>
<span data-ttu-id="10c82-108">依名稱刪除配額。</span><span class="sxs-lookup"><span data-stu-id="10c82-108">Delete a quota by name.</span></span>

## <span data-ttu-id="10c82-109">示例</span><span class="sxs-lookup"><span data-stu-id="10c82-109">EXAMPLES</span></span>

### <span data-ttu-id="10c82-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="10c82-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="10c82-111">依名稱移除網路配額。</span><span class="sxs-lookup"><span data-stu-id="10c82-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="10c82-112">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="10c82-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="10c82-113">使用管道移除網路配額。</span><span class="sxs-lookup"><span data-stu-id="10c82-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="10c82-114">--------------------------範例 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="10c82-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="10c82-115">移除網路配額。</span><span class="sxs-lookup"><span data-stu-id="10c82-115">Remove a network quota.</span></span>

## <span data-ttu-id="10c82-116">參數</span><span class="sxs-lookup"><span data-stu-id="10c82-116">PARAMETERS</span></span>

### <span data-ttu-id="10c82-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10c82-117">-AsJob</span></span>
<span data-ttu-id="10c82-118">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="10c82-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="10c82-119">-Force</span><span class="sxs-lookup"><span data-stu-id="10c82-119">-Force</span></span>
<span data-ttu-id="10c82-120">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="10c82-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="10c82-121">-位置</span><span class="sxs-lookup"><span data-stu-id="10c82-121">-Location</span></span>
<span data-ttu-id="10c82-122">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="10c82-122">Location of the resource.</span></span>

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

### <span data-ttu-id="10c82-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="10c82-123">-Name</span></span>
<span data-ttu-id="10c82-124">資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="10c82-124">Name of the resource.</span></span>

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

### <span data-ttu-id="10c82-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10c82-125">-ResourceId</span></span>
<span data-ttu-id="10c82-126">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="10c82-126">The resource id.</span></span>

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

### <span data-ttu-id="10c82-127">-確認</span><span class="sxs-lookup"><span data-stu-id="10c82-127">-Confirm</span></span>
<span data-ttu-id="10c82-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10c82-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10c82-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10c82-129">-WhatIf</span></span>
<span data-ttu-id="10c82-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10c82-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10c82-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10c82-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10c82-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c82-132">CommonParameters</span></span>
<span data-ttu-id="10c82-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10c82-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c82-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="10c82-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c82-135">輸入</span><span class="sxs-lookup"><span data-stu-id="10c82-135">INPUTS</span></span>

## <span data-ttu-id="10c82-136">輸出</span><span class="sxs-lookup"><span data-stu-id="10c82-136">OUTPUTS</span></span>

## <span data-ttu-id="10c82-137">筆記</span><span class="sxs-lookup"><span data-stu-id="10c82-137">NOTES</span></span>

## <span data-ttu-id="10c82-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="10c82-138">RELATED LINKS</span></span>
