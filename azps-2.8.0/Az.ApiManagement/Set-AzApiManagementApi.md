---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 973dc9bac629ee9a82b7624053f689bf7884fd8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613895"
---
# <span data-ttu-id="fe746-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fe746-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="fe746-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe746-102">SYNOPSIS</span></span>
<span data-ttu-id="fe746-103">修改 API。</span><span class="sxs-lookup"><span data-stu-id="fe746-103">Modifies an API.</span></span>

## <span data-ttu-id="fe746-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe746-104">SYNTAX</span></span>

### <span data-ttu-id="fe746-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="fe746-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe746-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fe746-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe746-107">說明</span><span class="sxs-lookup"><span data-stu-id="fe746-107">DESCRIPTION</span></span>
<span data-ttu-id="fe746-108">**AzApiManagementApi** Cmdlet 會修改 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="fe746-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="fe746-109">示例</span><span class="sxs-lookup"><span data-stu-id="fe746-109">EXAMPLES</span></span>

### <span data-ttu-id="fe746-110">範例1修改 API</span><span class="sxs-lookup"><span data-stu-id="fe746-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="fe746-111">範例2將 API 新增至現有的 ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="fe746-111">Example 2 Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```
<span data-ttu-id="fe746-112">這個範例會將 API 新增至現有的 API 版本集</span><span class="sxs-lookup"><span data-stu-id="fe746-112">This example adds an API to an existing API Version Set</span></span>

## <span data-ttu-id="fe746-113">參數</span><span class="sxs-lookup"><span data-stu-id="fe746-113">PARAMETERS</span></span>

### <span data-ttu-id="fe746-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fe746-114">-ApiId</span></span>
<span data-ttu-id="fe746-115">指定要修改的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe746-115">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="fe746-116">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="fe746-116">-AuthorizationScope</span></span>
<span data-ttu-id="fe746-117">指定 OAuth 作業範圍。</span><span class="sxs-lookup"><span data-stu-id="fe746-117">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="fe746-118">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="fe746-118">The default value is $Null.</span></span>

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

### <span data-ttu-id="fe746-119">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="fe746-119">-AuthorizationServerId</span></span>
<span data-ttu-id="fe746-120">指定 OAuth 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe746-120">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="fe746-121">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="fe746-121">The default value is $Null.</span></span>
<span data-ttu-id="fe746-122">如果已指定 *AuthorizationScope* ，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="fe746-122">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="fe746-123">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="fe746-123">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="fe746-124">將存取權杖傳遞至 API 的 OpenId 授權伺服器機制。</span><span class="sxs-lookup"><span data-stu-id="fe746-124">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="fe746-125">請參閱 http://tools.ietf.org/html/rfc6749#section-4 。</span><span class="sxs-lookup"><span data-stu-id="fe746-125">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="fe746-126">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="fe746-126">This parameter is optional.</span></span> <span data-ttu-id="fe746-127">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="fe746-127">Default value is $null.</span></span>

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

### <span data-ttu-id="fe746-128">-內容</span><span class="sxs-lookup"><span data-stu-id="fe746-128">-Context</span></span>
<span data-ttu-id="fe746-129">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="fe746-129">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fe746-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe746-130">-DefaultProfile</span></span>
<span data-ttu-id="fe746-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe746-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe746-132">-描述</span><span class="sxs-lookup"><span data-stu-id="fe746-132">-Description</span></span>
<span data-ttu-id="fe746-133">指定 web API 的描述。</span><span class="sxs-lookup"><span data-stu-id="fe746-133">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="fe746-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe746-134">-InputObject</span></span>
<span data-ttu-id="fe746-135">PsApiManagementApi 的實例。</span><span class="sxs-lookup"><span data-stu-id="fe746-135">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="fe746-136">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="fe746-136">This parameter is required.</span></span>

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

### <span data-ttu-id="fe746-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe746-137">-Name</span></span>
<span data-ttu-id="fe746-138">指定 web API 的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe746-138">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="fe746-139">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="fe746-139">-OpenIdProviderId</span></span>
<span data-ttu-id="fe746-140">OpenId 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe746-140">OpenId authorization server identifier.</span></span> <span data-ttu-id="fe746-141">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="fe746-141">This parameter is optional.</span></span> <span data-ttu-id="fe746-142">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="fe746-142">Default value is $null.</span></span> <span data-ttu-id="fe746-143">如果已指定 BearerTokenSendingMethods，則必須加以指定。</span><span class="sxs-lookup"><span data-stu-id="fe746-143">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="fe746-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe746-144">-PassThru</span></span>
<span data-ttu-id="fe746-145">passthru</span><span class="sxs-lookup"><span data-stu-id="fe746-145">passthru</span></span>

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

### <span data-ttu-id="fe746-146">-Path</span><span class="sxs-lookup"><span data-stu-id="fe746-146">-Path</span></span>
<span data-ttu-id="fe746-147">指定 web API 路徑，該路徑是 API 公用 URL 的最後一部分。</span><span class="sxs-lookup"><span data-stu-id="fe746-147">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="fe746-148">這個 URL 是由 API 消費者用來傳送要求至 web 服務的，而且必須是一個至400字元長。</span><span class="sxs-lookup"><span data-stu-id="fe746-148">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="fe746-149">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="fe746-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="fe746-150">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="fe746-150">-Protocols</span></span>
<span data-ttu-id="fe746-151">指定 web API 通訊協定的陣列。</span><span class="sxs-lookup"><span data-stu-id="fe746-151">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="fe746-152">psdx_paramvalues HTTP 和 HTTPs。</span><span class="sxs-lookup"><span data-stu-id="fe746-152">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="fe746-153">這些是可供使用 API 的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="fe746-153">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="fe746-154">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="fe746-154">The default value is $Null.</span></span>

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

### <span data-ttu-id="fe746-155">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="fe746-155">-ServiceUrl</span></span>
<span data-ttu-id="fe746-156">指定公開 API 之 web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="fe746-156">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="fe746-157">這個 URL 只能由 Azure API 管理使用，而且不會公開。</span><span class="sxs-lookup"><span data-stu-id="fe746-157">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="fe746-158">URL 必須是一個至2000字元的長度。</span><span class="sxs-lookup"><span data-stu-id="fe746-158">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="fe746-159">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="fe746-159">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="fe746-160">指定訂閱金鑰標頭的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe746-160">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="fe746-161">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="fe746-161">The default value is $Null.</span></span>

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

### <span data-ttu-id="fe746-162">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="fe746-162">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="fe746-163">指定訂閱金鑰查詢字串參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe746-163">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="fe746-164">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="fe746-164">The default value is $Null.</span></span>

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

### <span data-ttu-id="fe746-165">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="fe746-165">-SubscriptionRequired</span></span>
<span data-ttu-id="fe746-166">[標記] 可強制 SubscriptionRequired Api 要求的要求。</span><span class="sxs-lookup"><span data-stu-id="fe746-166">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="fe746-167">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="fe746-167">This parameter is optional.</span></span>

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

### <span data-ttu-id="fe746-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe746-168">CommonParameters</span></span>
<span data-ttu-id="fe746-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe746-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe746-170">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fe746-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe746-171">輸入</span><span class="sxs-lookup"><span data-stu-id="fe746-171">INPUTS</span></span>

### <span data-ttu-id="fe746-172">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fe746-172">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fe746-173">System.object</span><span class="sxs-lookup"><span data-stu-id="fe746-173">System.String</span></span>

### <span data-ttu-id="fe746-174">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fe746-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="fe746-175">PsApiManagementSchema []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="fe746-175">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="fe746-176">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="fe746-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fe746-177">輸出</span><span class="sxs-lookup"><span data-stu-id="fe746-177">OUTPUTS</span></span>

### <span data-ttu-id="fe746-178">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fe746-178">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="fe746-179">筆記</span><span class="sxs-lookup"><span data-stu-id="fe746-179">NOTES</span></span>

## <span data-ttu-id="fe746-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe746-180">RELATED LINKS</span></span>

[<span data-ttu-id="fe746-181">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fe746-181">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="fe746-182">AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fe746-182">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="fe746-183">匯入-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fe746-183">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="fe746-184">新-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fe746-184">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="fe746-185">移除-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fe746-185">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


