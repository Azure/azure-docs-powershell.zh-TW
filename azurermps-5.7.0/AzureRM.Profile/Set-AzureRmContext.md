---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
ms.openlocfilehash: bffd818df21be78d0418bf3d2ac1ebea401dbf19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454168"
---
# <span data-ttu-id="4e488-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="4e488-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="4e488-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e488-102">SYNOPSIS</span></span>
<span data-ttu-id="4e488-103">設定要在目前會話中使用之 Cmdlet 的租使用者、訂閱及環境。</span><span class="sxs-lookup"><span data-stu-id="4e488-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e488-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e488-104">SYNTAX</span></span>

### <span data-ttu-id="4e488-105">預設) 的內容 (</span><span class="sxs-lookup"><span data-stu-id="4e488-105">Context (Default)</span></span>
```
Set-AzureRmContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e488-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="4e488-106">TenantObject</span></span>
```
Set-AzureRmContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e488-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="4e488-107">SubscriptionObject</span></span>
```
Set-AzureRmContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e488-108">訂閱</span><span class="sxs-lookup"><span data-stu-id="4e488-108">Subscription</span></span>
```
Set-AzureRmContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e488-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="4e488-109">TenantNameOnly</span></span>
```
Set-AzureRmContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e488-110">說明</span><span class="sxs-lookup"><span data-stu-id="4e488-110">DESCRIPTION</span></span>
<span data-ttu-id="4e488-111">Set-AzureRmContext Cmdlet 會針對您在目前會話中執行的 Cmdlet 設定驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="4e488-111">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="4e488-112">內容包括租使用者、訂閱及環境資訊。</span><span class="sxs-lookup"><span data-stu-id="4e488-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="4e488-113">示例</span><span class="sxs-lookup"><span data-stu-id="4e488-113">EXAMPLES</span></span>

### <span data-ttu-id="4e488-114">範例1：設定訂閱內容</span><span class="sxs-lookup"><span data-stu-id="4e488-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="4e488-115">這個命令會將內容設定為使用指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e488-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="4e488-116">參數</span><span class="sxs-lookup"><span data-stu-id="4e488-116">PARAMETERS</span></span>

### <span data-ttu-id="4e488-117">-內容</span><span class="sxs-lookup"><span data-stu-id="4e488-117">-Context</span></span>
<span data-ttu-id="4e488-118">指定目前會話的內容。</span><span class="sxs-lookup"><span data-stu-id="4e488-118">Specifies the context for the current session.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e488-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e488-119">-DefaultProfile</span></span>
<span data-ttu-id="4e488-120">用於與 azure 進行通訊的認證、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e488-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e488-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="4e488-121">-ExtendedProperty</span></span>
<span data-ttu-id="4e488-122">其他內容屬性</span><span class="sxs-lookup"><span data-stu-id="4e488-122">Additional context properties</span></span>

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

### <span data-ttu-id="4e488-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4e488-123">-Force</span></span>
<span data-ttu-id="4e488-124">使用相同的名稱覆寫現有的內容（如果有）。</span><span class="sxs-lookup"><span data-stu-id="4e488-124">Overwrite the existing context with the same name, if any.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e488-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e488-125">-Name</span></span>
<span data-ttu-id="4e488-126">內容的名稱</span><span class="sxs-lookup"><span data-stu-id="4e488-126">Name of the context</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e488-127">-範圍</span><span class="sxs-lookup"><span data-stu-id="4e488-127">-Scope</span></span>
<span data-ttu-id="4e488-128">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="4e488-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e488-129">-訂閱</span><span class="sxs-lookup"><span data-stu-id="4e488-129">-Subscription</span></span>
<span data-ttu-id="4e488-130">訂閱名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="4e488-130">Subscription Name or Id</span></span>

```yaml
Type: String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e488-131">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="4e488-131">-SubscriptionObject</span></span>
<span data-ttu-id="4e488-132">訂閱物件</span><span class="sxs-lookup"><span data-stu-id="4e488-132">A subscription object</span></span>

```yaml
Type: PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e488-133">-租使用者</span><span class="sxs-lookup"><span data-stu-id="4e488-133">-Tenant</span></span>
<span data-ttu-id="4e488-134">租使用者名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="4e488-134">Tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e488-135">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="4e488-135">-TenantObject</span></span>
<span data-ttu-id="4e488-136">租使用者物件</span><span class="sxs-lookup"><span data-stu-id="4e488-136">A Tenant Object</span></span>

```yaml
Type: PSAzureTenant
Parameter Sets: TenantObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e488-137">-確認</span><span class="sxs-lookup"><span data-stu-id="4e488-137">-Confirm</span></span>
<span data-ttu-id="4e488-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4e488-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e488-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e488-139">-WhatIf</span></span>
<span data-ttu-id="4e488-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4e488-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e488-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e488-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e488-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e488-142">CommonParameters</span></span>
<span data-ttu-id="4e488-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e488-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e488-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4e488-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e488-145">輸入</span><span class="sxs-lookup"><span data-stu-id="4e488-145">INPUTS</span></span>

### <span data-ttu-id="4e488-146">PSAzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="4e488-146">PSAzureContext</span></span>
<span data-ttu-id="4e488-147">參數「CoNtext」接受來自管線的 "PSAzureCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="4e488-147">Parameter 'Context' accepts value of type 'PSAzureContext' from the pipeline</span></span>

## <span data-ttu-id="4e488-148">輸出</span><span class="sxs-lookup"><span data-stu-id="4e488-148">OUTPUTS</span></span>

### <span data-ttu-id="4e488-149">PSAzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="4e488-149">PSAzureContext</span></span>

## <span data-ttu-id="4e488-150">筆記</span><span class="sxs-lookup"><span data-stu-id="4e488-150">NOTES</span></span>

## <span data-ttu-id="4e488-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e488-151">RELATED LINKS</span></span>

[<span data-ttu-id="4e488-152">AzureRMCoNtext</span><span class="sxs-lookup"><span data-stu-id="4e488-152">Get-AzureRMContext</span></span>](./Get-AzureRMContext.md)
