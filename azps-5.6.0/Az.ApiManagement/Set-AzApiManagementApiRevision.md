---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: b8eac81d90f20617399048464ecca40e0df8d93f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905301"
---
# <span data-ttu-id="bf139-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="bf139-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="bf139-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bf139-102">SYNOPSIS</span></span>
<span data-ttu-id="bf139-103">修改 API 修訂</span><span class="sxs-lookup"><span data-stu-id="bf139-103">Modifies an API Revision</span></span>

## <span data-ttu-id="bf139-104">語法</span><span class="sxs-lookup"><span data-stu-id="bf139-104">SYNTAX</span></span>

### <span data-ttu-id="bf139-105">展開Parameter (預設) </span><span class="sxs-lookup"><span data-stu-id="bf139-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf139-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bf139-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf139-107">描述</span><span class="sxs-lookup"><span data-stu-id="bf139-107">DESCRIPTION</span></span>
<span data-ttu-id="bf139-108">**Set-AzApiManagementApiRevision** Cmdlet 會修改 Azure API 管理 API 修訂。</span><span class="sxs-lookup"><span data-stu-id="bf139-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="bf139-109">例子</span><span class="sxs-lookup"><span data-stu-id="bf139-109">EXAMPLES</span></span>

### <span data-ttu-id="bf139-110">範例 1：修改 API 修訂</span><span class="sxs-lookup"><span data-stu-id="bf139-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="bf139-111">Cmdlet 會以新的描述、通訊協定和路徑更新 `2` API `echo-api` 的修訂。</span><span class="sxs-lookup"><span data-stu-id="bf139-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="bf139-112">參數</span><span class="sxs-lookup"><span data-stu-id="bf139-112">PARAMETERS</span></span>

### <span data-ttu-id="bf139-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bf139-113">-ApiId</span></span>
<span data-ttu-id="bf139-114">現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf139-114">Identifier of existing API.</span></span>
<span data-ttu-id="bf139-115">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="bf139-115">This parameter is required.</span></span>

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

### <span data-ttu-id="bf139-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="bf139-116">-ApiRevision</span></span>
<span data-ttu-id="bf139-117">現有 API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf139-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="bf139-118">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="bf139-118">This parameter is required.</span></span>

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

### <span data-ttu-id="bf139-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="bf139-119">-AuthorizationScope</span></span>
<span data-ttu-id="bf139-120">OAuth 操作範圍。</span><span class="sxs-lookup"><span data-stu-id="bf139-120">OAuth operations scope.</span></span>
<span data-ttu-id="bf139-121">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="bf139-121">This parameter is optional.</span></span>
<span data-ttu-id="bf139-122">預設值會$null。</span><span class="sxs-lookup"><span data-stu-id="bf139-122">Default value is $null.</span></span>

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

### <span data-ttu-id="bf139-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="bf139-123">-AuthorizationServerId</span></span>
<span data-ttu-id="bf139-124">OAuth 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf139-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="bf139-125">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="bf139-125">This parameter is optional.</span></span>
<span data-ttu-id="bf139-126">預設值會$null。</span><span class="sxs-lookup"><span data-stu-id="bf139-126">Default value is $null.</span></span>
<span data-ttu-id="bf139-127">必須指定是否指定 AuthorizationScope。</span><span class="sxs-lookup"><span data-stu-id="bf139-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="bf139-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="bf139-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="bf139-129">將存取權杖傳遞至 API 的 OpenId 授權伺服器機制。</span><span class="sxs-lookup"><span data-stu-id="bf139-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="bf139-130">參照 http://tools.ietf.org/html/rfc6749#section-4 到 。</span><span class="sxs-lookup"><span data-stu-id="bf139-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="bf139-131">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="bf139-131">This parameter is optional.</span></span> <span data-ttu-id="bf139-132">預設值會$null。</span><span class="sxs-lookup"><span data-stu-id="bf139-132">Default value is $null.</span></span>

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

### <span data-ttu-id="bf139-133">-內容</span><span class="sxs-lookup"><span data-stu-id="bf139-133">-Context</span></span>
<span data-ttu-id="bf139-134">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="bf139-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bf139-135">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="bf139-135">This parameter is required.</span></span>

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

### <span data-ttu-id="bf139-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf139-136">-DefaultProfile</span></span>
<span data-ttu-id="bf139-137">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf139-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf139-138">-描述</span><span class="sxs-lookup"><span data-stu-id="bf139-138">-Description</span></span>
<span data-ttu-id="bf139-139">Web API 描述。</span><span class="sxs-lookup"><span data-stu-id="bf139-139">Web API description.</span></span>
<span data-ttu-id="bf139-140">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="bf139-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="bf139-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf139-141">-InputObject</span></span>
<span data-ttu-id="bf139-142">PsApiManagementApi 實例。</span><span class="sxs-lookup"><span data-stu-id="bf139-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="bf139-143">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="bf139-143">This parameter is required.</span></span>

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

### <span data-ttu-id="bf139-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="bf139-144">-Name</span></span>
<span data-ttu-id="bf139-145">Web API 名稱。</span><span class="sxs-lookup"><span data-stu-id="bf139-145">Web API name.</span></span>
<span data-ttu-id="bf139-146">顯示在開發人員和系統管理入口網站中的 API 公用名稱。</span><span class="sxs-lookup"><span data-stu-id="bf139-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="bf139-147">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="bf139-147">This parameter is required.</span></span>

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

### <span data-ttu-id="bf139-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="bf139-148">-OpenIdProviderId</span></span>
<span data-ttu-id="bf139-149">OpenId 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf139-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="bf139-150">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="bf139-150">This parameter is optional.</span></span> <span data-ttu-id="bf139-151">預設值會$null。</span><span class="sxs-lookup"><span data-stu-id="bf139-151">Default value is $null.</span></span> <span data-ttu-id="bf139-152">必須指定已指定 BearerTokenSendingMethods。</span><span class="sxs-lookup"><span data-stu-id="bf139-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="bf139-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf139-153">-PassThru</span></span>
<span data-ttu-id="bf139-154">如果指定的話，代表集 API 的 Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi 類型實例。</span><span class="sxs-lookup"><span data-stu-id="bf139-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="bf139-155">-路徑</span><span class="sxs-lookup"><span data-stu-id="bf139-155">-Path</span></span>
<span data-ttu-id="bf139-156">Web API 路徑。</span><span class="sxs-lookup"><span data-stu-id="bf139-156">Web API Path.</span></span>
<span data-ttu-id="bf139-157">API 公用 URL 的最後一部分。</span><span class="sxs-lookup"><span data-stu-id="bf139-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="bf139-158">API 消費者會使用這個 URL 來傳送要求至 Web 服務。</span><span class="sxs-lookup"><span data-stu-id="bf139-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="bf139-159">必須長 1 到 400 個字元。</span><span class="sxs-lookup"><span data-stu-id="bf139-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="bf139-160">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="bf139-160">This parameter is optional.</span></span>
<span data-ttu-id="bf139-161">預設值會$null。</span><span class="sxs-lookup"><span data-stu-id="bf139-161">Default value is $null.</span></span>

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

### <span data-ttu-id="bf139-162">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="bf139-162">-Protocols</span></span>
<span data-ttu-id="bf139-163">Web API 通訊協定 (HTTP、HTTPs) 。</span><span class="sxs-lookup"><span data-stu-id="bf139-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="bf139-164">提供 API 的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="bf139-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="bf139-165">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="bf139-165">This parameter is required.</span></span>
<span data-ttu-id="bf139-166">預設值會$null。</span><span class="sxs-lookup"><span data-stu-id="bf139-166">Default value is $null.</span></span>

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

### <span data-ttu-id="bf139-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="bf139-167">-ServiceUrl</span></span>
<span data-ttu-id="bf139-168">公開 API 之 Web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="bf139-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="bf139-169">此 URL 將僅由 Azure API 管理使用，不會公開。</span><span class="sxs-lookup"><span data-stu-id="bf139-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="bf139-170">必須長 1 到 2000 個字元。</span><span class="sxs-lookup"><span data-stu-id="bf139-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="bf139-171">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="bf139-171">This parameter is required.</span></span>

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

### <span data-ttu-id="bf139-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="bf139-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="bf139-173">訂閱金鑰標題名稱。</span><span class="sxs-lookup"><span data-stu-id="bf139-173">Subscription key header name.</span></span>
<span data-ttu-id="bf139-174">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="bf139-174">This parameter is optional.</span></span>
<span data-ttu-id="bf139-175">預設值會$null。</span><span class="sxs-lookup"><span data-stu-id="bf139-175">Default value is $null.</span></span>

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

### <span data-ttu-id="bf139-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="bf139-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="bf139-177">訂閱金鑰查詢字串參數名稱。</span><span class="sxs-lookup"><span data-stu-id="bf139-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="bf139-178">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="bf139-178">This parameter is optional.</span></span>
<span data-ttu-id="bf139-179">預設值會$null。</span><span class="sxs-lookup"><span data-stu-id="bf139-179">Default value is $null.</span></span>

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

### <span data-ttu-id="bf139-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="bf139-180">-SubscriptionRequired</span></span>
<span data-ttu-id="bf139-181">針對 Api 的要求，標出要強制執行 SubscriptionRequired。</span><span class="sxs-lookup"><span data-stu-id="bf139-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="bf139-182">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="bf139-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="bf139-183">-確認</span><span class="sxs-lookup"><span data-stu-id="bf139-183">-Confirm</span></span>
<span data-ttu-id="bf139-184">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bf139-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf139-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf139-185">-WhatIf</span></span>
<span data-ttu-id="bf139-186">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bf139-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf139-187">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bf139-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf139-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf139-188">CommonParameters</span></span>
<span data-ttu-id="bf139-189">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bf139-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf139-190">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf139-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf139-191">輸入</span><span class="sxs-lookup"><span data-stu-id="bf139-191">INPUTS</span></span>

### <span data-ttu-id="bf139-192">System.String</span><span class="sxs-lookup"><span data-stu-id="bf139-192">System.String</span></span>

### <span data-ttu-id="bf139-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="bf139-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bf139-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bf139-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="bf139-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="bf139-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="bf139-196">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bf139-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bf139-197">輸出</span><span class="sxs-lookup"><span data-stu-id="bf139-197">OUTPUTS</span></span>

### <span data-ttu-id="bf139-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bf139-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="bf139-199">筆記</span><span class="sxs-lookup"><span data-stu-id="bf139-199">NOTES</span></span>

## <span data-ttu-id="bf139-200">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf139-200">RELATED LINKS</span></span>

[<span data-ttu-id="bf139-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="bf139-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="bf139-202">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="bf139-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="bf139-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="bf139-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)