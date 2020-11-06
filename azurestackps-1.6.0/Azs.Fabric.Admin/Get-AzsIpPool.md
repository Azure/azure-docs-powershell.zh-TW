---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2528d9b4f9443d8857006b6fc1e94100b0b477ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442563"
---
# <span data-ttu-id="8f3b9-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="8f3b9-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="8f3b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f3b9-102">SYNOPSIS</span></span>
<span data-ttu-id="8f3b9-103">傳回特定位置的所有 IP 池清單。</span><span class="sxs-lookup"><span data-stu-id="8f3b9-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="8f3b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f3b9-104">SYNTAX</span></span>

### <span data-ttu-id="8f3b9-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="8f3b9-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8f3b9-106">獲取</span><span class="sxs-lookup"><span data-stu-id="8f3b9-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="8f3b9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f3b9-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8f3b9-108">說明</span><span class="sxs-lookup"><span data-stu-id="8f3b9-108">DESCRIPTION</span></span>
<span data-ttu-id="8f3b9-109">傳回特定位置的所有 IP 池清單。</span><span class="sxs-lookup"><span data-stu-id="8f3b9-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="8f3b9-110">示例</span><span class="sxs-lookup"><span data-stu-id="8f3b9-110">EXAMPLES</span></span>

### <span data-ttu-id="8f3b9-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8f3b9-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="8f3b9-112">取得所有基礎結構 ip 池。</span><span class="sxs-lookup"><span data-stu-id="8f3b9-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="8f3b9-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="8f3b9-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="8f3b9-114">根據名稱取得基礎結構 ip 池。</span><span class="sxs-lookup"><span data-stu-id="8f3b9-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="8f3b9-115">參數</span><span class="sxs-lookup"><span data-stu-id="8f3b9-115">PARAMETERS</span></span>

### <span data-ttu-id="8f3b9-116">-篩選</span><span class="sxs-lookup"><span data-stu-id="8f3b9-116">-Filter</span></span>
<span data-ttu-id="8f3b9-117">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="8f3b9-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="8f3b9-118">-位置</span><span class="sxs-lookup"><span data-stu-id="8f3b9-118">-Location</span></span>
<span data-ttu-id="8f3b9-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="8f3b9-119">Location of the resource.</span></span>

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

### <span data-ttu-id="8f3b9-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f3b9-120">-Name</span></span>
<span data-ttu-id="8f3b9-121">IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="8f3b9-121">IP pool name.</span></span>

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

### <span data-ttu-id="8f3b9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f3b9-122">-ResourceGroupName</span></span>
<span data-ttu-id="8f3b9-123">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8f3b9-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="8f3b9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f3b9-124">-ResourceId</span></span>
<span data-ttu-id="8f3b9-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8f3b9-125">The resource id.</span></span>

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

### <span data-ttu-id="8f3b9-126">-略過</span><span class="sxs-lookup"><span data-stu-id="8f3b9-126">-Skip</span></span>
<span data-ttu-id="8f3b9-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="8f3b9-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="8f3b9-128">-上方</span><span class="sxs-lookup"><span data-stu-id="8f3b9-128">-Top</span></span>
<span data-ttu-id="8f3b9-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="8f3b9-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="8f3b9-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="8f3b9-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="8f3b9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f3b9-131">CommonParameters</span></span>
<span data-ttu-id="8f3b9-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f3b9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f3b9-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f3b9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f3b9-134">輸入</span><span class="sxs-lookup"><span data-stu-id="8f3b9-134">INPUTS</span></span>

## <span data-ttu-id="8f3b9-135">輸出</span><span class="sxs-lookup"><span data-stu-id="8f3b9-135">OUTPUTS</span></span>

### <span data-ttu-id="8f3b9-136">IpPool 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="8f3b9-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="8f3b9-137">筆記</span><span class="sxs-lookup"><span data-stu-id="8f3b9-137">NOTES</span></span>

## <span data-ttu-id="8f3b9-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f3b9-138">RELATED LINKS</span></span>

