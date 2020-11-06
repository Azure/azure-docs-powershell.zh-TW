---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: 01cc9210e57edbb19caa8406e9015b36942b99d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444456"
---
# <span data-ttu-id="2e1e8-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="2e1e8-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="2e1e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e1e8-102">SYNOPSIS</span></span>
<span data-ttu-id="2e1e8-103">使用已驗證的帳戶連線至 Azure，以與 Azure 資源管理器 Cmdlet 要求搭配使用。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e1e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e1e8-104">SYNTAX</span></span>

### <span data-ttu-id="2e1e8-105">UserWithSubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="2e1e8-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e1e8-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e1e8-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e1e8-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e1e8-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e1e8-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e1e8-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e1e8-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="2e1e8-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e1e8-110">說明</span><span class="sxs-lookup"><span data-stu-id="2e1e8-110">DESCRIPTION</span></span>
<span data-ttu-id="2e1e8-111">Connect-AzureRmAccount Cmdlet 會以已驗證的帳戶連線至 Azure，以便與 Azure 資源管理器 Cmdlet 要求搭配使用。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="2e1e8-112">您只能將這個經過驗證的帳戶用於 Azure 資源管理器 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>

<span data-ttu-id="2e1e8-113">若要新增與服務管理 Cmdlet 搭配使用的已驗證帳戶，請使用 Add-AzureAccount 或 Import-AzurePublishSettingsFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

<span data-ttu-id="2e1e8-114">執行此 Cmdlet 之後，您可以使用 [中斷連線] 從 Azure 帳戶中斷連線 AzureRmAccount。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-114">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="2e1e8-115">示例</span><span class="sxs-lookup"><span data-stu-id="2e1e8-115">EXAMPLES</span></span>

### <span data-ttu-id="2e1e8-116">範例1：使用互動式登入來連線至 Azure 帳戶</span><span class="sxs-lookup"><span data-stu-id="2e1e8-116">Example 1: Use an interactive login to connect to an Azure account</span></span>
```
PS C:\> Connect-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="2e1e8-117">這個命令會連接至 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-117">This command connects to an Azure account.</span></span>

<span data-ttu-id="2e1e8-118">若要使用此帳戶執行 Azure 資源管理器 Cmdlet，您必須在系統提示時提供 Microsoft 帳戶或組織識別碼認證。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-118">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="2e1e8-119">如果您的認證已啟用多重要素驗證，您必須使用互動式選項登入，或使用服務主體驗證。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-119">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="2e1e8-120">範例2：使用組織識別碼認證連線至 Azure 帳戶</span><span class="sxs-lookup"><span data-stu-id="2e1e8-120">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="2e1e8-121">第一個命令會取得使用者認證，然後將它們儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-121">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="2e1e8-122">第二個命令會使用儲存在 $Credential 中的認證，連線至 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-122">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>

<span data-ttu-id="2e1e8-123">這個帳戶使用組織識別碼認證與 Azure 資源管理器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-123">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>

<span data-ttu-id="2e1e8-124">您無法使用多重要素驗證或 Microsoft 帳號憑證來執行 Azure 資源管理器 Cmdlet 與此帳戶。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-124">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="2e1e8-125">範例3：連線至 Azure 服務主要帳戶</span><span class="sxs-lookup"><span data-stu-id="2e1e8-125">Example 3: Connect to an Azure service principal account</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="2e1e8-126">第一個命令會取得使用者認證，然後將它們儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-126">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="2e1e8-127">第二個命令使用儲存在指定租使用者 $Credential 中的服務主體認證來連線至 Azure。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-127">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>

<span data-ttu-id="2e1e8-128">ServicePrincipal 切換參數表示該帳戶會以服務主體進行驗證。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-128">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="2e1e8-129">範例4：使用互動式登入來連線至特定租使用者和訂閱的帳戶</span><span class="sxs-lookup"><span data-stu-id="2e1e8-129">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="2e1e8-130">這個命令會連線至 Azure 帳戶，並設定 AzureRM PowerShell，以預設為指定的租使用者和訂閱執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-130">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="2e1e8-131">範例5：使用 Managed Services Identity Login 來新增帳戶</span><span class="sxs-lookup"><span data-stu-id="2e1e8-131">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```
PS C:\>Add-AzureRmAccount -MSI
Account: MSI@50342
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="2e1e8-132">這個命令會使用主機環境的 managed 服務身分識別， (例如，如果在已指派受管理服務身分識別的 VirtualMachine 上執行，這將允許程式碼使用指定的身分識別來登入) </span><span class="sxs-lookup"><span data-stu-id="2e1e8-132">This command logs in using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

## <span data-ttu-id="2e1e8-133">參數</span><span class="sxs-lookup"><span data-stu-id="2e1e8-133">PARAMETERS</span></span>

### <span data-ttu-id="2e1e8-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="2e1e8-134">-AccessToken</span></span>
<span data-ttu-id="2e1e8-135">指定存取權杖。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1e8-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="2e1e8-136">-AccountId</span></span>
<span data-ttu-id="2e1e8-137">存取權杖的帳戶識別碼</span><span class="sxs-lookup"><span data-stu-id="2e1e8-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1e8-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2e1e8-138">-ApplicationId</span></span>
<span data-ttu-id="2e1e8-139">SPN</span><span class="sxs-lookup"><span data-stu-id="2e1e8-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1e8-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="2e1e8-140">-CertificateThumbprint</span></span>
<span data-ttu-id="2e1e8-141">憑證雜湊 (指紋) </span><span class="sxs-lookup"><span data-stu-id="2e1e8-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1e8-142">-CoNtextName</span><span class="sxs-lookup"><span data-stu-id="2e1e8-142">-ContextName</span></span>
<span data-ttu-id="2e1e8-143">此登入的預設內容名稱。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-143">Name of the default context from this login.</span></span>  <span data-ttu-id="2e1e8-144">登入後，您就可以使用此名稱來選取此內容。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-144">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="2e1e8-145">-認證</span><span class="sxs-lookup"><span data-stu-id="2e1e8-145">-Credential</span></span>
<span data-ttu-id="2e1e8-146">指定 PSCredential 物件。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-146">Specifies a PSCredential object.</span></span>
<span data-ttu-id="2e1e8-147">如需 PSCredential 物件的詳細資訊，請輸入 Get-Help 取得認證。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-147">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="2e1e8-148">PSCredential 物件會提供組織識別碼認證的使用者識別碼和密碼，或是應用程式識別碼和服務主體認證的密碼。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-148">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1e8-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e1e8-149">-DefaultProfile</span></span>
<span data-ttu-id="2e1e8-150">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e1e8-151">-環境</span><span class="sxs-lookup"><span data-stu-id="2e1e8-151">-Environment</span></span>
<span data-ttu-id="2e1e8-152">包含要登入之帳戶的環境</span><span class="sxs-lookup"><span data-stu-id="2e1e8-152">Environment containing the account to log into</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1e8-153">-Force</span><span class="sxs-lookup"><span data-stu-id="2e1e8-153">-Force</span></span>
<span data-ttu-id="2e1e8-154">使用相同的名稱覆寫現有的內容（如果有）。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-154">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="2e1e8-155">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="2e1e8-155">-GraphAccessToken</span></span>
<span data-ttu-id="2e1e8-156">圖形服務的 AccessToken</span><span class="sxs-lookup"><span data-stu-id="2e1e8-156">AccessToken for Graph Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1e8-157">身分識別</span><span class="sxs-lookup"><span data-stu-id="2e1e8-157">-Identity</span></span>
<span data-ttu-id="2e1e8-158">在目前的環境中使用受管理的服務標識登入。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-158">Login using managed service identity in the current environment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1e8-159">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="2e1e8-159">-KeyVaultAccessToken</span></span>
<span data-ttu-id="2e1e8-160">AccessToken for KeyVault Service</span><span class="sxs-lookup"><span data-stu-id="2e1e8-160">AccessToken for KeyVault Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1e8-161">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="2e1e8-161">-ManagedServiceHostName</span></span>
<span data-ttu-id="2e1e8-162">受管理的服務登入的主機名稱</span><span class="sxs-lookup"><span data-stu-id="2e1e8-162">Host name for managed service login</span></span>

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1e8-163">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="2e1e8-163">-ManagedServicePort</span></span>
<span data-ttu-id="2e1e8-164">受管理的服務登入的埠號碼</span><span class="sxs-lookup"><span data-stu-id="2e1e8-164">Port number for managed service login</span></span>

```yaml
Type: Int32
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1e8-165">-範圍</span><span class="sxs-lookup"><span data-stu-id="2e1e8-165">-Scope</span></span>
<span data-ttu-id="2e1e8-166">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="2e1e8-167">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2e1e8-167">-ServicePrincipal</span></span>
<span data-ttu-id="2e1e8-168">指示此帳戶透過提供服務主體認證來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-168">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1e8-169">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="2e1e8-169">-SkipValidation</span></span>
<span data-ttu-id="2e1e8-170">跳過存取權杖的驗證</span><span class="sxs-lookup"><span data-stu-id="2e1e8-170">Skip validation for access token</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1e8-171">-訂閱</span><span class="sxs-lookup"><span data-stu-id="2e1e8-171">-Subscription</span></span>
<span data-ttu-id="2e1e8-172">訂閱名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="2e1e8-172">Subscription Name or ID</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e1e8-173">-TenantId</span><span class="sxs-lookup"><span data-stu-id="2e1e8-173">-TenantId</span></span>
<span data-ttu-id="2e1e8-174">選用的租使用者名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="2e1e8-174">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1e8-175">-確認</span><span class="sxs-lookup"><span data-stu-id="2e1e8-175">-Confirm</span></span>
<span data-ttu-id="2e1e8-176">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e1e8-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e1e8-177">-WhatIf</span></span>
<span data-ttu-id="2e1e8-178">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e1e8-179">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e1e8-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e1e8-180">CommonParameters</span></span>
<span data-ttu-id="2e1e8-181">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e1e8-182">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e1e8-183">輸入</span><span class="sxs-lookup"><span data-stu-id="2e1e8-183">INPUTS</span></span>

### <span data-ttu-id="2e1e8-184">字串</span><span class="sxs-lookup"><span data-stu-id="2e1e8-184">String</span></span>
<span data-ttu-id="2e1e8-185">參數 "SubscriptionId" 接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="2e1e8-185">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="2e1e8-186">字串</span><span class="sxs-lookup"><span data-stu-id="2e1e8-186">String</span></span>
<span data-ttu-id="2e1e8-187">"SubscriptionName" 參數從管線接受類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="2e1e8-187">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="2e1e8-188">輸出</span><span class="sxs-lookup"><span data-stu-id="2e1e8-188">OUTPUTS</span></span>

### <span data-ttu-id="2e1e8-189">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="2e1e8-189">PSAzureProfile</span></span>
<span data-ttu-id="2e1e8-190">登入使用者的認證、訂閱、帳戶和租使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="2e1e8-190">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="2e1e8-191">筆記</span><span class="sxs-lookup"><span data-stu-id="2e1e8-191">NOTES</span></span>

## <span data-ttu-id="2e1e8-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e1e8-192">RELATED LINKS</span></span>

