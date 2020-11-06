---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b4e3e69a0c55188514a31dbe7377f8336784b114
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442875"
---
# <span data-ttu-id="fea4f-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fea4f-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="fea4f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fea4f-102">SYNOPSIS</span></span>
<span data-ttu-id="fea4f-103">取消刪除已刪除的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="fea4f-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="fea4f-104">句法</span><span class="sxs-lookup"><span data-stu-id="fea4f-104">SYNTAX</span></span>

### <span data-ttu-id="fea4f-105">取消刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="fea4f-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fea4f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fea4f-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fea4f-107">說明</span><span class="sxs-lookup"><span data-stu-id="fea4f-107">DESCRIPTION</span></span>
<span data-ttu-id="fea4f-108">取消刪除已刪除的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="fea4f-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="fea4f-109">示例</span><span class="sxs-lookup"><span data-stu-id="fea4f-109">EXAMPLES</span></span>

### <span data-ttu-id="fea4f-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fea4f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="fea4f-111">取消刪除已刪除的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="fea4f-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="fea4f-112">參數</span><span class="sxs-lookup"><span data-stu-id="fea4f-112">PARAMETERS</span></span>

### <span data-ttu-id="fea4f-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="fea4f-113">-FarmName</span></span>
<span data-ttu-id="fea4f-114">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="fea4f-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea4f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fea4f-115">-Force</span></span>
<span data-ttu-id="fea4f-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="fea4f-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fea4f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fea4f-117">-Name</span></span>
<span data-ttu-id="fea4f-118">租使用者看不到的內部儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="fea4f-118">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea4f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea4f-119">-ResourceGroupName</span></span>
<span data-ttu-id="fea4f-120">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="fea4f-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea4f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fea4f-121">-ResourceId</span></span>
<span data-ttu-id="fea4f-122">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="fea4f-122">The resource id.</span></span>

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

### <span data-ttu-id="fea4f-123">-確認</span><span class="sxs-lookup"><span data-stu-id="fea4f-123">-Confirm</span></span>
<span data-ttu-id="fea4f-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fea4f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fea4f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fea4f-125">-WhatIf</span></span>
<span data-ttu-id="fea4f-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fea4f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fea4f-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fea4f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fea4f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea4f-128">CommonParameters</span></span>
<span data-ttu-id="fea4f-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fea4f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea4f-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fea4f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea4f-131">輸入</span><span class="sxs-lookup"><span data-stu-id="fea4f-131">INPUTS</span></span>

## <span data-ttu-id="fea4f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="fea4f-132">OUTPUTS</span></span>

## <span data-ttu-id="fea4f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="fea4f-133">NOTES</span></span>

## <span data-ttu-id="fea4f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="fea4f-134">RELATED LINKS</span></span>

