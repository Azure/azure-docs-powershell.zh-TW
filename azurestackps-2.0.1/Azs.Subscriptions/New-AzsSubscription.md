---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/new-azssubscription
schema: 2.0.0
ms.openlocfilehash: ef8ee9ce81e8ba656a43330ac564c147bcd5d615
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966621"
---
# <span data-ttu-id="4ef86-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="4ef86-101">New-AzsSubscription</span></span>

## <span data-ttu-id="4ef86-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ef86-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef86-103">建立或更新訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ef86-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="4ef86-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ef86-104">SYNTAX</span></span>

```
New-AzsSubscription -OfferId <String> [-SubscriptionId <String>] [-DisplayName <String>] [-Id <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4ef86-105">說明</span><span class="sxs-lookup"><span data-stu-id="4ef86-105">DESCRIPTION</span></span>
<span data-ttu-id="4ef86-106">建立或更新訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ef86-106">Create or updates a subscription.</span></span>

## <span data-ttu-id="4ef86-107">示例</span><span class="sxs-lookup"><span data-stu-id="4ef86-107">EXAMPLES</span></span>

### <span data-ttu-id="4ef86-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4ef86-108">Example 1</span></span>
```powershell
PS C:\> New-AzsSubscription -OfferId '/delegatedProviders/default/offers/testoffer' -DisplayName 'testsubscription' | fl *

DisplayName    : testsubscription
Id             : /subscriptions/7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
OfferId        : /delegatedProviders/default/offers/testoffer
State          : Enabled
SubscriptionId : 7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="4ef86-109">建立訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ef86-109">Create a subscription.</span></span>

## <span data-ttu-id="4ef86-110">參數</span><span class="sxs-lookup"><span data-stu-id="4ef86-110">PARAMETERS</span></span>

### <span data-ttu-id="4ef86-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ef86-111">-DefaultProfile</span></span>
<span data-ttu-id="4ef86-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ef86-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ef86-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4ef86-113">-DisplayName</span></span>
<span data-ttu-id="4ef86-114">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="4ef86-114">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ef86-115">-識別碼</span><span class="sxs-lookup"><span data-stu-id="4ef86-115">-Id</span></span>
<span data-ttu-id="4ef86-116">完全限定識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ef86-116">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ef86-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="4ef86-117">-OfferId</span></span>
<span data-ttu-id="4ef86-118">受委派提供者範圍內提供的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ef86-118">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ef86-119">-State</span><span class="sxs-lookup"><span data-stu-id="4ef86-119">-State</span></span>
<span data-ttu-id="4ef86-120">訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="4ef86-120">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ef86-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ef86-121">-SubscriptionId</span></span>
<span data-ttu-id="4ef86-122">訂閱的 Id。</span><span class="sxs-lookup"><span data-stu-id="4ef86-122">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ef86-123">-TenantId</span><span class="sxs-lookup"><span data-stu-id="4ef86-123">-TenantId</span></span>
<span data-ttu-id="4ef86-124">目錄租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ef86-124">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ef86-125">-確認</span><span class="sxs-lookup"><span data-stu-id="4ef86-125">-Confirm</span></span>
<span data-ttu-id="4ef86-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ef86-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ef86-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ef86-127">-WhatIf</span></span>
<span data-ttu-id="4ef86-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ef86-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ef86-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ef86-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4ef86-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef86-130">CommonParameters</span></span>
<span data-ttu-id="4ef86-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ef86-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef86-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4ef86-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef86-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4ef86-133">INPUTS</span></span>

## <span data-ttu-id="4ef86-134">輸出</span><span class="sxs-lookup"><span data-stu-id="4ef86-134">OUTPUTS</span></span>

### <span data-ttu-id="4ef86-135">ISubscription 中的 [Api20151101] （訂閱）。</span><span class="sxs-lookup"><span data-stu-id="4ef86-135">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="4ef86-136">筆記</span><span class="sxs-lookup"><span data-stu-id="4ef86-136">NOTES</span></span>

## <span data-ttu-id="4ef86-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ef86-137">RELATED LINKS</span></span>
