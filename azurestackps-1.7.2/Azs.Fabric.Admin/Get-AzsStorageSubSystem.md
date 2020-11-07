---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2abc9073b9e7bcbcd4644150ada4c19cd351f660
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792988"
---
# <span data-ttu-id="c93ef-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="c93ef-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="c93ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c93ef-102">SYNOPSIS</span></span>
<span data-ttu-id="c93ef-103">針對比例單位傳回所有儲存子系統的清單。</span><span class="sxs-lookup"><span data-stu-id="c93ef-103">Returns a list of all storage subsystems for a scale unit.</span></span>

## <span data-ttu-id="c93ef-104">句法</span><span class="sxs-lookup"><span data-stu-id="c93ef-104">SYNTAX</span></span>

### <span data-ttu-id="c93ef-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="c93ef-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c93ef-106">獲取</span><span class="sxs-lookup"><span data-stu-id="c93ef-106">Get</span></span>
```
Get-AzsStorageSubSystem [-Name] <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c93ef-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c93ef-107">ResourceId</span></span>
```
Get-AzsStorageSubSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c93ef-108">說明</span><span class="sxs-lookup"><span data-stu-id="c93ef-108">DESCRIPTION</span></span>
<span data-ttu-id="c93ef-109">針對比例單位傳回所有儲存子系統的清單。</span><span class="sxs-lookup"><span data-stu-id="c93ef-109">Returns a list of all storage subsystems for a scale unit.</span></span>

## <span data-ttu-id="c93ef-110">示例</span><span class="sxs-lookup"><span data-stu-id="c93ef-110">EXAMPLES</span></span>

### <span data-ttu-id="c93ef-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c93ef-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit S-Cluster
```

<span data-ttu-id="c93ef-112">從比例單位取得所有儲存子系統。</span><span class="sxs-lookup"><span data-stu-id="c93ef-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="c93ef-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c93ef-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit S-Cluster -Name S-Cluster.azurestack.local
```

<span data-ttu-id="c93ef-114">取得具有縮放比例單位和名稱的儲存子系統。</span><span class="sxs-lookup"><span data-stu-id="c93ef-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="c93ef-115">參數</span><span class="sxs-lookup"><span data-stu-id="c93ef-115">PARAMETERS</span></span>

### <span data-ttu-id="c93ef-116">-篩選</span><span class="sxs-lookup"><span data-stu-id="c93ef-116">-Filter</span></span>
<span data-ttu-id="c93ef-117">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="c93ef-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="c93ef-118">-位置</span><span class="sxs-lookup"><span data-stu-id="c93ef-118">-Location</span></span>
<span data-ttu-id="c93ef-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="c93ef-119">Location of the resource.</span></span>

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

### <span data-ttu-id="c93ef-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c93ef-120">-Name</span></span>
<span data-ttu-id="c93ef-121">儲存子系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="c93ef-121">Name of the storage subsystem.</span></span>

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

### <span data-ttu-id="c93ef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c93ef-122">-ResourceGroupName</span></span>
<span data-ttu-id="c93ef-123">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c93ef-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c93ef-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c93ef-124">-ResourceId</span></span>
<span data-ttu-id="c93ef-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="c93ef-125">The resource id.</span></span>

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

### <span data-ttu-id="c93ef-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c93ef-126">-ScaleUnit</span></span>
<span data-ttu-id="c93ef-127">縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="c93ef-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="c93ef-128">-上方</span><span class="sxs-lookup"><span data-stu-id="c93ef-128">-Top</span></span>
<span data-ttu-id="c93ef-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="c93ef-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c93ef-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="c93ef-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c93ef-131">-略過</span><span class="sxs-lookup"><span data-stu-id="c93ef-131">-Skip</span></span>
<span data-ttu-id="c93ef-132">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="c93ef-132">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c93ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c93ef-133">CommonParameters</span></span>
<span data-ttu-id="c93ef-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c93ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c93ef-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c93ef-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c93ef-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c93ef-136">INPUTS</span></span>

## <span data-ttu-id="c93ef-137">輸出</span><span class="sxs-lookup"><span data-stu-id="c93ef-137">OUTPUTS</span></span>

### <span data-ttu-id="c93ef-138">StorageSubSystem 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="c93ef-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSubSystem</span></span>
## <span data-ttu-id="c93ef-139">筆記</span><span class="sxs-lookup"><span data-stu-id="c93ef-139">NOTES</span></span>

## <span data-ttu-id="c93ef-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="c93ef-140">RELATED LINKS</span></span>
