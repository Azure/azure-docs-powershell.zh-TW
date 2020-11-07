---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 32a5c4ac20d584c26d95724a3f4ab4630504fb6d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958973"
---
# <span data-ttu-id="d5fce-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="d5fce-101">Connect-AzAccount</span></span>

## <span data-ttu-id="d5fce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d5fce-102">SYNOPSIS</span></span>
<span data-ttu-id="d5fce-103">使用已驗證的帳戶連線至 Azure，以便與 Az PowerShell 模組中的 Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d5fce-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="d5fce-104">句法</span><span class="sxs-lookup"><span data-stu-id="d5fce-104">SYNTAX</span></span>

### <span data-ttu-id="d5fce-105">UserWithSubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="d5fce-105">UserWithSubscriptionId (Default)</span></span>

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>]
 [-ContextName <String>] [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5fce-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5fce-106">ServicePrincipalWithSubscriptionId</span></span>

```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> -ServicePrincipal
 -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5fce-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="d5fce-107">UserWithCredential</span></span>

```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5fce-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5fce-108">ServicePrincipalCertificateWithSubscriptionId</span></span>

```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5fce-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5fce-109">AccessTokenWithSubscriptionId</span></span>

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5fce-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="d5fce-110">ManagedServiceLogin</span></span>

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] -Identity
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>]
 [-ManagedServiceSecret <SecureString>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5fce-111">說明</span><span class="sxs-lookup"><span data-stu-id="d5fce-111">DESCRIPTION</span></span>

<span data-ttu-id="d5fce-112">Cmdlet 會以 `Connect-AzAccount` 已驗證帳戶連線至 Azure，以便與 Az PowerShell 模組中的 Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d5fce-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="d5fce-113">您只能將這個經過驗證的帳戶用於 Azure 資源管理員要求。</span><span class="sxs-lookup"><span data-stu-id="d5fce-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="d5fce-114">若要新增與服務管理搭配使用的已驗證帳戶，請使用 `Add-AzureAccount` 來自 Azure PowerShell 模組的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d5fce-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="d5fce-115">如果找不到目前使用者的任何內容，則會在使用者的內容清單中填入前25個訂閱的內容。</span><span class="sxs-lookup"><span data-stu-id="d5fce-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="d5fce-116">建立給使用者的上下文清單可透過執行來找到 `Get-AzContext -ListAvailable` 。</span><span class="sxs-lookup"><span data-stu-id="d5fce-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="d5fce-117">若要略過此內容填充，請指定 **SkipCoNtextPopulation** 切換參數。</span><span class="sxs-lookup"><span data-stu-id="d5fce-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="d5fce-118">執行此 Cmdlet 之後，您可以使用連線從 Azure 帳戶中斷連線 `Disconnect-AzAccount` 。</span><span class="sxs-lookup"><span data-stu-id="d5fce-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="d5fce-119">示例</span><span class="sxs-lookup"><span data-stu-id="d5fce-119">EXAMPLES</span></span>

### <span data-ttu-id="d5fce-120">範例1：連線至 Azure 帳戶</span><span class="sxs-lookup"><span data-stu-id="d5fce-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="d5fce-121">這個範例會連線至 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="d5fce-121">This example connects to an Azure account.</span></span> <span data-ttu-id="d5fce-122">您必須提供 Microsoft 帳戶或組織識別碼認證。</span><span class="sxs-lookup"><span data-stu-id="d5fce-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="d5fce-123">如果您的認證已啟用多重要素驗證，您必須使用互動式選項登入，或使用服務主體驗證。</span><span class="sxs-lookup"><span data-stu-id="d5fce-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="d5fce-124">範例2： (Windows PowerShell 5.1 只) 使用組織識別碼認證連線至 Azure</span><span class="sxs-lookup"><span data-stu-id="d5fce-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="d5fce-125">這個案例只適用于 Windows PowerShell 5.1。</span><span class="sxs-lookup"><span data-stu-id="d5fce-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="d5fce-126">第一個命令會提示使用者認證，並將其儲存在 `$Credential` 變數中。</span><span class="sxs-lookup"><span data-stu-id="d5fce-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="d5fce-127">第二個命令會使用儲存在的認證來連接至 Azure 帳戶 `$Credential` 。</span><span class="sxs-lookup"><span data-stu-id="d5fce-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="d5fce-128">這個帳戶會使用組織識別碼認證與 Azure 進行驗證。</span><span class="sxs-lookup"><span data-stu-id="d5fce-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="d5fce-129">範例3：使用服務主要帳戶連接至 Azure</span><span class="sxs-lookup"><span data-stu-id="d5fce-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="d5fce-130">第一個命令會提示服務主體認證，並將其儲存在 `$Credential` 變數中。</span><span class="sxs-lookup"><span data-stu-id="d5fce-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="d5fce-131">在出現提示時，輸入您的使用者名稱和服務主體密碼做為密碼的您的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="d5fce-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="d5fce-132">第二個命令會使用儲存在變數中的服務主體認證來連接指定的 Azure 租使用者 `$Credential` 。</span><span class="sxs-lookup"><span data-stu-id="d5fce-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="d5fce-133">**ServicePrincipal** 切換參數表示該帳戶會以服務主體進行驗證。</span><span class="sxs-lookup"><span data-stu-id="d5fce-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="d5fce-134">範例4：使用互動式登入來連線至特定的租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d5fce-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="d5fce-135">此範例會使用指定的租使用者和訂閱連線至 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="d5fce-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="d5fce-136">範例5：使用受管理的服務身分識別</span><span class="sxs-lookup"><span data-stu-id="d5fce-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="d5fce-137">這個範例會使用主機環境中受管理的服務身分識別 (MSI) 連線。</span><span class="sxs-lookup"><span data-stu-id="d5fce-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="d5fce-138">例如，您是從已指派 MSI 的虛擬機器登入 Azure。</span><span class="sxs-lookup"><span data-stu-id="d5fce-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="d5fce-139">範例6：使用 Managed Service 身分識別登入和 ClientId 連線</span><span class="sxs-lookup"><span data-stu-id="d5fce-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="d5fce-140">這個範例會使用 **myUserAssignedIdentity** 的 Managed 服務身分識別來連線。</span><span class="sxs-lookup"><span data-stu-id="d5fce-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="d5fce-141">它會將指派身分識別的使用者新增至虛擬機器，然後使用使用者指派身分識別的使用者的 ClientId 進行連接。</span><span class="sxs-lookup"><span data-stu-id="d5fce-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="d5fce-142">如需詳細資訊，請參閱 [在 AZURE VM 上設定 azure 資源的 managed](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)身分識別。</span><span class="sxs-lookup"><span data-stu-id="d5fce-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

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

### <span data-ttu-id="d5fce-143">範例7：使用憑證連線</span><span class="sxs-lookup"><span data-stu-id="d5fce-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="d5fce-144">這個範例會使用以憑證為基礎的服務主體驗證來連線至 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="d5fce-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="d5fce-145">用於驗證的服務主體必須以指定的憑證建立。</span><span class="sxs-lookup"><span data-stu-id="d5fce-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="d5fce-146">如需建立自我簽署憑證並指派許可權的詳細資訊，請參閱 [使用 Azure PowerShell 建立含憑證的服務主體](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span><span class="sxs-lookup"><span data-stu-id="d5fce-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

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

## <span data-ttu-id="d5fce-147">參數</span><span class="sxs-lookup"><span data-stu-id="d5fce-147">PARAMETERS</span></span>

### <span data-ttu-id="d5fce-148">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="d5fce-148">-AccessToken</span></span>

<span data-ttu-id="d5fce-149">指定存取權杖。</span><span class="sxs-lookup"><span data-stu-id="d5fce-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="d5fce-150">存取權杖是一種認證類型。</span><span class="sxs-lookup"><span data-stu-id="d5fce-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="d5fce-151">您應該採取適當的安全性預防措施，將它們保密。</span><span class="sxs-lookup"><span data-stu-id="d5fce-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="d5fce-152">存取權杖也會超時，而且可能會阻止長時間執行的工作完成。</span><span class="sxs-lookup"><span data-stu-id="d5fce-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

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

### <span data-ttu-id="d5fce-153">-AccountId</span><span class="sxs-lookup"><span data-stu-id="d5fce-153">-AccountId</span></span>

<span data-ttu-id="d5fce-154">在 **AccessToken** 參數集中存取權杖的帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="d5fce-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="d5fce-155">受管理的服務在 **ManagedService** 參數集中的帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="d5fce-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="d5fce-156">可以是受管理的服務資源識別碼，或相關聯的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="d5fce-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="d5fce-157">若要使用系統指派的身分識別，請將此欄位留白。</span><span class="sxs-lookup"><span data-stu-id="d5fce-157">To use the system assigned identity, leave this field blank.</span></span>

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

### <span data-ttu-id="d5fce-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d5fce-158">-ApplicationId</span></span>

<span data-ttu-id="d5fce-159">服務主體的 [應用程式識別碼]。</span><span class="sxs-lookup"><span data-stu-id="d5fce-159">Application ID of the service principal.</span></span>

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

### <span data-ttu-id="d5fce-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="d5fce-160">-CertificateThumbprint</span></span>

<span data-ttu-id="d5fce-161">[憑證雜湊] 或 [指紋]。</span><span class="sxs-lookup"><span data-stu-id="d5fce-161">Certificate Hash or Thumbprint.</span></span>

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

### <span data-ttu-id="d5fce-162">-CoNtextName</span><span class="sxs-lookup"><span data-stu-id="d5fce-162">-ContextName</span></span>

<span data-ttu-id="d5fce-163">此登入的預設 Azure 內容名稱。</span><span class="sxs-lookup"><span data-stu-id="d5fce-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="d5fce-164">如需有關 Azure 內容的詳細資訊，請參閱 [Azure PowerShell 內容物件](/powershell/azure/context-persistence)。</span><span class="sxs-lookup"><span data-stu-id="d5fce-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

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

### <span data-ttu-id="d5fce-165">-認證</span><span class="sxs-lookup"><span data-stu-id="d5fce-165">-Credential</span></span>

<span data-ttu-id="d5fce-166">指定 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="d5fce-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="d5fce-167">如需 **PSCredential** 物件的詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="d5fce-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="d5fce-168">**PSCredential** 物件會提供組織識別碼認證的使用者識別碼和密碼，或是應用程式識別碼和服務主體認證的密碼。</span><span class="sxs-lookup"><span data-stu-id="d5fce-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="d5fce-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5fce-169">-DefaultProfile</span></span>

<span data-ttu-id="d5fce-170">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d5fce-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5fce-171">-環境</span><span class="sxs-lookup"><span data-stu-id="d5fce-171">-Environment</span></span>

<span data-ttu-id="d5fce-172">包含 Azure 帳戶的環境。</span><span class="sxs-lookup"><span data-stu-id="d5fce-172">Environment containing the Azure account.</span></span>

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

### <span data-ttu-id="d5fce-173">-Force</span><span class="sxs-lookup"><span data-stu-id="d5fce-173">-Force</span></span>

<span data-ttu-id="d5fce-174">使用相同的名稱覆寫現有的內容而不需提示。</span><span class="sxs-lookup"><span data-stu-id="d5fce-174">Overwrite the existing context with the same name without prompting.</span></span>

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

### <span data-ttu-id="d5fce-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="d5fce-175">-GraphAccessToken</span></span>

<span data-ttu-id="d5fce-176">圖形服務的 AccessToken。</span><span class="sxs-lookup"><span data-stu-id="d5fce-176">AccessToken for Graph Service.</span></span>

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

### <span data-ttu-id="d5fce-177">身分識別</span><span class="sxs-lookup"><span data-stu-id="d5fce-177">-Identity</span></span>

<span data-ttu-id="d5fce-178">使用受管理的服務身分識別登入。</span><span class="sxs-lookup"><span data-stu-id="d5fce-178">Login using a Managed Service Identity.</span></span>

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

### <span data-ttu-id="d5fce-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="d5fce-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="d5fce-180">AccessToken for KeyVault Service。</span><span class="sxs-lookup"><span data-stu-id="d5fce-180">AccessToken for KeyVault Service.</span></span>

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

### <span data-ttu-id="d5fce-181">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="d5fce-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="d5fce-182">受管理服務的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="d5fce-182">Host name for the managed service.</span></span>

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

### <span data-ttu-id="d5fce-183">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="d5fce-183">-ManagedServicePort</span></span>

<span data-ttu-id="d5fce-184">受管理服務的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="d5fce-184">Port number for the managed service.</span></span>

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

### <span data-ttu-id="d5fce-185">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="d5fce-185">-ManagedServiceSecret</span></span>

<span data-ttu-id="d5fce-186">受管理的服務登入的權杖。</span><span class="sxs-lookup"><span data-stu-id="d5fce-186">Token for the managed service login.</span></span>

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

### <span data-ttu-id="d5fce-187">-範圍</span><span class="sxs-lookup"><span data-stu-id="d5fce-187">-Scope</span></span>

<span data-ttu-id="d5fce-188">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="d5fce-188">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="d5fce-189">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d5fce-189">-ServicePrincipal</span></span>

<span data-ttu-id="d5fce-190">指示此帳戶透過提供服務主體認證來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="d5fce-190">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="d5fce-191">-SkipCoNtextPopulation</span><span class="sxs-lookup"><span data-stu-id="d5fce-191">-SkipContextPopulation</span></span>

<span data-ttu-id="d5fce-192">如果找不到任何上下文，則會略過內容樣本。</span><span class="sxs-lookup"><span data-stu-id="d5fce-192">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="d5fce-193">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="d5fce-193">-SkipValidation</span></span>

<span data-ttu-id="d5fce-194">跳過存取權杖的驗證。</span><span class="sxs-lookup"><span data-stu-id="d5fce-194">Skip validation for access token.</span></span>

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

### <span data-ttu-id="d5fce-195">-訂閱</span><span class="sxs-lookup"><span data-stu-id="d5fce-195">-Subscription</span></span>

<span data-ttu-id="d5fce-196">訂閱名稱或 ID。</span><span class="sxs-lookup"><span data-stu-id="d5fce-196">Subscription Name or ID.</span></span>

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

### <span data-ttu-id="d5fce-197">-租使用者</span><span class="sxs-lookup"><span data-stu-id="d5fce-197">-Tenant</span></span>

<span data-ttu-id="d5fce-198">選用的租使用者名稱或 ID。</span><span class="sxs-lookup"><span data-stu-id="d5fce-198">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="d5fce-199">由於目前 API 的限制，在與企業對企業 (B2B) 帳戶連線時，您必須使用租使用者識別碼，而不是租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="d5fce-199">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

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

### <span data-ttu-id="d5fce-200">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="d5fce-200">-UseDeviceAuthentication</span></span>

<span data-ttu-id="d5fce-201">使用裝置程式碼驗證，而非瀏覽器控制項。</span><span class="sxs-lookup"><span data-stu-id="d5fce-201">Use device code authentication instead of a browser control.</span></span> <span data-ttu-id="d5fce-202">這是 PowerShell 版本6及更新版本的預設驗證類型。</span><span class="sxs-lookup"><span data-stu-id="d5fce-202">This is the default authentication type for PowerShell version 6 and higher.</span></span>

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

### <span data-ttu-id="d5fce-203">-確認</span><span class="sxs-lookup"><span data-stu-id="d5fce-203">-Confirm</span></span>

<span data-ttu-id="d5fce-204">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d5fce-204">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5fce-205">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5fce-205">-WhatIf</span></span>

<span data-ttu-id="d5fce-206">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d5fce-206">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5fce-207">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d5fce-207">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5fce-208">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5fce-208">CommonParameters</span></span>

<span data-ttu-id="d5fce-209">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d5fce-209">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5fce-210">如需詳細資訊，請參閱 [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)。</span><span class="sxs-lookup"><span data-stu-id="d5fce-210">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
<span data-ttu-id="d5fce-211">(http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5fce-211">(http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5fce-212">輸入</span><span class="sxs-lookup"><span data-stu-id="d5fce-212">INPUTS</span></span>

### <span data-ttu-id="d5fce-213">System.object</span><span class="sxs-lookup"><span data-stu-id="d5fce-213">System.String</span></span>

## <span data-ttu-id="d5fce-214">輸出</span><span class="sxs-lookup"><span data-stu-id="d5fce-214">OUTPUTS</span></span>

### <span data-ttu-id="d5fce-215">PSAzureProfile 的基本設定檔。</span><span class="sxs-lookup"><span data-stu-id="d5fce-215">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="d5fce-216">筆記</span><span class="sxs-lookup"><span data-stu-id="d5fce-216">NOTES</span></span>

## <span data-ttu-id="d5fce-217">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5fce-217">RELATED LINKS</span></span>
