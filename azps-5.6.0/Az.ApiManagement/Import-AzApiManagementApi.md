---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 604ba6be4129b627f10f879e6272eb0bc1cfbb2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904558"
---
# <span data-ttu-id="de67d-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="de67d-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="de67d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="de67d-102">SYNOPSIS</span></span>
<span data-ttu-id="de67d-103">從檔案或 URL 中導入 API。</span><span class="sxs-lookup"><span data-stu-id="de67d-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="de67d-104">語法</span><span class="sxs-lookup"><span data-stu-id="de67d-104">SYNTAX</span></span>

### <span data-ttu-id="de67d-105">ImportFromLocalFile (預設) </span><span class="sxs-lookup"><span data-stu-id="de67d-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de67d-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="de67d-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de67d-107">描述</span><span class="sxs-lookup"><span data-stu-id="de67d-107">DESCRIPTION</span></span>
<span data-ttu-id="de67d-108">**Import-AzApiManagementApi** Cmdlet 會從 Web 應用程式描述語言 (WADL) 、Web 服務描述語言 (WSDL) 或 Swa解格式中的檔案或 URL 中，將 Azure API 管理 API 導入。</span><span class="sxs-lookup"><span data-stu-id="de67d-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="de67d-109">例子</span><span class="sxs-lookup"><span data-stu-id="de67d-109">EXAMPLES</span></span>

### <span data-ttu-id="de67d-110">範例 1：從 WADL 檔案中匯出 API</span><span class="sxs-lookup"><span data-stu-id="de67d-110">Example 1: Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="de67d-111">此命令會從指定的 WADL 檔案中輸入 API。</span><span class="sxs-lookup"><span data-stu-id="de67d-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="de67d-112">範例 2：從 Swagger 檔案中匯出 API</span><span class="sxs-lookup"><span data-stu-id="de67d-112">Example 2: Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="de67d-113">此命令會從指定的 Swagger 檔案中輸入 API。</span><span class="sxs-lookup"><span data-stu-id="de67d-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="de67d-114">範例 3：從 WADL 連結導入 API</span><span class="sxs-lookup"><span data-stu-id="de67d-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="de67d-115">此命令會從指定的 WADL 連結中導入 API。</span><span class="sxs-lookup"><span data-stu-id="de67d-115">This command imports an API from the specified WADL link.</span></span>

### <span data-ttu-id="de67d-116">範例 4：從 Open Api 連結導入 API</span><span class="sxs-lookup"><span data-stu-id="de67d-116">Example 4: Import an API from a Open Api Link</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationFormat OpenApi -SpecificationUrl https://raw.githubusercontent.com/OAI/OpenAPI-Specification/master/examples/v3.0/petstore.yaml -Path "petstore30"

ApiId                         : af3f57bab399455aa875d7050654e9d1
Name                          : Swagger Petstore
Description                   :
ServiceUrl                    : http://petstore.swagger.io/v1
Path                          : petstore30
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    :
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/af3f57bab399455aa875d7050654e9d1     
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="de67d-117">此命令會從指定的 Open 3.0 規格連結中輸入 API。</span><span class="sxs-lookup"><span data-stu-id="de67d-117">This command imports an API from the specified Open 3.0 specification link.</span></span>

### <span data-ttu-id="de67d-118">範例 5：從 Open Api 連結將 API 導入 ApiVersion 集</span><span class="sxs-lookup"><span data-stu-id="de67d-118">Example 5:  Import an API from a Open Api Link into a ApiVersion Set</span></span>

```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationPath "C:\contoso\specifications\uspto.yml" -SpecificationFormat OpenApi -Path uspostal -ApiVersionSetId 0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd -ApiVersion v2

ApiId                         : 6c3f20c66e5745b19229d06cd865948f
Name                          : USPTO Data Set API
Description                   : The Data Set API (DSAPI) allows the public users to discover and search USPTO exported data sets. This is a generic API that allows USPTO users to make any CSV based data files
                                searchable through API. With the help of GET call, it returns the list of data fields that are searchable. With the help of POST call, data can be fetched based on the filters on the    
                                field names. Please note that POST call is used to search the actual data. The reason for the POST call is that it allows users to specify any complex search criteria without worry      
                                about the GET size limitations as well as encoding of the input parameters.
ServiceUrl                    : https://developer.uspto.gov/ds-api
Path                          : uspostal
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v2
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd
Id                            : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis/6c3f20c66e5745b19229d06cd865948f    
ResourceGroupName             : Api-Default-East-US
ServiceName                   : contoso
```

<span data-ttu-id="de67d-119">此命令會從指定的 Open 3.0 規格檔導入 API，然後建立新 ApiVersion。</span><span class="sxs-lookup"><span data-stu-id="de67d-119">This command imports an API from the specified Open 3.0 specification document and create a new ApiVersion.</span></span>

## <span data-ttu-id="de67d-120">參數</span><span class="sxs-lookup"><span data-stu-id="de67d-120">PARAMETERS</span></span>

### <span data-ttu-id="de67d-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="de67d-121">-ApiId</span></span>
<span data-ttu-id="de67d-122">指定要匯出之 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="de67d-122">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="de67d-123">如果您未指定此參數，系統即會針對您產生識別碼。</span><span class="sxs-lookup"><span data-stu-id="de67d-123">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="de67d-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="de67d-124">-ApiRevision</span></span>
<span data-ttu-id="de67d-125">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="de67d-125">Identifier of API Revision.</span></span> <span data-ttu-id="de67d-126">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="de67d-126">This parameter is optional.</span></span> <span data-ttu-id="de67d-127">如果未指定，將會將匯出完成至目前使用中的修訂或新的 api。</span><span class="sxs-lookup"><span data-stu-id="de67d-127">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="de67d-128">-ApiType</span><span class="sxs-lookup"><span data-stu-id="de67d-128">-ApiType</span></span>
<span data-ttu-id="de67d-129">此參數為選擇性，預設值為 HTTP。</span><span class="sxs-lookup"><span data-stu-id="de67d-129">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="de67d-130">Soap 選項僅適用于輸入 WSDL，並且會建立 SOAP Passthrough API。</span><span class="sxs-lookup"><span data-stu-id="de67d-130">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de67d-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="de67d-131">-ApiVersion</span></span>
<span data-ttu-id="de67d-132">要建立 Api 版本的 Api。</span><span class="sxs-lookup"><span data-stu-id="de67d-132">Api Version of the Api to create.</span></span> <span data-ttu-id="de67d-133">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="de67d-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="de67d-134">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="de67d-134">-ApiVersionSetId</span></span>
<span data-ttu-id="de67d-135">相關 Api 版本集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="de67d-135">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="de67d-136">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="de67d-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="de67d-137">-內容</span><span class="sxs-lookup"><span data-stu-id="de67d-137">-Context</span></span>
<span data-ttu-id="de67d-138">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="de67d-138">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="de67d-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de67d-139">-DefaultProfile</span></span>
<span data-ttu-id="de67d-140">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="de67d-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de67d-141">-路徑</span><span class="sxs-lookup"><span data-stu-id="de67d-141">-Path</span></span>
<span data-ttu-id="de67d-142">指定 Web API 路徑做為 API 公用 URL 的最後一部分。</span><span class="sxs-lookup"><span data-stu-id="de67d-142">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="de67d-143">API 消費者會使用這個 URL 來傳送要求至 Web 服務。</span><span class="sxs-lookup"><span data-stu-id="de67d-143">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="de67d-144">必須長 1 到 400 個字元。</span><span class="sxs-lookup"><span data-stu-id="de67d-144">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="de67d-145">預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="de67d-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="de67d-146">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="de67d-146">-Protocol</span></span>
<span data-ttu-id="de67d-147">Web API 通訊協定 (HTTP、HTTPs) 。</span><span class="sxs-lookup"><span data-stu-id="de67d-147">Web API protocols (http, https).</span></span> <span data-ttu-id="de67d-148">提供 API 的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="de67d-148">Protocols over which API is made available.</span></span> <span data-ttu-id="de67d-149">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="de67d-149">This parameter is optional.</span></span> <span data-ttu-id="de67d-150">如果提供的話，它會優先于規格檔中指定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="de67d-150">If provided it will override the protocols specified in the specifications document.</span></span>

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

### <span data-ttu-id="de67d-151">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="de67d-151">-ServiceUrl</span></span>
<span data-ttu-id="de67d-152">公開 API 之 Web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="de67d-152">A URL of the web service exposing the API.</span></span> <span data-ttu-id="de67d-153">此 URL 將僅由 Azure API 管理使用，不會公開。</span><span class="sxs-lookup"><span data-stu-id="de67d-153">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="de67d-154">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="de67d-154">This parameter is optional.</span></span> <span data-ttu-id="de67d-155">如果提供的話，它會覆蓋在規格檔中指定的 ServiceUrl。</span><span class="sxs-lookup"><span data-stu-id="de67d-155">If provided it will override the ServiceUrl specified in the Specifications document.</span></span>

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

### <span data-ttu-id="de67d-156">-規格格式</span><span class="sxs-lookup"><span data-stu-id="de67d-156">-SpecificationFormat</span></span>
<span data-ttu-id="de67d-157">指定規格格式。</span><span class="sxs-lookup"><span data-stu-id="de67d-157">Specifies the specification format.</span></span>
<span data-ttu-id="de67d-158">psdx_paramvalues Wadl、Wsdl 和 Swagger。</span><span class="sxs-lookup"><span data-stu-id="de67d-158">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de67d-159">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="de67d-159">-SpecificationPath</span></span>
<span data-ttu-id="de67d-160">指定規格檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="de67d-160">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromLocalFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de67d-161">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="de67d-161">-SpecificationUrl</span></span>
<span data-ttu-id="de67d-162">指定規格 URL。</span><span class="sxs-lookup"><span data-stu-id="de67d-162">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de67d-163">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="de67d-163">-WsdlEndpointName</span></span>
<span data-ttu-id="de67d-164">要匯出的 WSDL 端點 (埠) 名稱。</span><span class="sxs-lookup"><span data-stu-id="de67d-164">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="de67d-165">必須長 1 到 400 個字元。</span><span class="sxs-lookup"><span data-stu-id="de67d-165">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="de67d-166">此參數為選擇性，而且只有在輸入 Wsdl 時才需要。</span><span class="sxs-lookup"><span data-stu-id="de67d-166">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="de67d-167">預設值會$null。</span><span class="sxs-lookup"><span data-stu-id="de67d-167">Default value is $null.</span></span>

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

### <span data-ttu-id="de67d-168">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="de67d-168">-WsdlServiceName</span></span>
<span data-ttu-id="de67d-169">要導入的 WSDL 服務的當地名稱。</span><span class="sxs-lookup"><span data-stu-id="de67d-169">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="de67d-170">必須長 1 到 400 個字元。</span><span class="sxs-lookup"><span data-stu-id="de67d-170">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="de67d-171">此參數為選擇性，而且只有在輸入 Wsdl 時才需要。</span><span class="sxs-lookup"><span data-stu-id="de67d-171">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="de67d-172">預設值會$null。</span><span class="sxs-lookup"><span data-stu-id="de67d-172">Default value is $null.</span></span>

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

### <span data-ttu-id="de67d-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de67d-173">CommonParameters</span></span>
<span data-ttu-id="de67d-174">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="de67d-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de67d-175">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de67d-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de67d-176">輸入</span><span class="sxs-lookup"><span data-stu-id="de67d-176">INPUTS</span></span>

### <span data-ttu-id="de67d-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="de67d-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="de67d-178">System.String</span><span class="sxs-lookup"><span data-stu-id="de67d-178">System.String</span></span>

### <span data-ttu-id="de67d-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="de67d-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="de67d-180">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="de67d-180">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="de67d-181">輸出</span><span class="sxs-lookup"><span data-stu-id="de67d-181">OUTPUTS</span></span>

### <span data-ttu-id="de67d-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="de67d-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="de67d-183">筆記</span><span class="sxs-lookup"><span data-stu-id="de67d-183">NOTES</span></span>

## <span data-ttu-id="de67d-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="de67d-184">RELATED LINKS</span></span>

[<span data-ttu-id="de67d-185">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="de67d-185">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="de67d-186">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="de67d-186">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="de67d-187">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="de67d-187">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="de67d-188">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="de67d-188">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="de67d-189">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="de67d-189">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


