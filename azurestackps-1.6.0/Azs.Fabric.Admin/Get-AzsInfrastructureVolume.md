---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdb6542f9e7bfd594130374d5d72fed8b26596e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443200"
---
# <span data-ttu-id="b1e60-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="b1e60-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="b1e60-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1e60-102">SYNOPSIS</span></span>
<span data-ttu-id="b1e60-103">傳回位於某個位置的所有儲存空間清單。</span><span class="sxs-lookup"><span data-stu-id="b1e60-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="b1e60-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1e60-104">SYNTAX</span></span>

### <span data-ttu-id="b1e60-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="b1e60-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b1e60-106">獲取</span><span class="sxs-lookup"><span data-stu-id="b1e60-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b1e60-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1e60-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b1e60-108">說明</span><span class="sxs-lookup"><span data-stu-id="b1e60-108">DESCRIPTION</span></span>
<span data-ttu-id="b1e60-109">傳回位於某個位置的所有儲存空間清單。</span><span class="sxs-lookup"><span data-stu-id="b1e60-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="b1e60-110">示例</span><span class="sxs-lookup"><span data-stu-id="b1e60-110">EXAMPLES</span></span>

### <span data-ttu-id="b1e60-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b1e60-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="b1e60-112">取得指定位置上所有儲存空間的清單。</span><span class="sxs-lookup"><span data-stu-id="b1e60-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="b1e60-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b1e60-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="b1e60-114">依名稱在指定位置取得儲存空間量。</span><span class="sxs-lookup"><span data-stu-id="b1e60-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="b1e60-115">參數</span><span class="sxs-lookup"><span data-stu-id="b1e60-115">PARAMETERS</span></span>

### <span data-ttu-id="b1e60-116">-篩選</span><span class="sxs-lookup"><span data-stu-id="b1e60-116">-Filter</span></span>
<span data-ttu-id="b1e60-117">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="b1e60-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="b1e60-118">-位置</span><span class="sxs-lookup"><span data-stu-id="b1e60-118">-Location</span></span>
<span data-ttu-id="b1e60-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="b1e60-119">Location of the resource.</span></span>

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

### <span data-ttu-id="b1e60-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1e60-120">-Name</span></span>
<span data-ttu-id="b1e60-121">儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1e60-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="b1e60-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1e60-122">-ResourceGroupName</span></span>
<span data-ttu-id="b1e60-123">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b1e60-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b1e60-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1e60-124">-ResourceId</span></span>
<span data-ttu-id="b1e60-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="b1e60-125">The resource id.</span></span>

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

### <span data-ttu-id="b1e60-126">-略過</span><span class="sxs-lookup"><span data-stu-id="b1e60-126">-Skip</span></span>
<span data-ttu-id="b1e60-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="b1e60-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b1e60-128">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="b1e60-128">-StoragePool</span></span>
<span data-ttu-id="b1e60-129">儲存空間池名稱。</span><span class="sxs-lookup"><span data-stu-id="b1e60-129">Storage pool name.</span></span>

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

### <span data-ttu-id="b1e60-130">-It</span><span class="sxs-lookup"><span data-stu-id="b1e60-130">-StorageSystem</span></span>
<span data-ttu-id="b1e60-131">基礎結構卷所在的儲存系統。</span><span class="sxs-lookup"><span data-stu-id="b1e60-131">Storage system in which the infrastructure volume is located.</span></span>

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

### <span data-ttu-id="b1e60-132">-上方</span><span class="sxs-lookup"><span data-stu-id="b1e60-132">-Top</span></span>
<span data-ttu-id="b1e60-133">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="b1e60-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b1e60-134">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="b1e60-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b1e60-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1e60-135">CommonParameters</span></span>
<span data-ttu-id="b1e60-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1e60-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1e60-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b1e60-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1e60-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b1e60-138">INPUTS</span></span>

## <span data-ttu-id="b1e60-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b1e60-139">OUTPUTS</span></span>

### <span data-ttu-id="b1e60-140">AzureStack （管理模型）。</span><span class="sxs-lookup"><span data-stu-id="b1e60-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="b1e60-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b1e60-141">NOTES</span></span>

## <span data-ttu-id="b1e60-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1e60-142">RELATED LINKS</span></span>

