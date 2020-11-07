---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5999718cc3085eb69da482df27fa0cb4379ed40
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793850"
---
# <span data-ttu-id="daa90-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="daa90-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="daa90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="daa90-102">SYNOPSIS</span></span>
<span data-ttu-id="daa90-103">傳回特定位置的所有 IP 池清單。</span><span class="sxs-lookup"><span data-stu-id="daa90-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="daa90-104">句法</span><span class="sxs-lookup"><span data-stu-id="daa90-104">SYNTAX</span></span>

### <span data-ttu-id="daa90-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="daa90-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="daa90-106">獲取</span><span class="sxs-lookup"><span data-stu-id="daa90-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="daa90-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="daa90-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="daa90-108">說明</span><span class="sxs-lookup"><span data-stu-id="daa90-108">DESCRIPTION</span></span>
<span data-ttu-id="daa90-109">傳回特定位置的所有 IP 池清單。</span><span class="sxs-lookup"><span data-stu-id="daa90-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="daa90-110">示例</span><span class="sxs-lookup"><span data-stu-id="daa90-110">EXAMPLES</span></span>

### <span data-ttu-id="daa90-111">範例1</span><span class="sxs-lookup"><span data-stu-id="daa90-111">EXAMPLE 1</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="daa90-112">取得所有基礎結構 ip 池。</span><span class="sxs-lookup"><span data-stu-id="daa90-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="daa90-113">範例2</span><span class="sxs-lookup"><span data-stu-id="daa90-113">EXAMPLE 2</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="daa90-114">根據名稱取得基礎結構 ip 池。</span><span class="sxs-lookup"><span data-stu-id="daa90-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="daa90-115">參數</span><span class="sxs-lookup"><span data-stu-id="daa90-115">PARAMETERS</span></span>

### <span data-ttu-id="daa90-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="daa90-116">-Name</span></span>
<span data-ttu-id="daa90-117">IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="daa90-117">IP pool name.</span></span>

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

### <span data-ttu-id="daa90-118">-位置</span><span class="sxs-lookup"><span data-stu-id="daa90-118">-Location</span></span>
<span data-ttu-id="daa90-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="daa90-119">Location of the resource.</span></span>

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

### <span data-ttu-id="daa90-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daa90-120">-ResourceGroupName</span></span>
<span data-ttu-id="daa90-121">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="daa90-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="daa90-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="daa90-122">-ResourceId</span></span>
<span data-ttu-id="daa90-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="daa90-123">The resource id.</span></span>

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

### <span data-ttu-id="daa90-124">-篩選</span><span class="sxs-lookup"><span data-stu-id="daa90-124">-Filter</span></span>
<span data-ttu-id="daa90-125">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="daa90-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="daa90-126">-略過</span><span class="sxs-lookup"><span data-stu-id="daa90-126">-Skip</span></span>
<span data-ttu-id="daa90-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="daa90-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="daa90-128">-上方</span><span class="sxs-lookup"><span data-stu-id="daa90-128">-Top</span></span>
<span data-ttu-id="daa90-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="daa90-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="daa90-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="daa90-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="daa90-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa90-131">CommonParameters</span></span>
<span data-ttu-id="daa90-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="daa90-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa90-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="daa90-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa90-134">輸入</span><span class="sxs-lookup"><span data-stu-id="daa90-134">INPUTS</span></span>

## <span data-ttu-id="daa90-135">輸出</span><span class="sxs-lookup"><span data-stu-id="daa90-135">OUTPUTS</span></span>

### <span data-ttu-id="daa90-136">IpPool 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="daa90-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="daa90-137">筆記</span><span class="sxs-lookup"><span data-stu-id="daa90-137">NOTES</span></span>

## <span data-ttu-id="daa90-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="daa90-138">RELATED LINKS</span></span>
