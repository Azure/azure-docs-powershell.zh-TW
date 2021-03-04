---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: 03bceaee69bfa739268fa4cb1be8c9699f26f405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916689"
---
# <span data-ttu-id="07bd7-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="07bd7-101">Set-AzContext</span></span>

## <span data-ttu-id="07bd7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="07bd7-102">SYNOPSIS</span></span>
<span data-ttu-id="07bd7-103">設定 Cmdlet 要用於目前會話的租使用者、訂閱及環境。</span><span class="sxs-lookup"><span data-stu-id="07bd7-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="07bd7-104">語法</span><span class="sxs-lookup"><span data-stu-id="07bd7-104">SYNTAX</span></span>

### <span data-ttu-id="07bd7-105">上下文 (預設) </span><span class="sxs-lookup"><span data-stu-id="07bd7-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07bd7-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="07bd7-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07bd7-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="07bd7-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07bd7-108">訂閱</span><span class="sxs-lookup"><span data-stu-id="07bd7-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07bd7-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="07bd7-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07bd7-110">描述</span><span class="sxs-lookup"><span data-stu-id="07bd7-110">DESCRIPTION</span></span>
<span data-ttu-id="07bd7-111">此Set-AzContext Cmdlet 會針對您目前會話執行 Cmdlet 設定驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="07bd7-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="07bd7-112">內容包括租使用者、訂閱及環境資訊。</span><span class="sxs-lookup"><span data-stu-id="07bd7-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="07bd7-113">例子</span><span class="sxs-lookup"><span data-stu-id="07bd7-113">EXAMPLES</span></span>

### <span data-ttu-id="07bd7-114">範例 1：設定訂閱內容</span><span class="sxs-lookup"><span data-stu-id="07bd7-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -Subscription "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="07bd7-115">此命令會設定使用指定訂閱的上下文。</span><span class="sxs-lookup"><span data-stu-id="07bd7-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="07bd7-116">參數</span><span class="sxs-lookup"><span data-stu-id="07bd7-116">PARAMETERS</span></span>

### <span data-ttu-id="07bd7-117">-內容</span><span class="sxs-lookup"><span data-stu-id="07bd7-117">-Context</span></span>
<span data-ttu-id="07bd7-118">指定目前會話的上下文。</span><span class="sxs-lookup"><span data-stu-id="07bd7-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: Context
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07bd7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07bd7-119">-DefaultProfile</span></span>
<span data-ttu-id="07bd7-120">用於與 azure 通訊的認證、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="07bd7-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07bd7-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="07bd7-121">-ExtendedProperty</span></span>
<span data-ttu-id="07bd7-122">其他內容屬性</span><span class="sxs-lookup"><span data-stu-id="07bd7-122">Additional context properties</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bd7-123">-強制</span><span class="sxs-lookup"><span data-stu-id="07bd7-123">-Force</span></span>
<span data-ttu-id="07bd7-124">使用相同名稱覆寫現有內容 （如果有）。</span><span class="sxs-lookup"><span data-stu-id="07bd7-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="07bd7-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="07bd7-125">-Name</span></span>
<span data-ttu-id="07bd7-126">內容名稱</span><span class="sxs-lookup"><span data-stu-id="07bd7-126">Name of the context</span></span>

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

### <span data-ttu-id="07bd7-127">-範圍</span><span class="sxs-lookup"><span data-stu-id="07bd7-127">-Scope</span></span>
<span data-ttu-id="07bd7-128">決定上下文變更的範圍，例如，變更是否僅適用于目前的程式，或適用于此使用者啟動的所有會話。</span><span class="sxs-lookup"><span data-stu-id="07bd7-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bd7-129">-訂閱</span><span class="sxs-lookup"><span data-stu-id="07bd7-129">-Subscription</span></span>
<span data-ttu-id="07bd7-130">內容應設定為訂閱的名稱或識別碼。</span><span class="sxs-lookup"><span data-stu-id="07bd7-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="07bd7-131">此參數具有 -SubscriptionName 和 -SubscriptionId 的別名，因此為了清楚起見，您可以分別在指定名稱和識別碼時，使用其中一個來取代 -Subscription。</span><span class="sxs-lookup"><span data-stu-id="07bd7-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bd7-132">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="07bd7-132">-SubscriptionObject</span></span>
<span data-ttu-id="07bd7-133">訂閱物件</span><span class="sxs-lookup"><span data-stu-id="07bd7-133">A subscription object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07bd7-134">-租使用者</span><span class="sxs-lookup"><span data-stu-id="07bd7-134">-Tenant</span></span>
<span data-ttu-id="07bd7-135">租使用者名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="07bd7-135">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bd7-136">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="07bd7-136">-TenantObject</span></span>
<span data-ttu-id="07bd7-137">租使用者物件</span><span class="sxs-lookup"><span data-stu-id="07bd7-137">A Tenant Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureTenant
Parameter Sets: TenantObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07bd7-138">-確認</span><span class="sxs-lookup"><span data-stu-id="07bd7-138">-Confirm</span></span>
<span data-ttu-id="07bd7-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="07bd7-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bd7-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07bd7-140">-WhatIf</span></span>
<span data-ttu-id="07bd7-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="07bd7-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07bd7-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07bd7-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07bd7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07bd7-143">CommonParameters</span></span>
<span data-ttu-id="07bd7-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="07bd7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07bd7-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07bd7-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07bd7-146">輸入</span><span class="sxs-lookup"><span data-stu-id="07bd7-146">INPUTS</span></span>

### <span data-ttu-id="07bd7-147">Microsoft.Azure.Commands.Profile.models.Core.PSAzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="07bd7-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="07bd7-148">Microsoft.Azure.Commands.Profile.models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="07bd7-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="07bd7-149">Microsoft.Azure.Commands.Profile.models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="07bd7-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="07bd7-150">輸出</span><span class="sxs-lookup"><span data-stu-id="07bd7-150">OUTPUTS</span></span>

### <span data-ttu-id="07bd7-151">Microsoft.Azure.Commands.Profile.models.Core.PSAzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="07bd7-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="07bd7-152">筆記</span><span class="sxs-lookup"><span data-stu-id="07bd7-152">NOTES</span></span>

## <span data-ttu-id="07bd7-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="07bd7-153">RELATED LINKS</span></span>

[<span data-ttu-id="07bd7-154">Get-AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="07bd7-154">Get-AzContext</span></span>](./Get-AzContext.md)

