---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 533982757e4ea953c1f5d07ba67ac70af2161a10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442692"
---
# <span data-ttu-id="1f751-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="1f751-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="1f751-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f751-102">SYNOPSIS</span></span>
<span data-ttu-id="1f751-103">新增要用於 Azure 資源管理器 Cmdlet 要求的已驗證帳戶。</span><span class="sxs-lookup"><span data-stu-id="1f751-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="1f751-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f751-104">SYNTAX</span></span>

### <span data-ttu-id="1f751-105">UserWithSubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="1f751-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f751-106">UserWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1f751-106">UserWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f751-107">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f751-107">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f751-108">ServicePrincipalWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1f751-108">ServicePrincipalWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f751-109">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f751-109">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f751-110">ServicePrincipalCertificateWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1f751-110">ServicePrincipalCertificateWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f751-111">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f751-111">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f751-112">AccessTokenWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1f751-112">AccessTokenWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f751-113">說明</span><span class="sxs-lookup"><span data-stu-id="1f751-113">DESCRIPTION</span></span>
<span data-ttu-id="1f751-114">Add-AzureRmAcccount Cmdlet 會新增已驗證的 Azure 帳戶以用於 Azure 資源管理器 Cmdlet 要求。</span><span class="sxs-lookup"><span data-stu-id="1f751-114">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="1f751-115">您只能將這個經過驗證的帳戶用於 Azure 資源管理器 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f751-115">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="1f751-116">若要新增與服務管理 Cmdlet 搭配使用的已驗證帳戶，請使用 Add-AzureAccount 或 Import-AzurePublishSettingsFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f751-116">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="1f751-117">示例</span><span class="sxs-lookup"><span data-stu-id="1f751-117">EXAMPLES</span></span>

### <span data-ttu-id="1f751-118">範例1：新增需要互動式登入的帳戶</span><span class="sxs-lookup"><span data-stu-id="1f751-118">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="1f751-119">這個命令會新增 Azure 資源管理員帳戶。</span><span class="sxs-lookup"><span data-stu-id="1f751-119">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="1f751-120">若要使用此帳戶執行 Azure 資源管理器 Cmdlet，您必須在系統提示時提供 Microsoft 帳戶或組織識別碼認證。</span><span class="sxs-lookup"><span data-stu-id="1f751-120">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="1f751-121">如果您的認證已啟用多重要素驗證，您必須使用互動式選項登入，或使用服務主體驗證。</span><span class="sxs-lookup"><span data-stu-id="1f751-121">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="1f751-122">範例2：新增使用組織識別碼認證進行驗證的帳戶</span><span class="sxs-lookup"><span data-stu-id="1f751-122">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="1f751-123">第一個命令會取得使用者認證，然後將它們儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="1f751-123">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="1f751-124">第二個命令會在 $Credential 中新增含認證的 Azure 資源管理器帳戶。</span><span class="sxs-lookup"><span data-stu-id="1f751-124">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="1f751-125">這個帳戶使用組織識別碼認證與 Azure 資源管理器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="1f751-125">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="1f751-126">您無法使用多重要素驗證或 Microsoft 帳號憑證來執行 Azure 資源管理器 Cmdlet 與此帳戶。</span><span class="sxs-lookup"><span data-stu-id="1f751-126">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="1f751-127">範例3：新增以服務主體認證進行驗證的帳戶</span><span class="sxs-lookup"><span data-stu-id="1f751-127">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="1f751-128">第一個命令會取得使用者認證，然後將它們儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="1f751-128">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="1f751-129">第二個命令會使用儲存在指定租使用者 $Credential 中的憑證來新增 Azure 資源管理器帳戶。</span><span class="sxs-lookup"><span data-stu-id="1f751-129">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="1f751-130">ServicePrincipal 切換參數表示該帳戶會以服務主體進行驗證。</span><span class="sxs-lookup"><span data-stu-id="1f751-130">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="1f751-131">範例4：新增特定租使用者和訂閱的帳戶</span><span class="sxs-lookup"><span data-stu-id="1f751-131">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="1f751-132">這個命令會新增 Azure 資源管理員帳戶，以針對指定的租使用者及訂閱執行 Cmdlet （預設為）。</span><span class="sxs-lookup"><span data-stu-id="1f751-132">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="1f751-133">參數</span><span class="sxs-lookup"><span data-stu-id="1f751-133">PARAMETERS</span></span>

### <span data-ttu-id="1f751-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="1f751-134">-AccessToken</span></span>
<span data-ttu-id="1f751-135">指定存取權杖。</span><span class="sxs-lookup"><span data-stu-id="1f751-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f751-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="1f751-136">-AccountId</span></span>
<span data-ttu-id="1f751-137">存取權杖的帳戶識別碼</span><span class="sxs-lookup"><span data-stu-id="1f751-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f751-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1f751-138">-ApplicationId</span></span>
<span data-ttu-id="1f751-139">SPN</span><span class="sxs-lookup"><span data-stu-id="1f751-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f751-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="1f751-140">-CertificateThumbprint</span></span>
<span data-ttu-id="1f751-141">憑證雜湊 (指紋) </span><span class="sxs-lookup"><span data-stu-id="1f751-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f751-142">-認證</span><span class="sxs-lookup"><span data-stu-id="1f751-142">-Credential</span></span>
<span data-ttu-id="1f751-143">指定 PSCredential 物件。</span><span class="sxs-lookup"><span data-stu-id="1f751-143">Specifies a PSCredential object.</span></span>
<span data-ttu-id="1f751-144">如需 PSCredential 物件的詳細資訊，請輸入 Get-Help 取得認證。</span><span class="sxs-lookup"><span data-stu-id="1f751-144">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="1f751-145">PSCredential 物件會提供組織識別碼認證的使用者識別碼和密碼，或是應用程式識別碼和服務主體認證的密碼。</span><span class="sxs-lookup"><span data-stu-id="1f751-145">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f751-146">-環境</span><span class="sxs-lookup"><span data-stu-id="1f751-146">-Environment</span></span>
<span data-ttu-id="1f751-147">包含要登入之帳戶的環境</span><span class="sxs-lookup"><span data-stu-id="1f751-147">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="1f751-148">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1f751-148">-ServicePrincipal</span></span>
<span data-ttu-id="1f751-149">指示此帳戶透過提供服務主體認證來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="1f751-149">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f751-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f751-150">-SubscriptionId</span></span>
<span data-ttu-id="1f751-151">指定訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1f751-151">Specifies the ID of the subscription.</span></span>
<span data-ttu-id="1f751-152">如果您沒有指定此參數，則會使用訂閱清單中的第一個訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f751-152">If you do not specify this parameter, the first subscription from the subscription list is used.</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId, AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f751-153">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1f751-153">-SubscriptionName</span></span>
<span data-ttu-id="1f751-154">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="1f751-154">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionName, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionName, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f751-155">-TenantId</span><span class="sxs-lookup"><span data-stu-id="1f751-155">-TenantId</span></span>
<span data-ttu-id="1f751-156">選用的租使用者名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="1f751-156">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName, AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f751-157">-確認</span><span class="sxs-lookup"><span data-stu-id="1f751-157">-Confirm</span></span>
<span data-ttu-id="1f751-158">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1f751-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f751-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f751-159">-WhatIf</span></span>
<span data-ttu-id="1f751-160">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f751-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f751-161">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f751-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f751-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f751-162">CommonParameters</span></span>
<span data-ttu-id="1f751-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f751-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f751-164">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f751-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f751-165">輸入</span><span class="sxs-lookup"><span data-stu-id="1f751-165">INPUTS</span></span>

## <span data-ttu-id="1f751-166">輸出</span><span class="sxs-lookup"><span data-stu-id="1f751-166">OUTPUTS</span></span>

### <span data-ttu-id="1f751-167">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="1f751-167">PSAzureProfile</span></span>

## <span data-ttu-id="1f751-168">筆記</span><span class="sxs-lookup"><span data-stu-id="1f751-168">NOTES</span></span>

## <span data-ttu-id="1f751-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f751-169">RELATED LINKS</span></span>

