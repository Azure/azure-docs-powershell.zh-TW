---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 39955a2b99ffd7e3c604b4fc288f117face8205f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442532"
---
# <span data-ttu-id="0c973-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="0c973-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="0c973-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c973-102">SYNOPSIS</span></span>
<span data-ttu-id="0c973-103">傳回位置上所有結構角色實例的清單。</span><span class="sxs-lookup"><span data-stu-id="0c973-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="0c973-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c973-104">SYNTAX</span></span>

### <span data-ttu-id="0c973-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="0c973-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0c973-106">獲取</span><span class="sxs-lookup"><span data-stu-id="0c973-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c973-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c973-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0c973-108">說明</span><span class="sxs-lookup"><span data-stu-id="0c973-108">DESCRIPTION</span></span>
<span data-ttu-id="0c973-109">傳回位置上所有結構角色實例的清單。</span><span class="sxs-lookup"><span data-stu-id="0c973-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="0c973-110">示例</span><span class="sxs-lookup"><span data-stu-id="0c973-110">EXAMPLES</span></span>

### <span data-ttu-id="0c973-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0c973-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="0c973-112">傳回所有結構角色實例的清單。</span><span class="sxs-lookup"><span data-stu-id="0c973-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="0c973-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0c973-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="0c973-114">根據名稱傳回單一的結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="0c973-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="0c973-115">參數</span><span class="sxs-lookup"><span data-stu-id="0c973-115">PARAMETERS</span></span>

### <span data-ttu-id="0c973-116">-篩選</span><span class="sxs-lookup"><span data-stu-id="0c973-116">-Filter</span></span>
<span data-ttu-id="0c973-117">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="0c973-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="0c973-118">-位置</span><span class="sxs-lookup"><span data-stu-id="0c973-118">-Location</span></span>
<span data-ttu-id="0c973-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="0c973-119">Location of the resource.</span></span>

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

### <span data-ttu-id="0c973-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="0c973-120">-Name</span></span>
<span data-ttu-id="0c973-121">結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c973-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="0c973-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c973-122">-ResourceGroupName</span></span>
<span data-ttu-id="0c973-123">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0c973-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="0c973-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c973-124">-ResourceId</span></span>
<span data-ttu-id="0c973-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="0c973-125">The resource id.</span></span>

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

### <span data-ttu-id="0c973-126">-略過</span><span class="sxs-lookup"><span data-stu-id="0c973-126">-Skip</span></span>
<span data-ttu-id="0c973-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="0c973-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="0c973-128">-上方</span><span class="sxs-lookup"><span data-stu-id="0c973-128">-Top</span></span>
<span data-ttu-id="0c973-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="0c973-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0c973-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="0c973-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="0c973-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c973-131">CommonParameters</span></span>
<span data-ttu-id="0c973-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c973-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c973-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0c973-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c973-134">輸入</span><span class="sxs-lookup"><span data-stu-id="0c973-134">INPUTS</span></span>

## <span data-ttu-id="0c973-135">輸出</span><span class="sxs-lookup"><span data-stu-id="0c973-135">OUTPUTS</span></span>

### <span data-ttu-id="0c973-136">InfraRoleInstance 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="0c973-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="0c973-137">筆記</span><span class="sxs-lookup"><span data-stu-id="0c973-137">NOTES</span></span>

## <span data-ttu-id="0c973-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c973-138">RELATED LINKS</span></span>

