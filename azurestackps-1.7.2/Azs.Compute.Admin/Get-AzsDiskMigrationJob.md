---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cf36bf232ae48891b28562313fa2063e14a2be8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792804"
---
# <span data-ttu-id="9b699-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="9b699-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="9b699-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b699-102">SYNOPSIS</span></span>
<span data-ttu-id="9b699-103">傳回受管理磁片遷移作業的清單。</span><span class="sxs-lookup"><span data-stu-id="9b699-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="9b699-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b699-104">SYNTAX</span></span>

### <span data-ttu-id="9b699-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="9b699-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="9b699-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b699-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="9b699-107">獲取</span><span class="sxs-lookup"><span data-stu-id="9b699-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="9b699-108">說明</span><span class="sxs-lookup"><span data-stu-id="9b699-108">DESCRIPTION</span></span>
<span data-ttu-id="9b699-109">傳回磁片遷移作業的清單。</span><span class="sxs-lookup"><span data-stu-id="9b699-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="9b699-110">示例</span><span class="sxs-lookup"><span data-stu-id="9b699-110">EXAMPLES</span></span>

### <span data-ttu-id="9b699-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9b699-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="9b699-112">取得特定的受管理磁片遷移作業。</span><span class="sxs-lookup"><span data-stu-id="9b699-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="9b699-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="9b699-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="9b699-114">傳回本機位置的受管理磁片遷移作業清單。</span><span class="sxs-lookup"><span data-stu-id="9b699-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="9b699-115">參數</span><span class="sxs-lookup"><span data-stu-id="9b699-115">PARAMETERS</span></span>

### <span data-ttu-id="9b699-116">-位置</span><span class="sxs-lookup"><span data-stu-id="9b699-116">-Location</span></span>
<span data-ttu-id="9b699-117">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="9b699-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b699-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b699-118">-Name</span></span>
<span data-ttu-id="9b699-119">[遷移作業 guid] 名稱。</span><span class="sxs-lookup"><span data-stu-id="9b699-119">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b699-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b699-120">-ResourceId</span></span>
<span data-ttu-id="9b699-121">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="9b699-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b699-122">-狀態</span><span class="sxs-lookup"><span data-stu-id="9b699-122">-Status</span></span>
<span data-ttu-id="9b699-123">磁片遷移作業狀態的參數。</span><span class="sxs-lookup"><span data-stu-id="9b699-123">The parameters of disk migration job status.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b699-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b699-124">CommonParameters</span></span>
<span data-ttu-id="9b699-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b699-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b699-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b699-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b699-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9b699-127">INPUTS</span></span>

## <span data-ttu-id="9b699-128">輸出</span><span class="sxs-lookup"><span data-stu-id="9b699-128">OUTPUTS</span></span>

### <span data-ttu-id="9b699-129">AzureStack （DiskMigrationJob）的計算。</span><span class="sxs-lookup"><span data-stu-id="9b699-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="9b699-130">筆記</span><span class="sxs-lookup"><span data-stu-id="9b699-130">NOTES</span></span>

## <span data-ttu-id="9b699-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b699-131">RELATED LINKS</span></span>

