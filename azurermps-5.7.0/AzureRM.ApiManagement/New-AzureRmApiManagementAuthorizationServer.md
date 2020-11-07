---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: f1853c8f9e1e8449d0b607cadede215ec42b8952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623998"
---
# <span data-ttu-id="87c6a-101">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="87c6a-101">New-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="87c6a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87c6a-102">SYNOPSIS</span></span>
<span data-ttu-id="87c6a-103">建立授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="87c6a-103">Creates an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87c6a-104">句法</span><span class="sxs-lookup"><span data-stu-id="87c6a-104">SYNTAX</span></span>

```
New-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 -Name <String> [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87c6a-105">說明</span><span class="sxs-lookup"><span data-stu-id="87c6a-105">DESCRIPTION</span></span>
<span data-ttu-id="87c6a-106">**新的-AzureRmApiManagementAuthorizationServer** Cmdlet 會建立 Azure API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="87c6a-106">The **New-AzureRmApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="87c6a-107">示例</span><span class="sxs-lookup"><span data-stu-id="87c6a-107">EXAMPLES</span></span>

### <span data-ttu-id="87c6a-108">範例1：建立授權伺服器</span><span class="sxs-lookup"><span data-stu-id="87c6a-108">Example 1: Create an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="87c6a-109">這個命令會建立授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="87c6a-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="87c6a-110">參數</span><span class="sxs-lookup"><span data-stu-id="87c6a-110">PARAMETERS</span></span>

### <span data-ttu-id="87c6a-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="87c6a-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="87c6a-112">指定一組方法來傳送存取權杖。</span><span class="sxs-lookup"><span data-stu-id="87c6a-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="87c6a-113">psdx_paramvalues AuthorizationHeader 和 Query。</span><span class="sxs-lookup"><span data-stu-id="87c6a-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

```yaml
Type: PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="87c6a-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="87c6a-115">指定授權端點以驗證資源擁有者，並取得授權贈與。</span><span class="sxs-lookup"><span data-stu-id="87c6a-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="87c6a-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="87c6a-117">指定授權要求方法的陣列。</span><span class="sxs-lookup"><span data-stu-id="87c6a-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="87c6a-118">有效值為： [取得]、[張貼]。</span><span class="sxs-lookup"><span data-stu-id="87c6a-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="87c6a-119">預設值為 [取得]。</span><span class="sxs-lookup"><span data-stu-id="87c6a-119">The default value is GET.</span></span>

```yaml
Type: PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Get, Post

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="87c6a-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="87c6a-121">指定用戶端驗證方法的陣列。</span><span class="sxs-lookup"><span data-stu-id="87c6a-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="87c6a-122">psdx_paramvalues 基本與主體。</span><span class="sxs-lookup"><span data-stu-id="87c6a-122">psdx_paramvalues Basic and Body.</span></span>

```yaml
Type: PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="87c6a-123">-ClientId</span></span>
<span data-ttu-id="87c6a-124">指定作為用戶端應用程式之開發人員主控台的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="87c6a-124">Specifies the client ID of the developer console that is the client application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="87c6a-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="87c6a-126">指定用戶端註冊端點，以授權伺服器註冊用戶端並取得用戶端認證。</span><span class="sxs-lookup"><span data-stu-id="87c6a-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="87c6a-127">-ClientSecret</span></span>
<span data-ttu-id="87c6a-128">指定作為用戶端應用程式的開發人員主控台用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="87c6a-128">Specifies the client secret of developer console that is the client application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-129">-內容</span><span class="sxs-lookup"><span data-stu-id="87c6a-129">-Context</span></span>
<span data-ttu-id="87c6a-130">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="87c6a-130">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c6a-131">-DefaultProfile</span></span>
<span data-ttu-id="87c6a-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="87c6a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="87c6a-133">-DefaultScope</span></span>
<span data-ttu-id="87c6a-134">指定授權伺服器的預設範圍。</span><span class="sxs-lookup"><span data-stu-id="87c6a-134">Specifies the default scope for the authorization server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-135">-描述</span><span class="sxs-lookup"><span data-stu-id="87c6a-135">-Description</span></span>
<span data-ttu-id="87c6a-136">指定授權伺服器的描述。</span><span class="sxs-lookup"><span data-stu-id="87c6a-136">Specifies a description for an authorization server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="87c6a-137">-GrantTypes</span></span>
<span data-ttu-id="87c6a-138">指定授與類型的陣列。</span><span class="sxs-lookup"><span data-stu-id="87c6a-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="87c6a-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="87c6a-139">psdx_paramvalues</span></span>

- <span data-ttu-id="87c6a-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="87c6a-140">AuthorizationCode</span></span>
- <span data-ttu-id="87c6a-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="87c6a-141">ClientCredentials</span></span> 
- <span data-ttu-id="87c6a-142">續</span><span class="sxs-lookup"><span data-stu-id="87c6a-142">Implicit</span></span> 
- <span data-ttu-id="87c6a-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="87c6a-143">ResourceOwnerPassword</span></span>

```yaml
Type: PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases: 
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="87c6a-144">-Name</span></span>
<span data-ttu-id="87c6a-145">指定要建立的授權伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="87c6a-145">Specifies the name of the authorization server to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-146">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="87c6a-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="87c6a-147">指定資源擁有者密碼。</span><span class="sxs-lookup"><span data-stu-id="87c6a-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="87c6a-148">如果 ResourceOwnerPassword 是由 *GrantTypes* 參數指定，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="87c6a-148">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-149">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="87c6a-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="87c6a-150">指定資源擁有者的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="87c6a-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="87c6a-151">如果 ResourceOwnerPassword 是由 *GrantTypes* 參數指定，則您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="87c6a-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-152">-ServerId</span><span class="sxs-lookup"><span data-stu-id="87c6a-152">-ServerId</span></span>
<span data-ttu-id="87c6a-153">指定要建立的授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="87c6a-153">Specifies the ID of the authorization server to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-154">-SupportState</span><span class="sxs-lookup"><span data-stu-id="87c6a-154">-SupportState</span></span>
<span data-ttu-id="87c6a-155">指示是否支援 *State* 參數。</span><span class="sxs-lookup"><span data-stu-id="87c6a-155">Indicates whether to support the *State* parameter.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="87c6a-156">-TokenBodyParameters</span></span>
<span data-ttu-id="87c6a-157">使用 **應用程式/x-www 格式 urlencoded** 格式指定其他主體參數。</span><span class="sxs-lookup"><span data-stu-id="87c6a-157">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="87c6a-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="87c6a-159">指定用戶端用來在 exchange 中取得存取權杖的權杖端點 URL，以呈現授權授權或重新整理權杖。</span><span class="sxs-lookup"><span data-stu-id="87c6a-159">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c6a-160">CommonParameters</span></span>
<span data-ttu-id="87c6a-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87c6a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c6a-162">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87c6a-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c6a-163">輸入</span><span class="sxs-lookup"><span data-stu-id="87c6a-163">INPUTS</span></span>

### <span data-ttu-id="87c6a-164">所有</span><span class="sxs-lookup"><span data-stu-id="87c6a-164">None</span></span>
<span data-ttu-id="87c6a-165">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="87c6a-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="87c6a-166">輸出</span><span class="sxs-lookup"><span data-stu-id="87c6a-166">OUTPUTS</span></span>

### <span data-ttu-id="87c6a-167">ServiceManagement. PsApiManagementOAuth2AuthrozationServer （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="87c6a-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="87c6a-168">筆記</span><span class="sxs-lookup"><span data-stu-id="87c6a-168">NOTES</span></span>

## <span data-ttu-id="87c6a-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="87c6a-169">RELATED LINKS</span></span>

