---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: deaefa8e98e27572fb3faa9443c296e5a15accb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793513"
---
# <span data-ttu-id="f56bd-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="f56bd-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="f56bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f56bd-102">SYNOPSIS</span></span>
<span data-ttu-id="f56bd-103">傳回位於某個位置的所有儲存空間清單。</span><span class="sxs-lookup"><span data-stu-id="f56bd-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="f56bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="f56bd-104">SYNTAX</span></span>

### <span data-ttu-id="f56bd-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="f56bd-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f56bd-106">獲取</span><span class="sxs-lookup"><span data-stu-id="f56bd-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="f56bd-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f56bd-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f56bd-108">說明</span><span class="sxs-lookup"><span data-stu-id="f56bd-108">DESCRIPTION</span></span>
<span data-ttu-id="f56bd-109">傳回位於某個位置的所有儲存空間清單。</span><span class="sxs-lookup"><span data-stu-id="f56bd-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="f56bd-110">示例</span><span class="sxs-lookup"><span data-stu-id="f56bd-110">EXAMPLES</span></span>

### <span data-ttu-id="f56bd-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f56bd-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="f56bd-112">取得指定位置上所有儲存空間的清單。</span><span class="sxs-lookup"><span data-stu-id="f56bd-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="f56bd-113">範例2</span><span class="sxs-lookup"><span data-stu-id="f56bd-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="f56bd-114">依名稱在指定位置取得儲存空間量。</span><span class="sxs-lookup"><span data-stu-id="f56bd-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="f56bd-115">參數</span><span class="sxs-lookup"><span data-stu-id="f56bd-115">PARAMETERS</span></span>

### <span data-ttu-id="f56bd-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="f56bd-116">-Name</span></span>
<span data-ttu-id="f56bd-117">儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="f56bd-117">Name of the storage volume.</span></span>

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

### <span data-ttu-id="f56bd-118">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="f56bd-118">-StoragePool</span></span>
<span data-ttu-id="f56bd-119">儲存空間池名稱。</span><span class="sxs-lookup"><span data-stu-id="f56bd-119">Storage pool name.</span></span>

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

### <span data-ttu-id="f56bd-120">-It</span><span class="sxs-lookup"><span data-stu-id="f56bd-120">-StorageSystem</span></span>
<span data-ttu-id="f56bd-121">儲存系統資源的表示。</span><span class="sxs-lookup"><span data-stu-id="f56bd-121">Representation of a storage system resource.</span></span>

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

### <span data-ttu-id="f56bd-122">-位置</span><span class="sxs-lookup"><span data-stu-id="f56bd-122">-Location</span></span>
<span data-ttu-id="f56bd-123">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="f56bd-123">Location of the resource.</span></span>

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

### <span data-ttu-id="f56bd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f56bd-124">-ResourceGroupName</span></span>
<span data-ttu-id="f56bd-125">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f56bd-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="f56bd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f56bd-126">-ResourceId</span></span>
<span data-ttu-id="f56bd-127">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="f56bd-127">The resource id.</span></span>

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

### <span data-ttu-id="f56bd-128">-篩選</span><span class="sxs-lookup"><span data-stu-id="f56bd-128">-Filter</span></span>
<span data-ttu-id="f56bd-129">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="f56bd-129">OData filter parameter.</span></span>

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

### <span data-ttu-id="f56bd-130">-略過</span><span class="sxs-lookup"><span data-stu-id="f56bd-130">-Skip</span></span>
<span data-ttu-id="f56bd-131">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="f56bd-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f56bd-132">-上方</span><span class="sxs-lookup"><span data-stu-id="f56bd-132">-Top</span></span>
<span data-ttu-id="f56bd-133">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="f56bd-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f56bd-134">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="f56bd-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f56bd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f56bd-135">CommonParameters</span></span>
<span data-ttu-id="f56bd-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f56bd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f56bd-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f56bd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f56bd-138">輸入</span><span class="sxs-lookup"><span data-stu-id="f56bd-138">INPUTS</span></span>

## <span data-ttu-id="f56bd-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f56bd-139">OUTPUTS</span></span>

### <span data-ttu-id="f56bd-140">AzureStack （管理模型）。</span><span class="sxs-lookup"><span data-stu-id="f56bd-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="f56bd-141">筆記</span><span class="sxs-lookup"><span data-stu-id="f56bd-141">NOTES</span></span>

## <span data-ttu-id="f56bd-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="f56bd-142">RELATED LINKS</span></span>
