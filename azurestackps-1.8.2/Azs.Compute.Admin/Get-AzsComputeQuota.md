---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 819cdc45e75c15c38c9ae28c583ac3c73e54f4ac
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968142"
---
# <span data-ttu-id="8489d-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="8489d-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="8489d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8489d-102">SYNOPSIS</span></span>
<span data-ttu-id="8489d-103">傳回指定計算物件配額限制的配額。</span><span class="sxs-lookup"><span data-stu-id="8489d-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="8489d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8489d-104">SYNTAX</span></span>

### <span data-ttu-id="8489d-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="8489d-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="8489d-106">獲取</span><span class="sxs-lookup"><span data-stu-id="8489d-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="8489d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8489d-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8489d-108">說明</span><span class="sxs-lookup"><span data-stu-id="8489d-108">DESCRIPTION</span></span>
<span data-ttu-id="8489d-109">取得現有配額的清單。</span><span class="sxs-lookup"><span data-stu-id="8489d-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="8489d-110">示例</span><span class="sxs-lookup"><span data-stu-id="8489d-110">EXAMPLES</span></span>

### <span data-ttu-id="8489d-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8489d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="8489d-112">取得指定位置的所有計算配額。</span><span class="sxs-lookup"><span data-stu-id="8489d-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="8489d-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="8489d-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="8489d-114">取得特定的計算配額。</span><span class="sxs-lookup"><span data-stu-id="8489d-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="8489d-115">參數</span><span class="sxs-lookup"><span data-stu-id="8489d-115">PARAMETERS</span></span>

### <span data-ttu-id="8489d-116">-位置</span><span class="sxs-lookup"><span data-stu-id="8489d-116">-Location</span></span>
<span data-ttu-id="8489d-117">{{Fill 位置描述}}</span><span class="sxs-lookup"><span data-stu-id="8489d-117">{{Fill Location Description}}</span></span>

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

### <span data-ttu-id="8489d-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="8489d-118">-Name</span></span>
<span data-ttu-id="8489d-119">配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="8489d-119">Name of the quota.</span></span>

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

### <span data-ttu-id="8489d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8489d-120">-ResourceId</span></span>
<span data-ttu-id="8489d-121">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8489d-121">The resource id.</span></span>

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

### <span data-ttu-id="8489d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8489d-122">CommonParameters</span></span>
<span data-ttu-id="8489d-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8489d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8489d-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8489d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8489d-125">輸入</span><span class="sxs-lookup"><span data-stu-id="8489d-125">INPUTS</span></span>

## <span data-ttu-id="8489d-126">輸出</span><span class="sxs-lookup"><span data-stu-id="8489d-126">OUTPUTS</span></span>

### <span data-ttu-id="8489d-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="8489d-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="8489d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="8489d-128">NOTES</span></span>

## <span data-ttu-id="8489d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="8489d-129">RELATED LINKS</span></span>

