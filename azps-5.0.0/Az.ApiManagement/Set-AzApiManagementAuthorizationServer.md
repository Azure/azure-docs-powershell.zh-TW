---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 4f484f200f2807cb814badbf93401061e670e72b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137728"
---
# <span data-ttu-id="aab2e-101">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="aab2e-101">Set-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="aab2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aab2e-102">SYNOPSIS</span></span>
<span data-ttu-id="aab2e-103">修改授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="aab2e-103">Modifies an authorization server.</span></span>

## <span data-ttu-id="aab2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="aab2e-104">SYNTAX</span></span>

```
Set-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aab2e-105">說明</span><span class="sxs-lookup"><span data-stu-id="aab2e-105">DESCRIPTION</span></span>
<span data-ttu-id="aab2e-106">**AzApiManagementAuthorizationServer** Cmdlet 會修改 Azure API 管理授權伺服器的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="aab2e-106">The **Set-AzApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="aab2e-107">示例</span><span class="sxs-lookup"><span data-stu-id="aab2e-107">EXAMPLES</span></span>

### <span data-ttu-id="aab2e-108">範例1：修改授權伺服器</span><span class="sxs-lookup"><span data-stu-id="aab2e-108">Example 1: Modify an authorization server</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="aab2e-109">這個命令會修改指定的 API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="aab2e-109">This command modifies the specified API Management authorization server.</span></span>

### <span data-ttu-id="aab2e-110">範例2</span><span class="sxs-lookup"><span data-stu-id="aab2e-110">Example 2</span></span>

<span data-ttu-id="aab2e-111">修改授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="aab2e-111">Modifies an authorization server.</span></span> <span data-ttu-id="aab2e-112"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="aab2e-112">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementAuthorizationServer -AccessTokenSendingMethods AuthorizationHeader -AuthorizationEndpointUrl 'https://contoso/authv2' -AuthorizationRequestMethods Get -ClientAuthenticationMethods Basic -ClientId 'clientid' -ClientRegistrationPageUrl 'https://contoso/signupv2' -ClientSecret '0000000000000000000000000000000000000' -Context <PsApiManagementContext> -DefaultScope <String> -GrantTypes AuthorizationCode -Name 'Contoso OAuth2 server' -ServerId 0123456789 -TokenEndpointUrl 'https://contoso/tokenv2'
```

## <span data-ttu-id="aab2e-113">參數</span><span class="sxs-lookup"><span data-stu-id="aab2e-113">PARAMETERS</span></span>

### <span data-ttu-id="aab2e-114">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="aab2e-114">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="aab2e-115">指定一組方法來傳送存取權杖。</span><span class="sxs-lookup"><span data-stu-id="aab2e-115">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="aab2e-116">psdx_paramvalues AuthorizationHeader 和 Query。</span><span class="sxs-lookup"><span data-stu-id="aab2e-116">psdx_paramvalues AuthorizationHeader and Query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aab2e-117">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="aab2e-117">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="aab2e-118">指定授權端點以驗證資源擁有者，並取得授權贈與。</span><span class="sxs-lookup"><span data-stu-id="aab2e-118">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="aab2e-119">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="aab2e-119">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="aab2e-120">指定授權要求方法的陣列。</span><span class="sxs-lookup"><span data-stu-id="aab2e-120">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="aab2e-121">psdx_paramvalues 取得與張貼。</span><span class="sxs-lookup"><span data-stu-id="aab2e-121">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="aab2e-122">預設值為 [取得]。</span><span class="sxs-lookup"><span data-stu-id="aab2e-122">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Get, Post, Head, Options, Trace, Put, Patch, Delete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aab2e-123">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="aab2e-123">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="aab2e-124">指定用戶端驗證方法的陣列。</span><span class="sxs-lookup"><span data-stu-id="aab2e-124">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="aab2e-125">psdx_paramvalues 基本與主體。</span><span class="sxs-lookup"><span data-stu-id="aab2e-125">psdx_paramvalues Basic and Body.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aab2e-126">-ClientId</span><span class="sxs-lookup"><span data-stu-id="aab2e-126">-ClientId</span></span>
<span data-ttu-id="aab2e-127">指定作為用戶端應用程式之開發人員主控台的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="aab2e-127">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="aab2e-128">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="aab2e-128">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="aab2e-129">指定用戶端註冊端點，以授權伺服器註冊用戶端並取得用戶端認證。</span><span class="sxs-lookup"><span data-stu-id="aab2e-129">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="aab2e-130">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="aab2e-130">-ClientSecret</span></span>
<span data-ttu-id="aab2e-131">指定作為用戶端應用程式的開發人員主控台用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="aab2e-131">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="aab2e-132">-內容</span><span class="sxs-lookup"><span data-stu-id="aab2e-132">-Context</span></span>
<span data-ttu-id="aab2e-133">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="aab2e-133">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="aab2e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab2e-134">-DefaultProfile</span></span>
<span data-ttu-id="aab2e-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aab2e-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aab2e-136">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="aab2e-136">-DefaultScope</span></span>
<span data-ttu-id="aab2e-137">指定授權伺服器的預設範圍。</span><span class="sxs-lookup"><span data-stu-id="aab2e-137">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="aab2e-138">-描述</span><span class="sxs-lookup"><span data-stu-id="aab2e-138">-Description</span></span>
<span data-ttu-id="aab2e-139">指定授權伺服器的描述。</span><span class="sxs-lookup"><span data-stu-id="aab2e-139">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="aab2e-140">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="aab2e-140">-GrantTypes</span></span>
<span data-ttu-id="aab2e-141">指定授與類型的陣列。</span><span class="sxs-lookup"><span data-stu-id="aab2e-141">Specifies an array of grant types.</span></span>
<span data-ttu-id="aab2e-142">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="aab2e-142">psdx_paramvalues</span></span>
- <span data-ttu-id="aab2e-143">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="aab2e-143">AuthorizationCode</span></span>
- <span data-ttu-id="aab2e-144">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="aab2e-144">ClientCredentials</span></span> 
- <span data-ttu-id="aab2e-145">續</span><span class="sxs-lookup"><span data-stu-id="aab2e-145">Implicit</span></span> 
- <span data-ttu-id="aab2e-146">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="aab2e-146">ResourceOwnerPassword</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aab2e-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="aab2e-147">-Name</span></span>
<span data-ttu-id="aab2e-148">指定要修改的授權伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="aab2e-148">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="aab2e-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aab2e-149">-PassThru</span></span>
<span data-ttu-id="aab2e-150">passthru</span><span class="sxs-lookup"><span data-stu-id="aab2e-150">passthru</span></span>

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

### <span data-ttu-id="aab2e-151">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="aab2e-151">-ResourceOwnerPassword</span></span>
<span data-ttu-id="aab2e-152">指定資源擁有者密碼。</span><span class="sxs-lookup"><span data-stu-id="aab2e-152">Specifies the resource owner password.</span></span>
<span data-ttu-id="aab2e-153">如果 ResourceOwnerPassword 是由 *GrantTypes* 參數指定，則您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="aab2e-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="aab2e-154">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="aab2e-154">-ResourceOwnerUsername</span></span>
<span data-ttu-id="aab2e-155">指定資源擁有者的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="aab2e-155">Specifies the resource owner user name.</span></span>
<span data-ttu-id="aab2e-156">如果 ResourceOwnerPassword 是由 *GrantTypes* 參數指定，則您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="aab2e-156">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="aab2e-157">-ServerId</span><span class="sxs-lookup"><span data-stu-id="aab2e-157">-ServerId</span></span>
<span data-ttu-id="aab2e-158">指定要修改的授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="aab2e-158">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="aab2e-159">-SupportState</span><span class="sxs-lookup"><span data-stu-id="aab2e-159">-SupportState</span></span>
<span data-ttu-id="aab2e-160">指示是否支援 *State* 參數。</span><span class="sxs-lookup"><span data-stu-id="aab2e-160">Indicates whether to support the *State* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aab2e-161">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="aab2e-161">-TokenBodyParameters</span></span>
<span data-ttu-id="aab2e-162">使用應用程式/x-www 格式 urlencoded 格式指定其他主體參數。</span><span class="sxs-lookup"><span data-stu-id="aab2e-162">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aab2e-163">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="aab2e-163">-TokenEndpointUrl</span></span>
<span data-ttu-id="aab2e-164">指定用戶端的權杖端點，以取得 exchange 中提供的存取權杖，以呈現授權授權或重新整理權杖。</span><span class="sxs-lookup"><span data-stu-id="aab2e-164">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="aab2e-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab2e-165">CommonParameters</span></span>
<span data-ttu-id="aab2e-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aab2e-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab2e-167">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="aab2e-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab2e-168">輸入</span><span class="sxs-lookup"><span data-stu-id="aab2e-168">INPUTS</span></span>

### <span data-ttu-id="aab2e-169">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="aab2e-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aab2e-170">System.object</span><span class="sxs-lookup"><span data-stu-id="aab2e-170">System.String</span></span>

### <span data-ttu-id="aab2e-171">PsApiManagementAuthorizationRequestMethod []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="aab2e-171">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="aab2e-172">PsApiManagementGrantType []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="aab2e-172">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="aab2e-173">PsApiManagementClientAuthenticationMethod []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="aab2e-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="aab2e-174">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="aab2e-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="aab2e-175">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="aab2e-175">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="aab2e-176">PsApiManagementAccessTokenSendingMethod []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="aab2e-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

### <span data-ttu-id="aab2e-177">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="aab2e-177">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aab2e-178">輸出</span><span class="sxs-lookup"><span data-stu-id="aab2e-178">OUTPUTS</span></span>

### <span data-ttu-id="aab2e-179">ServiceManagement. PsApiManagementOAuth2AuthorizationServer （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="aab2e-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="aab2e-180">筆記</span><span class="sxs-lookup"><span data-stu-id="aab2e-180">NOTES</span></span>

## <span data-ttu-id="aab2e-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="aab2e-181">RELATED LINKS</span></span>

[<span data-ttu-id="aab2e-182">AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="aab2e-182">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="aab2e-183">新-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="aab2e-183">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="aab2e-184">移除-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="aab2e-184">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

