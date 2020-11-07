---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 641017c75243a253a6b9eb0054df7737a674f671
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968460"
---
# <span data-ttu-id="fc3ee-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="fc3ee-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="fc3ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc3ee-102">SYNOPSIS</span></span>
<span data-ttu-id="fc3ee-103">建立或更新現有的儲存配額。</span><span class="sxs-lookup"><span data-stu-id="fc3ee-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="fc3ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc3ee-104">SYNTAX</span></span>

### <span data-ttu-id="fc3ee-105">更新 (預設) </span><span class="sxs-lookup"><span data-stu-id="fc3ee-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc3ee-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc3ee-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc3ee-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="fc3ee-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc3ee-108">說明</span><span class="sxs-lookup"><span data-stu-id="fc3ee-108">DESCRIPTION</span></span>
<span data-ttu-id="fc3ee-109">建立或更新現有的儲存配額。</span><span class="sxs-lookup"><span data-stu-id="fc3ee-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="fc3ee-110">示例</span><span class="sxs-lookup"><span data-stu-id="fc3ee-110">EXAMPLES</span></span>

### <span data-ttu-id="fc3ee-111">範例1</span><span class="sxs-lookup"><span data-stu-id="fc3ee-111">EXAMPLE 1</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="fc3ee-112">更新現有的儲存配額。</span><span class="sxs-lookup"><span data-stu-id="fc3ee-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="fc3ee-113">參數</span><span class="sxs-lookup"><span data-stu-id="fc3ee-113">PARAMETERS</span></span>

### <span data-ttu-id="fc3ee-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc3ee-114">-Name</span></span>
<span data-ttu-id="fc3ee-115">儲存配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc3ee-115">The name of the storage quota.</span></span>

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

### <span data-ttu-id="fc3ee-116">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="fc3ee-116">-CapacityInGb</span></span>
<span data-ttu-id="fc3ee-117">Maxium 容量 (GB) 。</span><span class="sxs-lookup"><span data-stu-id="fc3ee-117">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="fc3ee-118">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="fc3ee-118">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="fc3ee-119">儲存空間帳戶的總數。</span><span class="sxs-lookup"><span data-stu-id="fc3ee-119">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="fc3ee-120">-位置</span><span class="sxs-lookup"><span data-stu-id="fc3ee-120">-Location</span></span>
<span data-ttu-id="fc3ee-121">資源位置。</span><span class="sxs-lookup"><span data-stu-id="fc3ee-121">Resource location.</span></span>

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

### <span data-ttu-id="fc3ee-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc3ee-122">-ResourceId</span></span>
<span data-ttu-id="fc3ee-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="fc3ee-123">The resource id.</span></span>

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

### <span data-ttu-id="fc3ee-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc3ee-124">-InputObject</span></span>
<span data-ttu-id="fc3ee-125">Posbbily 由 AzsStorageQuota 傳回的已修改儲存配額。</span><span class="sxs-lookup"><span data-stu-id="fc3ee-125">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

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

### <span data-ttu-id="fc3ee-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc3ee-126">-WhatIf</span></span>
<span data-ttu-id="fc3ee-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fc3ee-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc3ee-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc3ee-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc3ee-129">-確認</span><span class="sxs-lookup"><span data-stu-id="fc3ee-129">-Confirm</span></span>
<span data-ttu-id="fc3ee-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fc3ee-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc3ee-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc3ee-131">CommonParameters</span></span>
<span data-ttu-id="fc3ee-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc3ee-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc3ee-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fc3ee-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc3ee-134">輸入</span><span class="sxs-lookup"><span data-stu-id="fc3ee-134">INPUTS</span></span>

## <span data-ttu-id="fc3ee-135">輸出</span><span class="sxs-lookup"><span data-stu-id="fc3ee-135">OUTPUTS</span></span>

### <span data-ttu-id="fc3ee-136">AzureStack （StorageQuota）的</span><span class="sxs-lookup"><span data-stu-id="fc3ee-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="fc3ee-137">筆記</span><span class="sxs-lookup"><span data-stu-id="fc3ee-137">NOTES</span></span>

## <span data-ttu-id="fc3ee-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc3ee-138">RELATED LINKS</span></span>
