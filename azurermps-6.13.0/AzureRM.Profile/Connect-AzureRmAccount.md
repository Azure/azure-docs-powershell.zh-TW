---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: a0f29e666a289faddbfce848b97cb0272ce67d0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626047"
---
# <span data-ttu-id="6f7d6-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="6f7d6-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="6f7d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f7d6-102">SYNOPSIS</span></span>
<span data-ttu-id="6f7d6-103">使用已驗證的帳戶連線至 Azure，以與 Azure 資源管理器 Cmdlet 要求搭配使用。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f7d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f7d6-104">SYNTAX</span></span>

### <span data-ttu-id="6f7d6-105">UserWithSubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="6f7d6-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f7d6-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6f7d6-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f7d6-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6f7d6-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f7d6-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6f7d6-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f7d6-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="6f7d6-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6f7d6-110">說明</span><span class="sxs-lookup"><span data-stu-id="6f7d6-110">DESCRIPTION</span></span>
<span data-ttu-id="6f7d6-111">Connect-AzureRmAccount Cmdlet 會以已驗證的帳戶連線至 Azure，以便與 Azure 資源管理器 Cmdlet 要求搭配使用。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="6f7d6-112">您只能將這個經過驗證的帳戶用於 Azure 資源管理器 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="6f7d6-113">若要新增與服務管理 Cmdlet 搭配使用的已驗證帳戶，請使用 Add-AzureAccount 或 Import-AzurePublishSettingsFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="6f7d6-114">如果找不到目前使用者的任何內容，這個命令會在使用者的內容清單中填入每一個 (前25個) 訂閱的內容。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-114">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="6f7d6-115">您可以透過執行「AzureRmCoNtext-ListAvailable」，找到為使用者建立的上下文清單。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-115">The list of contexts created for the user can be found by running "Get-AzureRmContext -ListAvailable".</span></span> <span data-ttu-id="6f7d6-116">若要略過此內容填充，您可以使用 "-SkipCoNtextPopulation" 切換參數執行此命令。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-116">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="6f7d6-117">執行此 Cmdlet 之後，您可以使用 [中斷連線] 從 Azure 帳戶中斷連線 AzureRmAccount。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-117">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="6f7d6-118">示例</span><span class="sxs-lookup"><span data-stu-id="6f7d6-118">EXAMPLES</span></span>

### <span data-ttu-id="6f7d6-119">範例1：使用互動式登入來連線至 Azure 帳戶</span><span class="sxs-lookup"><span data-stu-id="6f7d6-119">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzureRmAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="6f7d6-120">這個命令會連接至 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-120">This command connects to an Azure account.</span></span>
<span data-ttu-id="6f7d6-121">若要使用此帳戶執行 Azure 資源管理器 Cmdlet，您必須在系統提示時提供 Microsoft 帳戶或組織識別碼認證。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-121">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="6f7d6-122">如果您的認證已啟用多重要素驗證，您必須使用互動式選項登入，或使用服務主體驗證。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-122">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="6f7d6-123">範例2：使用組織識別碼認證連線至 Azure 帳戶</span><span class="sxs-lookup"><span data-stu-id="6f7d6-123">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="6f7d6-124">第一個命令會提示使用者認證 (使用者名稱和密碼) ，然後將它們儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-124">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="6f7d6-125">第二個命令會使用儲存在 $Credential 中的認證，連線至 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-125">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="6f7d6-126">這個帳戶使用組織識別碼認證與 Azure 資源管理器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-126">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="6f7d6-127">您無法使用多重要素驗證或 Microsoft 帳號憑證來執行 Azure 資源管理器 Cmdlet 與此帳戶。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-127">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="6f7d6-128">範例3：連線至 Azure 服務主要帳戶</span><span class="sxs-lookup"><span data-stu-id="6f7d6-128">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential

PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="6f7d6-129">第一個命令會取得服務主體認證 (應用程式識別碼和服務主體密碼) ，然後將它們儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-129">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="6f7d6-130">第二個命令使用儲存在指定租使用者 $Credential 中的服務主體認證來連線至 Azure。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-130">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="6f7d6-131">ServicePrincipal 切換參數表示該帳戶會以服務主體進行驗證。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-131">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="6f7d6-132">範例4：使用互動式登入來連線至特定租使用者和訂閱的帳戶</span><span class="sxs-lookup"><span data-stu-id="6f7d6-132">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="6f7d6-133">這個命令會連線至 Azure 帳戶，並設定 AzureRM PowerShell，以預設為指定的租使用者和訂閱執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-133">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="6f7d6-134">範例5：使用 Managed Services Identity Login 來新增帳戶</span><span class="sxs-lookup"><span data-stu-id="6f7d6-134">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -MSI

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="6f7d6-135">這個命令會使用主機環境的 managed 服務身分識別 (例如，如果在已指派受管理服務身分識別的 VirtualMachine 上執行，這將允許程式碼使用指定的身分識別來登入) </span><span class="sxs-lookup"><span data-stu-id="6f7d6-135">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="6f7d6-136">範例6：使用憑證新增帳戶</span><span class="sxs-lookup"><span data-stu-id="6f7d6-136">Example 6: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzureRmAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="6f7d6-137">這個命令會使用以憑證為基礎的服務主體驗證來連線至 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-137">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="6f7d6-138">已使用指定憑證建立驗證所用的 Theservice 主體。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-138">Theservice principal used for authentication should have been created with the given certificate.</span></span>

## <span data-ttu-id="6f7d6-139">參數</span><span class="sxs-lookup"><span data-stu-id="6f7d6-139">PARAMETERS</span></span>

### <span data-ttu-id="6f7d6-140">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="6f7d6-140">-AccessToken</span></span>
<span data-ttu-id="6f7d6-141">指定存取權杖。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-141">Specifies an access token.</span></span>

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

### <span data-ttu-id="6f7d6-142">-AccountId</span><span class="sxs-lookup"><span data-stu-id="6f7d6-142">-AccountId</span></span>
<span data-ttu-id="6f7d6-143">存取權杖的帳戶識別碼</span><span class="sxs-lookup"><span data-stu-id="6f7d6-143">Account Id for access token</span></span>

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

### <span data-ttu-id="6f7d6-144">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6f7d6-144">-ApplicationId</span></span>
<span data-ttu-id="6f7d6-145">SPN</span><span class="sxs-lookup"><span data-stu-id="6f7d6-145">SPN</span></span>

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

### <span data-ttu-id="6f7d6-146">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="6f7d6-146">-CertificateThumbprint</span></span>
<span data-ttu-id="6f7d6-147">憑證雜湊 (指紋) </span><span class="sxs-lookup"><span data-stu-id="6f7d6-147">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="6f7d6-148">-CoNtextName</span><span class="sxs-lookup"><span data-stu-id="6f7d6-148">-ContextName</span></span>
<span data-ttu-id="6f7d6-149">此登入的預設內容名稱。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-149">Name of the default context from this login.</span></span>  <span data-ttu-id="6f7d6-150">登入後，您就可以使用此名稱來選取此內容。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-150">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="6f7d6-151">-認證</span><span class="sxs-lookup"><span data-stu-id="6f7d6-151">-Credential</span></span>
<span data-ttu-id="6f7d6-152">指定 PSCredential 物件。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-152">Specifies a PSCredential object.</span></span>
<span data-ttu-id="6f7d6-153">如需 PSCredential 物件的詳細資訊，請輸入 Get-Help 取得認證。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-153">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="6f7d6-154">PSCredential 物件會提供組織識別碼認證的使用者識別碼和密碼，或是應用程式識別碼和服務主體認證的密碼。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-154">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="6f7d6-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f7d6-155">-DefaultProfile</span></span>
<span data-ttu-id="6f7d6-156">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f7d6-157">-環境</span><span class="sxs-lookup"><span data-stu-id="6f7d6-157">-Environment</span></span>
<span data-ttu-id="6f7d6-158">包含要登入之帳戶的環境</span><span class="sxs-lookup"><span data-stu-id="6f7d6-158">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="6f7d6-159">-Force</span><span class="sxs-lookup"><span data-stu-id="6f7d6-159">-Force</span></span>
<span data-ttu-id="6f7d6-160">使用相同的名稱覆寫現有的內容（如果有）。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-160">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="6f7d6-161">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="6f7d6-161">-GraphAccessToken</span></span>
<span data-ttu-id="6f7d6-162">圖形服務的 AccessToken</span><span class="sxs-lookup"><span data-stu-id="6f7d6-162">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="6f7d6-163">身分識別</span><span class="sxs-lookup"><span data-stu-id="6f7d6-163">-Identity</span></span>
<span data-ttu-id="6f7d6-164">在目前的環境中使用受管理的服務標識登入。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-164">Login using managed service identity in the current environment.</span></span>

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

### <span data-ttu-id="6f7d6-165">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="6f7d6-165">-KeyVaultAccessToken</span></span>
<span data-ttu-id="6f7d6-166">AccessToken for KeyVault Service</span><span class="sxs-lookup"><span data-stu-id="6f7d6-166">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="6f7d6-167">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="6f7d6-167">-ManagedServiceHostName</span></span>
<span data-ttu-id="6f7d6-168">受管理的服務登入的主機名稱</span><span class="sxs-lookup"><span data-stu-id="6f7d6-168">Host name for managed service login</span></span>

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

### <span data-ttu-id="6f7d6-169">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="6f7d6-169">-ManagedServicePort</span></span>
<span data-ttu-id="6f7d6-170">受管理的服務登入的埠號碼</span><span class="sxs-lookup"><span data-stu-id="6f7d6-170">Port number for managed service login</span></span>

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

### <span data-ttu-id="6f7d6-171">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="6f7d6-171">-ManagedServiceSecret</span></span>
<span data-ttu-id="6f7d6-172">秘密，用於某些類型的受管理的服務登入。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-172">Secret, used for some kinds of managed service login.</span></span>

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

### <span data-ttu-id="6f7d6-173">-範圍</span><span class="sxs-lookup"><span data-stu-id="6f7d6-173">-Scope</span></span>
<span data-ttu-id="6f7d6-174">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-174">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="6f7d6-175">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6f7d6-175">-ServicePrincipal</span></span>
<span data-ttu-id="6f7d6-176">指示此帳戶透過提供服務主體認證來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-176">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="6f7d6-177">-SkipCoNtextPopulation</span><span class="sxs-lookup"><span data-stu-id="6f7d6-177">-SkipContextPopulation</span></span>
<span data-ttu-id="6f7d6-178">如果找不到任何上下文，則會略過內容樣本。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-178">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="6f7d6-179">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="6f7d6-179">-SkipValidation</span></span>
<span data-ttu-id="6f7d6-180">跳過存取權杖的驗證</span><span class="sxs-lookup"><span data-stu-id="6f7d6-180">Skip validation for access token</span></span>

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

### <span data-ttu-id="6f7d6-181">-訂閱</span><span class="sxs-lookup"><span data-stu-id="6f7d6-181">-Subscription</span></span>
<span data-ttu-id="6f7d6-182">訂閱名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="6f7d6-182">Subscription Name or ID</span></span>

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

### <span data-ttu-id="6f7d6-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="6f7d6-183">-TenantId</span></span>
<span data-ttu-id="6f7d6-184">[選用功能變數名稱] 或 [租使用者識別碼]。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-184">Optional domain name or tenant ID.</span></span> <span data-ttu-id="6f7d6-185">在所有登入的情況下，功能變數名稱將無法運作。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-185">Domain name will not work in all sign-in situations.</span></span> <span data-ttu-id="6f7d6-186">若是雲端方案提供者 (CSP) 登入，則需要租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-186">For Cloud Solution Provider (CSP) sign-in, tenant ID is required.</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
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

### <span data-ttu-id="6f7d6-187">-確認</span><span class="sxs-lookup"><span data-stu-id="6f7d6-187">-Confirm</span></span>
<span data-ttu-id="6f7d6-188">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f7d6-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f7d6-189">-WhatIf</span></span>
<span data-ttu-id="6f7d6-190">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f7d6-191">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f7d6-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f7d6-192">CommonParameters</span></span>
<span data-ttu-id="6f7d6-193">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f7d6-194">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f7d6-195">輸入</span><span class="sxs-lookup"><span data-stu-id="6f7d6-195">INPUTS</span></span>

### <span data-ttu-id="6f7d6-196">System.object</span><span class="sxs-lookup"><span data-stu-id="6f7d6-196">System.String</span></span>
<span data-ttu-id="6f7d6-197">參數：訂閱 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="6f7d6-197">Parameters: Subscription (ByValue)</span></span>

## <span data-ttu-id="6f7d6-198">輸出</span><span class="sxs-lookup"><span data-stu-id="6f7d6-198">OUTPUTS</span></span>

### <span data-ttu-id="6f7d6-199">PSAzureProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="6f7d6-199">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="6f7d6-200">筆記</span><span class="sxs-lookup"><span data-stu-id="6f7d6-200">NOTES</span></span>

## <span data-ttu-id="6f7d6-201">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f7d6-201">RELATED LINKS</span></span>
