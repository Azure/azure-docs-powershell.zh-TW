---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 87e8615e7862e8b3314c9dace4849621a8ed4c78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794154"
---
# <span data-ttu-id="8659b-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="8659b-101">Connect-AzAccount</span></span>

## <span data-ttu-id="8659b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8659b-102">SYNOPSIS</span></span>
<span data-ttu-id="8659b-103">使用已驗證的帳戶連線至 Azure，以與 Azure 資源管理器 Cmdlet 要求搭配使用。</span><span class="sxs-lookup"><span data-stu-id="8659b-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="8659b-104">句法</span><span class="sxs-lookup"><span data-stu-id="8659b-104">SYNTAX</span></span>

### <span data-ttu-id="8659b-105">UserWithSubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="8659b-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8659b-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8659b-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8659b-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="8659b-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8659b-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8659b-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8659b-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8659b-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8659b-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="8659b-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8659b-111">說明</span><span class="sxs-lookup"><span data-stu-id="8659b-111">DESCRIPTION</span></span>
<span data-ttu-id="8659b-112">Connect-AzAccount Cmdlet 會以已驗證的帳戶連線至 Azure，以便與 Azure 資源管理器 Cmdlet 要求搭配使用。</span><span class="sxs-lookup"><span data-stu-id="8659b-112">The Connect-AzAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="8659b-113">您只能將這個經過驗證的帳戶用於 Azure 資源管理器 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8659b-113">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="8659b-114">若要新增與服務管理 Cmdlet 搭配使用的已驗證帳戶，請使用 Add-AzAccount 或 Import-AzPublishSettingsFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8659b-114">To add an authenticated account for use with Service Management cmdlets, use the Add-AzAccount or the Import-AzPublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="8659b-115">如果找不到目前使用者的任何內容，這個命令會在使用者的內容清單中填入每一個 (前25個) 訂閱的內容。</span><span class="sxs-lookup"><span data-stu-id="8659b-115">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="8659b-116">您可以透過執行「AzCoNtext-ListAvailable」，找到為使用者建立的上下文清單。</span><span class="sxs-lookup"><span data-stu-id="8659b-116">The list of contexts created for the user can be found by running "Get-AzContext -ListAvailable".</span></span> <span data-ttu-id="8659b-117">若要略過此內容填充，您可以使用 "-SkipCoNtextPopulation" 切換參數執行此命令。</span><span class="sxs-lookup"><span data-stu-id="8659b-117">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="8659b-118">執行此 Cmdlet 之後，您可以使用 [中斷連線] 從 Azure 帳戶中斷連線 AzAccount。</span><span class="sxs-lookup"><span data-stu-id="8659b-118">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzAccount.</span></span>

## <span data-ttu-id="8659b-119">示例</span><span class="sxs-lookup"><span data-stu-id="8659b-119">EXAMPLES</span></span>

### <span data-ttu-id="8659b-120">範例1：使用互動式登入來連線至 Azure 帳戶</span><span class="sxs-lookup"><span data-stu-id="8659b-120">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="8659b-121">這個命令會連接至 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="8659b-121">This command connects to an Azure account.</span></span>
<span data-ttu-id="8659b-122">若要使用此帳戶執行 Azure 資源管理器 Cmdlet，您必須在系統提示時提供 Microsoft 帳戶或組織識別碼認證。</span><span class="sxs-lookup"><span data-stu-id="8659b-122">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="8659b-123">如果您的認證已啟用多重要素驗證，您必須使用互動式選項登入，或使用服務主體驗證。</span><span class="sxs-lookup"><span data-stu-id="8659b-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="8659b-124">範例2：僅 (Windows PowerShell 5.1) 使用組織識別碼認證連線至 Azure 帳戶</span><span class="sxs-lookup"><span data-stu-id="8659b-124">Example 2: (Windows PowerShell 5.1 only) Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="8659b-125">這個案例只適用于 Windows PowerShell 5.1。</span><span class="sxs-lookup"><span data-stu-id="8659b-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="8659b-126">第一個命令會提示使用者認證 (使用者名稱和密碼) ，然後將它們儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="8659b-126">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="8659b-127">第二個命令會使用儲存在 $Credential 中的認證，連線至 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="8659b-127">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="8659b-128">這個帳戶使用組織識別碼認證與 Azure 資源管理器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="8659b-128">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="8659b-129">您無法使用多重要素驗證或 Microsoft 帳號憑證來執行 Azure 資源管理器 Cmdlet 與此帳戶。</span><span class="sxs-lookup"><span data-stu-id="8659b-129">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="8659b-130">範例3：連線至 Azure 服務主要帳戶</span><span class="sxs-lookup"><span data-stu-id="8659b-130">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="8659b-131">第一個命令會取得服務主體認證 (應用程式識別碼和服務主體密碼) ，然後將它們儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="8659b-131">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="8659b-132">第二個命令使用儲存在指定租使用者 $Credential 中的服務主體認證來連線至 Azure。</span><span class="sxs-lookup"><span data-stu-id="8659b-132">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="8659b-133">ServicePrincipal 切換參數表示該帳戶會以服務主體進行驗證。</span><span class="sxs-lookup"><span data-stu-id="8659b-133">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="8659b-134">範例4：使用互動式登入來連線至特定租使用者和訂閱的帳戶</span><span class="sxs-lookup"><span data-stu-id="8659b-134">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="8659b-135">這個命令會連線至 Azure 帳戶，並設定 AzureRM PowerShell，以預設為指定的租使用者和訂閱執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8659b-135">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="8659b-136">範例5：使用 Managed Services Identity Login 來新增帳戶</span><span class="sxs-lookup"><span data-stu-id="8659b-136">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzAccount -Identity

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="8659b-137">這個命令會使用主機環境的 managed 服務身分識別 (例如，如果在已指派受管理服務身分識別的 VirtualMachine 上執行，這將允許程式碼使用指定的身分識別來登入) </span><span class="sxs-lookup"><span data-stu-id="8659b-137">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="8659b-138">範例6：使用 Managed Services 身分識別登入和 ClientId 來新增帳戶</span><span class="sxs-lookup"><span data-stu-id="8659b-138">Example 6: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="8659b-139">這個命令會透過將指派身分識別的使用者新增至虛擬機器，然後使用使用者指派身分識別的使用者來連線，以使用受管理的服務身分識別 "myUserAssignedIdentity" 來連接。</span><span class="sxs-lookup"><span data-stu-id="8659b-139">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the ClientId of the User Assigned Identity.</span></span>
<span data-ttu-id="8659b-140">您可以在以下網址找到有關設定 Managed 身分識別的詳細資訊： https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm 。</span><span class="sxs-lookup"><span data-stu-id="8659b-140">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="8659b-141">範例7：使用 Managed Services 身分識別登入和 ClientId 來新增帳戶</span><span class="sxs-lookup"><span data-stu-id="8659b-141">Example 7: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.Id # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="8659b-142">這個命令會使用受管理的「myUserAssignedIdentity」服務身分識別，方法是將指派身分識別的使用者新增至虛擬機器，然後使用指派身分識別身分識別的使用者識別碼來連接。</span><span class="sxs-lookup"><span data-stu-id="8659b-142">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the Id of the User Assigned Identity.</span></span>
<span data-ttu-id="8659b-143">您可以在以下網址找到有關設定 Managed 身分識別的詳細資訊： https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm 。</span><span class="sxs-lookup"><span data-stu-id="8659b-143">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="8659b-144">範例8：使用憑證新增帳戶</span><span class="sxs-lookup"><span data-stu-id="8659b-144">Example 8: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="8659b-145">這個命令會使用以憑證為基礎的服務主體驗證來連線至 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="8659b-145">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="8659b-146">已使用指定的憑證建立驗證所用的服務主體。</span><span class="sxs-lookup"><span data-stu-id="8659b-146">The service principal used for authentication should have been created with the given certificate.</span></span>

### <span data-ttu-id="8659b-147">範例9：使用 AccessToken 驗證新增帳戶</span><span class="sxs-lookup"><span data-stu-id="8659b-147">Example 9: Add an account using AccessToken authentication</span></span>
```powershell
PS C:\> $url = "https://login.windows.net/<TenantId>/oauth2/token"
PS C:\> $body = "grant_type=refresh_token&refresh_token=<refreshtoken>" # Refresh token obtained from ~/.azure/TokenCache.dat
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body
PS C:\> $AccessToken = $response.access_token
PS C:\> $body1 = $body + "&resource=https%3A%2F%2Fvault.azure.net"
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body1
PS C:\> $body2 = $body + "&resource=https%3A%2F%2Fgraph.windows.net"
PS C:\> $GraphAccessToken = $response.access_token
PS C:\> Connect-AzAccount -AccountId "azureuser@contoso.com" -AccessToken $AccessToken -KeyVaultAccessToken $KeyVaultAccessToken -GraphAccessToken $GraphAccessToken -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="8659b-148">這個命令會使用提供的 AccessToken 和 KeyVaultAccessToken，連線到 "AccountId" 中指定的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="8659b-148">This command connects to an Azure account specified in "AccountId" using the AccessToken and KeyVaultAccessToken provided.</span></span>

## <span data-ttu-id="8659b-149">參數</span><span class="sxs-lookup"><span data-stu-id="8659b-149">PARAMETERS</span></span>

### <span data-ttu-id="8659b-150">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="8659b-150">-AccessToken</span></span>
<span data-ttu-id="8659b-151">指定存取權杖。</span><span class="sxs-lookup"><span data-stu-id="8659b-151">Specifies an access token.</span></span>

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

### <span data-ttu-id="8659b-152">-AccountId</span><span class="sxs-lookup"><span data-stu-id="8659b-152">-AccountId</span></span>
<span data-ttu-id="8659b-153">在 AccessToken 參數集中存取權杖的帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="8659b-153">Account Id for access token in AccessToken parameter set.</span></span> <span data-ttu-id="8659b-154">受管理的服務在 ManagedService 參數集中的帳戶 Id。</span><span class="sxs-lookup"><span data-stu-id="8659b-154">Account Id for managed service in ManagedService parameter set.</span></span> <span data-ttu-id="8659b-155">可以是受管理的服務資源識別碼，或相關聯的用戶端識別碼。若要使用 SystemAssigned 身分識別，請將此欄位留白。</span><span class="sxs-lookup"><span data-stu-id="8659b-155">Can be a managed service resource Id, or the associated client id. To use the SystemAssigned identity, leave this field blank.</span></span>

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

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8659b-156">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8659b-156">-ApplicationId</span></span>
<span data-ttu-id="8659b-157">SPN</span><span class="sxs-lookup"><span data-stu-id="8659b-157">SPN</span></span>

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

### <span data-ttu-id="8659b-158">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="8659b-158">-CertificateThumbprint</span></span>
<span data-ttu-id="8659b-159">憑證雜湊 (指紋) </span><span class="sxs-lookup"><span data-stu-id="8659b-159">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="8659b-160">-CoNtextName</span><span class="sxs-lookup"><span data-stu-id="8659b-160">-ContextName</span></span>
<span data-ttu-id="8659b-161">此登入的預設內容名稱。</span><span class="sxs-lookup"><span data-stu-id="8659b-161">Name of the default context from this login.</span></span>  <span data-ttu-id="8659b-162">登入後，您就可以使用此名稱來選取此內容。</span><span class="sxs-lookup"><span data-stu-id="8659b-162">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="8659b-163">-認證</span><span class="sxs-lookup"><span data-stu-id="8659b-163">-Credential</span></span>
<span data-ttu-id="8659b-164">指定 PSCredential 物件。</span><span class="sxs-lookup"><span data-stu-id="8659b-164">Specifies a PSCredential object.</span></span>
<span data-ttu-id="8659b-165">如需 PSCredential 物件的詳細資訊，請輸入 Get-Help 取得認證。</span><span class="sxs-lookup"><span data-stu-id="8659b-165">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="8659b-166">PSCredential 物件會提供組織識別碼認證的使用者識別碼和密碼，或是應用程式識別碼和服務主體認證的密碼。</span><span class="sxs-lookup"><span data-stu-id="8659b-166">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, UserWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8659b-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8659b-167">-DefaultProfile</span></span>
<span data-ttu-id="8659b-168">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8659b-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8659b-169">-環境</span><span class="sxs-lookup"><span data-stu-id="8659b-169">-Environment</span></span>
<span data-ttu-id="8659b-170">包含要登入之帳戶的環境</span><span class="sxs-lookup"><span data-stu-id="8659b-170">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="8659b-171">-Force</span><span class="sxs-lookup"><span data-stu-id="8659b-171">-Force</span></span>
<span data-ttu-id="8659b-172">使用相同的名稱覆寫現有的內容（如果有）。</span><span class="sxs-lookup"><span data-stu-id="8659b-172">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="8659b-173">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="8659b-173">-GraphAccessToken</span></span>
<span data-ttu-id="8659b-174">圖形服務的 AccessToken</span><span class="sxs-lookup"><span data-stu-id="8659b-174">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="8659b-175">身分識別</span><span class="sxs-lookup"><span data-stu-id="8659b-175">-Identity</span></span>
<span data-ttu-id="8659b-176">在目前的環境中使用受管理的服務標識登入。</span><span class="sxs-lookup"><span data-stu-id="8659b-176">Login using managed service identity in the current environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8659b-177">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="8659b-177">-KeyVaultAccessToken</span></span>
<span data-ttu-id="8659b-178">AccessToken for KeyVault Service</span><span class="sxs-lookup"><span data-stu-id="8659b-178">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="8659b-179">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="8659b-179">-ManagedServiceHostName</span></span>
<span data-ttu-id="8659b-180">受管理的服務登入的主機名稱</span><span class="sxs-lookup"><span data-stu-id="8659b-180">Host name for managed service login</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8659b-181">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="8659b-181">-ManagedServicePort</span></span>
<span data-ttu-id="8659b-182">受管理的服務登入的埠號碼</span><span class="sxs-lookup"><span data-stu-id="8659b-182">Port number for managed service login</span></span>

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8659b-183">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="8659b-183">-ManagedServiceSecret</span></span>
<span data-ttu-id="8659b-184">秘密，用於某些類型的受管理的服務登入。</span><span class="sxs-lookup"><span data-stu-id="8659b-184">Secret, used for some kinds of managed service login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8659b-185">-範圍</span><span class="sxs-lookup"><span data-stu-id="8659b-185">-Scope</span></span>
<span data-ttu-id="8659b-186">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="8659b-186">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="8659b-187">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8659b-187">-ServicePrincipal</span></span>
<span data-ttu-id="8659b-188">指示此帳戶透過提供服務主體認證來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="8659b-188">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8659b-189">-SkipCoNtextPopulation</span><span class="sxs-lookup"><span data-stu-id="8659b-189">-SkipContextPopulation</span></span>
<span data-ttu-id="8659b-190">如果找不到任何上下文，則會略過內容樣本。</span><span class="sxs-lookup"><span data-stu-id="8659b-190">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="8659b-191">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="8659b-191">-SkipValidation</span></span>
<span data-ttu-id="8659b-192">跳過存取權杖的驗證</span><span class="sxs-lookup"><span data-stu-id="8659b-192">Skip validation for access token</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8659b-193">-訂閱</span><span class="sxs-lookup"><span data-stu-id="8659b-193">-Subscription</span></span>
<span data-ttu-id="8659b-194">訂閱名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="8659b-194">Subscription Name or ID</span></span>

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

### <span data-ttu-id="8659b-195">-租使用者</span><span class="sxs-lookup"><span data-stu-id="8659b-195">-Tenant</span></span>
<span data-ttu-id="8659b-196">選用的租使用者名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="8659b-196">Optional tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, UserWithCredential, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8659b-197">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="8659b-197">-UseDeviceAuthentication</span></span>
<span data-ttu-id="8659b-198">使用裝置代碼驗證，而非瀏覽器控制項</span><span class="sxs-lookup"><span data-stu-id="8659b-198">Use device code authentication instead of a browser control</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UserWithSubscriptionId
Aliases: DeviceCode, DeviceAuth, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8659b-199">-確認</span><span class="sxs-lookup"><span data-stu-id="8659b-199">-Confirm</span></span>
<span data-ttu-id="8659b-200">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8659b-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8659b-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8659b-201">-WhatIf</span></span>
<span data-ttu-id="8659b-202">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8659b-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8659b-203">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8659b-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8659b-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8659b-204">CommonParameters</span></span>
<span data-ttu-id="8659b-205">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8659b-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8659b-206">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8659b-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8659b-207">輸入</span><span class="sxs-lookup"><span data-stu-id="8659b-207">INPUTS</span></span>

### <span data-ttu-id="8659b-208">System.object</span><span class="sxs-lookup"><span data-stu-id="8659b-208">System.String</span></span>

## <span data-ttu-id="8659b-209">輸出</span><span class="sxs-lookup"><span data-stu-id="8659b-209">OUTPUTS</span></span>

### <span data-ttu-id="8659b-210">PSAzureProfile 的基本設定檔。</span><span class="sxs-lookup"><span data-stu-id="8659b-210">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="8659b-211">筆記</span><span class="sxs-lookup"><span data-stu-id="8659b-211">NOTES</span></span>

## <span data-ttu-id="8659b-212">相關連結</span><span class="sxs-lookup"><span data-stu-id="8659b-212">RELATED LINKS</span></span>
