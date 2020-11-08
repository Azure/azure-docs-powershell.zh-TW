---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: bfb074fe53afe2c3eb9d8a69580c817116cb9cd1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970004"
---
# <span data-ttu-id="34145-101">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="34145-101">New-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="34145-102">摘要</span><span class="sxs-lookup"><span data-stu-id="34145-102">SYNOPSIS</span></span>
<span data-ttu-id="34145-103">建立授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="34145-103">Creates an authorization server.</span></span>

## <span data-ttu-id="34145-104">句法</span><span class="sxs-lookup"><span data-stu-id="34145-104">SYNTAX</span></span>

```
New-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>] -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34145-105">說明</span><span class="sxs-lookup"><span data-stu-id="34145-105">DESCRIPTION</span></span>
<span data-ttu-id="34145-106">**新的-AzApiManagementAuthorizationServer** Cmdlet 會建立 Azure API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="34145-106">The **New-AzApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="34145-107">示例</span><span class="sxs-lookup"><span data-stu-id="34145-107">EXAMPLES</span></span>

### <span data-ttu-id="34145-108">範例1：建立授權伺服器</span><span class="sxs-lookup"><span data-stu-id="34145-108">Example 1: Create an authorization server</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="34145-109">這個命令會建立授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="34145-109">This command creates an authorization server.</span></span>

### <span data-ttu-id="34145-110">範例2</span><span class="sxs-lookup"><span data-stu-id="34145-110">Example 2</span></span>

<span data-ttu-id="34145-111">建立授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="34145-111">Creates an authorization server.</span></span> <span data-ttu-id="34145-112"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="34145-112">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementAuthorizationServer -AccessTokenSendingMethods AuthorizationHeader -AuthorizationEndpointUrl 'https://contoso/auth' -AuthorizationRequestMethods Get -ClientAuthenticationMethods Basic -ClientId 'clientid' -ClientRegistrationPageUrl 'https://contoso/signup' -ClientSecret '0000000000000000000000000000000000000' -Context <PsApiManagementContext> -GrantTypes AuthorizationCode -Name 'Contoso OAuth2 server' -ServerId '0123456789' -TokenBodyParameters @{'par1'='val1'} -TokenEndpointUrl 'https://contoso/token'
```

## <span data-ttu-id="34145-113">參數</span><span class="sxs-lookup"><span data-stu-id="34145-113">PARAMETERS</span></span>

### <span data-ttu-id="34145-114">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="34145-114">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="34145-115">指定一組方法來傳送存取權杖。</span><span class="sxs-lookup"><span data-stu-id="34145-115">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="34145-116">psdx_paramvalues AuthorizationHeader 和 Query。</span><span class="sxs-lookup"><span data-stu-id="34145-116">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="34145-117">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="34145-117">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="34145-118">指定授權端點以驗證資源擁有者，並取得授權贈與。</span><span class="sxs-lookup"><span data-stu-id="34145-118">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="34145-119">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="34145-119">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="34145-120">指定授權要求方法的陣列。</span><span class="sxs-lookup"><span data-stu-id="34145-120">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="34145-121">有效值為： [取得]、[張貼]。</span><span class="sxs-lookup"><span data-stu-id="34145-121">Valid values are: GET, POST.</span></span>
<span data-ttu-id="34145-122">預設值為 [取得]。</span><span class="sxs-lookup"><span data-stu-id="34145-122">The default value is GET.</span></span>

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

### <span data-ttu-id="34145-123">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="34145-123">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="34145-124">指定用戶端驗證方法的陣列。</span><span class="sxs-lookup"><span data-stu-id="34145-124">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="34145-125">psdx_paramvalues 基本與主體。</span><span class="sxs-lookup"><span data-stu-id="34145-125">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="34145-126">-ClientId</span><span class="sxs-lookup"><span data-stu-id="34145-126">-ClientId</span></span>
<span data-ttu-id="34145-127">指定作為用戶端應用程式之開發人員主控台的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="34145-127">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="34145-128">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="34145-128">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="34145-129">指定用戶端註冊端點，以授權伺服器註冊用戶端並取得用戶端認證。</span><span class="sxs-lookup"><span data-stu-id="34145-129">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="34145-130">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="34145-130">-ClientSecret</span></span>
<span data-ttu-id="34145-131">指定作為用戶端應用程式的開發人員主控台用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="34145-131">Specifies the client secret of developer console that is the client application.</span></span>

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

### <span data-ttu-id="34145-132">-內容</span><span class="sxs-lookup"><span data-stu-id="34145-132">-Context</span></span>
<span data-ttu-id="34145-133">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="34145-133">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="34145-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34145-134">-DefaultProfile</span></span>
<span data-ttu-id="34145-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="34145-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34145-136">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="34145-136">-DefaultScope</span></span>
<span data-ttu-id="34145-137">指定授權伺服器的預設範圍。</span><span class="sxs-lookup"><span data-stu-id="34145-137">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="34145-138">-描述</span><span class="sxs-lookup"><span data-stu-id="34145-138">-Description</span></span>
<span data-ttu-id="34145-139">指定授權伺服器的描述。</span><span class="sxs-lookup"><span data-stu-id="34145-139">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="34145-140">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="34145-140">-GrantTypes</span></span>
<span data-ttu-id="34145-141">指定授與類型的陣列。</span><span class="sxs-lookup"><span data-stu-id="34145-141">Specifies an array of grant types.</span></span>
<span data-ttu-id="34145-142">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="34145-142">psdx_paramvalues</span></span>
- <span data-ttu-id="34145-143">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="34145-143">AuthorizationCode</span></span>
- <span data-ttu-id="34145-144">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="34145-144">ClientCredentials</span></span> 
- <span data-ttu-id="34145-145">續</span><span class="sxs-lookup"><span data-stu-id="34145-145">Implicit</span></span> 
- <span data-ttu-id="34145-146">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="34145-146">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="34145-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="34145-147">-Name</span></span>
<span data-ttu-id="34145-148">指定要建立的授權伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="34145-148">Specifies the name of the authorization server to create.</span></span>

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

### <span data-ttu-id="34145-149">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="34145-149">-ResourceOwnerPassword</span></span>
<span data-ttu-id="34145-150">指定資源擁有者密碼。</span><span class="sxs-lookup"><span data-stu-id="34145-150">Specifies the resource owner password.</span></span>
<span data-ttu-id="34145-151">如果 ResourceOwnerPassword 是由 *GrantTypes* 參數指定，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="34145-151">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="34145-152">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="34145-152">-ResourceOwnerUsername</span></span>
<span data-ttu-id="34145-153">指定資源擁有者的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="34145-153">Specifies the resource owner user name.</span></span>
<span data-ttu-id="34145-154">如果 ResourceOwnerPassword 是由 *GrantTypes* 參數指定，則您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="34145-154">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="34145-155">-ServerId</span><span class="sxs-lookup"><span data-stu-id="34145-155">-ServerId</span></span>
<span data-ttu-id="34145-156">指定要建立的授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="34145-156">Specifies the ID of the authorization server to create.</span></span>

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

### <span data-ttu-id="34145-157">-SupportState</span><span class="sxs-lookup"><span data-stu-id="34145-157">-SupportState</span></span>
<span data-ttu-id="34145-158">指示是否支援 *State* 參數。</span><span class="sxs-lookup"><span data-stu-id="34145-158">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="34145-159">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="34145-159">-TokenBodyParameters</span></span>
<span data-ttu-id="34145-160">使用 **應用程式/x-www 格式 urlencoded** 格式指定其他主體參數。</span><span class="sxs-lookup"><span data-stu-id="34145-160">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

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

### <span data-ttu-id="34145-161">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="34145-161">-TokenEndpointUrl</span></span>
<span data-ttu-id="34145-162">指定用戶端用來在 exchange 中取得存取權杖的權杖端點 URL，以呈現授權授權或重新整理權杖。</span><span class="sxs-lookup"><span data-stu-id="34145-162">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="34145-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34145-163">CommonParameters</span></span>
<span data-ttu-id="34145-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="34145-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34145-165">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="34145-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34145-166">輸入</span><span class="sxs-lookup"><span data-stu-id="34145-166">INPUTS</span></span>

### <span data-ttu-id="34145-167">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="34145-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="34145-168">System.object</span><span class="sxs-lookup"><span data-stu-id="34145-168">System.String</span></span>

### <span data-ttu-id="34145-169">PsApiManagementAuthorizationRequestMethod []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="34145-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="34145-170">PsApiManagementGrantType []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="34145-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="34145-171">PsApiManagementClientAuthenticationMethod []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="34145-171">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="34145-172">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="34145-172">System.Collections.Hashtable</span></span>

### <span data-ttu-id="34145-173">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="34145-173">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="34145-174">PsApiManagementAccessTokenSendingMethod []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="34145-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

## <span data-ttu-id="34145-175">輸出</span><span class="sxs-lookup"><span data-stu-id="34145-175">OUTPUTS</span></span>

### <span data-ttu-id="34145-176">ServiceManagement. PsApiManagementOAuth2AuthorizationServer （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="34145-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="34145-177">筆記</span><span class="sxs-lookup"><span data-stu-id="34145-177">NOTES</span></span>

## <span data-ttu-id="34145-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="34145-178">RELATED LINKS</span></span>