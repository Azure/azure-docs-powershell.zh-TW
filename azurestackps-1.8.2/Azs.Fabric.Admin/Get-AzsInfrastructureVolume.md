---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: deaefa8e98e27572fb3faa9443c296e5a15accb0
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968576"
---
# <span data-ttu-id="5e41e-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="5e41e-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="5e41e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e41e-102">SYNOPSIS</span></span>
<span data-ttu-id="5e41e-103">傳回位於某個位置的所有儲存空間清單。</span><span class="sxs-lookup"><span data-stu-id="5e41e-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="5e41e-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e41e-104">SYNTAX</span></span>

### <span data-ttu-id="5e41e-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="5e41e-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5e41e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="5e41e-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="5e41e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e41e-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5e41e-108">說明</span><span class="sxs-lookup"><span data-stu-id="5e41e-108">DESCRIPTION</span></span>
<span data-ttu-id="5e41e-109">傳回位於某個位置的所有儲存空間清單。</span><span class="sxs-lookup"><span data-stu-id="5e41e-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="5e41e-110">示例</span><span class="sxs-lookup"><span data-stu-id="5e41e-110">EXAMPLES</span></span>

### <span data-ttu-id="5e41e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="5e41e-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="5e41e-112">取得指定位置上所有儲存空間的清單。</span><span class="sxs-lookup"><span data-stu-id="5e41e-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="5e41e-113">範例2</span><span class="sxs-lookup"><span data-stu-id="5e41e-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="5e41e-114">依名稱在指定位置取得儲存空間量。</span><span class="sxs-lookup"><span data-stu-id="5e41e-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="5e41e-115">參數</span><span class="sxs-lookup"><span data-stu-id="5e41e-115">PARAMETERS</span></span>

### <span data-ttu-id="5e41e-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e41e-116">-Name</span></span>
<span data-ttu-id="5e41e-117">儲存空間量的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e41e-117">Name of the storage volume.</span></span>

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

### <span data-ttu-id="5e41e-118">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="5e41e-118">-StoragePool</span></span>
<span data-ttu-id="5e41e-119">儲存空間池名稱。</span><span class="sxs-lookup"><span data-stu-id="5e41e-119">Storage pool name.</span></span>

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

### <span data-ttu-id="5e41e-120">-It</span><span class="sxs-lookup"><span data-stu-id="5e41e-120">-StorageSystem</span></span>
<span data-ttu-id="5e41e-121">儲存系統資源的表示。</span><span class="sxs-lookup"><span data-stu-id="5e41e-121">Representation of a storage system resource.</span></span>

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

### <span data-ttu-id="5e41e-122">-位置</span><span class="sxs-lookup"><span data-stu-id="5e41e-122">-Location</span></span>
<span data-ttu-id="5e41e-123">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="5e41e-123">Location of the resource.</span></span>

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

### <span data-ttu-id="5e41e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e41e-124">-ResourceGroupName</span></span>
<span data-ttu-id="5e41e-125">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5e41e-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="5e41e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e41e-126">-ResourceId</span></span>
<span data-ttu-id="5e41e-127">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="5e41e-127">The resource id.</span></span>

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

### <span data-ttu-id="5e41e-128">-篩選</span><span class="sxs-lookup"><span data-stu-id="5e41e-128">-Filter</span></span>
<span data-ttu-id="5e41e-129">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="5e41e-129">OData filter parameter.</span></span>

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

### <span data-ttu-id="5e41e-130">-略過</span><span class="sxs-lookup"><span data-stu-id="5e41e-130">-Skip</span></span>
<span data-ttu-id="5e41e-131">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="5e41e-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5e41e-132">-上方</span><span class="sxs-lookup"><span data-stu-id="5e41e-132">-Top</span></span>
<span data-ttu-id="5e41e-133">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="5e41e-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5e41e-134">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="5e41e-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5e41e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e41e-135">CommonParameters</span></span>
<span data-ttu-id="5e41e-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e41e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e41e-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e41e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e41e-138">輸入</span><span class="sxs-lookup"><span data-stu-id="5e41e-138">INPUTS</span></span>

## <span data-ttu-id="5e41e-139">輸出</span><span class="sxs-lookup"><span data-stu-id="5e41e-139">OUTPUTS</span></span>

### <span data-ttu-id="5e41e-140">AzureStack （管理模型）。</span><span class="sxs-lookup"><span data-stu-id="5e41e-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="5e41e-141">筆記</span><span class="sxs-lookup"><span data-stu-id="5e41e-141">NOTES</span></span>

## <span data-ttu-id="5e41e-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e41e-142">RELATED LINKS</span></span>
