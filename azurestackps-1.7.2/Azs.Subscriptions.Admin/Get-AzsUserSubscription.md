---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5ff90957a655837dbdf75ce3f4242222615f2a73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793386"
---
# <span data-ttu-id="ac468-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="ac468-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="ac468-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac468-102">SYNOPSIS</span></span>
<span data-ttu-id="ac468-103">取得使用者訂閱清單做為操作員。</span><span class="sxs-lookup"><span data-stu-id="ac468-103">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="ac468-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac468-104">SYNTAX</span></span>

### <span data-ttu-id="ac468-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="ac468-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="ac468-106">獲取</span><span class="sxs-lookup"><span data-stu-id="ac468-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="ac468-107">說明</span><span class="sxs-lookup"><span data-stu-id="ac468-107">DESCRIPTION</span></span>
<span data-ttu-id="ac468-108">取得使用者訂閱清單做為操作員。</span><span class="sxs-lookup"><span data-stu-id="ac468-108">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="ac468-109">示例</span><span class="sxs-lookup"><span data-stu-id="ac468-109">EXAMPLES</span></span>

### <span data-ttu-id="ac468-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ac468-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="ac468-111">取得使用者訂閱清單做為操作員。</span><span class="sxs-lookup"><span data-stu-id="ac468-111">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="ac468-112">參數</span><span class="sxs-lookup"><span data-stu-id="ac468-112">PARAMETERS</span></span>

### <span data-ttu-id="ac468-113">-篩選</span><span class="sxs-lookup"><span data-stu-id="ac468-113">-Filter</span></span>
<span data-ttu-id="ac468-114">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="ac468-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="ac468-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac468-115">-SubscriptionId</span></span>
<span data-ttu-id="ac468-116">[訂閱識別碼] 參數。</span><span class="sxs-lookup"><span data-stu-id="ac468-116">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac468-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac468-117">CommonParameters</span></span>
<span data-ttu-id="ac468-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac468-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac468-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ac468-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac468-120">輸入</span><span class="sxs-lookup"><span data-stu-id="ac468-120">INPUTS</span></span>

## <span data-ttu-id="ac468-121">輸出</span><span class="sxs-lookup"><span data-stu-id="ac468-121">OUTPUTS</span></span>

### <span data-ttu-id="ac468-122">AzureStack. 系統管理. 訂閱</span><span class="sxs-lookup"><span data-stu-id="ac468-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="ac468-123">筆記</span><span class="sxs-lookup"><span data-stu-id="ac468-123">NOTES</span></span>

## <span data-ttu-id="ac468-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac468-124">RELATED LINKS</span></span>

