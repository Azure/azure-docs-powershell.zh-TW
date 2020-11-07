---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c5fe6e28ff87cfd3f365441d0e09f09ef21dc454
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793515"
---
# <span data-ttu-id="deb0c-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="deb0c-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="deb0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="deb0c-102">SYNOPSIS</span></span>
<span data-ttu-id="deb0c-103">傳回位置上所有結構角色實例的清單。</span><span class="sxs-lookup"><span data-stu-id="deb0c-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="deb0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="deb0c-104">SYNTAX</span></span>

### <span data-ttu-id="deb0c-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="deb0c-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="deb0c-106">獲取</span><span class="sxs-lookup"><span data-stu-id="deb0c-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="deb0c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="deb0c-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="deb0c-108">說明</span><span class="sxs-lookup"><span data-stu-id="deb0c-108">DESCRIPTION</span></span>
<span data-ttu-id="deb0c-109">傳回位置上所有結構角色實例的清單。</span><span class="sxs-lookup"><span data-stu-id="deb0c-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="deb0c-110">示例</span><span class="sxs-lookup"><span data-stu-id="deb0c-110">EXAMPLES</span></span>

### <span data-ttu-id="deb0c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="deb0c-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="deb0c-112">傳回所有結構角色實例的清單。</span><span class="sxs-lookup"><span data-stu-id="deb0c-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="deb0c-113">範例2</span><span class="sxs-lookup"><span data-stu-id="deb0c-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="deb0c-114">根據名稱傳回單一的結構角色實例。</span><span class="sxs-lookup"><span data-stu-id="deb0c-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="deb0c-115">參數</span><span class="sxs-lookup"><span data-stu-id="deb0c-115">PARAMETERS</span></span>

### <span data-ttu-id="deb0c-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="deb0c-116">-Name</span></span>
<span data-ttu-id="deb0c-117">結構角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="deb0c-117">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="deb0c-118">-位置</span><span class="sxs-lookup"><span data-stu-id="deb0c-118">-Location</span></span>
<span data-ttu-id="deb0c-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="deb0c-119">Location of the resource.</span></span>

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

### <span data-ttu-id="deb0c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deb0c-120">-ResourceGroupName</span></span>
<span data-ttu-id="deb0c-121">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="deb0c-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="deb0c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="deb0c-122">-ResourceId</span></span>
<span data-ttu-id="deb0c-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="deb0c-123">The resource id.</span></span>

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

### <span data-ttu-id="deb0c-124">-篩選</span><span class="sxs-lookup"><span data-stu-id="deb0c-124">-Filter</span></span>
<span data-ttu-id="deb0c-125">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="deb0c-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="deb0c-126">-略過</span><span class="sxs-lookup"><span data-stu-id="deb0c-126">-Skip</span></span>
<span data-ttu-id="deb0c-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="deb0c-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="deb0c-128">-上方</span><span class="sxs-lookup"><span data-stu-id="deb0c-128">-Top</span></span>
<span data-ttu-id="deb0c-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="deb0c-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="deb0c-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="deb0c-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="deb0c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb0c-131">CommonParameters</span></span>
<span data-ttu-id="deb0c-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="deb0c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb0c-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="deb0c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb0c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="deb0c-134">INPUTS</span></span>

## <span data-ttu-id="deb0c-135">輸出</span><span class="sxs-lookup"><span data-stu-id="deb0c-135">OUTPUTS</span></span>

### <span data-ttu-id="deb0c-136">InfraRoleInstance 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="deb0c-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="deb0c-137">筆記</span><span class="sxs-lookup"><span data-stu-id="deb0c-137">NOTES</span></span>

## <span data-ttu-id="deb0c-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="deb0c-138">RELATED LINKS</span></span>
