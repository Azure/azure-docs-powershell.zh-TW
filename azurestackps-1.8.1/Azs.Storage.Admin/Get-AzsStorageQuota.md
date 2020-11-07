---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 687838573459c09ceaf08c0d1c3335caa4a99769
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793902"
---
# <span data-ttu-id="5bb96-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="5bb96-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="5bb96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5bb96-102">SYNOPSIS</span></span>
<span data-ttu-id="5bb96-103">傳回指定位置的儲存配額清單。</span><span class="sxs-lookup"><span data-stu-id="5bb96-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="5bb96-104">句法</span><span class="sxs-lookup"><span data-stu-id="5bb96-104">SYNTAX</span></span>

### <span data-ttu-id="5bb96-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="5bb96-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5bb96-106">獲取</span><span class="sxs-lookup"><span data-stu-id="5bb96-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="5bb96-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bb96-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5bb96-108">說明</span><span class="sxs-lookup"><span data-stu-id="5bb96-108">DESCRIPTION</span></span>
<span data-ttu-id="5bb96-109">傳回指定位置的儲存配額清單。</span><span class="sxs-lookup"><span data-stu-id="5bb96-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="5bb96-110">示例</span><span class="sxs-lookup"><span data-stu-id="5bb96-110">EXAMPLES</span></span>

### <span data-ttu-id="5bb96-111">範例1</span><span class="sxs-lookup"><span data-stu-id="5bb96-111">EXAMPLE 1</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="5bb96-112">取得儲存配額清單。</span><span class="sxs-lookup"><span data-stu-id="5bb96-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="5bb96-113">範例2</span><span class="sxs-lookup"><span data-stu-id="5bb96-113">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="5bb96-114">依名稱取得指定儲存配額的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5bb96-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="5bb96-115">參數</span><span class="sxs-lookup"><span data-stu-id="5bb96-115">PARAMETERS</span></span>

### <span data-ttu-id="5bb96-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="5bb96-116">-Name</span></span>
<span data-ttu-id="5bb96-117">儲存配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bb96-117">The name of the storage quota.</span></span>

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

### <span data-ttu-id="5bb96-118">-位置</span><span class="sxs-lookup"><span data-stu-id="5bb96-118">-Location</span></span>
<span data-ttu-id="5bb96-119">資源位置。</span><span class="sxs-lookup"><span data-stu-id="5bb96-119">Resource location.</span></span>

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

### <span data-ttu-id="5bb96-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bb96-120">-ResourceId</span></span>
<span data-ttu-id="5bb96-121">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="5bb96-121">The resource id.</span></span>

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

### <span data-ttu-id="5bb96-122">-略過</span><span class="sxs-lookup"><span data-stu-id="5bb96-122">-Skip</span></span>
<span data-ttu-id="5bb96-123">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="5bb96-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5bb96-124">-上方</span><span class="sxs-lookup"><span data-stu-id="5bb96-124">-Top</span></span>
<span data-ttu-id="5bb96-125">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="5bb96-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5bb96-126">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="5bb96-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5bb96-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bb96-127">CommonParameters</span></span>
<span data-ttu-id="5bb96-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5bb96-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bb96-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5bb96-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bb96-130">輸入</span><span class="sxs-lookup"><span data-stu-id="5bb96-130">INPUTS</span></span>

## <span data-ttu-id="5bb96-131">輸出</span><span class="sxs-lookup"><span data-stu-id="5bb96-131">OUTPUTS</span></span>

### <span data-ttu-id="5bb96-132">AzureStack （StorageQuota）的</span><span class="sxs-lookup"><span data-stu-id="5bb96-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="5bb96-133">筆記</span><span class="sxs-lookup"><span data-stu-id="5bb96-133">NOTES</span></span>

## <span data-ttu-id="5bb96-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="5bb96-134">RELATED LINKS</span></span>
