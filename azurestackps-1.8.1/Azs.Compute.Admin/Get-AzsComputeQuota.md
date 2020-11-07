---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 819cdc45e75c15c38c9ae28c583ac3c73e54f4ac
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793998"
---
# <span data-ttu-id="c2d60-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="c2d60-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="c2d60-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2d60-102">SYNOPSIS</span></span>
<span data-ttu-id="c2d60-103">傳回指定計算物件配額限制的配額。</span><span class="sxs-lookup"><span data-stu-id="c2d60-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="c2d60-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2d60-104">SYNTAX</span></span>

### <span data-ttu-id="c2d60-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="c2d60-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="c2d60-106">獲取</span><span class="sxs-lookup"><span data-stu-id="c2d60-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="c2d60-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2d60-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c2d60-108">說明</span><span class="sxs-lookup"><span data-stu-id="c2d60-108">DESCRIPTION</span></span>
<span data-ttu-id="c2d60-109">取得現有配額的清單。</span><span class="sxs-lookup"><span data-stu-id="c2d60-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="c2d60-110">示例</span><span class="sxs-lookup"><span data-stu-id="c2d60-110">EXAMPLES</span></span>

### <span data-ttu-id="c2d60-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c2d60-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="c2d60-112">取得指定位置的所有計算配額。</span><span class="sxs-lookup"><span data-stu-id="c2d60-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="c2d60-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c2d60-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="c2d60-114">取得特定的計算配額。</span><span class="sxs-lookup"><span data-stu-id="c2d60-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="c2d60-115">參數</span><span class="sxs-lookup"><span data-stu-id="c2d60-115">PARAMETERS</span></span>

### <span data-ttu-id="c2d60-116">-位置</span><span class="sxs-lookup"><span data-stu-id="c2d60-116">-Location</span></span>
<span data-ttu-id="c2d60-117">{{Fill 位置描述}}</span><span class="sxs-lookup"><span data-stu-id="c2d60-117">{{Fill Location Description}}</span></span>

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

### <span data-ttu-id="c2d60-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2d60-118">-Name</span></span>
<span data-ttu-id="c2d60-119">配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2d60-119">Name of the quota.</span></span>

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

### <span data-ttu-id="c2d60-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2d60-120">-ResourceId</span></span>
<span data-ttu-id="c2d60-121">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="c2d60-121">The resource id.</span></span>

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

### <span data-ttu-id="c2d60-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2d60-122">CommonParameters</span></span>
<span data-ttu-id="c2d60-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2d60-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2d60-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2d60-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2d60-125">輸入</span><span class="sxs-lookup"><span data-stu-id="c2d60-125">INPUTS</span></span>

## <span data-ttu-id="c2d60-126">輸出</span><span class="sxs-lookup"><span data-stu-id="c2d60-126">OUTPUTS</span></span>

### <span data-ttu-id="c2d60-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="c2d60-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="c2d60-128">筆記</span><span class="sxs-lookup"><span data-stu-id="c2d60-128">NOTES</span></span>

## <span data-ttu-id="c2d60-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2d60-129">RELATED LINKS</span></span>

