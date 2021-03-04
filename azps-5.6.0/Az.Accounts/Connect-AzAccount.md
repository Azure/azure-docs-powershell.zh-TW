---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: dcf4e78e9b6e467961eb05dd141396e426dfe5e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914229"
---
# <span data-ttu-id="2f8cf-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="2f8cf-101">Connect-AzAccount</span></span>

## <span data-ttu-id="2f8cf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2f8cf-102">SYNOPSIS</span></span>
<span data-ttu-id="2f8cf-103">使用經過驗證的帳戶連接至 Azure，以用於 Az PowerShell 模組中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="2f8cf-104">語法</span><span class="sxs-lookup"><span data-stu-id="2f8cf-104">SYNTAX</span></span>

### <span data-ttu-id="2f8cf-105">UserWithSubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="2f8cf-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f8cf-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f8cf-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f8cf-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="2f8cf-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f8cf-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f8cf-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f8cf-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f8cf-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f8cf-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="2f8cf-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f8cf-111">描述</span><span class="sxs-lookup"><span data-stu-id="2f8cf-111">DESCRIPTION</span></span>

<span data-ttu-id="2f8cf-112">Cmdlet 會使用已驗證的帳戶連接至 Azure，以用於 `Connect-AzAccount` Az PowerShell 模組中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="2f8cf-113">您僅能使用此已驗證帳戶與 Azure Resource Manager 要求。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="2f8cf-114">若要新增已驗證的帳戶以用於服務管理，請使用 Azure `Add-AzureAccount` PowerShell 模組中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="2f8cf-115">如果找不到目前使用者上下文，使用者的上下文清單會填上其前 25 個訂閱的每個內容。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="2f8cf-116">您可以執行找到為使用者建立上下文的清單 `Get-AzContext -ListAvailable` 。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="2f8cf-117">若要略過此內容人口，請指定 **SkipCoNtextPopulation 參數** 。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="2f8cf-118">執行此 Cmdlet 之後，您可以使用 `Disconnect-AzAccount` .</span><span class="sxs-lookup"><span data-stu-id="2f8cf-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="2f8cf-119">例子</span><span class="sxs-lookup"><span data-stu-id="2f8cf-119">EXAMPLES</span></span>

### <span data-ttu-id="2f8cf-120">範例 1：連接至 Azure 帳戶</span><span class="sxs-lookup"><span data-stu-id="2f8cf-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="2f8cf-121">此範例會連接到 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-121">This example connects to an Azure account.</span></span> <span data-ttu-id="2f8cf-122">您必須提供 Microsoft 帳戶或組織識別碼認證。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="2f8cf-123">如果您的認證已啟用多重要素驗證，您必須使用互動式選項登入或使用服務主體驗證。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="2f8cf-124">範例 2： (Windows PowerShell 5.1，) 使用組織識別碼認證連接至 Azure</span><span class="sxs-lookup"><span data-stu-id="2f8cf-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="2f8cf-125">此案例僅適用于 Windows PowerShell 5.1。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="2f8cf-126">第一個命令會提示輸入使用者認證，並儲存在 `$Credential` 變數中。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="2f8cf-127">第二個命令會使用儲存在 中的認證連接至 Azure 帳戶 `$Credential` 。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="2f8cf-128">此帳戶會使用組織識別碼認證向 Azure 進行驗證。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="2f8cf-129">範例 3：使用服務主體帳戶連接至 Azure</span><span class="sxs-lookup"><span data-stu-id="2f8cf-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="2f8cf-130">第一個命令會提示輸入服務主體認證，並儲存在 `$Credential` 變數中。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="2f8cf-131">系統提示時，輸入使用者名稱與服務主體密碼的應用程式識別碼作為密碼。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="2f8cf-132">第二個命令使用儲存在變數中的服務主體認證來連接指定的 Azure `$Credential` 租使用者。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="2f8cf-133">**ServicePrincipal** 參數表示帳戶已驗證為服務主體。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="2f8cf-134">範例 4：使用互動式登入來連接到特定的租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="2f8cf-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="2f8cf-135">此範例會連接到具有指定租使用者和訂閱的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="2f8cf-136">範例 5：使用 Managed Service 身分識別進行連接</span><span class="sxs-lookup"><span data-stu-id="2f8cf-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="2f8cf-137">此範例使用主機環境之 MSI (管理) 服務身分識別進行連接。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="2f8cf-138">例如，您從已指派 MSI 的虛擬機器來登錄 Azure。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="2f8cf-139">範例 6：使用 Managed Service Identity login 和 ClientId 進行連接</span><span class="sxs-lookup"><span data-stu-id="2f8cf-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="2f8cf-140">此範例使用 **myUserAssignedIdentity 的** Managed Service Identity 進行連接。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="2f8cf-141">它會將指派身分識別的使用者新增到虛擬機器，然後使用指派身分識別之使用者的 ClientId 進行連接。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="2f8cf-142">詳細資訊請參閱在 Azure VM 上[設定 Azure 資源的受管理身分。](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)</span><span class="sxs-lookup"><span data-stu-id="2f8cf-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

```powershell
$identity = Get-AzUserAssignedIdentity -ResourceGroupName 'myResourceGroup' -Name 'myUserAssignedIdentity'
Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the virtual machine
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="2f8cf-143">範例 7：使用憑證進行連接</span><span class="sxs-lookup"><span data-stu-id="2f8cf-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="2f8cf-144">此範例使用憑證式服務主體驗證來連接到 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="2f8cf-145">驗證所使用的服務主體必須使用指定的憑證建立。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="2f8cf-146">有關建立自我簽署憑證及指派許可權給他們的資訊，請參閱使用[Azure PowerShell](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)建立具有憑證的服務主體</span><span class="sxs-lookup"><span data-stu-id="2f8cf-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

```powershell
$Thumbprint = '0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV'
$TenantId = '4cd76576-b611-43d0-8f2b-adcb139531bf'
$ApplicationId = '3794a65a-e4e4-493d-ac1d-f04308d712dd'
Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal
```

```Output
Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

## <span data-ttu-id="2f8cf-147">參數</span><span class="sxs-lookup"><span data-stu-id="2f8cf-147">PARAMETERS</span></span>

### <span data-ttu-id="2f8cf-148">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="2f8cf-148">-AccessToken</span></span>

<span data-ttu-id="2f8cf-149">指定存取權杖。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="2f8cf-150">Access 權杖是一種認證類型。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="2f8cf-151">您應採取適當的安全性預防措施，以保密。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="2f8cf-152">Access 權杖也會超時，並可能導致長時間執行的工作無法完成。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

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

### <span data-ttu-id="2f8cf-153">-AccountId</span><span class="sxs-lookup"><span data-stu-id="2f8cf-153">-AccountId</span></span>

<span data-ttu-id="2f8cf-154">AccessToken 參數集 **存取權杖的帳戶** 識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="2f8cf-155">ManagedService 參數集中 **受管理服務** 的帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="2f8cf-156">可以是受管理的服務資源識別碼，或相關聯的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="2f8cf-157">若要使用系統指派的身分識別，請保留此欄位空白。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-157">To use the system assigned identity, leave this field blank.</span></span>

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

### <span data-ttu-id="2f8cf-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2f8cf-158">-ApplicationId</span></span>

<span data-ttu-id="2f8cf-159">服務主體的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-159">Application ID of the service principal.</span></span>

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

### <span data-ttu-id="2f8cf-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="2f8cf-160">-CertificateThumbprint</span></span>

<span data-ttu-id="2f8cf-161">憑證雜湊或指紋。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-161">Certificate Hash or Thumbprint.</span></span>

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

### <span data-ttu-id="2f8cf-162">-CoNtextName</span><span class="sxs-lookup"><span data-stu-id="2f8cf-162">-ContextName</span></span>

<span data-ttu-id="2f8cf-163">此登入的預設 Azure 上下文名稱。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="2f8cf-164">有關 Azure 上下文詳細資訊，請參閱 [Azure PowerShell 上下文物件](/powershell/azure/context-persistence)。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

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

### <span data-ttu-id="2f8cf-165">-認證</span><span class="sxs-lookup"><span data-stu-id="2f8cf-165">-Credential</span></span>

<span data-ttu-id="2f8cf-166">指定 **PSCredential 物件** 。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="2f8cf-167">有關 **PSCredential 物件的資訊，** 請鍵入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="2f8cf-168">**PSCredential 物件** 會提供組織識別碼認證的使用者識別碼和密碼，或是服務主體認證的應用程式識別碼和密碼。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="2f8cf-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f8cf-169">-DefaultProfile</span></span>

<span data-ttu-id="2f8cf-170">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f8cf-171">-環境</span><span class="sxs-lookup"><span data-stu-id="2f8cf-171">-Environment</span></span>

<span data-ttu-id="2f8cf-172">包含 Azure 帳戶的環境。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-172">Environment containing the Azure account.</span></span>

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

### <span data-ttu-id="2f8cf-173">-強制</span><span class="sxs-lookup"><span data-stu-id="2f8cf-173">-Force</span></span>

<span data-ttu-id="2f8cf-174">以相同的名稱覆寫現有內容，而不提示。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-174">Overwrite the existing context with the same name without prompting.</span></span>

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

### <span data-ttu-id="2f8cf-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="2f8cf-175">-GraphAccessToken</span></span>

<span data-ttu-id="2f8cf-176">AccessToken for Graph Service。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-176">AccessToken for Graph Service.</span></span>

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

### <span data-ttu-id="2f8cf-177">-身分識別</span><span class="sxs-lookup"><span data-stu-id="2f8cf-177">-Identity</span></span>

<span data-ttu-id="2f8cf-178">使用 Managed Service Identity 登入。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-178">Login using a Managed Service Identity.</span></span>

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

### <span data-ttu-id="2f8cf-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="2f8cf-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="2f8cf-180">適用于 KeyVault Service 的 AccessToken。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-180">AccessToken for KeyVault Service.</span></span>

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

### <span data-ttu-id="2f8cf-181">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="2f8cf-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="2f8cf-182">過時。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-182">Obsolete.</span></span> <span data-ttu-id="2f8cf-183">若要使用自訂的 MSI 端點，請設定環境變數MSI_ENDPOINT，例如" http://localhost:50342/oauth2/token "。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-183">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".</span></span> <span data-ttu-id="2f8cf-184">受管理服務的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-184">Host name for the managed service.</span></span>

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

### <span data-ttu-id="2f8cf-185">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="2f8cf-185">-ManagedServicePort</span></span>

<span data-ttu-id="2f8cf-186">過時。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-186">Obsolete.</span></span> <span data-ttu-id="2f8cf-187">若要使用自訂的 MSI 端點，請設定環境變數MSI_ENDPOINT，例如" http://localhost:50342/oauth2/token "。受管理服務的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-187">To use customized MSI endpoint, please set environment variable MSI_ENDPOINT, e.g. "http://localhost:50342/oauth2/token".Port number for the managed service.</span></span>

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

### <span data-ttu-id="2f8cf-188">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="2f8cf-188">-ManagedServiceSecret</span></span>

<span data-ttu-id="2f8cf-189">過時。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-189">Obsolete.</span></span> <span data-ttu-id="2f8cf-190">若要使用自訂的 MSI 機密，請設定環境變數MSI_SECRET。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-190">To use customized MSI secret, please set environment variable MSI_SECRET.</span></span> <span data-ttu-id="2f8cf-191">受管理服務登入的權杖。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-191">Token for the managed service login.</span></span>

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

### <span data-ttu-id="2f8cf-192">-MaxCoNtextPopulation</span><span class="sxs-lookup"><span data-stu-id="2f8cf-192">-MaxContextPopulation</span></span>

<span data-ttu-id="2f8cf-193">登入後，可填入內容的最大訂閱編號。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-193">Max subscription number to populate contexts after login.</span></span> <span data-ttu-id="2f8cf-194">預設值為 25。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-194">Default is 25.</span></span> <span data-ttu-id="2f8cf-195">若要填入所有訂閱至上下文，請設定為 -1。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-195">To populate all subscriptions to contexts, set to -1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f8cf-196">-範圍</span><span class="sxs-lookup"><span data-stu-id="2f8cf-196">-Scope</span></span>

<span data-ttu-id="2f8cf-197">決定上下文變更的範圍，例如，變更是否僅適用于目前的程式，或適用于此使用者啟動的所有會話。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-197">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="2f8cf-198">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2f8cf-198">-ServicePrincipal</span></span>

<span data-ttu-id="2f8cf-199">表示此帳戶會提供服務主體認證來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-199">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="2f8cf-200">-SkipCoNtextPopulation</span><span class="sxs-lookup"><span data-stu-id="2f8cf-200">-SkipContextPopulation</span></span>

<span data-ttu-id="2f8cf-201">如果沒有找到上下文，請略過內容人口。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-201">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="2f8cf-202">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="2f8cf-202">-SkipValidation</span></span>

<span data-ttu-id="2f8cf-203">略過存取權杖的驗證。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-203">Skip validation for access token.</span></span>

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

### <span data-ttu-id="2f8cf-204">-訂閱</span><span class="sxs-lookup"><span data-stu-id="2f8cf-204">-Subscription</span></span>

<span data-ttu-id="2f8cf-205">訂閱名稱或識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-205">Subscription Name or ID.</span></span>

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

### <span data-ttu-id="2f8cf-206">-租使用者</span><span class="sxs-lookup"><span data-stu-id="2f8cf-206">-Tenant</span></span>

<span data-ttu-id="2f8cf-207">選擇性的租使用者名稱或識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-207">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="2f8cf-208">由於目前 API 的限制，當您與企業對企業或 B2B 帳戶 (時，您必須使用租使用者識別碼) 名稱。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-208">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

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

### <span data-ttu-id="2f8cf-209">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="2f8cf-209">-UseDeviceAuthentication</span></span>

<span data-ttu-id="2f8cf-210">使用裝置代碼驗證，而不使用瀏覽器控制項。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-210">Use device code authentication instead of a browser control.</span></span>

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

### <span data-ttu-id="2f8cf-211">-確認</span><span class="sxs-lookup"><span data-stu-id="2f8cf-211">-Confirm</span></span>

<span data-ttu-id="2f8cf-212">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f8cf-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f8cf-213">-WhatIf</span></span>

<span data-ttu-id="2f8cf-214">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-214">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f8cf-215">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-215">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f8cf-216">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f8cf-216">CommonParameters</span></span>
<span data-ttu-id="2f8cf-217">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2f8cf-217">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f8cf-218">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f8cf-218">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f8cf-219">輸入</span><span class="sxs-lookup"><span data-stu-id="2f8cf-219">INPUTS</span></span>

### <span data-ttu-id="2f8cf-220">System.String</span><span class="sxs-lookup"><span data-stu-id="2f8cf-220">System.String</span></span>

## <span data-ttu-id="2f8cf-221">輸出</span><span class="sxs-lookup"><span data-stu-id="2f8cf-221">OUTPUTS</span></span>

### <span data-ttu-id="2f8cf-222">Microsoft.Azure.Commands.Profile.models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="2f8cf-222">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="2f8cf-223">筆記</span><span class="sxs-lookup"><span data-stu-id="2f8cf-223">NOTES</span></span>

## <span data-ttu-id="2f8cf-224">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f8cf-224">RELATED LINKS</span></span>
