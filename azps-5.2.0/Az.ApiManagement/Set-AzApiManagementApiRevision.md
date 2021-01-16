---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: fcae55c69b1874e06ce9110631baaf3b679fe99a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282171"
---
# <span data-ttu-id="f606a-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f606a-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="f606a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f606a-102">SYNOPSIS</span></span>
<span data-ttu-id="f606a-103">修改 API 修訂</span><span class="sxs-lookup"><span data-stu-id="f606a-103">Modifies an API Revision</span></span>

## <span data-ttu-id="f606a-104">句法</span><span class="sxs-lookup"><span data-stu-id="f606a-104">SYNTAX</span></span>

### <span data-ttu-id="f606a-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="f606a-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f606a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f606a-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f606a-107">說明</span><span class="sxs-lookup"><span data-stu-id="f606a-107">DESCRIPTION</span></span>
<span data-ttu-id="f606a-108">**AzApiManagementApiRevision** Cmdlet 會修改 Azure API 管理 API 修正。</span><span class="sxs-lookup"><span data-stu-id="f606a-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="f606a-109">示例</span><span class="sxs-lookup"><span data-stu-id="f606a-109">EXAMPLES</span></span>

### <span data-ttu-id="f606a-110">範例1：修改 API 修訂</span><span class="sxs-lookup"><span data-stu-id="f606a-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="f606a-111">此 Cmdlet 會 `2` `echo-api` 使用新的描述、通訊協定和路徑來更新 API 的修訂版本。</span><span class="sxs-lookup"><span data-stu-id="f606a-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="f606a-112">參數</span><span class="sxs-lookup"><span data-stu-id="f606a-112">PARAMETERS</span></span>

### <span data-ttu-id="f606a-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f606a-113">-ApiId</span></span>
<span data-ttu-id="f606a-114">現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f606a-114">Identifier of existing API.</span></span>
<span data-ttu-id="f606a-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f606a-115">This parameter is required.</span></span>

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

### <span data-ttu-id="f606a-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f606a-116">-ApiRevision</span></span>
<span data-ttu-id="f606a-117">現有 API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f606a-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="f606a-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f606a-118">This parameter is required.</span></span>

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

### <span data-ttu-id="f606a-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="f606a-119">-AuthorizationScope</span></span>
<span data-ttu-id="f606a-120">OAuth 作業範圍。</span><span class="sxs-lookup"><span data-stu-id="f606a-120">OAuth operations scope.</span></span>
<span data-ttu-id="f606a-121">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f606a-121">This parameter is optional.</span></span>
<span data-ttu-id="f606a-122">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="f606a-122">Default value is $null.</span></span>

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

### <span data-ttu-id="f606a-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="f606a-123">-AuthorizationServerId</span></span>
<span data-ttu-id="f606a-124">OAuth 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="f606a-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="f606a-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f606a-125">This parameter is optional.</span></span>
<span data-ttu-id="f606a-126">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="f606a-126">Default value is $null.</span></span>
<span data-ttu-id="f606a-127">如果已指定 AuthorizationScope，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="f606a-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="f606a-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="f606a-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="f606a-129">將存取權杖傳遞至 API 的 OpenId 授權伺服器機制。</span><span class="sxs-lookup"><span data-stu-id="f606a-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="f606a-130">請參閱 http://tools.ietf.org/html/rfc6749#section-4 。</span><span class="sxs-lookup"><span data-stu-id="f606a-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="f606a-131">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f606a-131">This parameter is optional.</span></span> <span data-ttu-id="f606a-132">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="f606a-132">Default value is $null.</span></span>

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

### <span data-ttu-id="f606a-133">-內容</span><span class="sxs-lookup"><span data-stu-id="f606a-133">-Context</span></span>
<span data-ttu-id="f606a-134">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="f606a-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f606a-135">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f606a-135">This parameter is required.</span></span>

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

### <span data-ttu-id="f606a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f606a-136">-DefaultProfile</span></span>
<span data-ttu-id="f606a-137">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f606a-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f606a-138">-描述</span><span class="sxs-lookup"><span data-stu-id="f606a-138">-Description</span></span>
<span data-ttu-id="f606a-139">Web API 說明。</span><span class="sxs-lookup"><span data-stu-id="f606a-139">Web API description.</span></span>
<span data-ttu-id="f606a-140">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f606a-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="f606a-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f606a-141">-InputObject</span></span>
<span data-ttu-id="f606a-142">PsApiManagementApi 的實例。</span><span class="sxs-lookup"><span data-stu-id="f606a-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="f606a-143">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f606a-143">This parameter is required.</span></span>

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

### <span data-ttu-id="f606a-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="f606a-144">-Name</span></span>
<span data-ttu-id="f606a-145">Web API 名稱。</span><span class="sxs-lookup"><span data-stu-id="f606a-145">Web API name.</span></span>
<span data-ttu-id="f606a-146">API 在開發人員和管理入口網站上顯示的公用名稱。</span><span class="sxs-lookup"><span data-stu-id="f606a-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="f606a-147">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f606a-147">This parameter is required.</span></span>

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

### <span data-ttu-id="f606a-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="f606a-148">-OpenIdProviderId</span></span>
<span data-ttu-id="f606a-149">OpenId 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="f606a-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="f606a-150">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f606a-150">This parameter is optional.</span></span> <span data-ttu-id="f606a-151">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="f606a-151">Default value is $null.</span></span> <span data-ttu-id="f606a-152">如果已指定 BearerTokenSendingMethods，則必須加以指定。</span><span class="sxs-lookup"><span data-stu-id="f606a-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="f606a-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f606a-153">-PassThru</span></span>
<span data-ttu-id="f606a-154">如果已指定，則 ServiceManagement 代表 set API 的 PsApiManagementApi 類型的 ApiManagement 的實例。</span><span class="sxs-lookup"><span data-stu-id="f606a-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="f606a-155">-Path</span><span class="sxs-lookup"><span data-stu-id="f606a-155">-Path</span></span>
<span data-ttu-id="f606a-156">Web API 路徑。</span><span class="sxs-lookup"><span data-stu-id="f606a-156">Web API Path.</span></span>
<span data-ttu-id="f606a-157">API 公用 URL 的最後一部分。</span><span class="sxs-lookup"><span data-stu-id="f606a-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="f606a-158">此 URL 將由 API 消費者用來傳送要求至 web 服務。</span><span class="sxs-lookup"><span data-stu-id="f606a-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="f606a-159">長度必須是1到400個字元。</span><span class="sxs-lookup"><span data-stu-id="f606a-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="f606a-160">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f606a-160">This parameter is optional.</span></span>
<span data-ttu-id="f606a-161">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="f606a-161">Default value is $null.</span></span>

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

### <span data-ttu-id="f606a-162">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="f606a-162">-Protocols</span></span>
<span data-ttu-id="f606a-163">Web API 通訊協定 (HTTP、HTTPs) 。</span><span class="sxs-lookup"><span data-stu-id="f606a-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="f606a-164">提供可用 API 的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f606a-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="f606a-165">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f606a-165">This parameter is required.</span></span>
<span data-ttu-id="f606a-166">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="f606a-166">Default value is $null.</span></span>

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

### <span data-ttu-id="f606a-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="f606a-167">-ServiceUrl</span></span>
<span data-ttu-id="f606a-168">公開 API 之 web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="f606a-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="f606a-169">這個 URL 將只由 Azure API 管理使用，不會公開。</span><span class="sxs-lookup"><span data-stu-id="f606a-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="f606a-170">長度必須是1到2000個字元。</span><span class="sxs-lookup"><span data-stu-id="f606a-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="f606a-171">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f606a-171">This parameter is required.</span></span>

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

### <span data-ttu-id="f606a-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="f606a-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="f606a-173">訂閱金鑰標頭名稱。</span><span class="sxs-lookup"><span data-stu-id="f606a-173">Subscription key header name.</span></span>
<span data-ttu-id="f606a-174">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f606a-174">This parameter is optional.</span></span>
<span data-ttu-id="f606a-175">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="f606a-175">Default value is $null.</span></span>

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

### <span data-ttu-id="f606a-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="f606a-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="f606a-177">訂閱金鑰查詢字串參數名稱。</span><span class="sxs-lookup"><span data-stu-id="f606a-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="f606a-178">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f606a-178">This parameter is optional.</span></span>
<span data-ttu-id="f606a-179">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="f606a-179">Default value is $null.</span></span>

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

### <span data-ttu-id="f606a-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="f606a-180">-SubscriptionRequired</span></span>
<span data-ttu-id="f606a-181">[標記] 可強制 SubscriptionRequired Api 要求的要求。</span><span class="sxs-lookup"><span data-stu-id="f606a-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="f606a-182">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f606a-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="f606a-183">-確認</span><span class="sxs-lookup"><span data-stu-id="f606a-183">-Confirm</span></span>
<span data-ttu-id="f606a-184">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f606a-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f606a-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f606a-185">-WhatIf</span></span>
<span data-ttu-id="f606a-186">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f606a-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f606a-187">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f606a-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f606a-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f606a-188">CommonParameters</span></span>
<span data-ttu-id="f606a-189">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f606a-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f606a-190">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f606a-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f606a-191">輸入</span><span class="sxs-lookup"><span data-stu-id="f606a-191">INPUTS</span></span>

### <span data-ttu-id="f606a-192">System.object</span><span class="sxs-lookup"><span data-stu-id="f606a-192">System.String</span></span>

### <span data-ttu-id="f606a-193">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f606a-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f606a-194">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f606a-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="f606a-195">PsApiManagementSchema []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="f606a-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="f606a-196">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="f606a-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f606a-197">輸出</span><span class="sxs-lookup"><span data-stu-id="f606a-197">OUTPUTS</span></span>

### <span data-ttu-id="f606a-198">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f606a-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="f606a-199">筆記</span><span class="sxs-lookup"><span data-stu-id="f606a-199">NOTES</span></span>

## <span data-ttu-id="f606a-200">相關連結</span><span class="sxs-lookup"><span data-stu-id="f606a-200">RELATED LINKS</span></span>

[<span data-ttu-id="f606a-201">AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f606a-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="f606a-202">新-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f606a-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="f606a-203">移除-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f606a-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)