---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75f6b7cee1517a3f9ae363a7e28df420e18d37ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969442"
---
# <span data-ttu-id="f9581-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f9581-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f9581-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9581-102">SYNOPSIS</span></span>
<span data-ttu-id="f9581-103">建立新的身分識別提供者配置。</span><span class="sxs-lookup"><span data-stu-id="f9581-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="f9581-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9581-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SigninTenant <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9581-105">說明</span><span class="sxs-lookup"><span data-stu-id="f9581-105">DESCRIPTION</span></span>
<span data-ttu-id="f9581-106">建立新的身分識別提供者配置。</span><span class="sxs-lookup"><span data-stu-id="f9581-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="f9581-107">示例</span><span class="sxs-lookup"><span data-stu-id="f9581-107">EXAMPLES</span></span>

### <span data-ttu-id="f9581-108">範例1：將 Facebook 配置為開發人員入口網站登錄的身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="f9581-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="f9581-109">這個命令會在 ApiManagement 服務的開發人員入口網站上，將 Facebook 身分識別為已接受的身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="f9581-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="f9581-110">這會採用 Facebook 應用程式的 ClientId 與 ClientSecret 做為輸入。</span><span class="sxs-lookup"><span data-stu-id="f9581-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="f9581-111">範例2：將 adB2C 設定為開發人員入口網站登錄的身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="f9581-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $context -Type AadB2C -ClientId 6b1fc750-9e68-450c-97d2-ba6acd0fbc20 -ClientSecret "foobar" -AllowedTenants 'samirtestbc.onmicrosoft.com' -SignupPolicyName B2C_1_signup-policy

Type                     : AadB2C
ClientId                 : 6b1fc750-9e68-450c-97d2-ba6acd0fbc20
ClientSecret             : foobar
AllowedTenants           : {samirtestbc.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_signup-policy
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
Id                       : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-WestUS
ServiceName              : contoso
```

<span data-ttu-id="f9581-112">這個命令會在 ApiManagement 服務的開發人員入口網站上，將 Facebook 身分識別為已接受的身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="f9581-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="f9581-113">這會採用 Facebook 應用程式的 ClientId 與 ClientSecret 做為輸入。</span><span class="sxs-lookup"><span data-stu-id="f9581-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="f9581-114">參數</span><span class="sxs-lookup"><span data-stu-id="f9581-114">PARAMETERS</span></span>

### <span data-ttu-id="f9581-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="f9581-115">-AllowedTenants</span></span>
<span data-ttu-id="f9581-116">允許的 Azure Active Directory 承租人清單</span><span class="sxs-lookup"><span data-stu-id="f9581-116">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9581-117">-頒發機構</span><span class="sxs-lookup"><span data-stu-id="f9581-117">-Authority</span></span>
<span data-ttu-id="f9581-118">AAD 或 AAD B2C 的 OpenID Connect 探索端點主機名稱。</span><span class="sxs-lookup"><span data-stu-id="f9581-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="f9581-119">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f9581-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9581-120">-ClientId</span><span class="sxs-lookup"><span data-stu-id="f9581-120">-ClientId</span></span>
<span data-ttu-id="f9581-121">外部身分識別提供者中應用程式的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="f9581-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="f9581-122">它是 Facebook 登入的應用程式識別碼、Google 登入的用戶端識別碼、Microsoft 的 App ID。</span><span class="sxs-lookup"><span data-stu-id="f9581-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9581-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="f9581-123">-ClientSecret</span></span>
<span data-ttu-id="f9581-124">外部身分識別提供者的應用程式的用戶端密碼，用來驗證登入要求。</span><span class="sxs-lookup"><span data-stu-id="f9581-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="f9581-125">例如，它是 Facebook login 的 App 機密、Google 登入的 API 金鑰、Microsoft 的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="f9581-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9581-126">-內容</span><span class="sxs-lookup"><span data-stu-id="f9581-126">-Context</span></span>
<span data-ttu-id="f9581-127">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="f9581-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f9581-128">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f9581-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9581-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9581-129">-DefaultProfile</span></span>
<span data-ttu-id="f9581-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9581-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9581-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="f9581-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="f9581-132">密碼重設策略名稱。</span><span class="sxs-lookup"><span data-stu-id="f9581-132">Password Reset Policy Name.</span></span> <span data-ttu-id="f9581-133">僅適用于 AAD 的 B2C 身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="f9581-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="f9581-134">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f9581-134">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9581-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="f9581-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="f9581-136">設定檔編輯原則名稱。</span><span class="sxs-lookup"><span data-stu-id="f9581-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="f9581-137">僅適用于 AAD 的 B2C 身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="f9581-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="f9581-138">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f9581-138">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9581-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="f9581-139">-SigninPolicyName</span></span>
<span data-ttu-id="f9581-140">登錄原則名稱。</span><span class="sxs-lookup"><span data-stu-id="f9581-140">Signin Policy Name.</span></span> <span data-ttu-id="f9581-141">僅適用于 AAD 的 B2C 身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="f9581-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="f9581-142">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f9581-142">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9581-143">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="f9581-143">-SigninTenant</span></span>
<span data-ttu-id="f9581-144">在 AAD B2C （而不是租使用者）中登入要覆蓋的租使用者 `common`</span><span class="sxs-lookup"><span data-stu-id="f9581-144">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9581-145">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="f9581-145">-SignupPolicyName</span></span>
<span data-ttu-id="f9581-146">註冊原則名稱。</span><span class="sxs-lookup"><span data-stu-id="f9581-146">Signup Policy Name.</span></span> <span data-ttu-id="f9581-147">僅適用于 AAD 的 B2C 身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="f9581-147">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="f9581-148">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f9581-148">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9581-149">-類型</span><span class="sxs-lookup"><span data-stu-id="f9581-149">-Type</span></span>
<span data-ttu-id="f9581-150">身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f9581-150">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="f9581-151">如果已指定，將會嘗試透過識別碼尋找身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="f9581-151">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="f9581-152">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f9581-152">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9581-153">-確認</span><span class="sxs-lookup"><span data-stu-id="f9581-153">-Confirm</span></span>
<span data-ttu-id="f9581-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f9581-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9581-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9581-155">-WhatIf</span></span>
<span data-ttu-id="f9581-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9581-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9581-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9581-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9581-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9581-158">CommonParameters</span></span>
<span data-ttu-id="f9581-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9581-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9581-160">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f9581-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9581-161">輸入</span><span class="sxs-lookup"><span data-stu-id="f9581-161">INPUTS</span></span>

### <span data-ttu-id="f9581-162">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f9581-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f9581-163">ServiceManagement. PsApiManagementIdentityProviderType （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f9581-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="f9581-164">System.object</span><span class="sxs-lookup"><span data-stu-id="f9581-164">System.String</span></span>

### <span data-ttu-id="f9581-165">System.object []</span><span class="sxs-lookup"><span data-stu-id="f9581-165">System.String[]</span></span>

## <span data-ttu-id="f9581-166">輸出</span><span class="sxs-lookup"><span data-stu-id="f9581-166">OUTPUTS</span></span>

### <span data-ttu-id="f9581-167">ServiceManagement. PsApiManagementIdentityProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f9581-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f9581-168">筆記</span><span class="sxs-lookup"><span data-stu-id="f9581-168">NOTES</span></span>

## <span data-ttu-id="f9581-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9581-169">RELATED LINKS</span></span>

[<span data-ttu-id="f9581-170">AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f9581-170">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="f9581-171">移除-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f9581-171">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="f9581-172">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f9581-172">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)