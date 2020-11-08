---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4285a7423390f5d9b5384faa63f95c4206840d71
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968555"
---
# <span data-ttu-id="7ed90-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="7ed90-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="7ed90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7ed90-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed90-103">傳回服務下每個資源的健全性清單。</span><span class="sxs-lookup"><span data-stu-id="7ed90-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="7ed90-104">句法</span><span class="sxs-lookup"><span data-stu-id="7ed90-104">SYNTAX</span></span>

### <span data-ttu-id="7ed90-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="7ed90-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7ed90-106">獲取</span><span class="sxs-lookup"><span data-stu-id="7ed90-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> -ResourceRegistrationId <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="7ed90-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ed90-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="7ed90-108">說明</span><span class="sxs-lookup"><span data-stu-id="7ed90-108">DESCRIPTION</span></span>
<span data-ttu-id="7ed90-109">傳回服務下每個資源的健全性清單。</span><span class="sxs-lookup"><span data-stu-id="7ed90-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="7ed90-110">示例</span><span class="sxs-lookup"><span data-stu-id="7ed90-110">EXAMPLES</span></span>

### <span data-ttu-id="7ed90-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7ed90-111">EXAMPLE 1</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="7ed90-112">傳回服務下每個資源的健全性清單。</span><span class="sxs-lookup"><span data-stu-id="7ed90-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="7ed90-113">範例2</span><span class="sxs-lookup"><span data-stu-id="7ed90-113">EXAMPLE 2</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationId $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="7ed90-114">傳回 [for Microsoft Fabric.] 下的 [健康情況] 狀態。</span><span class="sxs-lookup"><span data-stu-id="7ed90-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="7ed90-115">參數</span><span class="sxs-lookup"><span data-stu-id="7ed90-115">PARAMETERS</span></span>

### <span data-ttu-id="7ed90-116">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="7ed90-116">-ServiceRegistrationId</span></span>
<span data-ttu-id="7ed90-117">[服務註冊識別碼]。</span><span class="sxs-lookup"><span data-stu-id="7ed90-117">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ed90-118">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="7ed90-118">-ResourceRegistrationId</span></span>


```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ed90-119">-位置</span><span class="sxs-lookup"><span data-stu-id="7ed90-119">-Location</span></span>
<span data-ttu-id="7ed90-120">地區名稱</span><span class="sxs-lookup"><span data-stu-id="7ed90-120">Name of the region</span></span>

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

### <span data-ttu-id="7ed90-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ed90-121">-ResourceGroupName</span></span>
<span data-ttu-id="7ed90-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ed90-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="7ed90-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ed90-123">-ResourceId</span></span>
<span data-ttu-id="7ed90-124">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="7ed90-124">The resource id.</span></span>

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

### <span data-ttu-id="7ed90-125">-篩選</span><span class="sxs-lookup"><span data-stu-id="7ed90-125">-Filter</span></span>
<span data-ttu-id="7ed90-126">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="7ed90-126">OData filter parameter.</span></span>

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

### <span data-ttu-id="7ed90-127">-上方</span><span class="sxs-lookup"><span data-stu-id="7ed90-127">-Top</span></span>
<span data-ttu-id="7ed90-128">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="7ed90-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7ed90-129">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="7ed90-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="7ed90-130">-略過</span><span class="sxs-lookup"><span data-stu-id="7ed90-130">-Skip</span></span>
<span data-ttu-id="7ed90-131">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="7ed90-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="7ed90-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed90-132">CommonParameters</span></span>
<span data-ttu-id="7ed90-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7ed90-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed90-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7ed90-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed90-135">輸入</span><span class="sxs-lookup"><span data-stu-id="7ed90-135">INPUTS</span></span>

## <span data-ttu-id="7ed90-136">輸出</span><span class="sxs-lookup"><span data-stu-id="7ed90-136">OUTPUTS</span></span>

### <span data-ttu-id="7ed90-137">AzureStack InfrastructureInsights. ResourceHealth （）</span><span class="sxs-lookup"><span data-stu-id="7ed90-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="7ed90-138">筆記</span><span class="sxs-lookup"><span data-stu-id="7ed90-138">NOTES</span></span>

## <span data-ttu-id="7ed90-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ed90-139">RELATED LINKS</span></span>