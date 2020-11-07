---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ba118c80656676c47a2d6740ef7c0266fd491af6
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793773"
---
# <span data-ttu-id="c6a18-101">New-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="c6a18-101">New-SubscriptionObject</span></span>

## <span data-ttu-id="c6a18-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6a18-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a18-103">支援的作業清單。</span><span class="sxs-lookup"><span data-stu-id="c6a18-103">List of supported operations.</span></span>

## <span data-ttu-id="c6a18-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6a18-104">SYNTAX</span></span>

```
New-SubscriptionObject [[-TenantId] <String>] [[-SubscriptionId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-Name] <String>] [[-Owner] <String>]
 [[-RoutingResourceManagerType] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-OfferId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="c6a18-105">說明</span><span class="sxs-lookup"><span data-stu-id="c6a18-105">DESCRIPTION</span></span>
<span data-ttu-id="c6a18-106">支援的作業清單。</span><span class="sxs-lookup"><span data-stu-id="c6a18-106">List of supported operations.</span></span>

## <span data-ttu-id="c6a18-107">示例</span><span class="sxs-lookup"><span data-stu-id="c6a18-107">EXAMPLES</span></span>

### <span data-ttu-id="c6a18-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c6a18-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c6a18-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="c6a18-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c6a18-110">參數</span><span class="sxs-lookup"><span data-stu-id="c6a18-110">PARAMETERS</span></span>

### <span data-ttu-id="c6a18-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6a18-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="c6a18-112">父 DelegatedProvider 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6a18-112">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="c6a18-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c6a18-113">-DisplayName</span></span>
<span data-ttu-id="c6a18-114">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="c6a18-114">Subscription name.</span></span>

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

### <span data-ttu-id="c6a18-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="c6a18-115">-ExternalReferenceId</span></span>
<span data-ttu-id="c6a18-116">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6a18-116">External reference identifier.</span></span>

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

### <span data-ttu-id="c6a18-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="c6a18-117">-Id</span></span>
<span data-ttu-id="c6a18-118">完全限定識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6a18-118">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="c6a18-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6a18-119">-Name</span></span>
<span data-ttu-id="c6a18-120">資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6a18-120">Name of the resource.</span></span>

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

### <span data-ttu-id="c6a18-121">-OfferId</span><span class="sxs-lookup"><span data-stu-id="c6a18-121">-OfferId</span></span>
<span data-ttu-id="c6a18-122">受委派提供者範圍內提供的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6a18-122">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="c6a18-123">-擁有者</span><span class="sxs-lookup"><span data-stu-id="c6a18-123">-Owner</span></span>
<span data-ttu-id="c6a18-124">訂閱擁有者。</span><span class="sxs-lookup"><span data-stu-id="c6a18-124">Subscription owner.</span></span>

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

### <span data-ttu-id="c6a18-125">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="c6a18-125">-RoutingResourceManagerType</span></span>
<span data-ttu-id="c6a18-126">路由資源管理器類型。</span><span class="sxs-lookup"><span data-stu-id="c6a18-126">Routing resource manager type.</span></span>

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

### <span data-ttu-id="c6a18-127">-State</span><span class="sxs-lookup"><span data-stu-id="c6a18-127">-State</span></span>
<span data-ttu-id="c6a18-128">訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="c6a18-128">Subscription state.</span></span>

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

### <span data-ttu-id="c6a18-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6a18-129">-SubscriptionId</span></span>
<span data-ttu-id="c6a18-130">[訂閱識別碼]。</span><span class="sxs-lookup"><span data-stu-id="c6a18-130">Subscription identifier.</span></span>

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

### <span data-ttu-id="c6a18-131">-TenantId</span><span class="sxs-lookup"><span data-stu-id="c6a18-131">-TenantId</span></span>
<span data-ttu-id="c6a18-132">目錄租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6a18-132">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="c6a18-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a18-133">CommonParameters</span></span>
<span data-ttu-id="c6a18-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6a18-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a18-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c6a18-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a18-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c6a18-136">INPUTS</span></span>

## <span data-ttu-id="c6a18-137">輸出</span><span class="sxs-lookup"><span data-stu-id="c6a18-137">OUTPUTS</span></span>

## <span data-ttu-id="c6a18-138">筆記</span><span class="sxs-lookup"><span data-stu-id="c6a18-138">NOTES</span></span>

## <span data-ttu-id="c6a18-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6a18-139">RELATED LINKS</span></span>

