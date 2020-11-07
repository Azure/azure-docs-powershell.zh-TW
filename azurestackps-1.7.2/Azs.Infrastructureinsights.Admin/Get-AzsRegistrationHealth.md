---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d73e2db2f09ba504e9c6adbf15a0bbc2629452ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793380"
---
# <span data-ttu-id="ebc15-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="ebc15-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="ebc15-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ebc15-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc15-103">傳回服務下每個資源的健全性清單。</span><span class="sxs-lookup"><span data-stu-id="ebc15-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="ebc15-104">句法</span><span class="sxs-lookup"><span data-stu-id="ebc15-104">SYNTAX</span></span>

### <span data-ttu-id="ebc15-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="ebc15-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ebc15-106">獲取</span><span class="sxs-lookup"><span data-stu-id="ebc15-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="ebc15-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebc15-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="ebc15-108">說明</span><span class="sxs-lookup"><span data-stu-id="ebc15-108">DESCRIPTION</span></span>
<span data-ttu-id="ebc15-109">傳回服務下每個資源的健全性清單。</span><span class="sxs-lookup"><span data-stu-id="ebc15-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="ebc15-110">示例</span><span class="sxs-lookup"><span data-stu-id="ebc15-110">EXAMPLES</span></span>

### <span data-ttu-id="ebc15-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ebc15-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="ebc15-112">傳回服務下每個資源的健全性清單。</span><span class="sxs-lookup"><span data-stu-id="ebc15-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="ebc15-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ebc15-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="ebc15-114">傳回 [for Microsoft Fabric.] 下的 [健康情況] 狀態。</span><span class="sxs-lookup"><span data-stu-id="ebc15-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="ebc15-115">參數</span><span class="sxs-lookup"><span data-stu-id="ebc15-115">PARAMETERS</span></span>

### <span data-ttu-id="ebc15-116">-篩選</span><span class="sxs-lookup"><span data-stu-id="ebc15-116">-Filter</span></span>
<span data-ttu-id="ebc15-117">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="ebc15-117">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebc15-118">-位置</span><span class="sxs-lookup"><span data-stu-id="ebc15-118">-Location</span></span>
<span data-ttu-id="ebc15-119">地區名稱</span><span class="sxs-lookup"><span data-stu-id="ebc15-119">Name of the region</span></span>

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

### <span data-ttu-id="ebc15-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ebc15-120">-Name</span></span>
<span data-ttu-id="ebc15-121">與資源註冊識別碼相對應的 health 物件資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ebc15-121">The resource name of the health object which corresponds to the resource registration id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebc15-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebc15-122">-ResourceGroupName</span></span>
<span data-ttu-id="ebc15-123">資源所駐留的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ebc15-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="ebc15-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebc15-124">-ResourceId</span></span>
<span data-ttu-id="ebc15-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="ebc15-125">The resource id.</span></span>

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

### <span data-ttu-id="ebc15-126">-ServiceRegistrationName</span><span class="sxs-lookup"><span data-stu-id="ebc15-126">-ServiceRegistrationName</span></span>
<span data-ttu-id="ebc15-127">[服務註冊識別碼]。</span><span class="sxs-lookup"><span data-stu-id="ebc15-127">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ServiceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebc15-128">-略過</span><span class="sxs-lookup"><span data-stu-id="ebc15-128">-Skip</span></span>
<span data-ttu-id="ebc15-129">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="ebc15-129">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebc15-130">-上方</span><span class="sxs-lookup"><span data-stu-id="ebc15-130">-Top</span></span>
<span data-ttu-id="ebc15-131">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="ebc15-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ebc15-132">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="ebc15-132">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebc15-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc15-133">CommonParameters</span></span>
<span data-ttu-id="ebc15-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ebc15-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc15-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ebc15-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc15-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ebc15-136">INPUTS</span></span>

## <span data-ttu-id="ebc15-137">輸出</span><span class="sxs-lookup"><span data-stu-id="ebc15-137">OUTPUTS</span></span>

### <span data-ttu-id="ebc15-138">AzureStack InfrastructureInsights. ResourceHealth （）</span><span class="sxs-lookup"><span data-stu-id="ebc15-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="ebc15-139">筆記</span><span class="sxs-lookup"><span data-stu-id="ebc15-139">NOTES</span></span>

## <span data-ttu-id="ebc15-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebc15-140">RELATED LINKS</span></span>

