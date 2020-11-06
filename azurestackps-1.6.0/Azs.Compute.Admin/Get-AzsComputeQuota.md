---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 30a1bc70b4e704d8dadf864dedf7173476909cf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442419"
---
# <span data-ttu-id="4ec7e-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="4ec7e-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="4ec7e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ec7e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec7e-103">傳回指定計算物件配額限制的配額。</span><span class="sxs-lookup"><span data-stu-id="4ec7e-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="4ec7e-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ec7e-104">SYNTAX</span></span>

### <span data-ttu-id="4ec7e-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="4ec7e-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="4ec7e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="4ec7e-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="4ec7e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ec7e-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="4ec7e-108">說明</span><span class="sxs-lookup"><span data-stu-id="4ec7e-108">DESCRIPTION</span></span>
<span data-ttu-id="4ec7e-109">取得現有配額的清單。</span><span class="sxs-lookup"><span data-stu-id="4ec7e-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="4ec7e-110">示例</span><span class="sxs-lookup"><span data-stu-id="4ec7e-110">EXAMPLES</span></span>

### <span data-ttu-id="4ec7e-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4ec7e-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="4ec7e-112">取得指定位置的所有計算配額。</span><span class="sxs-lookup"><span data-stu-id="4ec7e-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="4ec7e-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="4ec7e-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="4ec7e-114">取得特定的計算配額。</span><span class="sxs-lookup"><span data-stu-id="4ec7e-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="4ec7e-115">參數</span><span class="sxs-lookup"><span data-stu-id="4ec7e-115">PARAMETERS</span></span>

### <span data-ttu-id="4ec7e-116">-位置</span><span class="sxs-lookup"><span data-stu-id="4ec7e-116">-Location</span></span>
<span data-ttu-id="4ec7e-117">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="4ec7e-117">Location of the resource.</span></span>

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

### <span data-ttu-id="4ec7e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ec7e-118">-Name</span></span>
<span data-ttu-id="4ec7e-119">配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ec7e-119">Name of the quota.</span></span>

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

### <span data-ttu-id="4ec7e-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ec7e-120">-ResourceId</span></span>
<span data-ttu-id="4ec7e-121">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="4ec7e-121">The resource id.</span></span>

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

### <span data-ttu-id="4ec7e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec7e-122">CommonParameters</span></span>
<span data-ttu-id="4ec7e-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ec7e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec7e-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4ec7e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec7e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="4ec7e-125">INPUTS</span></span>

## <span data-ttu-id="4ec7e-126">輸出</span><span class="sxs-lookup"><span data-stu-id="4ec7e-126">OUTPUTS</span></span>

### <span data-ttu-id="4ec7e-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="4ec7e-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="4ec7e-128">筆記</span><span class="sxs-lookup"><span data-stu-id="4ec7e-128">NOTES</span></span>

## <span data-ttu-id="4ec7e-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ec7e-129">RELATED LINKS</span></span>

