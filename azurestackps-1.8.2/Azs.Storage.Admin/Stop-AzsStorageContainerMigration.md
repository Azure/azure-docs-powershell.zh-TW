---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c9a27b1722c1c7f08d9daeab0205dd20d9ba8b9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968049"
---
# <span data-ttu-id="d00cf-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="d00cf-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="d00cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d00cf-102">SYNOPSIS</span></span>
<span data-ttu-id="d00cf-103">取消容器遷移作業。</span><span class="sxs-lookup"><span data-stu-id="d00cf-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="d00cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="d00cf-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d00cf-105">說明</span><span class="sxs-lookup"><span data-stu-id="d00cf-105">DESCRIPTION</span></span>
<span data-ttu-id="d00cf-106">取消容器遷移作業。</span><span class="sxs-lookup"><span data-stu-id="d00cf-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="d00cf-107">示例</span><span class="sxs-lookup"><span data-stu-id="d00cf-107">EXAMPLES</span></span>

### <span data-ttu-id="d00cf-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d00cf-108">EXAMPLE 1</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="d00cf-109">[取消容器遷移]。</span><span class="sxs-lookup"><span data-stu-id="d00cf-109">Cancel container migration.</span></span>

## <span data-ttu-id="d00cf-110">參數</span><span class="sxs-lookup"><span data-stu-id="d00cf-110">PARAMETERS</span></span>

### <span data-ttu-id="d00cf-111">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="d00cf-111">-JobId</span></span>
<span data-ttu-id="d00cf-112">操作 Id。</span><span class="sxs-lookup"><span data-stu-id="d00cf-112">Operation Id.</span></span>

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

### <span data-ttu-id="d00cf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d00cf-113">-ResourceGroupName</span></span>
<span data-ttu-id="d00cf-114">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d00cf-114">Resource group name.</span></span>

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

### <span data-ttu-id="d00cf-115">-FarmName</span><span class="sxs-lookup"><span data-stu-id="d00cf-115">-FarmName</span></span>
<span data-ttu-id="d00cf-116">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="d00cf-116">Farm Id.</span></span>

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

### <span data-ttu-id="d00cf-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d00cf-117">-AsJob</span></span>
<span data-ttu-id="d00cf-118">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="d00cf-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d00cf-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d00cf-119">-Force</span></span>
<span data-ttu-id="d00cf-120">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="d00cf-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d00cf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d00cf-121">-WhatIf</span></span>
<span data-ttu-id="d00cf-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d00cf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d00cf-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d00cf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d00cf-124">-確認</span><span class="sxs-lookup"><span data-stu-id="d00cf-124">-Confirm</span></span>
<span data-ttu-id="d00cf-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d00cf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d00cf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d00cf-126">CommonParameters</span></span>
<span data-ttu-id="d00cf-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d00cf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d00cf-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d00cf-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d00cf-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d00cf-129">INPUTS</span></span>

## <span data-ttu-id="d00cf-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d00cf-130">OUTPUTS</span></span>

## <span data-ttu-id="d00cf-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d00cf-131">NOTES</span></span>

## <span data-ttu-id="d00cf-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d00cf-132">RELATED LINKS</span></span>
