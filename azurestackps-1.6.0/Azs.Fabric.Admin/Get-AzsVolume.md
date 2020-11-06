---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67835cc0ae5191f50aefb79f76148752c68508bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443239"
---
# <span data-ttu-id="04f4d-101">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="04f4d-101">Get-AzsVolume</span></span>

## <span data-ttu-id="04f4d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="04f4d-103">傳回位於某個位置的所有儲存空間清單。</span><span class="sxs-lookup"><span data-stu-id="04f4d-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="04f4d-104">句法</span><span class="sxs-lookup"><span data-stu-id="04f4d-104">SYNTAX</span></span>

### <span data-ttu-id="04f4d-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="04f4d-105">List (Default)</span></span>
```
Get-AzsVolume -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="04f4d-106">獲取</span><span class="sxs-lookup"><span data-stu-id="04f4d-106">Get</span></span>
```
Get-AzsVolume -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="04f4d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="04f4d-107">ResourceId</span></span>
```
Get-AzsVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="04f4d-108">說明</span><span class="sxs-lookup"><span data-stu-id="04f4d-108">DESCRIPTION</span></span>
<span data-ttu-id="04f4d-109">傳回位於某個位置的所有儲存空間清單。</span><span class="sxs-lookup"><span data-stu-id="04f4d-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="04f4d-110">示例</span><span class="sxs-lookup"><span data-stu-id="04f4d-110">EXAMPLES</span></span>

### <span data-ttu-id="04f4d-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="04f4d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="04f4d-112">取得指定位置上所有儲存空間的清單。</span><span class="sxs-lookup"><span data-stu-id="04f4d-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="04f4d-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="04f4d-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="04f4d-114">依名稱在指定位置取得儲存空間量。</span><span class="sxs-lookup"><span data-stu-id="04f4d-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="04f4d-115">參數</span><span class="sxs-lookup"><span data-stu-id="04f4d-115">PARAMETERS</span></span>

### <span data-ttu-id="04f4d-116">-篩選</span><span class="sxs-lookup"><span data-stu-id="04f4d-116">-Filter</span></span>
<span data-ttu-id="04f4d-117">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="04f4d-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="04f4d-118">-位置</span><span class="sxs-lookup"><span data-stu-id="04f4d-118">-Location</span></span>
<span data-ttu-id="04f4d-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="04f4d-119">Location of the resource.</span></span>

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

### <span data-ttu-id="04f4d-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="04f4d-120">-Name</span></span>
<span data-ttu-id="04f4d-121">儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="04f4d-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="04f4d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04f4d-122">-ResourceGroupName</span></span>
<span data-ttu-id="04f4d-123">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="04f4d-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="04f4d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04f4d-124">-ResourceId</span></span>
<span data-ttu-id="04f4d-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="04f4d-125">The resource id.</span></span>

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

### <span data-ttu-id="04f4d-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="04f4d-126">-ScaleUnit</span></span>
<span data-ttu-id="04f4d-127">縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="04f4d-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="04f4d-128">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="04f4d-128">-StorageSubSystem</span></span>
<span data-ttu-id="04f4d-129">卷所在的儲存子系統。</span><span class="sxs-lookup"><span data-stu-id="04f4d-129">Storage subsystem in which the volume is located.</span></span>

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

### <span data-ttu-id="04f4d-130">-上方</span><span class="sxs-lookup"><span data-stu-id="04f4d-130">-Top</span></span>
<span data-ttu-id="04f4d-131">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="04f4d-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="04f4d-132">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="04f4d-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="04f4d-133">-略過</span><span class="sxs-lookup"><span data-stu-id="04f4d-133">-Skip</span></span>
<span data-ttu-id="04f4d-134">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="04f4d-134">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="04f4d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04f4d-135">CommonParameters</span></span>
<span data-ttu-id="04f4d-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04f4d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04f4d-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="04f4d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04f4d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="04f4d-138">INPUTS</span></span>

## <span data-ttu-id="04f4d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="04f4d-139">OUTPUTS</span></span>

### <span data-ttu-id="04f4d-140">AzureStack （管理模型）。</span><span class="sxs-lookup"><span data-stu-id="04f4d-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>
## <span data-ttu-id="04f4d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="04f4d-141">NOTES</span></span>

## <span data-ttu-id="04f4d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="04f4d-142">RELATED LINKS</span></span>
