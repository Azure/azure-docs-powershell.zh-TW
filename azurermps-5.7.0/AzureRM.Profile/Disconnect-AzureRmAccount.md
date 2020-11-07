---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
ms.openlocfilehash: e72e326fd3251a9b3150b9def06e2fb60afb7d82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625464"
---
# <span data-ttu-id="05ace-101">Disconnect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="05ace-101">Disconnect-AzureRmAccount</span></span>

## <span data-ttu-id="05ace-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05ace-102">SYNOPSIS</span></span>
<span data-ttu-id="05ace-103">中斷連線的 Azure 帳戶，並移除與該帳戶相關聯的所有認證與內容。</span><span class="sxs-lookup"><span data-stu-id="05ace-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05ace-104">句法</span><span class="sxs-lookup"><span data-stu-id="05ace-104">SYNTAX</span></span>

### <span data-ttu-id="05ace-105">CoNtextName (預設) </span><span class="sxs-lookup"><span data-stu-id="05ace-105">ContextName (Default)</span></span>
```
Disconnect-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05ace-106">UserId</span><span class="sxs-lookup"><span data-stu-id="05ace-106">UserId</span></span>
```
Disconnect-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05ace-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="05ace-107">ServicePrincipal</span></span>
```
Disconnect-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05ace-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="05ace-108">AccountObject</span></span>
```
Disconnect-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05ace-109">CoNtextObject</span><span class="sxs-lookup"><span data-stu-id="05ace-109">ContextObject</span></span>
```
Disconnect-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05ace-110">說明</span><span class="sxs-lookup"><span data-stu-id="05ace-110">DESCRIPTION</span></span>
<span data-ttu-id="05ace-111">Disconnect-AzureRmAccount Cmdlet 會中斷連線的 Azure 帳戶，並移除與該帳戶相關聯的所有認證與內容 (訂閱與租使用者) 資訊。</span><span class="sxs-lookup"><span data-stu-id="05ace-111">The Disconnect-AzureRmAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>

<span data-ttu-id="05ace-112">執行此 Cmdlet 之後，您將需要使用 [AzureRmAccount] 再次登入。</span><span class="sxs-lookup"><span data-stu-id="05ace-112">After executing this cmdlet, you will need to login again using Connect-AzureRmAccount.</span></span>

## <span data-ttu-id="05ace-113">示例</span><span class="sxs-lookup"><span data-stu-id="05ace-113">EXAMPLES</span></span>

### <span data-ttu-id="05ace-114">登出目前的帳戶</span><span class="sxs-lookup"><span data-stu-id="05ace-114">Logout of the current account</span></span>
```
PS C:\> Disconnect-AzureRmAccount
```

<span data-ttu-id="05ace-115">登出與目前內容相關聯的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="05ace-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="05ace-116">登出與特定內容相關聯的帳戶</span><span class="sxs-lookup"><span data-stu-id="05ace-116">Logout of the account associated with a particular context</span></span>
```
PS C:\> Get-AzureRmContext "Work" | Disconnect-AzureRmAccount -Scope CurrentUser
```

<span data-ttu-id="05ace-117">登出 (名為「Work」 ) 的指定內容相關聯的帳戶。</span><span class="sxs-lookup"><span data-stu-id="05ace-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="05ace-118">因為這會使用 "CurrentUser" 範圍，所以所有認證和內容都會永久刪除。</span><span class="sxs-lookup"><span data-stu-id="05ace-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="05ace-119">登出特定使用者</span><span class="sxs-lookup"><span data-stu-id="05ace-119">Log out a particular user</span></span>
```
PS C:\> Disconnect-AzureRmAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="05ace-120">登出 [] user1@contoso.org 使用者-所有認證，所有與此使用者相關聯的內容將會被移除。</span><span class="sxs-lookup"><span data-stu-id="05ace-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="05ace-121">參數</span><span class="sxs-lookup"><span data-stu-id="05ace-121">PARAMETERS</span></span>

### <span data-ttu-id="05ace-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="05ace-122">-ApplicationId</span></span>
<span data-ttu-id="05ace-123">ServicePrincipal 識別碼 (全域唯一識別碼) </span><span class="sxs-lookup"><span data-stu-id="05ace-123">ServicePrincipal id (globally unique id)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ace-124">-AzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="05ace-124">-AzureContext</span></span>
<span data-ttu-id="05ace-125">這裡</span><span class="sxs-lookup"><span data-stu-id="05ace-125">Context</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: ContextObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05ace-126">-CoNtextName</span><span class="sxs-lookup"><span data-stu-id="05ace-126">-ContextName</span></span>
<span data-ttu-id="05ace-127">要登出之內容的名稱</span><span class="sxs-lookup"><span data-stu-id="05ace-127">Name of the context to log out of</span></span>

```yaml
Type: String
Parameter Sets: ContextName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ace-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05ace-128">-DefaultProfile</span></span>
<span data-ttu-id="05ace-129">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="05ace-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05ace-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05ace-130">-InputObject</span></span>
<span data-ttu-id="05ace-131">要移除的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="05ace-131">The account object to remove</span></span>

```yaml
Type: PSAzureRmAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05ace-132">-範圍</span><span class="sxs-lookup"><span data-stu-id="05ace-132">-Scope</span></span>
<span data-ttu-id="05ace-133">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="05ace-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="05ace-134">-TenantId</span><span class="sxs-lookup"><span data-stu-id="05ace-134">-TenantId</span></span>
<span data-ttu-id="05ace-135">租使用者識別碼 (全域唯一識別碼) </span><span class="sxs-lookup"><span data-stu-id="05ace-135">Tenant id (globally unique id)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ace-136">-Username</span><span class="sxs-lookup"><span data-stu-id="05ace-136">-Username</span></span>
<span data-ttu-id="05ace-137">表單 "" 的使用者名稱 user@contoso.org</span><span class="sxs-lookup"><span data-stu-id="05ace-137">User name of the form 'user@contoso.org'</span></span>

```yaml
Type: String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ace-138">-確認</span><span class="sxs-lookup"><span data-stu-id="05ace-138">-Confirm</span></span>
<span data-ttu-id="05ace-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="05ace-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ace-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05ace-140">-WhatIf</span></span>
<span data-ttu-id="05ace-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="05ace-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05ace-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05ace-142">The cmdlet is not executed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ace-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ace-143">CommonParameters</span></span>
<span data-ttu-id="05ace-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05ace-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ace-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="05ace-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ace-146">輸入</span><span class="sxs-lookup"><span data-stu-id="05ace-146">INPUTS</span></span>

### <span data-ttu-id="05ace-147">PSAzureRmAccount 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="05ace-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="05ace-148">PSAzureCoNtext 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="05ace-148">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="05ace-149">輸出</span><span class="sxs-lookup"><span data-stu-id="05ace-149">OUTPUTS</span></span>

### <span data-ttu-id="05ace-150">PSAzureRmAccount 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="05ace-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="05ace-151">筆記</span><span class="sxs-lookup"><span data-stu-id="05ace-151">NOTES</span></span>

## <span data-ttu-id="05ace-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="05ace-152">RELATED LINKS</span></span>
