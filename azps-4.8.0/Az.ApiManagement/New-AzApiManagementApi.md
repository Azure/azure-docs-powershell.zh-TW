---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 3312c725d63bcb42aab7d82144c5a8f6f8e67641
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970691"
---
# <span data-ttu-id="6915e-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6915e-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="6915e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6915e-102">SYNOPSIS</span></span>
<span data-ttu-id="6915e-103">建立 API。</span><span class="sxs-lookup"><span data-stu-id="6915e-103">Creates an API.</span></span>

## <span data-ttu-id="6915e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6915e-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6915e-105">說明</span><span class="sxs-lookup"><span data-stu-id="6915e-105">DESCRIPTION</span></span>
<span data-ttu-id="6915e-106">**新的-AzApiManagementApi** Cmdlet 會建立 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="6915e-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="6915e-107">示例</span><span class="sxs-lookup"><span data-stu-id="6915e-107">EXAMPLES</span></span>

### <span data-ttu-id="6915e-108">範例1：建立 API</span><span class="sxs-lookup"><span data-stu-id="6915e-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="6915e-109">這個命令會建立一個名為 EchoApi 且具有指定 URL 的 API。</span><span class="sxs-lookup"><span data-stu-id="6915e-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="6915e-110">範例2：將所有操作、標籤、產品及原則從回音式 API 複製到 ApiVersionSet，以建立 API</span><span class="sxs-lookup"><span data-stu-id="6915e-110">Example 2: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
```powershell
PS D:\github\azure-powershell>$context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso
PS D:\github\azure-powershell>$versionSet = Get-AzApiManagementApiVersionSet -Context $context -ApiVersionSetId "xmsVersionSet"
PS D:\github\azure-powershell> New-AzApiManagementApi -Context $context -Name "echoapiv4" -Description "Create Echo Api V4" -SubscriptionRequired -ServiceUrl "https://echoapi.cloudapp.net/v4" -Path "echov3" -Protocols @("http", "https") -ApiVersionSetId $versionSet.ApiVersionSetId -SourceApiId "echo-api" -ApiVersion "v4"


ApiId                         : 691b7d410125414a929c108541c60e06
Name                          : echoapiv4
Description                   : Create Echo Api V4
ServiceUrl                    : https://echoapi.cloudapp.net/v4 
Path                          : echov3
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v4
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/xmsVersionSet
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/691b7d410125414a929c108541c60e06    
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="6915e-111">這個命令會 `echoapiv3` 在 ApiVersionSet 中建立 API， `xmsVersionSet` 並從來源 API 複製所有的操作、標記和原則 `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="6915e-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="6915e-112">它會覆寫 SubscriptionRequired、ServiceUrl、Path、通訊協定</span><span class="sxs-lookup"><span data-stu-id="6915e-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

### <span data-ttu-id="6915e-113">範例3</span><span class="sxs-lookup"><span data-stu-id="6915e-113">Example 3</span></span>

<span data-ttu-id="6915e-114">建立 API。</span><span class="sxs-lookup"><span data-stu-id="6915e-114">Creates an API.</span></span> <span data-ttu-id="6915e-115"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="6915e-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementApi -ApiId '0001' -Context <PsApiManagementContext> -Name 'Echo api' -Path 'echov3' -Protocols Http -ServiceUrl 'https://contoso.com/apis/echo'
```

## <span data-ttu-id="6915e-116">參數</span><span class="sxs-lookup"><span data-stu-id="6915e-116">PARAMETERS</span></span>

### <span data-ttu-id="6915e-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6915e-117">-ApiId</span></span>
<span data-ttu-id="6915e-118">指定要建立的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="6915e-118">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="6915e-119">如果您沒有指定此參數，這個 Cmdlet 會為您產生識別碼。</span><span class="sxs-lookup"><span data-stu-id="6915e-119">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="6915e-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6915e-120">-ApiVersion</span></span>
<span data-ttu-id="6915e-121">要建立的 api api 版本。</span><span class="sxs-lookup"><span data-stu-id="6915e-121">Api Version of the Api to create.</span></span> <span data-ttu-id="6915e-122">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="6915e-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="6915e-123">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="6915e-123">-ApiVersionDescription</span></span>
<span data-ttu-id="6915e-124">Api 版本描述。</span><span class="sxs-lookup"><span data-stu-id="6915e-124">Api Version Description.</span></span> <span data-ttu-id="6915e-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="6915e-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="6915e-126">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="6915e-126">-ApiVersionSetId</span></span>
<span data-ttu-id="6915e-127">相關 Api 版本集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6915e-127">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="6915e-128">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="6915e-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="6915e-129">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="6915e-129">-AuthorizationScope</span></span>
<span data-ttu-id="6915e-130">指定 OAuth 作業範圍。</span><span class="sxs-lookup"><span data-stu-id="6915e-130">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="6915e-131">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="6915e-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="6915e-132">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="6915e-132">-AuthorizationServerId</span></span>
<span data-ttu-id="6915e-133">指定 OAuth 授權伺服器 ID。</span><span class="sxs-lookup"><span data-stu-id="6915e-133">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="6915e-134">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="6915e-134">The default value is $Null.</span></span>
<span data-ttu-id="6915e-135">如果已指定 *AuthorizationScope* ，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="6915e-135">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="6915e-136">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="6915e-136">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="6915e-137">將存取權杖傳遞至 API 的 OpenId 授權伺服器機制。</span><span class="sxs-lookup"><span data-stu-id="6915e-137">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="6915e-138">請參閱 http://tools.ietf.org/html/rfc6749#section-4 。</span><span class="sxs-lookup"><span data-stu-id="6915e-138">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="6915e-139">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="6915e-139">This parameter is optional.</span></span> <span data-ttu-id="6915e-140">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="6915e-140">Default value is $null.</span></span>

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

### <span data-ttu-id="6915e-141">-內容</span><span class="sxs-lookup"><span data-stu-id="6915e-141">-Context</span></span>
<span data-ttu-id="6915e-142">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="6915e-142">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6915e-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6915e-143">-DefaultProfile</span></span>
<span data-ttu-id="6915e-144">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6915e-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6915e-145">-描述</span><span class="sxs-lookup"><span data-stu-id="6915e-145">-Description</span></span>
<span data-ttu-id="6915e-146">指定 web API 的描述。</span><span class="sxs-lookup"><span data-stu-id="6915e-146">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="6915e-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="6915e-147">-Name</span></span>
<span data-ttu-id="6915e-148">指定 web API 的名稱。</span><span class="sxs-lookup"><span data-stu-id="6915e-148">Specifies the name of the web API.</span></span>
<span data-ttu-id="6915e-149">這是 API 在開發人員和管理入口網站上顯示的公用名稱。</span><span class="sxs-lookup"><span data-stu-id="6915e-149">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="6915e-150">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="6915e-150">-OpenIdProviderId</span></span>
<span data-ttu-id="6915e-151">OpenId 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="6915e-151">OpenId authorization server identifier.</span></span> <span data-ttu-id="6915e-152">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="6915e-152">This parameter is optional.</span></span> <span data-ttu-id="6915e-153">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="6915e-153">Default value is $null.</span></span> <span data-ttu-id="6915e-154">如果已指定 BearerTokenSendingMethods，則必須加以指定。</span><span class="sxs-lookup"><span data-stu-id="6915e-154">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="6915e-155">-Path</span><span class="sxs-lookup"><span data-stu-id="6915e-155">-Path</span></span>
<span data-ttu-id="6915e-156">指定 web API 路徑，該路徑是 API 公用 URL 的最後一部分，並對應至管理入口網站中的 [Web API URL 尾碼] 欄位。</span><span class="sxs-lookup"><span data-stu-id="6915e-156">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="6915e-157">這個 URL 是由 API 消費者用來傳送要求至 web 服務的，而且必須是一個至400字元長。</span><span class="sxs-lookup"><span data-stu-id="6915e-157">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="6915e-158">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="6915e-158">The default value is $Null.</span></span>

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

### <span data-ttu-id="6915e-159">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="6915e-159">-ProductIds</span></span>
<span data-ttu-id="6915e-160">指定要將新 API 新增至其中的產品識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="6915e-160">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="6915e-161">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="6915e-161">-Protocols</span></span>
<span data-ttu-id="6915e-162">指定 web API 通訊協定的陣列。</span><span class="sxs-lookup"><span data-stu-id="6915e-162">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="6915e-163">有效值為 HTTP、HTTPs。</span><span class="sxs-lookup"><span data-stu-id="6915e-163">Valid values are http, https.</span></span>
<span data-ttu-id="6915e-164">這些是可供使用 API 的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6915e-164">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="6915e-165">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="6915e-165">The default value is $Null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6915e-166">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="6915e-166">-ServiceUrl</span></span>
<span data-ttu-id="6915e-167">指定公開 API 之 web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="6915e-167">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="6915e-168">這個 URL 只能由 Azure API 管理使用，而且不會公開。</span><span class="sxs-lookup"><span data-stu-id="6915e-168">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="6915e-169">URL 必須是一個至2000字元的長度。</span><span class="sxs-lookup"><span data-stu-id="6915e-169">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="6915e-170">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="6915e-170">-SourceApiId</span></span>
<span data-ttu-id="6915e-171">來源 API 的 Api 識別碼。</span><span class="sxs-lookup"><span data-stu-id="6915e-171">Api identifier of the source API.</span></span> <span data-ttu-id="6915e-172">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="6915e-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="6915e-173">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="6915e-173">-SourceApiRevision</span></span>
<span data-ttu-id="6915e-174">來源 API 的 Api 修訂版本。</span><span class="sxs-lookup"><span data-stu-id="6915e-174">Api Revision of the source API.</span></span> <span data-ttu-id="6915e-175">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="6915e-175">This parameter is optional.</span></span>

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

### <span data-ttu-id="6915e-176">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="6915e-176">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="6915e-177">指定訂閱金鑰標頭名稱。</span><span class="sxs-lookup"><span data-stu-id="6915e-177">Specifies the subscription key header name.</span></span>
<span data-ttu-id="6915e-178">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="6915e-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="6915e-179">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="6915e-179">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="6915e-180">指定訂閱金鑰查詢字串參數名稱。</span><span class="sxs-lookup"><span data-stu-id="6915e-180">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="6915e-181">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="6915e-181">The default value is $Null.</span></span>

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

### <span data-ttu-id="6915e-182">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="6915e-182">-SubscriptionRequired</span></span>
<span data-ttu-id="6915e-183">[標記] 可強制 SubscriptionRequired Api 要求的要求。</span><span class="sxs-lookup"><span data-stu-id="6915e-183">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="6915e-184">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="6915e-184">This parameter is optional.</span></span>

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

### <span data-ttu-id="6915e-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6915e-185">CommonParameters</span></span>
<span data-ttu-id="6915e-186">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6915e-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6915e-187">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6915e-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6915e-188">輸入</span><span class="sxs-lookup"><span data-stu-id="6915e-188">INPUTS</span></span>

### <span data-ttu-id="6915e-189">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="6915e-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6915e-190">System.object</span><span class="sxs-lookup"><span data-stu-id="6915e-190">System.String</span></span>

### <span data-ttu-id="6915e-191">PsApiManagementSchema []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="6915e-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="6915e-192">System.object []</span><span class="sxs-lookup"><span data-stu-id="6915e-192">System.String[]</span></span>

## <span data-ttu-id="6915e-193">輸出</span><span class="sxs-lookup"><span data-stu-id="6915e-193">OUTPUTS</span></span>

### <span data-ttu-id="6915e-194">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="6915e-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="6915e-195">筆記</span><span class="sxs-lookup"><span data-stu-id="6915e-195">NOTES</span></span>

## <span data-ttu-id="6915e-196">相關連結</span><span class="sxs-lookup"><span data-stu-id="6915e-196">RELATED LINKS</span></span>

[<span data-ttu-id="6915e-197">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6915e-197">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="6915e-198">AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6915e-198">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="6915e-199">匯入-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6915e-199">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="6915e-200">移除-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6915e-200">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="6915e-201">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6915e-201">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


