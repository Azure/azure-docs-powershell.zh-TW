---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7256c6ffa7dc3b8a227b516faad9482eb44242d5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968398"
---
# <span data-ttu-id="42299-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="42299-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="42299-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42299-102">SYNOPSIS</span></span>
<span data-ttu-id="42299-103">在已刪除的儲存空間物件上啟動垃圾收集。</span><span class="sxs-lookup"><span data-stu-id="42299-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="42299-104">句法</span><span class="sxs-lookup"><span data-stu-id="42299-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42299-105">說明</span><span class="sxs-lookup"><span data-stu-id="42299-105">DESCRIPTION</span></span>
<span data-ttu-id="42299-106">在已刪除的儲存空間物件上啟動垃圾收集。</span><span class="sxs-lookup"><span data-stu-id="42299-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="42299-107">示例</span><span class="sxs-lookup"><span data-stu-id="42299-107">EXAMPLES</span></span>

### <span data-ttu-id="42299-108">範例1</span><span class="sxs-lookup"><span data-stu-id="42299-108">EXAMPLE 1</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="42299-109">啟動垃圾收集。</span><span class="sxs-lookup"><span data-stu-id="42299-109">Start garbage collection.</span></span>

## <span data-ttu-id="42299-110">參數</span><span class="sxs-lookup"><span data-stu-id="42299-110">PARAMETERS</span></span>

### <span data-ttu-id="42299-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42299-111">-ResourceGroupName</span></span>
<span data-ttu-id="42299-112">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="42299-112">Resource group name.</span></span>

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

### <span data-ttu-id="42299-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="42299-113">-FarmName</span></span>
<span data-ttu-id="42299-114">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="42299-114">Farm Id.</span></span>

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

### <span data-ttu-id="42299-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42299-115">-AsJob</span></span>
<span data-ttu-id="42299-116">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="42299-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="42299-117">-Force</span><span class="sxs-lookup"><span data-stu-id="42299-117">-Force</span></span>
<span data-ttu-id="42299-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="42299-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="42299-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42299-119">-WhatIf</span></span>
<span data-ttu-id="42299-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="42299-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42299-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="42299-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42299-122">-確認</span><span class="sxs-lookup"><span data-stu-id="42299-122">-Confirm</span></span>
<span data-ttu-id="42299-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="42299-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42299-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42299-124">CommonParameters</span></span>
<span data-ttu-id="42299-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42299-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42299-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="42299-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42299-127">輸入</span><span class="sxs-lookup"><span data-stu-id="42299-127">INPUTS</span></span>

## <span data-ttu-id="42299-128">輸出</span><span class="sxs-lookup"><span data-stu-id="42299-128">OUTPUTS</span></span>

## <span data-ttu-id="42299-129">筆記</span><span class="sxs-lookup"><span data-stu-id="42299-129">NOTES</span></span>

## <span data-ttu-id="42299-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="42299-130">RELATED LINKS</span></span>
