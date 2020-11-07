---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b639a09789960393ac26d035a80157069dbaaa
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968135"
---
# <span data-ttu-id="df0f8-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="df0f8-101">Get-AzsDisk</span></span>

## <span data-ttu-id="df0f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df0f8-102">SYNOPSIS</span></span>
<span data-ttu-id="df0f8-103">傳回可在指定的共用中遷移的受管理磁片清單。</span><span class="sxs-lookup"><span data-stu-id="df0f8-103">Returns the list of managed disks which can be migrated in the specified share.</span></span>

## <span data-ttu-id="df0f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="df0f8-104">SYNTAX</span></span>

### <span data-ttu-id="df0f8-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="df0f8-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### <span data-ttu-id="df0f8-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="df0f8-106">ResourceId</span></span>
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="df0f8-107">獲取</span><span class="sxs-lookup"><span data-stu-id="df0f8-107">Get</span></span>
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="df0f8-108">說明</span><span class="sxs-lookup"><span data-stu-id="df0f8-108">DESCRIPTION</span></span>
<span data-ttu-id="df0f8-109">傳回磁片清單。</span><span class="sxs-lookup"><span data-stu-id="df0f8-109">Returns a list of disks.</span></span>

## <span data-ttu-id="df0f8-110">示例</span><span class="sxs-lookup"><span data-stu-id="df0f8-110">EXAMPLES</span></span>

### <span data-ttu-id="df0f8-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="df0f8-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$disks = Get-AzsDisk -location local
```

<span data-ttu-id="df0f8-112">傳回本機位置的受管理磁片清單。</span><span class="sxs-lookup"><span data-stu-id="df0f8-112">Returns a list of managed disks at the location local.</span></span>
<span data-ttu-id="df0f8-113">根據預設，它會是第一個100磁片</span><span class="sxs-lookup"><span data-stu-id="df0f8-113">By default, it will the first 100 disks</span></span>

### <span data-ttu-id="df0f8-114">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="df0f8-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$disk = Get-AzsDisk -location local -name $DiskId
```

<span data-ttu-id="df0f8-115">取得特定的受管理磁片。</span><span class="sxs-lookup"><span data-stu-id="df0f8-115">Get a specific managed disk.</span></span>

## <span data-ttu-id="df0f8-116">參數</span><span class="sxs-lookup"><span data-stu-id="df0f8-116">PARAMETERS</span></span>

### <span data-ttu-id="df0f8-117">-Count</span><span class="sxs-lookup"><span data-stu-id="df0f8-117">-Count</span></span>
<span data-ttu-id="df0f8-118">要傳回的磁片數量上限。</span><span class="sxs-lookup"><span data-stu-id="df0f8-118">The maximum number of disks to return.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df0f8-119">-位置</span><span class="sxs-lookup"><span data-stu-id="df0f8-119">-Location</span></span>
<span data-ttu-id="df0f8-120">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="df0f8-120">Location of the resource.</span></span>

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

### <span data-ttu-id="df0f8-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="df0f8-121">-Name</span></span>
<span data-ttu-id="df0f8-122">以身分識別的磁片 guid。</span><span class="sxs-lookup"><span data-stu-id="df0f8-122">The disk guid as identity.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df0f8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df0f8-123">-ResourceId</span></span>
<span data-ttu-id="df0f8-124">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="df0f8-124">The resource id.</span></span>

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

### <span data-ttu-id="df0f8-125">-SharePath</span><span class="sxs-lookup"><span data-stu-id="df0f8-125">-SharePath</span></span>
<span data-ttu-id="df0f8-126">資源所屬的來源共用。</span><span class="sxs-lookup"><span data-stu-id="df0f8-126">The source share which the resource belongs to.</span></span>

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

### <span data-ttu-id="df0f8-127">-開始</span><span class="sxs-lookup"><span data-stu-id="df0f8-127">-Start</span></span>
<span data-ttu-id="df0f8-128">Query 中磁片的起始索引。</span><span class="sxs-lookup"><span data-stu-id="df0f8-128">The start index of disks in query.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df0f8-129">-狀態</span><span class="sxs-lookup"><span data-stu-id="df0f8-129">-Status</span></span>
<span data-ttu-id="df0f8-130">磁片狀態的參數。</span><span class="sxs-lookup"><span data-stu-id="df0f8-130">The parameters of disk state.</span></span>

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

### <span data-ttu-id="df0f8-131">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df0f8-131">-UserSubscriptionId</span></span>
<span data-ttu-id="df0f8-132">資源所屬的租使用者訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="df0f8-132">Tenant Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="df0f8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df0f8-133">CommonParameters</span></span>
<span data-ttu-id="df0f8-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df0f8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df0f8-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="df0f8-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df0f8-136">輸入</span><span class="sxs-lookup"><span data-stu-id="df0f8-136">INPUTS</span></span>

## <span data-ttu-id="df0f8-137">輸出</span><span class="sxs-lookup"><span data-stu-id="df0f8-137">OUTPUTS</span></span>

### <span data-ttu-id="df0f8-138">AzureStack 的計算. 系統管理模型. 磁片</span><span class="sxs-lookup"><span data-stu-id="df0f8-138">Microsoft.AzureStack.Management.Compute.Admin.Models.Disk</span></span>

## <span data-ttu-id="df0f8-139">筆記</span><span class="sxs-lookup"><span data-stu-id="df0f8-139">NOTES</span></span>

## <span data-ttu-id="df0f8-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="df0f8-140">RELATED LINKS</span></span>

