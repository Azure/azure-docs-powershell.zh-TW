---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3a64a045d988d59c2b1aefa650aa695ba09486f
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793985"
---
# <span data-ttu-id="b1805-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="b1805-101">Get-AzsAlert</span></span>

## <span data-ttu-id="b1805-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1805-102">SYNOPSIS</span></span>
<span data-ttu-id="b1805-103">傳回指定位置中所有警示的清單。</span><span class="sxs-lookup"><span data-stu-id="b1805-103">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="b1805-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1805-104">SYNTAX</span></span>

### <span data-ttu-id="b1805-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="b1805-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b1805-106">獲取</span><span class="sxs-lookup"><span data-stu-id="b1805-106">Get</span></span>
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b1805-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1805-107">ResourceId</span></span>
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b1805-108">說明</span><span class="sxs-lookup"><span data-stu-id="b1805-108">DESCRIPTION</span></span>
<span data-ttu-id="b1805-109">傳回指定位置中所有警示的清單。</span><span class="sxs-lookup"><span data-stu-id="b1805-109">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="b1805-110">示例</span><span class="sxs-lookup"><span data-stu-id="b1805-110">EXAMPLES</span></span>

### <span data-ttu-id="b1805-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b1805-111">EXAMPLE 1</span></span>
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="b1805-112">透過名稱取得警示。</span><span class="sxs-lookup"><span data-stu-id="b1805-112">Get an alert by Name.</span></span>

### <span data-ttu-id="b1805-113">範例2</span><span class="sxs-lookup"><span data-stu-id="b1805-113">EXAMPLE 2</span></span>
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="b1805-114">取得所有的活動警示，並顯示其錯誤和標題。</span><span class="sxs-lookup"><span data-stu-id="b1805-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="b1805-115">參數</span><span class="sxs-lookup"><span data-stu-id="b1805-115">PARAMETERS</span></span>

### <span data-ttu-id="b1805-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1805-116">-Name</span></span>
<span data-ttu-id="b1805-117">警報識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1805-117">The alert identifier.</span></span>

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

### <span data-ttu-id="b1805-118">-位置</span><span class="sxs-lookup"><span data-stu-id="b1805-118">-Location</span></span>
<span data-ttu-id="b1805-119">位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1805-119">Name of the location.</span></span>

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

### <span data-ttu-id="b1805-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1805-120">-ResourceGroupName</span></span>
<span data-ttu-id="b1805-121">提醒的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b1805-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="b1805-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1805-122">-ResourceId</span></span>
<span data-ttu-id="b1805-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="b1805-123">The resource id.</span></span>

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

### <span data-ttu-id="b1805-124">-篩選</span><span class="sxs-lookup"><span data-stu-id="b1805-124">-Filter</span></span>
<span data-ttu-id="b1805-125">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="b1805-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="b1805-126">-上方</span><span class="sxs-lookup"><span data-stu-id="b1805-126">-Top</span></span>
<span data-ttu-id="b1805-127">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="b1805-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b1805-128">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="b1805-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b1805-129">-略過</span><span class="sxs-lookup"><span data-stu-id="b1805-129">-Skip</span></span>
<span data-ttu-id="b1805-130">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="b1805-130">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b1805-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1805-131">CommonParameters</span></span>
<span data-ttu-id="b1805-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1805-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1805-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b1805-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1805-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b1805-134">INPUTS</span></span>

## <span data-ttu-id="b1805-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b1805-135">OUTPUTS</span></span>

### <span data-ttu-id="b1805-136">AzureStack InfrastructureInsights. Alert. 警示</span><span class="sxs-lookup"><span data-stu-id="b1805-136">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="b1805-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b1805-137">NOTES</span></span>

## <span data-ttu-id="b1805-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1805-138">RELATED LINKS</span></span>
