---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2eec56d9fc157da994521a5b258cd28132344c52
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793565"
---
# <span data-ttu-id="4bbba-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="4bbba-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="4bbba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4bbba-102">SYNOPSIS</span></span>
<span data-ttu-id="4bbba-103">建立或更新現有的儲存配額。</span><span class="sxs-lookup"><span data-stu-id="4bbba-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="4bbba-104">句法</span><span class="sxs-lookup"><span data-stu-id="4bbba-104">SYNTAX</span></span>

### <span data-ttu-id="4bbba-105">更新 (預設) </span><span class="sxs-lookup"><span data-stu-id="4bbba-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bbba-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bbba-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bbba-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="4bbba-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bbba-108">說明</span><span class="sxs-lookup"><span data-stu-id="4bbba-108">DESCRIPTION</span></span>
<span data-ttu-id="4bbba-109">建立或更新現有的儲存配額。</span><span class="sxs-lookup"><span data-stu-id="4bbba-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="4bbba-110">示例</span><span class="sxs-lookup"><span data-stu-id="4bbba-110">EXAMPLES</span></span>

### <span data-ttu-id="4bbba-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4bbba-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="4bbba-112">更新現有的儲存配額。</span><span class="sxs-lookup"><span data-stu-id="4bbba-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="4bbba-113">參數</span><span class="sxs-lookup"><span data-stu-id="4bbba-113">PARAMETERS</span></span>

### <span data-ttu-id="4bbba-114">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="4bbba-114">-CapacityInGb</span></span>
<span data-ttu-id="4bbba-115">Maxium 容量 (GB) 。</span><span class="sxs-lookup"><span data-stu-id="4bbba-115">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbba-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bbba-116">-InputObject</span></span>
<span data-ttu-id="4bbba-117">Posbbily 由 AzsStorageQuota 傳回的已修改儲存配額。</span><span class="sxs-lookup"><span data-stu-id="4bbba-117">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

```yaml
Type: StorageQuota
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bbba-118">-位置</span><span class="sxs-lookup"><span data-stu-id="4bbba-118">-Location</span></span>
<span data-ttu-id="4bbba-119">資源位置。</span><span class="sxs-lookup"><span data-stu-id="4bbba-119">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbba-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="4bbba-120">-Name</span></span>
<span data-ttu-id="4bbba-121">儲存配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bbba-121">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbba-122">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="4bbba-122">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="4bbba-123">儲存空間帳戶的總數。</span><span class="sxs-lookup"><span data-stu-id="4bbba-123">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbba-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bbba-124">-ResourceId</span></span>
<span data-ttu-id="4bbba-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="4bbba-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bbba-126">-確認</span><span class="sxs-lookup"><span data-stu-id="4bbba-126">-Confirm</span></span>
<span data-ttu-id="4bbba-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4bbba-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bbba-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bbba-128">-WhatIf</span></span>
<span data-ttu-id="4bbba-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4bbba-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bbba-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4bbba-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bbba-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bbba-131">CommonParameters</span></span>
<span data-ttu-id="4bbba-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4bbba-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bbba-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4bbba-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bbba-134">輸入</span><span class="sxs-lookup"><span data-stu-id="4bbba-134">INPUTS</span></span>

## <span data-ttu-id="4bbba-135">輸出</span><span class="sxs-lookup"><span data-stu-id="4bbba-135">OUTPUTS</span></span>

### <span data-ttu-id="4bbba-136">AzureStack （StorageQuota）的</span><span class="sxs-lookup"><span data-stu-id="4bbba-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="4bbba-137">筆記</span><span class="sxs-lookup"><span data-stu-id="4bbba-137">NOTES</span></span>

## <span data-ttu-id="4bbba-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="4bbba-138">RELATED LINKS</span></span>

