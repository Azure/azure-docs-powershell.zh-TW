---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cc08220a92dce5a49544cf958db79d7243b9ebb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968503"
---
# <span data-ttu-id="f1b33-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="f1b33-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="f1b33-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1b33-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b33-103">建立新的儲存配額。</span><span class="sxs-lookup"><span data-stu-id="f1b33-103">Create a new storage quota.</span></span>

## <span data-ttu-id="f1b33-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1b33-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1b33-105">說明</span><span class="sxs-lookup"><span data-stu-id="f1b33-105">DESCRIPTION</span></span>
<span data-ttu-id="f1b33-106">建立新的儲存配額。</span><span class="sxs-lookup"><span data-stu-id="f1b33-106">Create a new storage quota.</span></span>

## <span data-ttu-id="f1b33-107">示例</span><span class="sxs-lookup"><span data-stu-id="f1b33-107">EXAMPLES</span></span>

### <span data-ttu-id="f1b33-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f1b33-108">EXAMPLE 1</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="f1b33-109">使用指定的值建立新的儲存配額。</span><span class="sxs-lookup"><span data-stu-id="f1b33-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="f1b33-110">參數</span><span class="sxs-lookup"><span data-stu-id="f1b33-110">PARAMETERS</span></span>

### <span data-ttu-id="f1b33-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1b33-111">-Name</span></span>
<span data-ttu-id="f1b33-112">儲存配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1b33-112">The name of the storage quota.</span></span>

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

### <span data-ttu-id="f1b33-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="f1b33-113">-CapacityInGb</span></span>
<span data-ttu-id="f1b33-114">Maxium 容量 (GB) 。</span><span class="sxs-lookup"><span data-stu-id="f1b33-114">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="f1b33-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="f1b33-115">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="f1b33-116">儲存空間帳戶的總數。</span><span class="sxs-lookup"><span data-stu-id="f1b33-116">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="f1b33-117">-位置</span><span class="sxs-lookup"><span data-stu-id="f1b33-117">-Location</span></span>
<span data-ttu-id="f1b33-118">資源位置。</span><span class="sxs-lookup"><span data-stu-id="f1b33-118">Resource location.</span></span>

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

### <span data-ttu-id="f1b33-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1b33-119">-WhatIf</span></span>
<span data-ttu-id="f1b33-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1b33-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1b33-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1b33-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1b33-122">-確認</span><span class="sxs-lookup"><span data-stu-id="f1b33-122">-Confirm</span></span>
<span data-ttu-id="f1b33-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1b33-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1b33-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b33-124">CommonParameters</span></span>
<span data-ttu-id="f1b33-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1b33-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b33-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f1b33-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b33-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f1b33-127">INPUTS</span></span>

## <span data-ttu-id="f1b33-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f1b33-128">OUTPUTS</span></span>

### <span data-ttu-id="f1b33-129">AzureStack （StorageQuota）的</span><span class="sxs-lookup"><span data-stu-id="f1b33-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="f1b33-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f1b33-130">NOTES</span></span>

## <span data-ttu-id="f1b33-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1b33-131">RELATED LINKS</span></span>
