---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140743"
---
# <span data-ttu-id="2ac71-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="2ac71-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="2ac71-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ac71-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac71-103">建立新的別名及訂閱</span><span class="sxs-lookup"><span data-stu-id="2ac71-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="2ac71-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ac71-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ac71-105">說明</span><span class="sxs-lookup"><span data-stu-id="2ac71-105">DESCRIPTION</span></span>
<span data-ttu-id="2ac71-106">**新的-AzSubscriptionAlias** Cmdlet 會建立新的別名及訂閱</span><span class="sxs-lookup"><span data-stu-id="2ac71-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="2ac71-107">示例</span><span class="sxs-lookup"><span data-stu-id="2ac71-107">EXAMPLES</span></span>

### <span data-ttu-id="2ac71-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2ac71-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="2ac71-109">建立新的別名及訂閱</span><span class="sxs-lookup"><span data-stu-id="2ac71-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="2ac71-110">參數</span><span class="sxs-lookup"><span data-stu-id="2ac71-110">PARAMETERS</span></span>

### <span data-ttu-id="2ac71-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="2ac71-111">-AliasName</span></span>
<span data-ttu-id="2ac71-112">訂閱的別名</span><span class="sxs-lookup"><span data-stu-id="2ac71-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="2ac71-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ac71-113">-AsJob</span></span>
<span data-ttu-id="2ac71-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2ac71-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ac71-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="2ac71-115">-BillingScope</span></span>
<span data-ttu-id="2ac71-116">計費範圍</span><span class="sxs-lookup"><span data-stu-id="2ac71-116">Billing Scope</span></span>

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

### <span data-ttu-id="2ac71-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac71-117">-DefaultProfile</span></span>
<span data-ttu-id="2ac71-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ac71-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ac71-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="2ac71-119">-ResellerId</span></span>
<span data-ttu-id="2ac71-120">轉銷商識別碼</span><span class="sxs-lookup"><span data-stu-id="2ac71-120">Reseller Id</span></span>

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

### <span data-ttu-id="2ac71-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ac71-121">-SubscriptionId</span></span>
<span data-ttu-id="2ac71-122">現有訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="2ac71-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="2ac71-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="2ac71-123">-SubscriptionName</span></span>
<span data-ttu-id="2ac71-124">訂閱的名稱</span><span class="sxs-lookup"><span data-stu-id="2ac71-124">Name of the subscription</span></span>

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

### <span data-ttu-id="2ac71-125">-工作負載</span><span class="sxs-lookup"><span data-stu-id="2ac71-125">-Workload</span></span>
<span data-ttu-id="2ac71-126">工作負荷類型</span><span class="sxs-lookup"><span data-stu-id="2ac71-126">Type of Workload</span></span>

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

### <span data-ttu-id="2ac71-127">-確認</span><span class="sxs-lookup"><span data-stu-id="2ac71-127">-Confirm</span></span>
<span data-ttu-id="2ac71-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2ac71-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ac71-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ac71-129">-WhatIf</span></span>
<span data-ttu-id="2ac71-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2ac71-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ac71-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ac71-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ac71-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac71-132">CommonParameters</span></span>
<span data-ttu-id="2ac71-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ac71-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac71-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2ac71-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac71-135">輸入</span><span class="sxs-lookup"><span data-stu-id="2ac71-135">INPUTS</span></span>

### <span data-ttu-id="2ac71-136">所有</span><span class="sxs-lookup"><span data-stu-id="2ac71-136">None</span></span>

## <span data-ttu-id="2ac71-137">輸出</span><span class="sxs-lookup"><span data-stu-id="2ac71-137">OUTPUTS</span></span>

### <span data-ttu-id="2ac71-138">PSAzureSubscription 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2ac71-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="2ac71-139">筆記</span><span class="sxs-lookup"><span data-stu-id="2ac71-139">NOTES</span></span>

## <span data-ttu-id="2ac71-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ac71-140">RELATED LINKS</span></span>
