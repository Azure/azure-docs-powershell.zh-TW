---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 6424ad453d7e2ee3c4933127cc58e6d3e1193e76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454776"
---
# <span data-ttu-id="b26fa-101">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b26fa-101">Set-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="b26fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b26fa-102">SYNOPSIS</span></span>
<span data-ttu-id="b26fa-103">修改授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="b26fa-103">Modifies an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b26fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="b26fa-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b26fa-105">說明</span><span class="sxs-lookup"><span data-stu-id="b26fa-105">DESCRIPTION</span></span>
<span data-ttu-id="b26fa-106">**AzureRmApiManagementAuthorizationServer** Cmdlet 會修改 Azure API 管理授權伺服器的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b26fa-106">The **Set-AzureRmApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="b26fa-107">示例</span><span class="sxs-lookup"><span data-stu-id="b26fa-107">EXAMPLES</span></span>

### <span data-ttu-id="b26fa-108">範例1：修改授權伺服器</span><span class="sxs-lookup"><span data-stu-id="b26fa-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="b26fa-109">這個命令會修改指定的 API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="b26fa-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="b26fa-110">參數</span><span class="sxs-lookup"><span data-stu-id="b26fa-110">PARAMETERS</span></span>

### <span data-ttu-id="b26fa-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="b26fa-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="b26fa-112">指定一組方法來傳送存取權杖。</span><span class="sxs-lookup"><span data-stu-id="b26fa-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="b26fa-113">psdx_paramvalues AuthorizationHeader 和 Query。</span><span class="sxs-lookup"><span data-stu-id="b26fa-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="b26fa-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="b26fa-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="b26fa-115">指定授權端點以驗證資源擁有者，並取得授權贈與。</span><span class="sxs-lookup"><span data-stu-id="b26fa-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="b26fa-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="b26fa-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="b26fa-117">指定授權要求方法的陣列。</span><span class="sxs-lookup"><span data-stu-id="b26fa-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="b26fa-118">psdx_paramvalues 取得與張貼。</span><span class="sxs-lookup"><span data-stu-id="b26fa-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="b26fa-119">預設值為 [取得]。</span><span class="sxs-lookup"><span data-stu-id="b26fa-119">The default value is GET.</span></span>

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

### <span data-ttu-id="b26fa-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="b26fa-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="b26fa-121">指定用戶端驗證方法的陣列。</span><span class="sxs-lookup"><span data-stu-id="b26fa-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="b26fa-122">psdx_paramvalues 基本與主體。</span><span class="sxs-lookup"><span data-stu-id="b26fa-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="b26fa-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="b26fa-123">-ClientId</span></span>
<span data-ttu-id="b26fa-124">指定作為用戶端應用程式之開發人員主控台的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="b26fa-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="b26fa-125">-ClientRegistrationPageUrl</span><span class="sxs-lookup"><span data-stu-id="b26fa-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="b26fa-126">指定用戶端註冊端點，以授權伺服器註冊用戶端並取得用戶端認證。</span><span class="sxs-lookup"><span data-stu-id="b26fa-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="b26fa-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="b26fa-127">-ClientSecret</span></span>
<span data-ttu-id="b26fa-128">指定作為用戶端應用程式的開發人員主控台用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="b26fa-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="b26fa-129">-內容</span><span class="sxs-lookup"><span data-stu-id="b26fa-129">-Context</span></span>
<span data-ttu-id="b26fa-130">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="b26fa-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b26fa-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b26fa-131">-DefaultProfile</span></span>
<span data-ttu-id="b26fa-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b26fa-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="b26fa-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="b26fa-133">-DefaultScope</span></span>
<span data-ttu-id="b26fa-134">指定授權伺服器的預設範圍。</span><span class="sxs-lookup"><span data-stu-id="b26fa-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="b26fa-135">-描述</span><span class="sxs-lookup"><span data-stu-id="b26fa-135">-Description</span></span>
<span data-ttu-id="b26fa-136">指定授權伺服器的描述。</span><span class="sxs-lookup"><span data-stu-id="b26fa-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="b26fa-137">-GrantTypes</span><span class="sxs-lookup"><span data-stu-id="b26fa-137">-GrantTypes</span></span>
<span data-ttu-id="b26fa-138">指定授與類型的陣列。</span><span class="sxs-lookup"><span data-stu-id="b26fa-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="b26fa-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="b26fa-139">psdx_paramvalues</span></span>

- <span data-ttu-id="b26fa-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="b26fa-140">AuthorizationCode</span></span>
- <span data-ttu-id="b26fa-141">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="b26fa-141">ClientCredentials</span></span> 
- <span data-ttu-id="b26fa-142">續</span><span class="sxs-lookup"><span data-stu-id="b26fa-142">Implicit</span></span> 
- <span data-ttu-id="b26fa-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="b26fa-143">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="b26fa-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="b26fa-144">-Name</span></span>
<span data-ttu-id="b26fa-145">指定要修改的授權伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b26fa-145">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="b26fa-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b26fa-146">-PassThru</span></span>
<span data-ttu-id="b26fa-147">passthru</span><span class="sxs-lookup"><span data-stu-id="b26fa-147">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b26fa-148">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="b26fa-148">-ResourceOwnerPassword</span></span>
<span data-ttu-id="b26fa-149">指定資源擁有者密碼。</span><span class="sxs-lookup"><span data-stu-id="b26fa-149">Specifies the resource owner password.</span></span>
<span data-ttu-id="b26fa-150">如果 ResourceOwnerPassword 是由 *GrantTypes* 參數指定，則您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="b26fa-150">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="b26fa-151">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="b26fa-151">-ResourceOwnerUsername</span></span>
<span data-ttu-id="b26fa-152">指定資源擁有者的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="b26fa-152">Specifies the resource owner user name.</span></span>
<span data-ttu-id="b26fa-153">如果 ResourceOwnerPassword 是由 *GrantTypes* 參數指定，則您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="b26fa-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="b26fa-154">-ServerId</span><span class="sxs-lookup"><span data-stu-id="b26fa-154">-ServerId</span></span>
<span data-ttu-id="b26fa-155">指定要修改的授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="b26fa-155">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="b26fa-156">-SupportState</span><span class="sxs-lookup"><span data-stu-id="b26fa-156">-SupportState</span></span>
<span data-ttu-id="b26fa-157">指示是否支援 *State* 參數。</span><span class="sxs-lookup"><span data-stu-id="b26fa-157">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="b26fa-158">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="b26fa-158">-TokenBodyParameters</span></span>
<span data-ttu-id="b26fa-159">使用應用程式/x-www 格式 urlencoded 格式指定其他主體參數。</span><span class="sxs-lookup"><span data-stu-id="b26fa-159">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

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

### <span data-ttu-id="b26fa-160">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="b26fa-160">-TokenEndpointUrl</span></span>
<span data-ttu-id="b26fa-161">指定用戶端的權杖端點，以取得 exchange 中提供的存取權杖，以呈現授權授權或重新整理權杖。</span><span class="sxs-lookup"><span data-stu-id="b26fa-161">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="b26fa-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b26fa-162">CommonParameters</span></span>
<span data-ttu-id="b26fa-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b26fa-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b26fa-164">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b26fa-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b26fa-165">輸入</span><span class="sxs-lookup"><span data-stu-id="b26fa-165">INPUTS</span></span>

### <span data-ttu-id="b26fa-166">所有</span><span class="sxs-lookup"><span data-stu-id="b26fa-166">None</span></span>
<span data-ttu-id="b26fa-167">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b26fa-167">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b26fa-168">輸出</span><span class="sxs-lookup"><span data-stu-id="b26fa-168">OUTPUTS</span></span>

### <span data-ttu-id="b26fa-169">ServiceManagement. PsApiManagementOAuth2AuthrozationServer （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="b26fa-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="b26fa-170">筆記</span><span class="sxs-lookup"><span data-stu-id="b26fa-170">NOTES</span></span>

## <span data-ttu-id="b26fa-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="b26fa-171">RELATED LINKS</span></span>

[<span data-ttu-id="b26fa-172">AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b26fa-172">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="b26fa-173">新-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b26fa-173">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="b26fa-174">移除-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b26fa-174">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)


