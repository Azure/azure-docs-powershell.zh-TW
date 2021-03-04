---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 61c02917d5381753ec8fd9e4b7560f68722d5f19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904554"
---
# <span data-ttu-id="4cec2-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4cec2-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="4cec2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4cec2-102">SYNOPSIS</span></span>
<span data-ttu-id="4cec2-103">建立 API。</span><span class="sxs-lookup"><span data-stu-id="4cec2-103">Creates an API.</span></span>

## <span data-ttu-id="4cec2-104">語法</span><span class="sxs-lookup"><span data-stu-id="4cec2-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cec2-105">描述</span><span class="sxs-lookup"><span data-stu-id="4cec2-105">DESCRIPTION</span></span>
<span data-ttu-id="4cec2-106">**New-AzApiManagementApi** Cmdlet 會建立 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="4cec2-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="4cec2-107">例子</span><span class="sxs-lookup"><span data-stu-id="4cec2-107">EXAMPLES</span></span>

### <span data-ttu-id="4cec2-108">範例 1：建立 API</span><span class="sxs-lookup"><span data-stu-id="4cec2-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="4cec2-109">此命令會建立一個名為 EchoApi 的 API，並包含指定的 URL。</span><span class="sxs-lookup"><span data-stu-id="4cec2-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="4cec2-110">範例 2：從 echo-api 複製所有作業、標記、產品與策略到 ApiVersionSet 以建立 API</span><span class="sxs-lookup"><span data-stu-id="4cec2-110">Example 2: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
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

<span data-ttu-id="4cec2-111">此命令在 `echoapiv3` ApiVersionSet 中建立 API，並複製來源 Api 的所有 `xmsVersionSet` 作業、標籤和策略 `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="4cec2-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="4cec2-112">它會覆蓋 SubscriptionRequired、ServiceUrl、Path、Protocols</span><span class="sxs-lookup"><span data-stu-id="4cec2-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

### <span data-ttu-id="4cec2-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="4cec2-113">Example 3</span></span>

<span data-ttu-id="4cec2-114">建立 API。</span><span class="sxs-lookup"><span data-stu-id="4cec2-114">Creates an API.</span></span> <span data-ttu-id="4cec2-115"> (自動) </span><span class="sxs-lookup"><span data-stu-id="4cec2-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementApi -ApiId '0001' -Context <PsApiManagementContext> -Name 'Echo api' -Path 'echov3' -Protocols Http -ServiceUrl 'https://contoso.com/apis/echo'
```

## <span data-ttu-id="4cec2-116">參數</span><span class="sxs-lookup"><span data-stu-id="4cec2-116">PARAMETERS</span></span>

### <span data-ttu-id="4cec2-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4cec2-117">-ApiId</span></span>
<span data-ttu-id="4cec2-118">指定要建立之 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4cec2-118">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="4cec2-119">如果您未指定此參數，此 Cmdlet 會產生您的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4cec2-119">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="4cec2-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4cec2-120">-ApiVersion</span></span>
<span data-ttu-id="4cec2-121">要建立 Api 版本的 Api。</span><span class="sxs-lookup"><span data-stu-id="4cec2-121">Api Version of the Api to create.</span></span> <span data-ttu-id="4cec2-122">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="4cec2-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="4cec2-123">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="4cec2-123">-ApiVersionDescription</span></span>
<span data-ttu-id="4cec2-124">Api 版本描述。</span><span class="sxs-lookup"><span data-stu-id="4cec2-124">Api Version Description.</span></span> <span data-ttu-id="4cec2-125">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="4cec2-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="4cec2-126">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="4cec2-126">-ApiVersionSetId</span></span>
<span data-ttu-id="4cec2-127">相關 Api 版本集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4cec2-127">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="4cec2-128">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="4cec2-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="4cec2-129">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="4cec2-129">-AuthorizationScope</span></span>
<span data-ttu-id="4cec2-130">指定 OAuth 作業範圍。</span><span class="sxs-lookup"><span data-stu-id="4cec2-130">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="4cec2-131">預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="4cec2-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="4cec2-132">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="4cec2-132">-AuthorizationServerId</span></span>
<span data-ttu-id="4cec2-133">指定 OAuth 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="4cec2-133">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="4cec2-134">預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="4cec2-134">The default value is $Null.</span></span>
<span data-ttu-id="4cec2-135">如果已指定 *AuthorizationScope，則必須* 指定此參數。</span><span class="sxs-lookup"><span data-stu-id="4cec2-135">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="4cec2-136">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="4cec2-136">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="4cec2-137">將存取權杖傳遞至 API 的 OpenId 授權伺服器機制。</span><span class="sxs-lookup"><span data-stu-id="4cec2-137">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="4cec2-138">參照 http://tools.ietf.org/html/rfc6749#section-4 到 。</span><span class="sxs-lookup"><span data-stu-id="4cec2-138">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="4cec2-139">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="4cec2-139">This parameter is optional.</span></span> <span data-ttu-id="4cec2-140">預設值會$null。</span><span class="sxs-lookup"><span data-stu-id="4cec2-140">Default value is $null.</span></span>

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

### <span data-ttu-id="4cec2-141">-內容</span><span class="sxs-lookup"><span data-stu-id="4cec2-141">-Context</span></span>
<span data-ttu-id="4cec2-142">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="4cec2-142">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4cec2-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cec2-143">-DefaultProfile</span></span>
<span data-ttu-id="4cec2-144">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4cec2-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cec2-145">-描述</span><span class="sxs-lookup"><span data-stu-id="4cec2-145">-Description</span></span>
<span data-ttu-id="4cec2-146">指定網頁 API 的描述。</span><span class="sxs-lookup"><span data-stu-id="4cec2-146">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="4cec2-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="4cec2-147">-Name</span></span>
<span data-ttu-id="4cec2-148">指定 Web API 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cec2-148">Specifies the name of the web API.</span></span>
<span data-ttu-id="4cec2-149">這是顯示在開發人員和系統管理入口網站中的 API 公用名稱。</span><span class="sxs-lookup"><span data-stu-id="4cec2-149">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="4cec2-150">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="4cec2-150">-OpenIdProviderId</span></span>
<span data-ttu-id="4cec2-151">OpenId 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="4cec2-151">OpenId authorization server identifier.</span></span> <span data-ttu-id="4cec2-152">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="4cec2-152">This parameter is optional.</span></span> <span data-ttu-id="4cec2-153">預設值會$null。</span><span class="sxs-lookup"><span data-stu-id="4cec2-153">Default value is $null.</span></span> <span data-ttu-id="4cec2-154">必須指定已指定 BearerTokenSendingMethods。</span><span class="sxs-lookup"><span data-stu-id="4cec2-154">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="4cec2-155">-路徑</span><span class="sxs-lookup"><span data-stu-id="4cec2-155">-Path</span></span>
<span data-ttu-id="4cec2-156">指定 Web API 路徑，這是 API 公用 URL 的最後一部分，並對應到系統管理入口網站中的 Web API URL 尾碼欄位。</span><span class="sxs-lookup"><span data-stu-id="4cec2-156">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="4cec2-157">API 消費者會使用這個 URL 來傳送要求到 Web 服務，而且必須長 1 到 400 個字元。</span><span class="sxs-lookup"><span data-stu-id="4cec2-157">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="4cec2-158">預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="4cec2-158">The default value is $Null.</span></span>

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

### <span data-ttu-id="4cec2-159">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="4cec2-159">-ProductIds</span></span>
<span data-ttu-id="4cec2-160">指定要新增 API 的產品識別碼 陣列。</span><span class="sxs-lookup"><span data-stu-id="4cec2-160">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="4cec2-161">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="4cec2-161">-Protocols</span></span>
<span data-ttu-id="4cec2-162">指定 Web API 通訊協定陣列。</span><span class="sxs-lookup"><span data-stu-id="4cec2-162">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="4cec2-163">有效的值為 HTTP、HTTPs。</span><span class="sxs-lookup"><span data-stu-id="4cec2-163">Valid values are http, https.</span></span>
<span data-ttu-id="4cec2-164">這些是提供 API 的 Web 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4cec2-164">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="4cec2-165">預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="4cec2-165">The default value is $Null.</span></span>

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

### <span data-ttu-id="4cec2-166">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="4cec2-166">-ServiceUrl</span></span>
<span data-ttu-id="4cec2-167">指定公開 API 的 Web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="4cec2-167">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="4cec2-168">此 URL 僅由 Azure API 管理使用，不會公開。</span><span class="sxs-lookup"><span data-stu-id="4cec2-168">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="4cec2-169">URL 必須長 1 到 2000 個字元。</span><span class="sxs-lookup"><span data-stu-id="4cec2-169">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="4cec2-170">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="4cec2-170">-SourceApiId</span></span>
<span data-ttu-id="4cec2-171">來源 API 的 Api 識別碼。</span><span class="sxs-lookup"><span data-stu-id="4cec2-171">Api identifier of the source API.</span></span> <span data-ttu-id="4cec2-172">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="4cec2-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="4cec2-173">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="4cec2-173">-SourceApiRevision</span></span>
<span data-ttu-id="4cec2-174">來源 API 的 Api 修訂。</span><span class="sxs-lookup"><span data-stu-id="4cec2-174">Api Revision of the source API.</span></span> <span data-ttu-id="4cec2-175">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="4cec2-175">This parameter is optional.</span></span>

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

### <span data-ttu-id="4cec2-176">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="4cec2-176">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="4cec2-177">指定訂閱金鑰標題名稱。</span><span class="sxs-lookup"><span data-stu-id="4cec2-177">Specifies the subscription key header name.</span></span>
<span data-ttu-id="4cec2-178">預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="4cec2-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="4cec2-179">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="4cec2-179">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="4cec2-180">指定訂閱金鑰查詢字串參數名稱。</span><span class="sxs-lookup"><span data-stu-id="4cec2-180">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="4cec2-181">預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="4cec2-181">The default value is $Null.</span></span>

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

### <span data-ttu-id="4cec2-182">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="4cec2-182">-SubscriptionRequired</span></span>
<span data-ttu-id="4cec2-183">針對 Api 的要求，標出要強制執行 SubscriptionRequired。</span><span class="sxs-lookup"><span data-stu-id="4cec2-183">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="4cec2-184">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="4cec2-184">This parameter is optional.</span></span>

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

### <span data-ttu-id="4cec2-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cec2-185">CommonParameters</span></span>
<span data-ttu-id="4cec2-186">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4cec2-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cec2-187">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4cec2-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cec2-188">輸入</span><span class="sxs-lookup"><span data-stu-id="4cec2-188">INPUTS</span></span>

### <span data-ttu-id="4cec2-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="4cec2-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4cec2-190">System.String</span><span class="sxs-lookup"><span data-stu-id="4cec2-190">System.String</span></span>

### <span data-ttu-id="4cec2-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="4cec2-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="4cec2-192">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4cec2-192">System.String[]</span></span>

## <span data-ttu-id="4cec2-193">輸出</span><span class="sxs-lookup"><span data-stu-id="4cec2-193">OUTPUTS</span></span>

### <span data-ttu-id="4cec2-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4cec2-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="4cec2-195">筆記</span><span class="sxs-lookup"><span data-stu-id="4cec2-195">NOTES</span></span>

## <span data-ttu-id="4cec2-196">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cec2-196">RELATED LINKS</span></span>

[<span data-ttu-id="4cec2-197">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4cec2-197">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="4cec2-198">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4cec2-198">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="4cec2-199">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4cec2-199">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="4cec2-200">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4cec2-200">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="4cec2-201">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4cec2-201">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


