---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: f7d6c1fcfe4a74601a8a27e85bd1520912b26350
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127856"
---
# <span data-ttu-id="1f09b-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="1f09b-101">Set-AzContext</span></span>

## <span data-ttu-id="1f09b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f09b-102">SYNOPSIS</span></span>
<span data-ttu-id="1f09b-103">設定要在目前會話中使用之 Cmdlet 的租使用者、訂閱及環境。</span><span class="sxs-lookup"><span data-stu-id="1f09b-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="1f09b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f09b-104">SYNTAX</span></span>

### <span data-ttu-id="1f09b-105">預設) 的內容 (</span><span class="sxs-lookup"><span data-stu-id="1f09b-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f09b-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="1f09b-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f09b-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="1f09b-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f09b-108">訂閱</span><span class="sxs-lookup"><span data-stu-id="1f09b-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f09b-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="1f09b-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f09b-110">說明</span><span class="sxs-lookup"><span data-stu-id="1f09b-110">DESCRIPTION</span></span>
<span data-ttu-id="1f09b-111">Set-AzContext Cmdlet 會針對您在目前會話中執行的 Cmdlet 設定驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="1f09b-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="1f09b-112">內容包括租使用者、訂閱及環境資訊。</span><span class="sxs-lookup"><span data-stu-id="1f09b-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="1f09b-113">示例</span><span class="sxs-lookup"><span data-stu-id="1f09b-113">EXAMPLES</span></span>

### <span data-ttu-id="1f09b-114">範例1：設定訂閱內容</span><span class="sxs-lookup"><span data-stu-id="1f09b-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="1f09b-115">這個命令會將內容設定為使用指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f09b-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="1f09b-116">參數</span><span class="sxs-lookup"><span data-stu-id="1f09b-116">PARAMETERS</span></span>

### <span data-ttu-id="1f09b-117">-內容</span><span class="sxs-lookup"><span data-stu-id="1f09b-117">-Context</span></span>
<span data-ttu-id="1f09b-118">指定目前會話的內容。</span><span class="sxs-lookup"><span data-stu-id="1f09b-118">Specifies the context for the current session.</span></span>

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

### <span data-ttu-id="1f09b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f09b-119">-DefaultProfile</span></span>
<span data-ttu-id="1f09b-120">用於與 azure 進行通訊的認證、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f09b-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f09b-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="1f09b-121">-ExtendedProperty</span></span>
<span data-ttu-id="1f09b-122">其他內容屬性</span><span class="sxs-lookup"><span data-stu-id="1f09b-122">Additional context properties</span></span>

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

### <span data-ttu-id="1f09b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1f09b-123">-Force</span></span>
<span data-ttu-id="1f09b-124">使用相同的名稱覆寫現有的內容（如果有）。</span><span class="sxs-lookup"><span data-stu-id="1f09b-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="1f09b-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f09b-125">-Name</span></span>
<span data-ttu-id="1f09b-126">內容的名稱</span><span class="sxs-lookup"><span data-stu-id="1f09b-126">Name of the context</span></span>

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

### <span data-ttu-id="1f09b-127">-範圍</span><span class="sxs-lookup"><span data-stu-id="1f09b-127">-Scope</span></span>
<span data-ttu-id="1f09b-128">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="1f09b-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="1f09b-129">-訂閱</span><span class="sxs-lookup"><span data-stu-id="1f09b-129">-Subscription</span></span>
<span data-ttu-id="1f09b-130">應將內容設定為之訂閱的名稱或識別碼。</span><span class="sxs-lookup"><span data-stu-id="1f09b-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="1f09b-131">這個參數具有-SubscriptionName 和-SubscriptionId 的別名，所以為了清楚起見，您可以在分別指定名稱和識別碼時，使用其中一種方式，而不是訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f09b-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

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

### <span data-ttu-id="1f09b-132">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="1f09b-132">-SubscriptionObject</span></span>
<span data-ttu-id="1f09b-133">訂閱物件</span><span class="sxs-lookup"><span data-stu-id="1f09b-133">A subscription object</span></span>

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

### <span data-ttu-id="1f09b-134">-租使用者</span><span class="sxs-lookup"><span data-stu-id="1f09b-134">-Tenant</span></span>
<span data-ttu-id="1f09b-135">租使用者名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="1f09b-135">Tenant name or ID</span></span>

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

### <span data-ttu-id="1f09b-136">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="1f09b-136">-TenantObject</span></span>
<span data-ttu-id="1f09b-137">租使用者物件</span><span class="sxs-lookup"><span data-stu-id="1f09b-137">A Tenant Object</span></span>

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

### <span data-ttu-id="1f09b-138">-確認</span><span class="sxs-lookup"><span data-stu-id="1f09b-138">-Confirm</span></span>
<span data-ttu-id="1f09b-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1f09b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f09b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f09b-140">-WhatIf</span></span>
<span data-ttu-id="1f09b-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f09b-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f09b-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f09b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f09b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f09b-143">CommonParameters</span></span>
<span data-ttu-id="1f09b-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f09b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f09b-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f09b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f09b-146">輸入</span><span class="sxs-lookup"><span data-stu-id="1f09b-146">INPUTS</span></span>

### <span data-ttu-id="1f09b-147">PSAzureCoNtext 的基本設定檔。</span><span class="sxs-lookup"><span data-stu-id="1f09b-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="1f09b-148">PSAzureTenant 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="1f09b-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="1f09b-149">PSAzureSubscription 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="1f09b-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="1f09b-150">輸出</span><span class="sxs-lookup"><span data-stu-id="1f09b-150">OUTPUTS</span></span>

### <span data-ttu-id="1f09b-151">PSAzureCoNtext 的基本設定檔。</span><span class="sxs-lookup"><span data-stu-id="1f09b-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="1f09b-152">筆記</span><span class="sxs-lookup"><span data-stu-id="1f09b-152">NOTES</span></span>

## <span data-ttu-id="1f09b-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f09b-153">RELATED LINKS</span></span>

[<span data-ttu-id="1f09b-154">AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="1f09b-154">Get-AzContext</span></span>](./Get-AzContext.md)

