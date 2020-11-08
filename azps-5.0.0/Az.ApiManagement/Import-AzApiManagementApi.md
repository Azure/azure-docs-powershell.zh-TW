---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 5a9141cf0f609eedd35c25f6fd3d7977201e58c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137908"
---
# <span data-ttu-id="84f5a-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="84f5a-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="84f5a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="84f5a-103">從檔案或 URL 匯入 API。</span><span class="sxs-lookup"><span data-stu-id="84f5a-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="84f5a-104">句法</span><span class="sxs-lookup"><span data-stu-id="84f5a-104">SYNTAX</span></span>

### <span data-ttu-id="84f5a-105">ImportFromLocalFile (預設) </span><span class="sxs-lookup"><span data-stu-id="84f5a-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84f5a-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="84f5a-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84f5a-107">說明</span><span class="sxs-lookup"><span data-stu-id="84f5a-107">DESCRIPTION</span></span>
<span data-ttu-id="84f5a-108">匯 **入-AzApiManagementApi** Cmdlet 會從 Web 應用程式描述語言 (WADL) 、Web 服務描述語言 (WSDL) 或 Swagger 格式），從檔案或 URL 中匯入 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="84f5a-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="84f5a-109">示例</span><span class="sxs-lookup"><span data-stu-id="84f5a-109">EXAMPLES</span></span>

### <span data-ttu-id="84f5a-110">範例1：從 WADL 檔案匯入 API</span><span class="sxs-lookup"><span data-stu-id="84f5a-110">Example 1: Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="84f5a-111">這個命令會從指定的 WADL 檔案匯入 API。</span><span class="sxs-lookup"><span data-stu-id="84f5a-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="84f5a-112">範例2：從 Swagger 檔案匯入 API</span><span class="sxs-lookup"><span data-stu-id="84f5a-112">Example 2: Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="84f5a-113">這個命令會從指定的 Swagger 檔案匯入 API。</span><span class="sxs-lookup"><span data-stu-id="84f5a-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="84f5a-114">範例3：從 WADL 連結匯入 API</span><span class="sxs-lookup"><span data-stu-id="84f5a-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="84f5a-115">這個命令會從指定的 WADL 連結匯入 API。</span><span class="sxs-lookup"><span data-stu-id="84f5a-115">This command imports an API from the specified WADL link.</span></span>

### <span data-ttu-id="84f5a-116">範例4：從開放式 Api 連結匯入 API</span><span class="sxs-lookup"><span data-stu-id="84f5a-116">Example 4: Import an API from a Open Api Link</span></span>
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

<span data-ttu-id="84f5a-117">這個命令會從指定的 Open 3.0 規格連結中匯入 API。</span><span class="sxs-lookup"><span data-stu-id="84f5a-117">This command imports an API from the specified Open 3.0 specification link.</span></span>

### <span data-ttu-id="84f5a-118">範例5：從開放式 Api 連結匯入 API 至 ApiVersion 集合</span><span class="sxs-lookup"><span data-stu-id="84f5a-118">Example 5:  Import an API from a Open Api Link into a ApiVersion Set</span></span>

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

<span data-ttu-id="84f5a-119">這個命令會從指定的開啟3.0 規格檔中匯入 API，並建立新的 ApiVersion。</span><span class="sxs-lookup"><span data-stu-id="84f5a-119">This command imports an API from the specified Open 3.0 specification document and create a new ApiVersion.</span></span>

## <span data-ttu-id="84f5a-120">參數</span><span class="sxs-lookup"><span data-stu-id="84f5a-120">PARAMETERS</span></span>

### <span data-ttu-id="84f5a-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="84f5a-121">-ApiId</span></span>
<span data-ttu-id="84f5a-122">指定要匯入的 API ID。</span><span class="sxs-lookup"><span data-stu-id="84f5a-122">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="84f5a-123">如果您沒有指定此參數，系統會為您產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="84f5a-123">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="84f5a-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="84f5a-124">-ApiRevision</span></span>
<span data-ttu-id="84f5a-125">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="84f5a-125">Identifier of API Revision.</span></span> <span data-ttu-id="84f5a-126">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="84f5a-126">This parameter is optional.</span></span> <span data-ttu-id="84f5a-127">如果未指定，將會在目前的活動修訂或新的 api 上完成匯入。</span><span class="sxs-lookup"><span data-stu-id="84f5a-127">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="84f5a-128">-ApiType</span><span class="sxs-lookup"><span data-stu-id="84f5a-128">-ApiType</span></span>
<span data-ttu-id="84f5a-129">這個參數是預設值 Http 的選用。</span><span class="sxs-lookup"><span data-stu-id="84f5a-129">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="84f5a-130">Soap 選項只適用于匯入 WSDL，且將建立 SOAP 直通 API。</span><span class="sxs-lookup"><span data-stu-id="84f5a-130">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="84f5a-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="84f5a-131">-ApiVersion</span></span>
<span data-ttu-id="84f5a-132">要建立的 api api 版本。</span><span class="sxs-lookup"><span data-stu-id="84f5a-132">Api Version of the Api to create.</span></span> <span data-ttu-id="84f5a-133">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="84f5a-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="84f5a-134">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="84f5a-134">-ApiVersionSetId</span></span>
<span data-ttu-id="84f5a-135">相關 Api 版本集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="84f5a-135">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="84f5a-136">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="84f5a-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="84f5a-137">-內容</span><span class="sxs-lookup"><span data-stu-id="84f5a-137">-Context</span></span>
<span data-ttu-id="84f5a-138">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="84f5a-138">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="84f5a-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84f5a-139">-DefaultProfile</span></span>
<span data-ttu-id="84f5a-140">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84f5a-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84f5a-141">-Path</span><span class="sxs-lookup"><span data-stu-id="84f5a-141">-Path</span></span>
<span data-ttu-id="84f5a-142">將 web API 路徑指定為 API 公用 URL 的最後一部分。</span><span class="sxs-lookup"><span data-stu-id="84f5a-142">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="84f5a-143">這個 URL 是由 API 消費者用來傳送要求至 web 服務的。</span><span class="sxs-lookup"><span data-stu-id="84f5a-143">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="84f5a-144">長度必須是1到400個字元。</span><span class="sxs-lookup"><span data-stu-id="84f5a-144">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="84f5a-145">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="84f5a-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="84f5a-146">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="84f5a-146">-Protocol</span></span>
<span data-ttu-id="84f5a-147">Web API 通訊協定 (HTTP、HTTPs) 。</span><span class="sxs-lookup"><span data-stu-id="84f5a-147">Web API protocols (http, https).</span></span> <span data-ttu-id="84f5a-148">提供可用 API 的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="84f5a-148">Protocols over which API is made available.</span></span> <span data-ttu-id="84f5a-149">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="84f5a-149">This parameter is optional.</span></span> <span data-ttu-id="84f5a-150">如果有的話，會覆寫 [規格] 檔中指定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="84f5a-150">If provided it will override the protocols specified in the specifications document.</span></span>

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

### <span data-ttu-id="84f5a-151">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="84f5a-151">-ServiceUrl</span></span>
<span data-ttu-id="84f5a-152">公開 API 之 web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="84f5a-152">A URL of the web service exposing the API.</span></span> <span data-ttu-id="84f5a-153">這個 URL 將只由 Azure API 管理使用，不會公開。</span><span class="sxs-lookup"><span data-stu-id="84f5a-153">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="84f5a-154">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="84f5a-154">This parameter is optional.</span></span> <span data-ttu-id="84f5a-155">如果有的話，會覆寫 [規格] 檔中指定的 ServiceUrl。</span><span class="sxs-lookup"><span data-stu-id="84f5a-155">If provided it will override the ServiceUrl specified in the Specifications document.</span></span>

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

### <span data-ttu-id="84f5a-156">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="84f5a-156">-SpecificationFormat</span></span>
<span data-ttu-id="84f5a-157">指定規格格式。</span><span class="sxs-lookup"><span data-stu-id="84f5a-157">Specifies the specification format.</span></span>
<span data-ttu-id="84f5a-158">psdx_paramvalues Wadl、Wsdl 和 Swagger。</span><span class="sxs-lookup"><span data-stu-id="84f5a-158">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

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

### <span data-ttu-id="84f5a-159">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="84f5a-159">-SpecificationPath</span></span>
<span data-ttu-id="84f5a-160">指定規格檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="84f5a-160">Specifies the specification file path.</span></span>

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

### <span data-ttu-id="84f5a-161">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="84f5a-161">-SpecificationUrl</span></span>
<span data-ttu-id="84f5a-162">指定規格 URL。</span><span class="sxs-lookup"><span data-stu-id="84f5a-162">Specifies the specification URL.</span></span>

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

### <span data-ttu-id="84f5a-163">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="84f5a-163">-WsdlEndpointName</span></span>
<span data-ttu-id="84f5a-164">要匯入 (埠) 的 WSDL 端點本機名稱。</span><span class="sxs-lookup"><span data-stu-id="84f5a-164">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="84f5a-165">長度必須是1到400個字元。</span><span class="sxs-lookup"><span data-stu-id="84f5a-165">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="84f5a-166">這個參數是選擇性的，只有在匯入 Wsdl 時才需要。</span><span class="sxs-lookup"><span data-stu-id="84f5a-166">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="84f5a-167">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="84f5a-167">Default value is $null.</span></span>

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

### <span data-ttu-id="84f5a-168">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="84f5a-168">-WsdlServiceName</span></span>
<span data-ttu-id="84f5a-169">要匯入之 WSDL 服務的本機名稱。</span><span class="sxs-lookup"><span data-stu-id="84f5a-169">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="84f5a-170">長度必須是1到400個字元。</span><span class="sxs-lookup"><span data-stu-id="84f5a-170">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="84f5a-171">這個參數是選擇性的，只有在匯入 Wsdl 時才需要。</span><span class="sxs-lookup"><span data-stu-id="84f5a-171">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="84f5a-172">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="84f5a-172">Default value is $null.</span></span>

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

### <span data-ttu-id="84f5a-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84f5a-173">CommonParameters</span></span>
<span data-ttu-id="84f5a-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84f5a-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84f5a-175">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="84f5a-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84f5a-176">輸入</span><span class="sxs-lookup"><span data-stu-id="84f5a-176">INPUTS</span></span>

### <span data-ttu-id="84f5a-177">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="84f5a-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="84f5a-178">System.object</span><span class="sxs-lookup"><span data-stu-id="84f5a-178">System.String</span></span>

### <span data-ttu-id="84f5a-179">ServiceManagement. PsApiManagementApiFormat （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="84f5a-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="84f5a-180">ApiManagement 為 Nullable "1 [PsApiManagementApiType，，ServiceManagement，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））））））</span><span class="sxs-lookup"><span data-stu-id="84f5a-180">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="84f5a-181">輸出</span><span class="sxs-lookup"><span data-stu-id="84f5a-181">OUTPUTS</span></span>

### <span data-ttu-id="84f5a-182">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="84f5a-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="84f5a-183">筆記</span><span class="sxs-lookup"><span data-stu-id="84f5a-183">NOTES</span></span>

## <span data-ttu-id="84f5a-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="84f5a-184">RELATED LINKS</span></span>

[<span data-ttu-id="84f5a-185">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="84f5a-185">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="84f5a-186">AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="84f5a-186">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="84f5a-187">新-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="84f5a-187">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="84f5a-188">移除-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="84f5a-188">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="84f5a-189">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="84f5a-189">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


