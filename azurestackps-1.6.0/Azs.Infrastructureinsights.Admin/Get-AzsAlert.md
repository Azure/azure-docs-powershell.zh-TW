---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fbec7ec2f8bcfc0d7595658f84866cf449d3e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443031"
---
# <span data-ttu-id="1b4a4-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="1b4a4-101">Get-AzsAlert</span></span>

## <span data-ttu-id="1b4a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b4a4-102">SYNOPSIS</span></span>
<span data-ttu-id="1b4a4-103">傳回指定位置中所有警示的清單。</span><span class="sxs-lookup"><span data-stu-id="1b4a4-103">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="1b4a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b4a4-104">SYNTAX</span></span>

### <span data-ttu-id="1b4a4-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="1b4a4-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1b4a4-106">獲取</span><span class="sxs-lookup"><span data-stu-id="1b4a4-106">Get</span></span>
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1b4a4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b4a4-107">ResourceId</span></span>
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1b4a4-108">說明</span><span class="sxs-lookup"><span data-stu-id="1b4a4-108">DESCRIPTION</span></span>
<span data-ttu-id="1b4a4-109">傳回指定位置中所有警示的清單。</span><span class="sxs-lookup"><span data-stu-id="1b4a4-109">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="1b4a4-110">示例</span><span class="sxs-lookup"><span data-stu-id="1b4a4-110">EXAMPLES</span></span>

### <span data-ttu-id="1b4a4-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1b4a4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="1b4a4-112">透過名稱取得警示。</span><span class="sxs-lookup"><span data-stu-id="1b4a4-112">Get an alert by Name.</span></span>

### <span data-ttu-id="1b4a4-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1b4a4-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="1b4a4-114">取得所有的活動警示，並顯示其錯誤和標題。</span><span class="sxs-lookup"><span data-stu-id="1b4a4-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="1b4a4-115">參數</span><span class="sxs-lookup"><span data-stu-id="1b4a4-115">PARAMETERS</span></span>

### <span data-ttu-id="1b4a4-116">-篩選</span><span class="sxs-lookup"><span data-stu-id="1b4a4-116">-Filter</span></span>
<span data-ttu-id="1b4a4-117">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="1b4a4-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="1b4a4-118">-位置</span><span class="sxs-lookup"><span data-stu-id="1b4a4-118">-Location</span></span>
<span data-ttu-id="1b4a4-119">位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b4a4-119">Name of the location.</span></span>

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

### <span data-ttu-id="1b4a4-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1b4a4-120">-Name</span></span>
<span data-ttu-id="1b4a4-121">警報識別碼。</span><span class="sxs-lookup"><span data-stu-id="1b4a4-121">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b4a4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b4a4-122">-ResourceGroupName</span></span>
<span data-ttu-id="1b4a4-123">資源所駐留的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1b4a4-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="1b4a4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b4a4-124">-ResourceId</span></span>
<span data-ttu-id="1b4a4-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="1b4a4-125">The resource id.</span></span>

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

### <span data-ttu-id="1b4a4-126">-略過</span><span class="sxs-lookup"><span data-stu-id="1b4a4-126">-Skip</span></span>
<span data-ttu-id="1b4a4-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="1b4a4-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1b4a4-128">-上方</span><span class="sxs-lookup"><span data-stu-id="1b4a4-128">-Top</span></span>
<span data-ttu-id="1b4a4-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="1b4a4-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1b4a4-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="1b4a4-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1b4a4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b4a4-131">CommonParameters</span></span>
<span data-ttu-id="1b4a4-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b4a4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b4a4-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b4a4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b4a4-134">輸入</span><span class="sxs-lookup"><span data-stu-id="1b4a4-134">INPUTS</span></span>

## <span data-ttu-id="1b4a4-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1b4a4-135">OUTPUTS</span></span>

### <span data-ttu-id="1b4a4-136">AzureStack InfrastructureInsights. Alert. 警示</span><span class="sxs-lookup"><span data-stu-id="1b4a4-136">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="1b4a4-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1b4a4-137">NOTES</span></span>

## <span data-ttu-id="1b4a4-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b4a4-138">RELATED LINKS</span></span>

