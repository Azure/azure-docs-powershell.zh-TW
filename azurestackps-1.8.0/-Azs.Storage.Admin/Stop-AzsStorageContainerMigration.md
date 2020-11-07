---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81bdb6a75e10af30b6febe9bbbf0989933818aec
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793704"
---
# <span data-ttu-id="80b86-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="80b86-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="80b86-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80b86-102">SYNOPSIS</span></span>
<span data-ttu-id="80b86-103">取消容器遷移作業。</span><span class="sxs-lookup"><span data-stu-id="80b86-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="80b86-104">句法</span><span class="sxs-lookup"><span data-stu-id="80b86-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80b86-105">說明</span><span class="sxs-lookup"><span data-stu-id="80b86-105">DESCRIPTION</span></span>
<span data-ttu-id="80b86-106">取消容器遷移作業。</span><span class="sxs-lookup"><span data-stu-id="80b86-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="80b86-107">示例</span><span class="sxs-lookup"><span data-stu-id="80b86-107">EXAMPLES</span></span>

### <span data-ttu-id="80b86-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="80b86-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="80b86-109">[取消容器遷移]。</span><span class="sxs-lookup"><span data-stu-id="80b86-109">Cancel container migration.</span></span>

## <span data-ttu-id="80b86-110">參數</span><span class="sxs-lookup"><span data-stu-id="80b86-110">PARAMETERS</span></span>

### <span data-ttu-id="80b86-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80b86-111">-AsJob</span></span>
<span data-ttu-id="80b86-112">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="80b86-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="80b86-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="80b86-113">-FarmName</span></span>
<span data-ttu-id="80b86-114">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="80b86-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b86-115">-Force</span><span class="sxs-lookup"><span data-stu-id="80b86-115">-Force</span></span>
<span data-ttu-id="80b86-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="80b86-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="80b86-117">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="80b86-117">-JobId</span></span>
<span data-ttu-id="80b86-118">操作 Id。</span><span class="sxs-lookup"><span data-stu-id="80b86-118">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b86-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80b86-119">-ResourceGroupName</span></span>
<span data-ttu-id="80b86-120">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="80b86-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b86-121">-確認</span><span class="sxs-lookup"><span data-stu-id="80b86-121">-Confirm</span></span>
<span data-ttu-id="80b86-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="80b86-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80b86-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80b86-123">-WhatIf</span></span>
<span data-ttu-id="80b86-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80b86-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80b86-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80b86-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80b86-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b86-126">CommonParameters</span></span>
<span data-ttu-id="80b86-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80b86-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b86-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80b86-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b86-129">輸入</span><span class="sxs-lookup"><span data-stu-id="80b86-129">INPUTS</span></span>

## <span data-ttu-id="80b86-130">輸出</span><span class="sxs-lookup"><span data-stu-id="80b86-130">OUTPUTS</span></span>

## <span data-ttu-id="80b86-131">筆記</span><span class="sxs-lookup"><span data-stu-id="80b86-131">NOTES</span></span>

## <span data-ttu-id="80b86-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="80b86-132">RELATED LINKS</span></span>

