---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 143f368b73aac490242e42f21ed76ee76ab012dc
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793577"
---
# <span data-ttu-id="1159e-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="1159e-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="1159e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1159e-102">SYNOPSIS</span></span>
<span data-ttu-id="1159e-103">建立新的儲存配額。</span><span class="sxs-lookup"><span data-stu-id="1159e-103">Create a new storage quota.</span></span>

## <span data-ttu-id="1159e-104">句法</span><span class="sxs-lookup"><span data-stu-id="1159e-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1159e-105">說明</span><span class="sxs-lookup"><span data-stu-id="1159e-105">DESCRIPTION</span></span>
<span data-ttu-id="1159e-106">建立新的儲存配額。</span><span class="sxs-lookup"><span data-stu-id="1159e-106">Create a new storage quota.</span></span>

## <span data-ttu-id="1159e-107">示例</span><span class="sxs-lookup"><span data-stu-id="1159e-107">EXAMPLES</span></span>

### <span data-ttu-id="1159e-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1159e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="1159e-109">使用指定的值建立新的儲存配額。</span><span class="sxs-lookup"><span data-stu-id="1159e-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="1159e-110">參數</span><span class="sxs-lookup"><span data-stu-id="1159e-110">PARAMETERS</span></span>

### <span data-ttu-id="1159e-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="1159e-111">-CapacityInGb</span></span>
<span data-ttu-id="1159e-112">Maxium 容量 (GB) 。</span><span class="sxs-lookup"><span data-stu-id="1159e-112">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1159e-113">-位置</span><span class="sxs-lookup"><span data-stu-id="1159e-113">-Location</span></span>
<span data-ttu-id="1159e-114">資源位置。</span><span class="sxs-lookup"><span data-stu-id="1159e-114">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1159e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="1159e-115">-Name</span></span>
<span data-ttu-id="1159e-116">儲存配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="1159e-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="1159e-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="1159e-117">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="1159e-118">儲存空間帳戶的總數。</span><span class="sxs-lookup"><span data-stu-id="1159e-118">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1159e-119">-確認</span><span class="sxs-lookup"><span data-stu-id="1159e-119">-Confirm</span></span>
<span data-ttu-id="1159e-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1159e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1159e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1159e-121">-WhatIf</span></span>
<span data-ttu-id="1159e-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1159e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1159e-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1159e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1159e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1159e-124">CommonParameters</span></span>
<span data-ttu-id="1159e-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1159e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1159e-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1159e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1159e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="1159e-127">INPUTS</span></span>

## <span data-ttu-id="1159e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="1159e-128">OUTPUTS</span></span>

### <span data-ttu-id="1159e-129">AzureStack （StorageQuota）的</span><span class="sxs-lookup"><span data-stu-id="1159e-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="1159e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="1159e-130">NOTES</span></span>

## <span data-ttu-id="1159e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="1159e-131">RELATED LINKS</span></span>

