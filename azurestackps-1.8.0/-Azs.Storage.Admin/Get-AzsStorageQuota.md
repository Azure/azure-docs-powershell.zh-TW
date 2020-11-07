---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e4277ee88af840674d6fc8e4e2d5f614e745ace
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793705"
---
# <span data-ttu-id="7d4a8-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="7d4a8-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="7d4a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d4a8-102">SYNOPSIS</span></span>
<span data-ttu-id="7d4a8-103">傳回指定位置的儲存配額清單。</span><span class="sxs-lookup"><span data-stu-id="7d4a8-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="7d4a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d4a8-104">SYNTAX</span></span>

### <span data-ttu-id="7d4a8-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="7d4a8-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7d4a8-106">獲取</span><span class="sxs-lookup"><span data-stu-id="7d4a8-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="7d4a8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d4a8-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7d4a8-108">說明</span><span class="sxs-lookup"><span data-stu-id="7d4a8-108">DESCRIPTION</span></span>
<span data-ttu-id="7d4a8-109">傳回指定位置的儲存配額清單。</span><span class="sxs-lookup"><span data-stu-id="7d4a8-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="7d4a8-110">示例</span><span class="sxs-lookup"><span data-stu-id="7d4a8-110">EXAMPLES</span></span>

### <span data-ttu-id="7d4a8-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7d4a8-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="7d4a8-112">取得儲存配額清單。</span><span class="sxs-lookup"><span data-stu-id="7d4a8-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="7d4a8-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="7d4a8-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="7d4a8-114">依名稱取得指定儲存配額的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7d4a8-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="7d4a8-115">參數</span><span class="sxs-lookup"><span data-stu-id="7d4a8-115">PARAMETERS</span></span>

### <span data-ttu-id="7d4a8-116">-位置</span><span class="sxs-lookup"><span data-stu-id="7d4a8-116">-Location</span></span>
<span data-ttu-id="7d4a8-117">資源位置。</span><span class="sxs-lookup"><span data-stu-id="7d4a8-117">Resource location.</span></span>

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

### <span data-ttu-id="7d4a8-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d4a8-118">-Name</span></span>
<span data-ttu-id="7d4a8-119">儲存配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d4a8-119">The name of the storage quota.</span></span>

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

### <span data-ttu-id="7d4a8-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d4a8-120">-ResourceId</span></span>
<span data-ttu-id="7d4a8-121">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="7d4a8-121">The resource id.</span></span>

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

### <span data-ttu-id="7d4a8-122">-略過</span><span class="sxs-lookup"><span data-stu-id="7d4a8-122">-Skip</span></span>
<span data-ttu-id="7d4a8-123">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="7d4a8-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="7d4a8-124">-上方</span><span class="sxs-lookup"><span data-stu-id="7d4a8-124">-Top</span></span>
<span data-ttu-id="7d4a8-125">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="7d4a8-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7d4a8-126">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="7d4a8-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="7d4a8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d4a8-127">CommonParameters</span></span>
<span data-ttu-id="7d4a8-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d4a8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d4a8-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d4a8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d4a8-130">輸入</span><span class="sxs-lookup"><span data-stu-id="7d4a8-130">INPUTS</span></span>

## <span data-ttu-id="7d4a8-131">輸出</span><span class="sxs-lookup"><span data-stu-id="7d4a8-131">OUTPUTS</span></span>

### <span data-ttu-id="7d4a8-132">AzureStack （StorageQuota）的</span><span class="sxs-lookup"><span data-stu-id="7d4a8-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="7d4a8-133">筆記</span><span class="sxs-lookup"><span data-stu-id="7d4a8-133">NOTES</span></span>

## <span data-ttu-id="7d4a8-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d4a8-134">RELATED LINKS</span></span>
