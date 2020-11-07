---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503661f4e50ddd7575cc9c98ef4c19e2028ddf83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793128"
---
# <span data-ttu-id="94bf6-101">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="94bf6-101">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="94bf6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="94bf6-103">取得位置的訂閱資源提供者配額清單。</span><span class="sxs-lookup"><span data-stu-id="94bf6-103">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="94bf6-104">句法</span><span class="sxs-lookup"><span data-stu-id="94bf6-104">SYNTAX</span></span>

### <span data-ttu-id="94bf6-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="94bf6-105">List (Default)</span></span>
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="94bf6-106">獲取</span><span class="sxs-lookup"><span data-stu-id="94bf6-106">Get</span></span>
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="94bf6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="94bf6-107">ResourceId</span></span>
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="94bf6-108">說明</span><span class="sxs-lookup"><span data-stu-id="94bf6-108">DESCRIPTION</span></span>
<span data-ttu-id="94bf6-109">取得位置的配額清單。</span><span class="sxs-lookup"><span data-stu-id="94bf6-109">Get the list of quotas at a location.</span></span>

## <span data-ttu-id="94bf6-110">示例</span><span class="sxs-lookup"><span data-stu-id="94bf6-110">EXAMPLES</span></span>

### <span data-ttu-id="94bf6-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="94bf6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionsQuota
```

<span data-ttu-id="94bf6-112">取得位置的訂閱資源提供者配額清單。</span><span class="sxs-lookup"><span data-stu-id="94bf6-112">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="94bf6-113">參數</span><span class="sxs-lookup"><span data-stu-id="94bf6-113">PARAMETERS</span></span>

### <span data-ttu-id="94bf6-114">-位置</span><span class="sxs-lookup"><span data-stu-id="94bf6-114">-Location</span></span>
<span data-ttu-id="94bf6-115">AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="94bf6-115">The AzureStack location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94bf6-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="94bf6-116">-Name</span></span>
<span data-ttu-id="94bf6-117">配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="94bf6-117">Name of the quota.</span></span>

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

### <span data-ttu-id="94bf6-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94bf6-118">-ResourceId</span></span>
<span data-ttu-id="94bf6-119">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="94bf6-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94bf6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94bf6-120">CommonParameters</span></span>
<span data-ttu-id="94bf6-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94bf6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94bf6-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="94bf6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94bf6-123">輸入</span><span class="sxs-lookup"><span data-stu-id="94bf6-123">INPUTS</span></span>

## <span data-ttu-id="94bf6-124">輸出</span><span class="sxs-lookup"><span data-stu-id="94bf6-124">OUTPUTS</span></span>

### <span data-ttu-id="94bf6-125">AzureStack. 系統管理. [管理員]。</span><span class="sxs-lookup"><span data-stu-id="94bf6-125">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Quota</span></span>

## <span data-ttu-id="94bf6-126">筆記</span><span class="sxs-lookup"><span data-stu-id="94bf6-126">NOTES</span></span>

## <span data-ttu-id="94bf6-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="94bf6-127">RELATED LINKS</span></span>

