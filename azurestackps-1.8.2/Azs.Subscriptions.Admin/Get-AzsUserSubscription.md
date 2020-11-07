---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968431"
---
# <span data-ttu-id="10dda-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="10dda-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="10dda-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10dda-102">SYNOPSIS</span></span>
<span data-ttu-id="10dda-103">以系統管理員身分取得使用者訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="10dda-103">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="10dda-104">句法</span><span class="sxs-lookup"><span data-stu-id="10dda-104">SYNTAX</span></span>

### <span data-ttu-id="10dda-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="10dda-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="10dda-106">獲取</span><span class="sxs-lookup"><span data-stu-id="10dda-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="10dda-107">說明</span><span class="sxs-lookup"><span data-stu-id="10dda-107">DESCRIPTION</span></span>
<span data-ttu-id="10dda-108">以系統管理員身分取得使用者訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="10dda-108">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="10dda-109">示例</span><span class="sxs-lookup"><span data-stu-id="10dda-109">EXAMPLES</span></span>

### <span data-ttu-id="10dda-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="10dda-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="10dda-111">以系統管理員身分取得使用者訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="10dda-111">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="10dda-112">參數</span><span class="sxs-lookup"><span data-stu-id="10dda-112">PARAMETERS</span></span>

### <span data-ttu-id="10dda-113">-篩選</span><span class="sxs-lookup"><span data-stu-id="10dda-113">-Filter</span></span>
<span data-ttu-id="10dda-114">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="10dda-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="10dda-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10dda-115">-SubscriptionId</span></span>
<span data-ttu-id="10dda-116">[訂閱識別碼] 參數。</span><span class="sxs-lookup"><span data-stu-id="10dda-116">Subscription Id parameter.</span></span>

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

### <span data-ttu-id="10dda-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10dda-117">CommonParameters</span></span>
<span data-ttu-id="10dda-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10dda-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10dda-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="10dda-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10dda-120">輸入</span><span class="sxs-lookup"><span data-stu-id="10dda-120">INPUTS</span></span>

## <span data-ttu-id="10dda-121">輸出</span><span class="sxs-lookup"><span data-stu-id="10dda-121">OUTPUTS</span></span>

### <span data-ttu-id="10dda-122">AzureStack. 系統管理. 訂閱</span><span class="sxs-lookup"><span data-stu-id="10dda-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="10dda-123">筆記</span><span class="sxs-lookup"><span data-stu-id="10dda-123">NOTES</span></span>

## <span data-ttu-id="10dda-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="10dda-124">RELATED LINKS</span></span>

