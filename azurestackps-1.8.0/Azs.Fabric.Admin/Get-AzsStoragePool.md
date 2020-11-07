---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcc4dbfdd4634c53835c588947a77c4c2e773af4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793495"
---
# <span data-ttu-id="5f1f9-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="5f1f9-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="5f1f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f1f9-102">SYNOPSIS</span></span>
<span data-ttu-id="5f1f9-103">傳回某個位置的所有儲存空間池清單。</span><span class="sxs-lookup"><span data-stu-id="5f1f9-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="5f1f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f1f9-104">SYNTAX</span></span>

### <span data-ttu-id="5f1f9-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="5f1f9-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5f1f9-106">獲取</span><span class="sxs-lookup"><span data-stu-id="5f1f9-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5f1f9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f1f9-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5f1f9-108">說明</span><span class="sxs-lookup"><span data-stu-id="5f1f9-108">DESCRIPTION</span></span>
<span data-ttu-id="5f1f9-109">傳回某個位置的所有儲存空間池清單。</span><span class="sxs-lookup"><span data-stu-id="5f1f9-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="5f1f9-110">示例</span><span class="sxs-lookup"><span data-stu-id="5f1f9-110">EXAMPLES</span></span>

### <span data-ttu-id="5f1f9-111">範例1</span><span class="sxs-lookup"><span data-stu-id="5f1f9-111">EXAMPLE 1</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="5f1f9-112">取得指定位置的所有儲存空間池。</span><span class="sxs-lookup"><span data-stu-id="5f1f9-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="5f1f9-113">範例2</span><span class="sxs-lookup"><span data-stu-id="5f1f9-113">EXAMPLE 2</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="5f1f9-114">在指定的位置取得儲存池名稱的儲存空間池。</span><span class="sxs-lookup"><span data-stu-id="5f1f9-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="5f1f9-115">參數</span><span class="sxs-lookup"><span data-stu-id="5f1f9-115">PARAMETERS</span></span>

### <span data-ttu-id="5f1f9-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="5f1f9-116">-Name</span></span>
<span data-ttu-id="5f1f9-117">儲存空間池名稱。</span><span class="sxs-lookup"><span data-stu-id="5f1f9-117">Storage pool name.</span></span>

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

### <span data-ttu-id="5f1f9-118">-It</span><span class="sxs-lookup"><span data-stu-id="5f1f9-118">-StorageSystem</span></span>
<span data-ttu-id="5f1f9-119">儲存空間子系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f1f9-119">Name of the Storage Sub System.</span></span>

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

### <span data-ttu-id="5f1f9-120">-位置</span><span class="sxs-lookup"><span data-stu-id="5f1f9-120">-Location</span></span>
<span data-ttu-id="5f1f9-121">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="5f1f9-121">Location of the resource.</span></span>

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

### <span data-ttu-id="5f1f9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f1f9-122">-ResourceGroupName</span></span>
<span data-ttu-id="5f1f9-123">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5f1f9-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="5f1f9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f1f9-124">-ResourceId</span></span>
<span data-ttu-id="5f1f9-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="5f1f9-125">The resource id.</span></span>

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

### <span data-ttu-id="5f1f9-126">-篩選</span><span class="sxs-lookup"><span data-stu-id="5f1f9-126">-Filter</span></span>
<span data-ttu-id="5f1f9-127">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="5f1f9-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="5f1f9-128">-略過</span><span class="sxs-lookup"><span data-stu-id="5f1f9-128">-Skip</span></span>
<span data-ttu-id="5f1f9-129">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="5f1f9-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5f1f9-130">-上方</span><span class="sxs-lookup"><span data-stu-id="5f1f9-130">-Top</span></span>
<span data-ttu-id="5f1f9-131">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="5f1f9-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5f1f9-132">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="5f1f9-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5f1f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f1f9-133">CommonParameters</span></span>
<span data-ttu-id="5f1f9-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f1f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f1f9-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5f1f9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f1f9-136">輸入</span><span class="sxs-lookup"><span data-stu-id="5f1f9-136">INPUTS</span></span>

## <span data-ttu-id="5f1f9-137">輸出</span><span class="sxs-lookup"><span data-stu-id="5f1f9-137">OUTPUTS</span></span>

### <span data-ttu-id="5f1f9-138">StoragePool 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="5f1f9-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="5f1f9-139">筆記</span><span class="sxs-lookup"><span data-stu-id="5f1f9-139">NOTES</span></span>

## <span data-ttu-id="5f1f9-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f1f9-140">RELATED LINKS</span></span>
