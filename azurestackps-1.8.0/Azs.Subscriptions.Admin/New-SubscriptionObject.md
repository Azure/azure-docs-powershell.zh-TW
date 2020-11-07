---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ba118c80656676c47a2d6740ef7c0266fd491af6
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793631"
---
# <span data-ttu-id="32d66-101">New-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="32d66-101">New-SubscriptionObject</span></span>

## <span data-ttu-id="32d66-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32d66-102">SYNOPSIS</span></span>
<span data-ttu-id="32d66-103">支援的作業清單。</span><span class="sxs-lookup"><span data-stu-id="32d66-103">List of supported operations.</span></span>

## <span data-ttu-id="32d66-104">句法</span><span class="sxs-lookup"><span data-stu-id="32d66-104">SYNTAX</span></span>

```
New-SubscriptionObject [[-TenantId] <String>] [[-SubscriptionId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-Name] <String>] [[-Owner] <String>]
 [[-RoutingResourceManagerType] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-OfferId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="32d66-105">說明</span><span class="sxs-lookup"><span data-stu-id="32d66-105">DESCRIPTION</span></span>
<span data-ttu-id="32d66-106">支援的作業清單。</span><span class="sxs-lookup"><span data-stu-id="32d66-106">List of supported operations.</span></span>

## <span data-ttu-id="32d66-107">示例</span><span class="sxs-lookup"><span data-stu-id="32d66-107">EXAMPLES</span></span>

### <span data-ttu-id="32d66-108">範例1</span><span class="sxs-lookup"><span data-stu-id="32d66-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="32d66-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="32d66-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="32d66-110">參數</span><span class="sxs-lookup"><span data-stu-id="32d66-110">PARAMETERS</span></span>

### <span data-ttu-id="32d66-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32d66-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="32d66-112">父 DelegatedProvider 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="32d66-112">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d66-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="32d66-113">-DisplayName</span></span>
<span data-ttu-id="32d66-114">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="32d66-114">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d66-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="32d66-115">-ExternalReferenceId</span></span>
<span data-ttu-id="32d66-116">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="32d66-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d66-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="32d66-117">-Id</span></span>
<span data-ttu-id="32d66-118">完全限定識別碼。</span><span class="sxs-lookup"><span data-stu-id="32d66-118">Fully qualified identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d66-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="32d66-119">-Name</span></span>
<span data-ttu-id="32d66-120">資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="32d66-120">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d66-121">-OfferId</span><span class="sxs-lookup"><span data-stu-id="32d66-121">-OfferId</span></span>
<span data-ttu-id="32d66-122">受委派提供者範圍內提供的識別碼。</span><span class="sxs-lookup"><span data-stu-id="32d66-122">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d66-123">-擁有者</span><span class="sxs-lookup"><span data-stu-id="32d66-123">-Owner</span></span>
<span data-ttu-id="32d66-124">訂閱擁有者。</span><span class="sxs-lookup"><span data-stu-id="32d66-124">Subscription owner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d66-125">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="32d66-125">-RoutingResourceManagerType</span></span>
<span data-ttu-id="32d66-126">路由資源管理器類型。</span><span class="sxs-lookup"><span data-stu-id="32d66-126">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d66-127">-State</span><span class="sxs-lookup"><span data-stu-id="32d66-127">-State</span></span>
<span data-ttu-id="32d66-128">訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="32d66-128">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d66-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32d66-129">-SubscriptionId</span></span>
<span data-ttu-id="32d66-130">[訂閱識別碼]。</span><span class="sxs-lookup"><span data-stu-id="32d66-130">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d66-131">-TenantId</span><span class="sxs-lookup"><span data-stu-id="32d66-131">-TenantId</span></span>
<span data-ttu-id="32d66-132">目錄租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="32d66-132">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d66-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d66-133">CommonParameters</span></span>
<span data-ttu-id="32d66-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32d66-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d66-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="32d66-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d66-136">輸入</span><span class="sxs-lookup"><span data-stu-id="32d66-136">INPUTS</span></span>

## <span data-ttu-id="32d66-137">輸出</span><span class="sxs-lookup"><span data-stu-id="32d66-137">OUTPUTS</span></span>

## <span data-ttu-id="32d66-138">筆記</span><span class="sxs-lookup"><span data-stu-id="32d66-138">NOTES</span></span>

## <span data-ttu-id="32d66-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="32d66-139">RELATED LINKS</span></span>

