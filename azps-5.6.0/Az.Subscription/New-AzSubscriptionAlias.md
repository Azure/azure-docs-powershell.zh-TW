---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 30c90d4b04c6c32144946cbdf98c59991133dbf9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917878"
---
# <span data-ttu-id="54a8e-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="54a8e-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="54a8e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="54a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="54a8e-103">建立新別名和訂閱</span><span class="sxs-lookup"><span data-stu-id="54a8e-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="54a8e-104">語法</span><span class="sxs-lookup"><span data-stu-id="54a8e-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54a8e-105">描述</span><span class="sxs-lookup"><span data-stu-id="54a8e-105">DESCRIPTION</span></span>
<span data-ttu-id="54a8e-106">**New-AzSubscriptionAlias** Cmdlet 會建立新的別名和訂閱</span><span class="sxs-lookup"><span data-stu-id="54a8e-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="54a8e-107">例子</span><span class="sxs-lookup"><span data-stu-id="54a8e-107">EXAMPLES</span></span>

### <span data-ttu-id="54a8e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="54a8e-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="54a8e-109">建立新別名和訂閱</span><span class="sxs-lookup"><span data-stu-id="54a8e-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="54a8e-110">參數</span><span class="sxs-lookup"><span data-stu-id="54a8e-110">PARAMETERS</span></span>

### <span data-ttu-id="54a8e-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="54a8e-111">-AliasName</span></span>
<span data-ttu-id="54a8e-112">訂閱的別名</span><span class="sxs-lookup"><span data-stu-id="54a8e-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="54a8e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54a8e-113">-AsJob</span></span>
<span data-ttu-id="54a8e-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54a8e-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a8e-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="54a8e-115">-BillingScope</span></span>
<span data-ttu-id="54a8e-116">帳單範圍</span><span class="sxs-lookup"><span data-stu-id="54a8e-116">Billing Scope</span></span>

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

### <span data-ttu-id="54a8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54a8e-117">-DefaultProfile</span></span>
<span data-ttu-id="54a8e-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="54a8e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a8e-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="54a8e-119">-ResellerId</span></span>
<span data-ttu-id="54a8e-120">轉銷商識別碼</span><span class="sxs-lookup"><span data-stu-id="54a8e-120">Reseller Id</span></span>

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

### <span data-ttu-id="54a8e-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54a8e-121">-SubscriptionId</span></span>
<span data-ttu-id="54a8e-122">現有的訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="54a8e-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="54a8e-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="54a8e-123">-SubscriptionName</span></span>
<span data-ttu-id="54a8e-124">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="54a8e-124">Name of the subscription</span></span>

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

### <span data-ttu-id="54a8e-125">-工作量</span><span class="sxs-lookup"><span data-stu-id="54a8e-125">-Workload</span></span>
<span data-ttu-id="54a8e-126">工作量類型</span><span class="sxs-lookup"><span data-stu-id="54a8e-126">Type of Workload</span></span>

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

### <span data-ttu-id="54a8e-127">-確認</span><span class="sxs-lookup"><span data-stu-id="54a8e-127">-Confirm</span></span>
<span data-ttu-id="54a8e-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="54a8e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54a8e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54a8e-129">-WhatIf</span></span>
<span data-ttu-id="54a8e-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54a8e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54a8e-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54a8e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54a8e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a8e-132">CommonParameters</span></span>
<span data-ttu-id="54a8e-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="54a8e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a8e-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54a8e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a8e-135">輸入</span><span class="sxs-lookup"><span data-stu-id="54a8e-135">INPUTS</span></span>

### <span data-ttu-id="54a8e-136">沒有</span><span class="sxs-lookup"><span data-stu-id="54a8e-136">None</span></span>

## <span data-ttu-id="54a8e-137">輸出</span><span class="sxs-lookup"><span data-stu-id="54a8e-137">OUTPUTS</span></span>

### <span data-ttu-id="54a8e-138">Microsoft.Azure.Commands.subscription.models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="54a8e-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="54a8e-139">筆記</span><span class="sxs-lookup"><span data-stu-id="54a8e-139">NOTES</span></span>

## <span data-ttu-id="54a8e-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="54a8e-140">RELATED LINKS</span></span>
