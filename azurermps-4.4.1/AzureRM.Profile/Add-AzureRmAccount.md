---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
ms.openlocfilehash: 11303438a50839bbe05139888cc665198ed09810
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455668"
---
# <span data-ttu-id="ddc85-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="ddc85-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="ddc85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ddc85-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc85-103">新增要用於 Azure 資源管理器 Cmdlet 要求的已驗證帳戶。</span><span class="sxs-lookup"><span data-stu-id="ddc85-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddc85-104">句法</span><span class="sxs-lookup"><span data-stu-id="ddc85-104">SYNTAX</span></span>

### <span data-ttu-id="ddc85-105">UserWithSubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="ddc85-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc85-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ddc85-106">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc85-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ddc85-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddc85-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ddc85-108">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddc85-109">說明</span><span class="sxs-lookup"><span data-stu-id="ddc85-109">DESCRIPTION</span></span>
<span data-ttu-id="ddc85-110">Add-AzureRmAcccount Cmdlet 會新增已驗證的 Azure 帳戶以用於 Azure 資源管理器 Cmdlet 要求。</span><span class="sxs-lookup"><span data-stu-id="ddc85-110">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="ddc85-111">您只能將這個經過驗證的帳戶用於 Azure 資源管理器 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddc85-111">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="ddc85-112">若要新增與服務管理 Cmdlet 搭配使用的已驗證帳戶，請使用 Add-AzureAccount 或 Import-AzurePublishSettingsFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddc85-112">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="ddc85-113">示例</span><span class="sxs-lookup"><span data-stu-id="ddc85-113">EXAMPLES</span></span>

### <span data-ttu-id="ddc85-114">範例1：新增需要互動式登入的帳戶</span><span class="sxs-lookup"><span data-stu-id="ddc85-114">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="ddc85-115">這個命令會新增 Azure 資源管理員帳戶。</span><span class="sxs-lookup"><span data-stu-id="ddc85-115">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="ddc85-116">若要使用此帳戶執行 Azure 資源管理器 Cmdlet，您必須在系統提示時提供 Microsoft 帳戶或組織識別碼認證。</span><span class="sxs-lookup"><span data-stu-id="ddc85-116">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="ddc85-117">如果您的認證已啟用多重要素驗證，您必須使用互動式選項登入，或使用服務主體驗證。</span><span class="sxs-lookup"><span data-stu-id="ddc85-117">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="ddc85-118">範例2：新增使用組織識別碼認證進行驗證的帳戶</span><span class="sxs-lookup"><span data-stu-id="ddc85-118">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="ddc85-119">第一個命令會取得使用者認證，然後將它們儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="ddc85-119">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="ddc85-120">第二個命令會在 $Credential 中新增含認證的 Azure 資源管理器帳戶。</span><span class="sxs-lookup"><span data-stu-id="ddc85-120">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="ddc85-121">這個帳戶使用組織識別碼認證與 Azure 資源管理器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="ddc85-121">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="ddc85-122">您無法使用多重要素驗證或 Microsoft 帳號憑證來執行 Azure 資源管理器 Cmdlet 與此帳戶。</span><span class="sxs-lookup"><span data-stu-id="ddc85-122">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="ddc85-123">範例3：新增以服務主體認證進行驗證的帳戶</span><span class="sxs-lookup"><span data-stu-id="ddc85-123">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="ddc85-124">第一個命令會取得使用者認證，然後將它們儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="ddc85-124">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="ddc85-125">第二個命令會使用儲存在指定租使用者 $Credential 中的憑證來新增 Azure 資源管理器帳戶。</span><span class="sxs-lookup"><span data-stu-id="ddc85-125">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="ddc85-126">ServicePrincipal 切換參數表示該帳戶會以服務主體進行驗證。</span><span class="sxs-lookup"><span data-stu-id="ddc85-126">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="ddc85-127">範例4：新增特定租使用者和訂閱的帳戶</span><span class="sxs-lookup"><span data-stu-id="ddc85-127">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="ddc85-128">這個命令會新增 Azure 資源管理員帳戶，以針對指定的租使用者及訂閱執行 Cmdlet （預設為）。</span><span class="sxs-lookup"><span data-stu-id="ddc85-128">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="ddc85-129">參數</span><span class="sxs-lookup"><span data-stu-id="ddc85-129">PARAMETERS</span></span>

### <span data-ttu-id="ddc85-130">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="ddc85-130">-AccessToken</span></span>
<span data-ttu-id="ddc85-131">指定存取權杖。</span><span class="sxs-lookup"><span data-stu-id="ddc85-131">Specifies an access token.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc85-132">-AccountId</span><span class="sxs-lookup"><span data-stu-id="ddc85-132">-AccountId</span></span>
<span data-ttu-id="ddc85-133">存取權杖的帳戶識別碼</span><span class="sxs-lookup"><span data-stu-id="ddc85-133">Account Id for access token</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc85-134">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ddc85-134">-ApplicationId</span></span>
<span data-ttu-id="ddc85-135">SPN</span><span class="sxs-lookup"><span data-stu-id="ddc85-135">SPN</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc85-136">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ddc85-136">-CertificateThumbprint</span></span>
<span data-ttu-id="ddc85-137">憑證雜湊 (指紋) </span><span class="sxs-lookup"><span data-stu-id="ddc85-137">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc85-138">-CoNtextName</span><span class="sxs-lookup"><span data-stu-id="ddc85-138">-ContextName</span></span>
<span data-ttu-id="ddc85-139">此登入的預設內容名稱。</span><span class="sxs-lookup"><span data-stu-id="ddc85-139">Name of the default context from this login.</span></span>  <span data-ttu-id="ddc85-140">登入後，您就可以使用此名稱來選取此內容。</span><span class="sxs-lookup"><span data-stu-id="ddc85-140">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="ddc85-141">-認證</span><span class="sxs-lookup"><span data-stu-id="ddc85-141">-Credential</span></span>
<span data-ttu-id="ddc85-142">指定 PSCredential 物件。</span><span class="sxs-lookup"><span data-stu-id="ddc85-142">Specifies a PSCredential object.</span></span>
<span data-ttu-id="ddc85-143">如需 PSCredential 物件的詳細資訊，請輸入 Get-Help 取得認證。</span><span class="sxs-lookup"><span data-stu-id="ddc85-143">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="ddc85-144">PSCredential 物件會提供組織識別碼認證的使用者識別碼和密碼，或是應用程式識別碼和服務主體認證的密碼。</span><span class="sxs-lookup"><span data-stu-id="ddc85-144">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc85-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc85-145">-DefaultProfile</span></span>
<span data-ttu-id="ddc85-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ddc85-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc85-147">-環境</span><span class="sxs-lookup"><span data-stu-id="ddc85-147">-Environment</span></span>
<span data-ttu-id="ddc85-148">包含要登入之帳戶的環境</span><span class="sxs-lookup"><span data-stu-id="ddc85-148">Environment containing the account to log into</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc85-149">-Force</span><span class="sxs-lookup"><span data-stu-id="ddc85-149">-Force</span></span>
<span data-ttu-id="ddc85-150">使用相同的名稱覆寫現有的內容（如果有）。</span><span class="sxs-lookup"><span data-stu-id="ddc85-150">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="ddc85-151">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="ddc85-151">-GraphAccessToken</span></span>
<span data-ttu-id="ddc85-152">圖形服務的 AccessToken</span><span class="sxs-lookup"><span data-stu-id="ddc85-152">AccessToken for Graph Service</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc85-153">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="ddc85-153">-KeyVaultAccessToken</span></span>
<span data-ttu-id="ddc85-154">AccessToken for KeyVault Service</span><span class="sxs-lookup"><span data-stu-id="ddc85-154">AccessToken for KeyVault Service</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc85-155">-範圍</span><span class="sxs-lookup"><span data-stu-id="ddc85-155">-Scope</span></span>
<span data-ttu-id="ddc85-156">決定內容變更的範圍，例如，wheher 變更只適用于 cusrrent 進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="ddc85-156">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="ddc85-157">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ddc85-157">-ServicePrincipal</span></span>
<span data-ttu-id="ddc85-158">指示此帳戶透過提供服務主體認證來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="ddc85-158">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc85-159">-訂閱</span><span class="sxs-lookup"><span data-stu-id="ddc85-159">-Subscription</span></span>
<span data-ttu-id="ddc85-160">訂閱名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="ddc85-160">Subscription Name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc85-161">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ddc85-161">-TenantId</span></span>
<span data-ttu-id="ddc85-162">選用的租使用者名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="ddc85-162">Optional tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc85-163">-確認</span><span class="sxs-lookup"><span data-stu-id="ddc85-163">-Confirm</span></span>
<span data-ttu-id="ddc85-164">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ddc85-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddc85-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc85-165">-WhatIf</span></span>
<span data-ttu-id="ddc85-166">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ddc85-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddc85-167">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddc85-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddc85-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc85-168">CommonParameters</span></span>
<span data-ttu-id="ddc85-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ddc85-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc85-170">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ddc85-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc85-171">輸入</span><span class="sxs-lookup"><span data-stu-id="ddc85-171">INPUTS</span></span>

### <span data-ttu-id="ddc85-172">字串</span><span class="sxs-lookup"><span data-stu-id="ddc85-172">String</span></span>
<span data-ttu-id="ddc85-173">參數 "SubscriptionId" 接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ddc85-173">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="ddc85-174">字串</span><span class="sxs-lookup"><span data-stu-id="ddc85-174">String</span></span>
<span data-ttu-id="ddc85-175">"SubscriptionName" 參數從管線接受類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="ddc85-175">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ddc85-176">輸出</span><span class="sxs-lookup"><span data-stu-id="ddc85-176">OUTPUTS</span></span>

### <span data-ttu-id="ddc85-177">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="ddc85-177">PSAzureProfile</span></span>
<span data-ttu-id="ddc85-178">登入使用者的認證、訂閱、帳戶和租使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="ddc85-178">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="ddc85-179">筆記</span><span class="sxs-lookup"><span data-stu-id="ddc85-179">NOTES</span></span>

## <span data-ttu-id="ddc85-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddc85-180">RELATED LINKS</span></span>

