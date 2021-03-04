---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: cdef3f217cec1401457f2f25daa91edafd4850b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917121"
---
# <span data-ttu-id="bf17d-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bf17d-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="bf17d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bf17d-102">SYNOPSIS</span></span>
<span data-ttu-id="bf17d-103">修改 API。</span><span class="sxs-lookup"><span data-stu-id="bf17d-103">Modifies an API.</span></span>

## <span data-ttu-id="bf17d-104">語法</span><span class="sxs-lookup"><span data-stu-id="bf17d-104">SYNTAX</span></span>

### <span data-ttu-id="bf17d-105">展開Parameter (預設) </span><span class="sxs-lookup"><span data-stu-id="bf17d-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf17d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bf17d-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf17d-107">描述</span><span class="sxs-lookup"><span data-stu-id="bf17d-107">DESCRIPTION</span></span>
<span data-ttu-id="bf17d-108">**Set-AzApiManagementApi** Cmdlet 會修改 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="bf17d-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="bf17d-109">例子</span><span class="sxs-lookup"><span data-stu-id="bf17d-109">EXAMPLES</span></span>

### <span data-ttu-id="bf17d-110">範例 1：修改 API</span><span class="sxs-lookup"><span data-stu-id="bf17d-110">Example 1: Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="bf17d-111">範例 2：新增 API 至現有的 ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="bf17d-111">Example 2: Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="bf17d-112">此範例會新增 API 至現有的 API 版本集</span><span class="sxs-lookup"><span data-stu-id="bf17d-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="bf17d-113">範例 3：變更 API 指向的後端 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="bf17d-113">Example 3: Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="bf17d-114">此範例會更新指向的 `echo-api` ServiceUrl。</span><span class="sxs-lookup"><span data-stu-id="bf17d-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="bf17d-115">參數</span><span class="sxs-lookup"><span data-stu-id="bf17d-115">PARAMETERS</span></span>

### <span data-ttu-id="bf17d-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bf17d-116">-ApiId</span></span>
<span data-ttu-id="bf17d-117">指定要修改的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf17d-117">Specifies the ID of the API to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf17d-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="bf17d-118">-AuthorizationScope</span></span>
<span data-ttu-id="bf17d-119">指定 OAuth 作業範圍。</span><span class="sxs-lookup"><span data-stu-id="bf17d-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="bf17d-120">預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="bf17d-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="bf17d-121">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="bf17d-121">-AuthorizationServerId</span></span>
<span data-ttu-id="bf17d-122">指定 OAuth 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf17d-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="bf17d-123">預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="bf17d-123">The default value is $Null.</span></span>
<span data-ttu-id="bf17d-124">如果已指定 *AuthorizationScope，則必須* 指定此參數。</span><span class="sxs-lookup"><span data-stu-id="bf17d-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="bf17d-125">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="bf17d-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="bf17d-126">將存取權杖傳遞至 API 的 OpenId 授權伺服器機制。</span><span class="sxs-lookup"><span data-stu-id="bf17d-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="bf17d-127">參照 http://tools.ietf.org/html/rfc6749#section-4 到 。</span><span class="sxs-lookup"><span data-stu-id="bf17d-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="bf17d-128">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="bf17d-128">This parameter is optional.</span></span> <span data-ttu-id="bf17d-129">預設值會$null。</span><span class="sxs-lookup"><span data-stu-id="bf17d-129">Default value is $null.</span></span>

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

### <span data-ttu-id="bf17d-130">-內容</span><span class="sxs-lookup"><span data-stu-id="bf17d-130">-Context</span></span>
<span data-ttu-id="bf17d-131">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="bf17d-131">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bf17d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf17d-132">-DefaultProfile</span></span>
<span data-ttu-id="bf17d-133">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf17d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf17d-134">-描述</span><span class="sxs-lookup"><span data-stu-id="bf17d-134">-Description</span></span>
<span data-ttu-id="bf17d-135">指定網頁 API 的描述。</span><span class="sxs-lookup"><span data-stu-id="bf17d-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="bf17d-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf17d-136">-InputObject</span></span>
<span data-ttu-id="bf17d-137">PsApiManagementApi 實例。</span><span class="sxs-lookup"><span data-stu-id="bf17d-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="bf17d-138">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="bf17d-138">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf17d-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="bf17d-139">-Name</span></span>
<span data-ttu-id="bf17d-140">指定 Web API 的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf17d-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="bf17d-141">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="bf17d-141">-OpenIdProviderId</span></span>
<span data-ttu-id="bf17d-142">OpenId 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf17d-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="bf17d-143">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="bf17d-143">This parameter is optional.</span></span> <span data-ttu-id="bf17d-144">預設值會$null。</span><span class="sxs-lookup"><span data-stu-id="bf17d-144">Default value is $null.</span></span> <span data-ttu-id="bf17d-145">必須指定已指定 BearerTokenSendingMethods。</span><span class="sxs-lookup"><span data-stu-id="bf17d-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="bf17d-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf17d-146">-PassThru</span></span>
<span data-ttu-id="bf17d-147">Passthru</span><span class="sxs-lookup"><span data-stu-id="bf17d-147">passthru</span></span>

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

### <span data-ttu-id="bf17d-148">-路徑</span><span class="sxs-lookup"><span data-stu-id="bf17d-148">-Path</span></span>
<span data-ttu-id="bf17d-149">指定 Web API 路徑，這是 API 公用 URL 的最後一部分。</span><span class="sxs-lookup"><span data-stu-id="bf17d-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="bf17d-150">API 消費者會使用這個 URL 來傳送要求到 Web 服務，而且必須長 1 到 400 個字元。</span><span class="sxs-lookup"><span data-stu-id="bf17d-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="bf17d-151">預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="bf17d-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="bf17d-152">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="bf17d-152">-Protocols</span></span>
<span data-ttu-id="bf17d-153">指定 Web API 通訊協定陣列。</span><span class="sxs-lookup"><span data-stu-id="bf17d-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="bf17d-154">psdx_paramvalues HTTP 和 HTTPs。</span><span class="sxs-lookup"><span data-stu-id="bf17d-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="bf17d-155">這些是提供 API 的 Web 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="bf17d-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="bf17d-156">預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="bf17d-156">The default value is $Null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf17d-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="bf17d-157">-ServiceUrl</span></span>
<span data-ttu-id="bf17d-158">指定公開 API 的 Web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="bf17d-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="bf17d-159">此 URL 僅由 Azure API 管理使用，不會公開。</span><span class="sxs-lookup"><span data-stu-id="bf17d-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="bf17d-160">URL 必須長 1 到 2000 個字元。</span><span class="sxs-lookup"><span data-stu-id="bf17d-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="bf17d-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="bf17d-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="bf17d-162">指定訂閱金鑰標題的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf17d-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="bf17d-163">預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="bf17d-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="bf17d-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="bf17d-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="bf17d-165">指定訂閱金鑰查詢字串參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf17d-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="bf17d-166">預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="bf17d-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="bf17d-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="bf17d-167">-SubscriptionRequired</span></span>
<span data-ttu-id="bf17d-168">針對 Api 的要求，標出要強制執行 SubscriptionRequired。</span><span class="sxs-lookup"><span data-stu-id="bf17d-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="bf17d-169">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="bf17d-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="bf17d-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf17d-170">CommonParameters</span></span>
<span data-ttu-id="bf17d-171">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bf17d-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf17d-172">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf17d-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf17d-173">輸入</span><span class="sxs-lookup"><span data-stu-id="bf17d-173">INPUTS</span></span>

### <span data-ttu-id="bf17d-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="bf17d-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bf17d-175">System.String</span><span class="sxs-lookup"><span data-stu-id="bf17d-175">System.String</span></span>

### <span data-ttu-id="bf17d-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bf17d-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="bf17d-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="bf17d-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="bf17d-178">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bf17d-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bf17d-179">輸出</span><span class="sxs-lookup"><span data-stu-id="bf17d-179">OUTPUTS</span></span>

### <span data-ttu-id="bf17d-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bf17d-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="bf17d-181">筆記</span><span class="sxs-lookup"><span data-stu-id="bf17d-181">NOTES</span></span>

## <span data-ttu-id="bf17d-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf17d-182">RELATED LINKS</span></span>

[<span data-ttu-id="bf17d-183">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bf17d-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="bf17d-184">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bf17d-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="bf17d-185">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bf17d-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="bf17d-186">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bf17d-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="bf17d-187">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bf17d-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


