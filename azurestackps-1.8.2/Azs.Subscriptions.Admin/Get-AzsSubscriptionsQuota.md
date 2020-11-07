---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3874c581d1d030f9c0b77abe82b5a5a289d8960d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968430"
---
# <span data-ttu-id="fe2e2-101">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="fe2e2-101">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="fe2e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe2e2-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2e2-103">取得位置的訂閱資源提供者配額清單。</span><span class="sxs-lookup"><span data-stu-id="fe2e2-103">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="fe2e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe2e2-104">SYNTAX</span></span>

### <span data-ttu-id="fe2e2-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="fe2e2-105">List (Default)</span></span>
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="fe2e2-106">獲取</span><span class="sxs-lookup"><span data-stu-id="fe2e2-106">Get</span></span>
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="fe2e2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe2e2-107">ResourceId</span></span>
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="fe2e2-108">說明</span><span class="sxs-lookup"><span data-stu-id="fe2e2-108">DESCRIPTION</span></span>
<span data-ttu-id="fe2e2-109">取得位置的配額清單。</span><span class="sxs-lookup"><span data-stu-id="fe2e2-109">Get the list of quotas at a location.</span></span>

## <span data-ttu-id="fe2e2-110">示例</span><span class="sxs-lookup"><span data-stu-id="fe2e2-110">EXAMPLES</span></span>

### <span data-ttu-id="fe2e2-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fe2e2-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionsQuota
```

<span data-ttu-id="fe2e2-112">取得位置的訂閱資源提供者配額清單。</span><span class="sxs-lookup"><span data-stu-id="fe2e2-112">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="fe2e2-113">參數</span><span class="sxs-lookup"><span data-stu-id="fe2e2-113">PARAMETERS</span></span>

### <span data-ttu-id="fe2e2-114">-位置</span><span class="sxs-lookup"><span data-stu-id="fe2e2-114">-Location</span></span>
<span data-ttu-id="fe2e2-115">AzureStack 位置。</span><span class="sxs-lookup"><span data-stu-id="fe2e2-115">The AzureStack location.</span></span>

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

### <span data-ttu-id="fe2e2-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe2e2-116">-Name</span></span>
<span data-ttu-id="fe2e2-117">配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe2e2-117">Name of the quota.</span></span>

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

### <span data-ttu-id="fe2e2-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe2e2-118">-ResourceId</span></span>
<span data-ttu-id="fe2e2-119">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="fe2e2-119">The resource id.</span></span>

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

### <span data-ttu-id="fe2e2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2e2-120">CommonParameters</span></span>
<span data-ttu-id="fe2e2-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe2e2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2e2-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe2e2-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2e2-123">輸入</span><span class="sxs-lookup"><span data-stu-id="fe2e2-123">INPUTS</span></span>

## <span data-ttu-id="fe2e2-124">輸出</span><span class="sxs-lookup"><span data-stu-id="fe2e2-124">OUTPUTS</span></span>

### <span data-ttu-id="fe2e2-125">AzureStack. 系統管理. [管理員]。</span><span class="sxs-lookup"><span data-stu-id="fe2e2-125">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Quota</span></span>

## <span data-ttu-id="fe2e2-126">筆記</span><span class="sxs-lookup"><span data-stu-id="fe2e2-126">NOTES</span></span>

## <span data-ttu-id="fe2e2-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe2e2-127">RELATED LINKS</span></span>

