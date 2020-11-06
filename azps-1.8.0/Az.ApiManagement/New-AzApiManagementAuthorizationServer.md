---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: b09ea243dac2952cc4ec630755537a0e3cc5a745
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611587"
---
# <span data-ttu-id="87b09-101">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="87b09-101">New-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="87b09-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87b09-102">SYNOPSIS</span></span>
<span data-ttu-id="87b09-103">建立授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="87b09-103">Creates an authorization server.</span></span>

## <span data-ttu-id="87b09-104">句法</span><span class="sxs-lookup"><span data-stu-id="87b09-104">SYNTAX</span></span>

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

## <span data-ttu-id="87b09-105">說明</span><span class="sxs-lookup"><span data-stu-id="87b09-105">DESCRIPTION</span></span>
<span data-ttu-id="87b09-106">**新的-AzApiManagementAuthorizationServer** Cmdlet 會建立 Azure API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="87b09-106">The **New-AzApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="87b09-107">示例</span><span class="sxs-lookup"><span data-stu-id="87b09-107">EXAMPLES</span></span>

### <span data-ttu-id="87b09-108">範例1：建立授權伺服器</span><span class="sxs-lookup"><span data-stu-id="87b09-108">Example 1: Create an authorization server</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementAuthrizarionServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="87b09-109">這個命令會建立授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="87b09-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="87b09-110">參數</span><span class="sxs-lookup"><span data-stu-id="87b09-110">PARAMETERS</span></span>

### <span data-ttu-id="87b09-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="87b09-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="87b09-112">指定一組方法來傳送存取權杖。</span><span class="sxs-lookup"><span data-stu-id="87b09-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="87b09-113">psdx_paramvalues AuthorizationHeader 和 Query。</span><span class="sxs-lookup"><span data-stu-id="87b09-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="87b09-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="87b09-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="87b09-115">指定授權端點以驗證資源擁有者，並取得授權贈與。</span><span class="sxs-lookup"><span data-stu-id="87b09-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="87b09-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="87b09-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="87b09-117">指定授權要求方法的陣列。</span><span class="sxs-lookup"><span data-stu-id="87b09-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="87b09-118">有效值為： [取得]、[張貼]。</span><span class="sxs-lookup"><span data-stu-id="87b09-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="87b09-119">預設值為 [取得]。</span><span class="sxs-lookup"><span data-stu-id="87b09-119">The default value is GET.</span></span>

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

### <span data-ttu-id="87b09-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="87b09-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="87b09-121">指定用戶端驗證方法的陣列。</span><span class="sxs-lookup"><span data-stu-id="87b09-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="87b09-122">psdx_paramvalues 基本與主體。</span><span class="sxs-lookup"><span data-stu-id="87b09-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="87b09-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="87b09-123">-ClientId</span></span>
<span data-ttu-id="87b09-124">指定作為用戶端應用程式之開發人員主控台的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="87b09-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="87b09-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="87b09-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="87b09-126">指定用戶端註冊端點，以授權伺服器註冊用戶端並取得用戶端認證。</span><span class="sxs-lookup"><span data-stu-id="87b09-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="87b09-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="87b09-127">-ClientSecret</span></span>
<span data-ttu-id="87b09-128">指定作為用戶端應用程式的開發人員主控台用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="87b09-128">Specifies the client secret of developer console that is the client application.</span></span>

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

### <span data-ttu-id="87b09-129">-內容</span><span class="sxs-lookup"><span data-stu-id="87b09-129">-Context</span></span>
<span data-ttu-id="87b09-130">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="87b09-130">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87b09-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b09-131">-DefaultProfile</span></span>
<span data-ttu-id="87b09-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="87b09-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87b09-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="87b09-133">-DefaultScope</span></span>
<span data-ttu-id="87b09-134">指定授權伺服器的預設範圍。</span><span class="sxs-lookup"><span data-stu-id="87b09-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="87b09-135">-描述</span><span class="sxs-lookup"><span data-stu-id="87b09-135">-Description</span></span>
<span data-ttu-id="87b09-136">指定授權伺服器的描述。</span><span class="sxs-lookup"><span data-stu-id="87b09-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="87b09-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="87b09-137">-GrantTypes</span></span>
<span data-ttu-id="87b09-138">指定授與類型的陣列。</span><span class="sxs-lookup"><span data-stu-id="87b09-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="87b09-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="87b09-139">psdx_paramvalues</span></span>
- <span data-ttu-id="87b09-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="87b09-140">AuthorizationCode</span></span>
- <span data-ttu-id="87b09-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="87b09-141">ClientCredentials</span></span> 
- <span data-ttu-id="87b09-142">續</span><span class="sxs-lookup"><span data-stu-id="87b09-142">Implicit</span></span> 
- <span data-ttu-id="87b09-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="87b09-143">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="87b09-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="87b09-144">-Name</span></span>
<span data-ttu-id="87b09-145">指定要建立的授權伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="87b09-145">Specifies the name of the authorization server to create.</span></span>

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

### <span data-ttu-id="87b09-146">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="87b09-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="87b09-147">指定資源擁有者密碼。</span><span class="sxs-lookup"><span data-stu-id="87b09-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="87b09-148">如果 ResourceOwnerPassword 是由 *GrantTypes* 參數指定，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="87b09-148">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="87b09-149">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="87b09-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="87b09-150">指定資源擁有者的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="87b09-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="87b09-151">如果 ResourceOwnerPassword 是由 *GrantTypes* 參數指定，則您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="87b09-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="87b09-152">-ServerId</span><span class="sxs-lookup"><span data-stu-id="87b09-152">-ServerId</span></span>
<span data-ttu-id="87b09-153">指定要建立的授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="87b09-153">Specifies the ID of the authorization server to create.</span></span>

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

### <span data-ttu-id="87b09-154">-SupportState</span><span class="sxs-lookup"><span data-stu-id="87b09-154">-SupportState</span></span>
<span data-ttu-id="87b09-155">指示是否支援 *State* 參數。</span><span class="sxs-lookup"><span data-stu-id="87b09-155">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="87b09-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="87b09-156">-TokenBodyParameters</span></span>
<span data-ttu-id="87b09-157">使用 **應用程式/x-www 格式 urlencoded** 格式指定其他主體參數。</span><span class="sxs-lookup"><span data-stu-id="87b09-157">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

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

### <span data-ttu-id="87b09-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="87b09-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="87b09-159">指定用戶端用來在 exchange 中取得存取權杖的權杖端點 URL，以呈現授權授權或重新整理權杖。</span><span class="sxs-lookup"><span data-stu-id="87b09-159">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="87b09-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b09-160">CommonParameters</span></span>
<span data-ttu-id="87b09-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87b09-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b09-162">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87b09-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b09-163">輸入</span><span class="sxs-lookup"><span data-stu-id="87b09-163">INPUTS</span></span>

### <span data-ttu-id="87b09-164">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="87b09-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="87b09-165">System.object</span><span class="sxs-lookup"><span data-stu-id="87b09-165">System.String</span></span>

### <span data-ttu-id="87b09-166">PsApiManagementAuthorizationRequestMethod []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="87b09-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="87b09-167">PsApiManagementGrantType []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="87b09-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="87b09-168">PsApiManagementClientAuthenticationMethod []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="87b09-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="87b09-169">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="87b09-169">System.Collections.Hashtable</span></span>

### <span data-ttu-id="87b09-170">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="87b09-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="87b09-171">PsApiManagementAccessTokenSendingMethod []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="87b09-171">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

## <span data-ttu-id="87b09-172">輸出</span><span class="sxs-lookup"><span data-stu-id="87b09-172">OUTPUTS</span></span>

### <span data-ttu-id="87b09-173">ServiceManagement. PsApiManagementOAuth2AuthrozationServer （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="87b09-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="87b09-174">筆記</span><span class="sxs-lookup"><span data-stu-id="87b09-174">NOTES</span></span>

## <span data-ttu-id="87b09-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="87b09-175">RELATED LINKS</span></span>
