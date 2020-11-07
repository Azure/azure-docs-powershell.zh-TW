---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06f2d231754fc422115cf800ef66189378e0cd4d
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793553"
---
# <span data-ttu-id="9d8d0-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="9d8d0-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="9d8d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d8d0-102">SYNOPSIS</span></span>
<span data-ttu-id="9d8d0-103">傳回受管理磁片遷移作業的清單。</span><span class="sxs-lookup"><span data-stu-id="9d8d0-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="9d8d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d8d0-104">SYNTAX</span></span>

### <span data-ttu-id="9d8d0-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="9d8d0-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="9d8d0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d8d0-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="9d8d0-107">獲取</span><span class="sxs-lookup"><span data-stu-id="9d8d0-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="9d8d0-108">說明</span><span class="sxs-lookup"><span data-stu-id="9d8d0-108">DESCRIPTION</span></span>
<span data-ttu-id="9d8d0-109">傳回磁片遷移作業的清單。</span><span class="sxs-lookup"><span data-stu-id="9d8d0-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="9d8d0-110">示例</span><span class="sxs-lookup"><span data-stu-id="9d8d0-110">EXAMPLES</span></span>

### <span data-ttu-id="9d8d0-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9d8d0-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="9d8d0-112">取得特定的受管理磁片遷移作業。</span><span class="sxs-lookup"><span data-stu-id="9d8d0-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="9d8d0-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="9d8d0-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="9d8d0-114">傳回本機位置的受管理磁片遷移作業清單。</span><span class="sxs-lookup"><span data-stu-id="9d8d0-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="9d8d0-115">參數</span><span class="sxs-lookup"><span data-stu-id="9d8d0-115">PARAMETERS</span></span>

### <span data-ttu-id="9d8d0-116">-位置</span><span class="sxs-lookup"><span data-stu-id="9d8d0-116">-Location</span></span>
<span data-ttu-id="9d8d0-117">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="9d8d0-117">Location of the resource.</span></span>

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

### <span data-ttu-id="9d8d0-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d8d0-118">-Name</span></span>
<span data-ttu-id="9d8d0-119">[遷移作業 guid] 名稱。</span><span class="sxs-lookup"><span data-stu-id="9d8d0-119">The migration job guid name.</span></span>

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

### <span data-ttu-id="9d8d0-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d8d0-120">-ResourceId</span></span>
<span data-ttu-id="9d8d0-121">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="9d8d0-121">The resource id.</span></span>

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

### <span data-ttu-id="9d8d0-122">-狀態</span><span class="sxs-lookup"><span data-stu-id="9d8d0-122">-Status</span></span>
<span data-ttu-id="9d8d0-123">磁片遷移作業狀態的參數。</span><span class="sxs-lookup"><span data-stu-id="9d8d0-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="9d8d0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d8d0-124">CommonParameters</span></span>
<span data-ttu-id="9d8d0-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d8d0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d8d0-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9d8d0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d8d0-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9d8d0-127">INPUTS</span></span>

## <span data-ttu-id="9d8d0-128">輸出</span><span class="sxs-lookup"><span data-stu-id="9d8d0-128">OUTPUTS</span></span>

### <span data-ttu-id="9d8d0-129">AzureStack （DiskMigrationJob）的計算。</span><span class="sxs-lookup"><span data-stu-id="9d8d0-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="9d8d0-130">筆記</span><span class="sxs-lookup"><span data-stu-id="9d8d0-130">NOTES</span></span>

## <span data-ttu-id="9d8d0-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d8d0-131">RELATED LINKS</span></span>

