---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 02a7a35f4498724266d4c352744169d733f5eeab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282123"
---
# <span data-ttu-id="1f066-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1f066-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="1f066-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f066-102">SYNOPSIS</span></span>
<span data-ttu-id="1f066-103">修改 API。</span><span class="sxs-lookup"><span data-stu-id="1f066-103">Modifies an API.</span></span>

## <span data-ttu-id="1f066-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f066-104">SYNTAX</span></span>

### <span data-ttu-id="1f066-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="1f066-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f066-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1f066-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f066-107">說明</span><span class="sxs-lookup"><span data-stu-id="1f066-107">DESCRIPTION</span></span>
<span data-ttu-id="1f066-108">**AzApiManagementApi** Cmdlet 會修改 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="1f066-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="1f066-109">示例</span><span class="sxs-lookup"><span data-stu-id="1f066-109">EXAMPLES</span></span>

### <span data-ttu-id="1f066-110">範例1：修改 API</span><span class="sxs-lookup"><span data-stu-id="1f066-110">Example 1: Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="1f066-111">範例2：將 API 新增至現有的 ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1f066-111">Example 2: Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="1f066-112">這個範例會將 API 新增至現有的 API 版本集</span><span class="sxs-lookup"><span data-stu-id="1f066-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="1f066-113">範例3：變更 API 指向的後端 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="1f066-113">Example 3: Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="1f066-114">這個範例會更新指向的 ServiceUrl `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="1f066-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="1f066-115">參數</span><span class="sxs-lookup"><span data-stu-id="1f066-115">PARAMETERS</span></span>

### <span data-ttu-id="1f066-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1f066-116">-ApiId</span></span>
<span data-ttu-id="1f066-117">指定要修改的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="1f066-117">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="1f066-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="1f066-118">-AuthorizationScope</span></span>
<span data-ttu-id="1f066-119">指定 OAuth 作業範圍。</span><span class="sxs-lookup"><span data-stu-id="1f066-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="1f066-120">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="1f066-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="1f066-121">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="1f066-121">-AuthorizationServerId</span></span>
<span data-ttu-id="1f066-122">指定 OAuth 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="1f066-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="1f066-123">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="1f066-123">The default value is $Null.</span></span>
<span data-ttu-id="1f066-124">如果已指定 *AuthorizationScope* ，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="1f066-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="1f066-125">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="1f066-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="1f066-126">將存取權杖傳遞至 API 的 OpenId 授權伺服器機制。</span><span class="sxs-lookup"><span data-stu-id="1f066-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="1f066-127">請參閱 http://tools.ietf.org/html/rfc6749#section-4 。</span><span class="sxs-lookup"><span data-stu-id="1f066-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="1f066-128">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="1f066-128">This parameter is optional.</span></span> <span data-ttu-id="1f066-129">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="1f066-129">Default value is $null.</span></span>

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

### <span data-ttu-id="1f066-130">-內容</span><span class="sxs-lookup"><span data-stu-id="1f066-130">-Context</span></span>
<span data-ttu-id="1f066-131">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="1f066-131">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1f066-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f066-132">-DefaultProfile</span></span>
<span data-ttu-id="1f066-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f066-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f066-134">-描述</span><span class="sxs-lookup"><span data-stu-id="1f066-134">-Description</span></span>
<span data-ttu-id="1f066-135">指定 web API 的描述。</span><span class="sxs-lookup"><span data-stu-id="1f066-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="1f066-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f066-136">-InputObject</span></span>
<span data-ttu-id="1f066-137">PsApiManagementApi 的實例。</span><span class="sxs-lookup"><span data-stu-id="1f066-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="1f066-138">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="1f066-138">This parameter is required.</span></span>

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

### <span data-ttu-id="1f066-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f066-139">-Name</span></span>
<span data-ttu-id="1f066-140">指定 web API 的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f066-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="1f066-141">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="1f066-141">-OpenIdProviderId</span></span>
<span data-ttu-id="1f066-142">OpenId 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="1f066-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="1f066-143">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="1f066-143">This parameter is optional.</span></span> <span data-ttu-id="1f066-144">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="1f066-144">Default value is $null.</span></span> <span data-ttu-id="1f066-145">如果已指定 BearerTokenSendingMethods，則必須加以指定。</span><span class="sxs-lookup"><span data-stu-id="1f066-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="1f066-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f066-146">-PassThru</span></span>
<span data-ttu-id="1f066-147">passthru</span><span class="sxs-lookup"><span data-stu-id="1f066-147">passthru</span></span>

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

### <span data-ttu-id="1f066-148">-Path</span><span class="sxs-lookup"><span data-stu-id="1f066-148">-Path</span></span>
<span data-ttu-id="1f066-149">指定 web API 路徑，該路徑是 API 公用 URL 的最後一部分。</span><span class="sxs-lookup"><span data-stu-id="1f066-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="1f066-150">這個 URL 是由 API 消費者用來傳送要求至 web 服務的，而且必須是一個至400字元長。</span><span class="sxs-lookup"><span data-stu-id="1f066-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="1f066-151">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="1f066-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="1f066-152">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="1f066-152">-Protocols</span></span>
<span data-ttu-id="1f066-153">指定 web API 通訊協定的陣列。</span><span class="sxs-lookup"><span data-stu-id="1f066-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="1f066-154">psdx_paramvalues HTTP 和 HTTPs。</span><span class="sxs-lookup"><span data-stu-id="1f066-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="1f066-155">這些是可供使用 API 的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1f066-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="1f066-156">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="1f066-156">The default value is $Null.</span></span>

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

### <span data-ttu-id="1f066-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="1f066-157">-ServiceUrl</span></span>
<span data-ttu-id="1f066-158">指定公開 API 之 web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="1f066-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="1f066-159">這個 URL 只能由 Azure API 管理使用，而且不會公開。</span><span class="sxs-lookup"><span data-stu-id="1f066-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="1f066-160">URL 必須是一個至2000字元的長度。</span><span class="sxs-lookup"><span data-stu-id="1f066-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="1f066-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="1f066-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="1f066-162">指定訂閱金鑰標頭的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f066-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="1f066-163">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="1f066-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="1f066-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="1f066-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="1f066-165">指定訂閱金鑰查詢字串參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f066-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="1f066-166">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="1f066-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="1f066-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="1f066-167">-SubscriptionRequired</span></span>
<span data-ttu-id="1f066-168">[標記] 可強制 SubscriptionRequired Api 要求的要求。</span><span class="sxs-lookup"><span data-stu-id="1f066-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="1f066-169">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="1f066-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="1f066-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f066-170">CommonParameters</span></span>
<span data-ttu-id="1f066-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f066-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f066-172">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1f066-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f066-173">輸入</span><span class="sxs-lookup"><span data-stu-id="1f066-173">INPUTS</span></span>

### <span data-ttu-id="1f066-174">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="1f066-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1f066-175">System.object</span><span class="sxs-lookup"><span data-stu-id="1f066-175">System.String</span></span>

### <span data-ttu-id="1f066-176">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="1f066-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="1f066-177">PsApiManagementSchema []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="1f066-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="1f066-178">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="1f066-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1f066-179">輸出</span><span class="sxs-lookup"><span data-stu-id="1f066-179">OUTPUTS</span></span>

### <span data-ttu-id="1f066-180">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="1f066-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="1f066-181">筆記</span><span class="sxs-lookup"><span data-stu-id="1f066-181">NOTES</span></span>

## <span data-ttu-id="1f066-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f066-182">RELATED LINKS</span></span>

[<span data-ttu-id="1f066-183">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1f066-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="1f066-184">AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1f066-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="1f066-185">匯入-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1f066-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="1f066-186">新-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1f066-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="1f066-187">移除-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1f066-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


