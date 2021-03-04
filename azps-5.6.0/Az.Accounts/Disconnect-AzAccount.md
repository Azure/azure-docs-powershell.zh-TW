---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/disconnect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
ms.openlocfilehash: 4f9dc4bebfa0c7e84c1d52e81796e5c4938e465f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914213"
---
# <span data-ttu-id="a1f12-101">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="a1f12-101">Disconnect-AzAccount</span></span>

## <span data-ttu-id="a1f12-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a1f12-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f12-103">中斷連接 Azure 帳戶的中斷，並移除所有與該帳戶相關聯的認證和上下文。</span><span class="sxs-lookup"><span data-stu-id="a1f12-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

## <span data-ttu-id="a1f12-104">語法</span><span class="sxs-lookup"><span data-stu-id="a1f12-104">SYNTAX</span></span>

### <span data-ttu-id="a1f12-105">CoNtextName (預設) </span><span class="sxs-lookup"><span data-stu-id="a1f12-105">ContextName (Default)</span></span>
```
Disconnect-AzAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f12-106">UserId</span><span class="sxs-lookup"><span data-stu-id="a1f12-106">UserId</span></span>
```
Disconnect-AzAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f12-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a1f12-107">ServicePrincipal</span></span>
```
Disconnect-AzAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f12-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a1f12-108">AccountObject</span></span>
```
Disconnect-AzAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f12-109">CoNtextObject</span><span class="sxs-lookup"><span data-stu-id="a1f12-109">ContextObject</span></span>
```
Disconnect-AzAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1f12-110">描述</span><span class="sxs-lookup"><span data-stu-id="a1f12-110">DESCRIPTION</span></span>
<span data-ttu-id="a1f12-111">此Disconnect-AzAccount Cmdlet 會中斷連接 Azure 帳戶的中斷，並移除所有與該帳戶相關聯的訂閱 (和租) 資訊。</span><span class="sxs-lookup"><span data-stu-id="a1f12-111">The Disconnect-AzAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="a1f12-112">執行此 Cmdlet 之後，您必須再次使用 Connect-AzAccount 登入。</span><span class="sxs-lookup"><span data-stu-id="a1f12-112">After executing this cmdlet, you will need to login again using Connect-AzAccount.</span></span>

## <span data-ttu-id="a1f12-113">例子</span><span class="sxs-lookup"><span data-stu-id="a1f12-113">EXAMPLES</span></span>

### <span data-ttu-id="a1f12-114">範例 1：登出目前帳戶</span><span class="sxs-lookup"><span data-stu-id="a1f12-114">Example 1: Logout of the current account</span></span>
```powershell
PS C:\> Disconnect-AzAccount
```

<span data-ttu-id="a1f12-115">登出與目前內容相關聯的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="a1f12-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="a1f12-116">範例 2：登出與特定內容相關聯的帳戶</span><span class="sxs-lookup"><span data-stu-id="a1f12-116">Example 2: Logout of the account associated with a particular context</span></span>
```powershell
PS C:\> Get-AzContext "Work" | Disconnect-AzAccount -Scope CurrentUser
```

<span data-ttu-id="a1f12-117">登出與指定內容相關聯的帳戶， (名為"Work') 。</span><span class="sxs-lookup"><span data-stu-id="a1f12-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="a1f12-118">由於這會使用 'CurrentUser' 範圍，因此將會永久刪除所有認證和上下文。</span><span class="sxs-lookup"><span data-stu-id="a1f12-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="a1f12-119">範例 3：登出特定使用者</span><span class="sxs-lookup"><span data-stu-id="a1f12-119">Example 3: Log out a particular user</span></span>
```powershell
PS C:\> Disconnect-AzAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="a1f12-120">登出 user1@contoso.org ''user - 所有認證和與此使用者相關聯的所有上下文都會移除。</span><span class="sxs-lookup"><span data-stu-id="a1f12-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="a1f12-121">參數</span><span class="sxs-lookup"><span data-stu-id="a1f12-121">PARAMETERS</span></span>

### <span data-ttu-id="a1f12-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a1f12-122">-ApplicationId</span></span>
<span data-ttu-id="a1f12-123">ServicePrincipal 識別碼 (全域唯一識別碼) </span><span class="sxs-lookup"><span data-stu-id="a1f12-123">ServicePrincipal id (globally unique id)</span></span>

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

### <span data-ttu-id="a1f12-124">-AzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="a1f12-124">-AzureContext</span></span>
<span data-ttu-id="a1f12-125">上下文</span><span class="sxs-lookup"><span data-stu-id="a1f12-125">Context</span></span>

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

### <span data-ttu-id="a1f12-126">-CoNtextName</span><span class="sxs-lookup"><span data-stu-id="a1f12-126">-ContextName</span></span>
<span data-ttu-id="a1f12-127">登出的上下文名稱</span><span class="sxs-lookup"><span data-stu-id="a1f12-127">Name of the context to log out of</span></span>

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

### <span data-ttu-id="a1f12-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f12-128">-DefaultProfile</span></span>
<span data-ttu-id="a1f12-129">用於與 Azure 通訊的認證、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a1f12-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1f12-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1f12-130">-InputObject</span></span>
<span data-ttu-id="a1f12-131">要移除的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="a1f12-131">The account object to remove</span></span>

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

### <span data-ttu-id="a1f12-132">-範圍</span><span class="sxs-lookup"><span data-stu-id="a1f12-132">-Scope</span></span>
<span data-ttu-id="a1f12-133">決定上下文變更的範圍，例如，變更是否僅適用于目前的程式，或適用于此使用者啟動的所有會話。</span><span class="sxs-lookup"><span data-stu-id="a1f12-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="a1f12-134">-TenantId</span><span class="sxs-lookup"><span data-stu-id="a1f12-134">-TenantId</span></span>
<span data-ttu-id="a1f12-135">租使用者識別碼 (全域唯一識別碼) </span><span class="sxs-lookup"><span data-stu-id="a1f12-135">Tenant id (globally unique id)</span></span>

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

### <span data-ttu-id="a1f12-136">-使用者名稱</span><span class="sxs-lookup"><span data-stu-id="a1f12-136">-Username</span></span>
<span data-ttu-id="a1f12-137">表單 '' 的使用者 user@contoso.org 名稱</span><span class="sxs-lookup"><span data-stu-id="a1f12-137">User name of the form 'user@contoso.org'</span></span>

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

### <span data-ttu-id="a1f12-138">-確認</span><span class="sxs-lookup"><span data-stu-id="a1f12-138">-Confirm</span></span>
<span data-ttu-id="a1f12-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a1f12-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1f12-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1f12-140">-WhatIf</span></span>
<span data-ttu-id="a1f12-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a1f12-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1f12-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a1f12-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="a1f12-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f12-143">CommonParameters</span></span>
<span data-ttu-id="a1f12-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a1f12-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f12-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1f12-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f12-146">輸入</span><span class="sxs-lookup"><span data-stu-id="a1f12-146">INPUTS</span></span>

### <span data-ttu-id="a1f12-147">Microsoft.Azure.Commands.Profile.models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="a1f12-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="a1f12-148">Microsoft.Azure.Commands.Profile.models.Core.PSAzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="a1f12-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="a1f12-149">輸出</span><span class="sxs-lookup"><span data-stu-id="a1f12-149">OUTPUTS</span></span>

### <span data-ttu-id="a1f12-150">Microsoft.Azure.Commands.Profile.models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="a1f12-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="a1f12-151">筆記</span><span class="sxs-lookup"><span data-stu-id="a1f12-151">NOTES</span></span>

## <span data-ttu-id="a1f12-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1f12-152">RELATED LINKS</span></span>
