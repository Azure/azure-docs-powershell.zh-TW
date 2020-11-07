---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disconnect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disconnect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disconnect-AzAccount.md
ms.openlocfilehash: bc266e7bf0df9897b24b8bd44575bb860cf8736a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794148"
---
# <span data-ttu-id="86142-101">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="86142-101">Disconnect-AzAccount</span></span>

## <span data-ttu-id="86142-102">摘要</span><span class="sxs-lookup"><span data-stu-id="86142-102">SYNOPSIS</span></span>
<span data-ttu-id="86142-103">中斷連線的 Azure 帳戶，並移除與該帳戶相關聯的所有認證與內容。</span><span class="sxs-lookup"><span data-stu-id="86142-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

## <span data-ttu-id="86142-104">句法</span><span class="sxs-lookup"><span data-stu-id="86142-104">SYNTAX</span></span>

### <span data-ttu-id="86142-105">CoNtextName (預設) </span><span class="sxs-lookup"><span data-stu-id="86142-105">ContextName (Default)</span></span>
```
Disconnect-AzAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86142-106">UserId</span><span class="sxs-lookup"><span data-stu-id="86142-106">UserId</span></span>
```
Disconnect-AzAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86142-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="86142-107">ServicePrincipal</span></span>
```
Disconnect-AzAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86142-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="86142-108">AccountObject</span></span>
```
Disconnect-AzAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86142-109">CoNtextObject</span><span class="sxs-lookup"><span data-stu-id="86142-109">ContextObject</span></span>
```
Disconnect-AzAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86142-110">說明</span><span class="sxs-lookup"><span data-stu-id="86142-110">DESCRIPTION</span></span>
<span data-ttu-id="86142-111">Disconnect-AzAccount Cmdlet 會中斷連線的 Azure 帳戶，並移除與該帳戶相關聯的所有認證與內容 (訂閱與租使用者) 資訊。</span><span class="sxs-lookup"><span data-stu-id="86142-111">The Disconnect-AzAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="86142-112">執行此 Cmdlet 之後，您將需要使用 [AzAccount] 再次登入。</span><span class="sxs-lookup"><span data-stu-id="86142-112">After executing this cmdlet, you will need to login again using Connect-AzAccount.</span></span>

## <span data-ttu-id="86142-113">示例</span><span class="sxs-lookup"><span data-stu-id="86142-113">EXAMPLES</span></span>

### <span data-ttu-id="86142-114">登出目前的帳戶</span><span class="sxs-lookup"><span data-stu-id="86142-114">Logout of the current account</span></span>
```
PS C:\> Disconnect-AzAccount
```

<span data-ttu-id="86142-115">登出與目前內容相關聯的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="86142-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="86142-116">登出與特定內容相關聯的帳戶</span><span class="sxs-lookup"><span data-stu-id="86142-116">Logout of the account associated with a particular context</span></span>
```
PS C:\> Get-AzContext "Work" | Disconnect-AzAccount -Scope CurrentUser
```

<span data-ttu-id="86142-117">登出 (名為「Work」 ) 的指定內容相關聯的帳戶。</span><span class="sxs-lookup"><span data-stu-id="86142-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="86142-118">因為這會使用 "CurrentUser" 範圍，所以所有認證和內容都會永久刪除。</span><span class="sxs-lookup"><span data-stu-id="86142-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="86142-119">登出特定使用者</span><span class="sxs-lookup"><span data-stu-id="86142-119">Log out a particular user</span></span>
```
PS C:\> Disconnect-AzAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="86142-120">登出 [] user1@contoso.org 使用者-所有認證，所有與此使用者相關聯的內容將會被移除。</span><span class="sxs-lookup"><span data-stu-id="86142-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="86142-121">參數</span><span class="sxs-lookup"><span data-stu-id="86142-121">PARAMETERS</span></span>

### <span data-ttu-id="86142-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="86142-122">-ApplicationId</span></span>
<span data-ttu-id="86142-123">ServicePrincipal 識別碼 (全域唯一識別碼) </span><span class="sxs-lookup"><span data-stu-id="86142-123">ServicePrincipal id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86142-124">-AzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="86142-124">-AzureContext</span></span>
<span data-ttu-id="86142-125">這裡</span><span class="sxs-lookup"><span data-stu-id="86142-125">Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: ContextObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86142-126">-CoNtextName</span><span class="sxs-lookup"><span data-stu-id="86142-126">-ContextName</span></span>
<span data-ttu-id="86142-127">要登出之內容的名稱</span><span class="sxs-lookup"><span data-stu-id="86142-127">Name of the context to log out of</span></span>

```yaml
Type: System.String
Parameter Sets: ContextName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86142-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86142-128">-DefaultProfile</span></span>
<span data-ttu-id="86142-129">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="86142-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86142-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86142-130">-InputObject</span></span>
<span data-ttu-id="86142-131">要移除的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="86142-131">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86142-132">-範圍</span><span class="sxs-lookup"><span data-stu-id="86142-132">-Scope</span></span>
<span data-ttu-id="86142-133">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="86142-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="86142-134">-TenantId</span><span class="sxs-lookup"><span data-stu-id="86142-134">-TenantId</span></span>
<span data-ttu-id="86142-135">租使用者識別碼 (全域唯一識別碼) </span><span class="sxs-lookup"><span data-stu-id="86142-135">Tenant id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86142-136">-Username</span><span class="sxs-lookup"><span data-stu-id="86142-136">-Username</span></span>
<span data-ttu-id="86142-137">表單 "" 的使用者名稱 user@contoso.org</span><span class="sxs-lookup"><span data-stu-id="86142-137">User name of the form 'user@contoso.org'</span></span>

```yaml
Type: System.String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86142-138">-確認</span><span class="sxs-lookup"><span data-stu-id="86142-138">-Confirm</span></span>
<span data-ttu-id="86142-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="86142-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86142-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86142-140">-WhatIf</span></span>
<span data-ttu-id="86142-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="86142-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86142-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="86142-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="86142-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86142-143">CommonParameters</span></span>
<span data-ttu-id="86142-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="86142-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86142-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="86142-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86142-146">輸入</span><span class="sxs-lookup"><span data-stu-id="86142-146">INPUTS</span></span>

### <span data-ttu-id="86142-147">PSAzureRmAccount 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="86142-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="86142-148">PSAzureCoNtext 的基本設定檔。</span><span class="sxs-lookup"><span data-stu-id="86142-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="86142-149">輸出</span><span class="sxs-lookup"><span data-stu-id="86142-149">OUTPUTS</span></span>

### <span data-ttu-id="86142-150">PSAzureRmAccount 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="86142-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="86142-151">筆記</span><span class="sxs-lookup"><span data-stu-id="86142-151">NOTES</span></span>

## <span data-ttu-id="86142-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="86142-152">RELATED LINKS</span></span>