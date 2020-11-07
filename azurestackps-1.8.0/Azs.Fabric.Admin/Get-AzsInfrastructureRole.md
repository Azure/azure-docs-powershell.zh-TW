---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a20f0fbc5b059e878f0062569ffba2c16794204
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793516"
---
# <span data-ttu-id="1e257-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="1e257-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="1e257-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e257-102">SYNOPSIS</span></span>
<span data-ttu-id="1e257-103">傳回位於某個位置的所有結構角色清單。</span><span class="sxs-lookup"><span data-stu-id="1e257-103">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="1e257-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e257-104">SYNTAX</span></span>

### <span data-ttu-id="1e257-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="1e257-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1e257-106">獲取</span><span class="sxs-lookup"><span data-stu-id="1e257-106">Get</span></span>
```
Get-AzsInfrastructureRole [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e257-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e257-107">ResourceId</span></span>
```
Get-AzsInfrastructureRole -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1e257-108">說明</span><span class="sxs-lookup"><span data-stu-id="1e257-108">DESCRIPTION</span></span>
<span data-ttu-id="1e257-109">傳回位於某個位置的所有結構角色清單。</span><span class="sxs-lookup"><span data-stu-id="1e257-109">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="1e257-110">示例</span><span class="sxs-lookup"><span data-stu-id="1e257-110">EXAMPLES</span></span>

### <span data-ttu-id="1e257-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1e257-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRole
```

<span data-ttu-id="1e257-112">取得所有基礎結構角色的清單。</span><span class="sxs-lookup"><span data-stu-id="1e257-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="1e257-113">範例2</span><span class="sxs-lookup"><span data-stu-id="1e257-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="1e257-114">根據名稱取得基礎結構角色。</span><span class="sxs-lookup"><span data-stu-id="1e257-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="1e257-115">參數</span><span class="sxs-lookup"><span data-stu-id="1e257-115">PARAMETERS</span></span>

### <span data-ttu-id="1e257-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="1e257-116">-Name</span></span>
<span data-ttu-id="1e257-117">結構角色名稱。</span><span class="sxs-lookup"><span data-stu-id="1e257-117">Infrastructure role name.</span></span>

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

### <span data-ttu-id="1e257-118">-位置</span><span class="sxs-lookup"><span data-stu-id="1e257-118">-Location</span></span>
<span data-ttu-id="1e257-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="1e257-119">Location of the resource.</span></span>

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

### <span data-ttu-id="1e257-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e257-120">-ResourceGroupName</span></span>
<span data-ttu-id="1e257-121">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1e257-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1e257-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e257-122">-ResourceId</span></span>
<span data-ttu-id="1e257-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="1e257-123">The resource id.</span></span>

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

### <span data-ttu-id="1e257-124">-篩選</span><span class="sxs-lookup"><span data-stu-id="1e257-124">-Filter</span></span>
<span data-ttu-id="1e257-125">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="1e257-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="1e257-126">-略過</span><span class="sxs-lookup"><span data-stu-id="1e257-126">-Skip</span></span>
<span data-ttu-id="1e257-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="1e257-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1e257-128">-上方</span><span class="sxs-lookup"><span data-stu-id="1e257-128">-Top</span></span>
<span data-ttu-id="1e257-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="1e257-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1e257-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="1e257-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1e257-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e257-131">CommonParameters</span></span>
<span data-ttu-id="1e257-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e257-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e257-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e257-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e257-134">輸入</span><span class="sxs-lookup"><span data-stu-id="1e257-134">INPUTS</span></span>

## <span data-ttu-id="1e257-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1e257-135">OUTPUTS</span></span>

### <span data-ttu-id="1e257-136">InfraRole 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="1e257-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRole</span></span>

## <span data-ttu-id="1e257-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1e257-137">NOTES</span></span>

## <span data-ttu-id="1e257-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e257-138">RELATED LINKS</span></span>
