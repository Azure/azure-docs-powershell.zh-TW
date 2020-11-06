---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: d2d689c9df73f7cd9bb6df6a5153e9afa71cb39d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613879"
---
# <span data-ttu-id="9f8e7-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9f8e7-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="9f8e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9f8e7-102">SYNOPSIS</span></span>
<span data-ttu-id="9f8e7-103">更新現有身分識別提供者的設定。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="9f8e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="9f8e7-104">SYNTAX</span></span>

### <span data-ttu-id="9f8e7-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="9f8e7-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f8e7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9f8e7-106">ByInputObject</span></span>
```
Set-AzApiManagementIdentityProvider -InputObject <PsApiManagementIdentityProvider> [-ClientId <String>]
 [-ClientSecret <String>] [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>]
 [-SigninPolicyName <String>] [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f8e7-107">說明</span><span class="sxs-lookup"><span data-stu-id="9f8e7-107">DESCRIPTION</span></span>
<span data-ttu-id="9f8e7-108">更新現有身分識別提供者的設定。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-108">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="9f8e7-109">示例</span><span class="sxs-lookup"><span data-stu-id="9f8e7-109">EXAMPLES</span></span>

### <span data-ttu-id="9f8e7-110">範例1：更新 facebook 身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="9f8e7-110">Example 1 : Update the facebook Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="9f8e7-111">Cmdlet 會更新 Facebook 身分識別提供者的用戶端密碼;</span><span class="sxs-lookup"><span data-stu-id="9f8e7-111">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="9f8e7-112">參數</span><span class="sxs-lookup"><span data-stu-id="9f8e7-112">PARAMETERS</span></span>

### <span data-ttu-id="9f8e7-113">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="9f8e7-113">-AllowedTenants</span></span>
<span data-ttu-id="9f8e7-114">允許的 Azure Active Directory 租使用者清單。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-114">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="9f8e7-115">-頒發機構</span><span class="sxs-lookup"><span data-stu-id="9f8e7-115">-Authority</span></span>
<span data-ttu-id="9f8e7-116">AAD 或 AAD B2C 的 OpenID Connect 探索端點主機名稱。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-116">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="9f8e7-117">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="9f8e7-118">-ClientId</span><span class="sxs-lookup"><span data-stu-id="9f8e7-118">-ClientId</span></span>
<span data-ttu-id="9f8e7-119">外部身分識別提供者中應用程式的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-119">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="9f8e7-120">它是 Facebook 登入的應用程式識別碼、Google 登入的用戶端識別碼、Microsoft 的 App ID。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-120">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="9f8e7-121">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="9f8e7-121">-ClientSecret</span></span>
<span data-ttu-id="9f8e7-122">外部身分識別提供者的應用程式的用戶端密碼，用來驗證登入要求。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-122">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="9f8e7-123">例如，它是 Facebook login 的 App 機密、Google 登入的 API 金鑰、Microsoft 的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-123">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="9f8e7-124">-內容</span><span class="sxs-lookup"><span data-stu-id="9f8e7-124">-Context</span></span>
<span data-ttu-id="9f8e7-125">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-125">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9f8e7-126">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f8e7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f8e7-127">-DefaultProfile</span></span>
<span data-ttu-id="9f8e7-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f8e7-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f8e7-129">-InputObject</span></span>
<span data-ttu-id="9f8e7-130">PsApiManagementIdentityProvider 的實例。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-130">Instance of PsApiManagementIdentityProvider.</span></span> <span data-ttu-id="9f8e7-131">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-131">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f8e7-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f8e7-132">-PassThru</span></span>
<span data-ttu-id="9f8e7-133">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的  **PsApiManagementIdentityProvider** 。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-133">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f8e7-134">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="9f8e7-134">-PasswordResetPolicyName</span></span>
<span data-ttu-id="9f8e7-135">密碼重設策略名稱。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-135">Password Reset Policy Name.</span></span> <span data-ttu-id="9f8e7-136">僅適用于 AAD 的 B2C 身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-136">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="9f8e7-137">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="9f8e7-138">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="9f8e7-138">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="9f8e7-139">設定檔編輯原則名稱。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-139">Profile Editing Policy Name.</span></span> <span data-ttu-id="9f8e7-140">僅適用于 AAD 的 B2C 身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-140">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="9f8e7-141">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="9f8e7-142">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="9f8e7-142">-SigninPolicyName</span></span>
<span data-ttu-id="9f8e7-143">登錄原則名稱。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-143">Signin Policy Name.</span></span> <span data-ttu-id="9f8e7-144">僅適用于 AAD 的 B2C 身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-144">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="9f8e7-145">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="9f8e7-146">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="9f8e7-146">-SignupPolicyName</span></span>
<span data-ttu-id="9f8e7-147">註冊原則名稱。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-147">Signup Policy Name.</span></span> <span data-ttu-id="9f8e7-148">僅適用于 AAD 的 B2C 身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-148">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="9f8e7-149">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="9f8e7-150">-類型</span><span class="sxs-lookup"><span data-stu-id="9f8e7-150">-Type</span></span>
<span data-ttu-id="9f8e7-151">現有身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-151">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="9f8e7-152">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-152">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: ExpandedParameter
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f8e7-153">-確認</span><span class="sxs-lookup"><span data-stu-id="9f8e7-153">-Confirm</span></span>
<span data-ttu-id="9f8e7-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f8e7-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f8e7-155">-WhatIf</span></span>
<span data-ttu-id="9f8e7-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f8e7-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f8e7-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f8e7-158">CommonParameters</span></span>
<span data-ttu-id="9f8e7-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f8e7-160">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9f8e7-160">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f8e7-161">輸入</span><span class="sxs-lookup"><span data-stu-id="9f8e7-161">INPUTS</span></span>

### <span data-ttu-id="9f8e7-162">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9f8e7-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9f8e7-163">ServiceManagement. PsApiManagementIdentityProviderType （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9f8e7-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="9f8e7-164">System.object</span><span class="sxs-lookup"><span data-stu-id="9f8e7-164">System.String</span></span>

### <span data-ttu-id="9f8e7-165">System.object []</span><span class="sxs-lookup"><span data-stu-id="9f8e7-165">System.String[]</span></span>

### <span data-ttu-id="9f8e7-166">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="9f8e7-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9f8e7-167">輸出</span><span class="sxs-lookup"><span data-stu-id="9f8e7-167">OUTPUTS</span></span>

### <span data-ttu-id="9f8e7-168">ServiceManagement. PsApiManagementIdentityProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9f8e7-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="9f8e7-169">筆記</span><span class="sxs-lookup"><span data-stu-id="9f8e7-169">NOTES</span></span>

## <span data-ttu-id="9f8e7-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f8e7-170">RELATED LINKS</span></span>

[<span data-ttu-id="9f8e7-171">新-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9f8e7-171">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="9f8e7-172">AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9f8e7-172">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="9f8e7-173">移除-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9f8e7-173">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)
