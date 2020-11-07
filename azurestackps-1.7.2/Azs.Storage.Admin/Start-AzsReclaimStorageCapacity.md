---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c7ec31ce2af23a4376f8b5f94deca302345e81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793227"
---
# <span data-ttu-id="5da05-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="5da05-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="5da05-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5da05-102">SYNOPSIS</span></span>
<span data-ttu-id="5da05-103">在已刪除的儲存空間物件上啟動垃圾收集。</span><span class="sxs-lookup"><span data-stu-id="5da05-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="5da05-104">句法</span><span class="sxs-lookup"><span data-stu-id="5da05-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5da05-105">說明</span><span class="sxs-lookup"><span data-stu-id="5da05-105">DESCRIPTION</span></span>
<span data-ttu-id="5da05-106">在已刪除的儲存空間物件上啟動垃圾收集。</span><span class="sxs-lookup"><span data-stu-id="5da05-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="5da05-107">示例</span><span class="sxs-lookup"><span data-stu-id="5da05-107">EXAMPLES</span></span>

### <span data-ttu-id="5da05-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5da05-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="5da05-109">啟動垃圾收集。</span><span class="sxs-lookup"><span data-stu-id="5da05-109">Start garbage collection.</span></span>

## <span data-ttu-id="5da05-110">參數</span><span class="sxs-lookup"><span data-stu-id="5da05-110">PARAMETERS</span></span>

### <span data-ttu-id="5da05-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5da05-111">-AsJob</span></span>
<span data-ttu-id="5da05-112">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="5da05-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="5da05-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="5da05-113">-FarmName</span></span>
<span data-ttu-id="5da05-114">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="5da05-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da05-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5da05-115">-Force</span></span>
<span data-ttu-id="5da05-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="5da05-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5da05-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5da05-117">-ResourceGroupName</span></span>
<span data-ttu-id="5da05-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="5da05-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da05-119">-確認</span><span class="sxs-lookup"><span data-stu-id="5da05-119">-Confirm</span></span>
<span data-ttu-id="5da05-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5da05-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5da05-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5da05-121">-WhatIf</span></span>
<span data-ttu-id="5da05-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5da05-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5da05-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5da05-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5da05-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da05-124">CommonParameters</span></span>
<span data-ttu-id="5da05-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5da05-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da05-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5da05-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da05-127">輸入</span><span class="sxs-lookup"><span data-stu-id="5da05-127">INPUTS</span></span>

## <span data-ttu-id="5da05-128">輸出</span><span class="sxs-lookup"><span data-stu-id="5da05-128">OUTPUTS</span></span>

## <span data-ttu-id="5da05-129">筆記</span><span class="sxs-lookup"><span data-stu-id="5da05-129">NOTES</span></span>

## <span data-ttu-id="5da05-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="5da05-130">RELATED LINKS</span></span>

