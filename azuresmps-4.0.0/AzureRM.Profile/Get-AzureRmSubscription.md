---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 13dd14f59b28e3b5730f207c675771e1275392d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442819"
---
# <span data-ttu-id="2ce63-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="2ce63-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="2ce63-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ce63-102">SYNOPSIS</span></span>
<span data-ttu-id="2ce63-103">取得目前帳戶可以存取的訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ce63-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="2ce63-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ce63-104">SYNTAX</span></span>

### <span data-ttu-id="2ce63-105">ListByIdInTenant (預設) </span><span class="sxs-lookup"><span data-stu-id="2ce63-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [<CommonParameters>]
```

### <span data-ttu-id="2ce63-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="2ce63-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [<CommonParameters>]
```

## <span data-ttu-id="2ce63-107">說明</span><span class="sxs-lookup"><span data-stu-id="2ce63-107">DESCRIPTION</span></span>
<span data-ttu-id="2ce63-108">Get-AzureRmSubscription Cmdlet 會取得目前帳戶可存取之訂閱的訂閱識別碼、訂閱名稱及家用租使用者。</span><span class="sxs-lookup"><span data-stu-id="2ce63-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="2ce63-109">示例</span><span class="sxs-lookup"><span data-stu-id="2ce63-109">EXAMPLES</span></span>

### <span data-ttu-id="2ce63-110">範例1：取得所有承租人中的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="2ce63-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription -All

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="2ce63-111">這個命令會取得所有針對目前帳戶授權的租使用者的訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ce63-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="2ce63-112">範例2：取得特定租使用者的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="2ce63-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="2ce63-113">列出已針對目前帳戶授權的指定租使用者中的所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ce63-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="2ce63-114">範例3：取得目前租使用者中的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="2ce63-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="2ce63-115">這個命令會在目前的租使用者中取得目前已授權的所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ce63-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="2ce63-116">範例4：變更目前的內容以使用特定的訂閱</span><span class="sxs-lookup"><span data-stu-id="2ce63-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="2ce63-117">這個命令會取得指定的訂閱，然後設定目前的內容來使用它。</span><span class="sxs-lookup"><span data-stu-id="2ce63-117">This command gets the specified subscription, and then sets the current context to use it.</span></span>
<span data-ttu-id="2ce63-118">此會話中的所有後續 Cmdlet 都會預設使用 (Contoso 訂閱 1) 的新訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ce63-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="2ce63-119">參數</span><span class="sxs-lookup"><span data-stu-id="2ce63-119">PARAMETERS</span></span>

### <span data-ttu-id="2ce63-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ce63-120">-SubscriptionId</span></span>
<span data-ttu-id="2ce63-121">指定要取得的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="2ce63-121">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ce63-122">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="2ce63-122">-SubscriptionName</span></span>
<span data-ttu-id="2ce63-123">指定要取得的訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="2ce63-123">Specifies the name of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ce63-124">-TenantId</span><span class="sxs-lookup"><span data-stu-id="2ce63-124">-TenantId</span></span>
<span data-ttu-id="2ce63-125">指定包含要取得之訂閱的租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="2ce63-125">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ce63-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ce63-126">CommonParameters</span></span>
<span data-ttu-id="2ce63-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ce63-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ce63-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2ce63-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ce63-129">輸入</span><span class="sxs-lookup"><span data-stu-id="2ce63-129">INPUTS</span></span>

## <span data-ttu-id="2ce63-130">輸出</span><span class="sxs-lookup"><span data-stu-id="2ce63-130">OUTPUTS</span></span>

### <span data-ttu-id="2ce63-131">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="2ce63-131">PSAzureSubscription</span></span>

## <span data-ttu-id="2ce63-132">筆記</span><span class="sxs-lookup"><span data-stu-id="2ce63-132">NOTES</span></span>

## <span data-ttu-id="2ce63-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ce63-133">RELATED LINKS</span></span>

