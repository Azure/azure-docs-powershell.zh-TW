---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88ba307bb9232176d4900b80856e0e08b3dc445b
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793927"
---
# <span data-ttu-id="49e07-101">Get-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="49e07-101">Get-AzsSubscription</span></span>

## <span data-ttu-id="49e07-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49e07-102">SYNOPSIS</span></span>
<span data-ttu-id="49e07-103">取得訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="49e07-103">Get the list of subscriptions.</span></span>

## <span data-ttu-id="49e07-104">句法</span><span class="sxs-lookup"><span data-stu-id="49e07-104">SYNTAX</span></span>

### <span data-ttu-id="49e07-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="49e07-105">List (Default)</span></span>
```
Get-AzsSubscription [<CommonParameters>]
```

### <span data-ttu-id="49e07-106">獲取</span><span class="sxs-lookup"><span data-stu-id="49e07-106">Get</span></span>
```
Get-AzsSubscription [-SubscriptionId] <String> [<CommonParameters>]
```

## <span data-ttu-id="49e07-107">說明</span><span class="sxs-lookup"><span data-stu-id="49e07-107">DESCRIPTION</span></span>
<span data-ttu-id="49e07-108">取得訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="49e07-108">Get the list of subscriptions.</span></span>

## <span data-ttu-id="49e07-109">示例</span><span class="sxs-lookup"><span data-stu-id="49e07-109">EXAMPLES</span></span>

### <span data-ttu-id="49e07-110">範例1</span><span class="sxs-lookup"><span data-stu-id="49e07-110">EXAMPLE 1</span></span>
```
Get-AzsSubscription
```

<span data-ttu-id="49e07-111">取得訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="49e07-111">Get the list of subscriptions.</span></span>

## <span data-ttu-id="49e07-112">參數</span><span class="sxs-lookup"><span data-stu-id="49e07-112">PARAMETERS</span></span>

### <span data-ttu-id="49e07-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49e07-113">-SubscriptionId</span></span>
<span data-ttu-id="49e07-114">訂閱的 Id。</span><span class="sxs-lookup"><span data-stu-id="49e07-114">Id of the subscription.</span></span>

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

### <span data-ttu-id="49e07-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e07-115">CommonParameters</span></span>
<span data-ttu-id="49e07-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49e07-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49e07-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49e07-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e07-118">輸入</span><span class="sxs-lookup"><span data-stu-id="49e07-118">INPUTS</span></span>

## <span data-ttu-id="49e07-119">輸出</span><span class="sxs-lookup"><span data-stu-id="49e07-119">OUTPUTS</span></span>

### <span data-ttu-id="49e07-120">AzureStack. SubscriptionModel 的 [訂閱]。</span><span class="sxs-lookup"><span data-stu-id="49e07-120">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="49e07-121">筆記</span><span class="sxs-lookup"><span data-stu-id="49e07-121">NOTES</span></span>

## <span data-ttu-id="49e07-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="49e07-122">RELATED LINKS</span></span>
