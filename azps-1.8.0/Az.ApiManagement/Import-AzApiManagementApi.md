---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 690ebbfb1bb3cca6de8feb1f199068510e41f1d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611600"
---
# <span data-ttu-id="95169-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="95169-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="95169-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95169-102">SYNOPSIS</span></span>
<span data-ttu-id="95169-103">從檔案或 URL 匯入 API。</span><span class="sxs-lookup"><span data-stu-id="95169-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="95169-104">句法</span><span class="sxs-lookup"><span data-stu-id="95169-104">SYNTAX</span></span>

### <span data-ttu-id="95169-105">ImportFromLocalFile (預設) </span><span class="sxs-lookup"><span data-stu-id="95169-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95169-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="95169-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95169-107">說明</span><span class="sxs-lookup"><span data-stu-id="95169-107">DESCRIPTION</span></span>
<span data-ttu-id="95169-108">匯 **入-AzApiManagementApi** Cmdlet 會從 Web 應用程式描述語言 (WADL) 、Web 服務描述語言 (WSDL) 或 Swagger 格式），從檔案或 URL 中匯入 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="95169-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="95169-109">示例</span><span class="sxs-lookup"><span data-stu-id="95169-109">EXAMPLES</span></span>

### <span data-ttu-id="95169-110">範例1從 WADL 檔案匯入 API</span><span class="sxs-lookup"><span data-stu-id="95169-110">Example 1 Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="95169-111">這個命令會從指定的 WADL 檔案匯入 API。</span><span class="sxs-lookup"><span data-stu-id="95169-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="95169-112">範例2從 Swagger 檔案匯入 API</span><span class="sxs-lookup"><span data-stu-id="95169-112">Example 2 Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="95169-113">這個命令會從指定的 Swagger 檔案匯入 API。</span><span class="sxs-lookup"><span data-stu-id="95169-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="95169-114">範例3：從 WADL 連結匯入 API</span><span class="sxs-lookup"><span data-stu-id="95169-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="95169-115">這個命令會從指定的 WADL 連結匯入 API。</span><span class="sxs-lookup"><span data-stu-id="95169-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="95169-116">參數</span><span class="sxs-lookup"><span data-stu-id="95169-116">PARAMETERS</span></span>

### <span data-ttu-id="95169-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="95169-117">-ApiId</span></span>
<span data-ttu-id="95169-118">指定要匯入的 API ID。</span><span class="sxs-lookup"><span data-stu-id="95169-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="95169-119">如果您沒有指定此參數，系統會為您產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="95169-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="95169-120">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="95169-120">-ApiRevision</span></span>
<span data-ttu-id="95169-121">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="95169-121">Identifier of API Revision.</span></span> <span data-ttu-id="95169-122">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="95169-122">This parameter is optional.</span></span> <span data-ttu-id="95169-123">如果未指定，將會在目前的活動修訂或新的 api 上完成匯入。</span><span class="sxs-lookup"><span data-stu-id="95169-123">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="95169-124">-ApiType</span><span class="sxs-lookup"><span data-stu-id="95169-124">-ApiType</span></span>
<span data-ttu-id="95169-125">這個參數是預設值 Http 的選用。</span><span class="sxs-lookup"><span data-stu-id="95169-125">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="95169-126">Soap 選項只適用于匯入 WSDL，且將建立 SOAP 直通 API。</span><span class="sxs-lookup"><span data-stu-id="95169-126">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="95169-127">-內容</span><span class="sxs-lookup"><span data-stu-id="95169-127">-Context</span></span>
<span data-ttu-id="95169-128">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="95169-128">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95169-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95169-129">-DefaultProfile</span></span>
<span data-ttu-id="95169-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="95169-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95169-131">-Path</span><span class="sxs-lookup"><span data-stu-id="95169-131">-Path</span></span>
<span data-ttu-id="95169-132">將 web API 路徑指定為 API 公用 URL 的最後一部分。</span><span class="sxs-lookup"><span data-stu-id="95169-132">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="95169-133">這個 URL 是由 API 消費者用來傳送要求至 web 服務的。</span><span class="sxs-lookup"><span data-stu-id="95169-133">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="95169-134">長度必須是1到400個字元。</span><span class="sxs-lookup"><span data-stu-id="95169-134">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="95169-135">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="95169-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="95169-136">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="95169-136">-SpecificationFormat</span></span>
<span data-ttu-id="95169-137">指定規格格式。</span><span class="sxs-lookup"><span data-stu-id="95169-137">Specifies the specification format.</span></span>
<span data-ttu-id="95169-138">psdx_paramvalues Wadl、Wsdl 和 Swagger。</span><span class="sxs-lookup"><span data-stu-id="95169-138">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95169-139">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="95169-139">-SpecificationPath</span></span>
<span data-ttu-id="95169-140">指定規格檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="95169-140">Specifies the specification file path.</span></span>

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

### <span data-ttu-id="95169-141">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="95169-141">-SpecificationUrl</span></span>
<span data-ttu-id="95169-142">指定規格 URL。</span><span class="sxs-lookup"><span data-stu-id="95169-142">Specifies the specification URL.</span></span>

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

### <span data-ttu-id="95169-143">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="95169-143">-WsdlEndpointName</span></span>
<span data-ttu-id="95169-144">要匯入 (埠) 的 WSDL 端點本機名稱。</span><span class="sxs-lookup"><span data-stu-id="95169-144">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="95169-145">長度必須是1到400個字元。</span><span class="sxs-lookup"><span data-stu-id="95169-145">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="95169-146">這個參數是選擇性的，只有在匯入 Wsdl 時才需要。</span><span class="sxs-lookup"><span data-stu-id="95169-146">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="95169-147">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="95169-147">Default value is $null.</span></span>

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

### <span data-ttu-id="95169-148">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="95169-148">-WsdlServiceName</span></span>
<span data-ttu-id="95169-149">要匯入之 WSDL 服務的本機名稱。</span><span class="sxs-lookup"><span data-stu-id="95169-149">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="95169-150">長度必須是1到400個字元。</span><span class="sxs-lookup"><span data-stu-id="95169-150">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="95169-151">這個參數是選擇性的，只有在匯入 Wsdl 時才需要。</span><span class="sxs-lookup"><span data-stu-id="95169-151">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="95169-152">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="95169-152">Default value is $null.</span></span>

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

### <span data-ttu-id="95169-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95169-153">CommonParameters</span></span>
<span data-ttu-id="95169-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95169-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95169-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="95169-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95169-156">輸入</span><span class="sxs-lookup"><span data-stu-id="95169-156">INPUTS</span></span>

### <span data-ttu-id="95169-157">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="95169-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="95169-158">System.object</span><span class="sxs-lookup"><span data-stu-id="95169-158">System.String</span></span>

### <span data-ttu-id="95169-159">ServiceManagement. PsApiManagementApiFormat （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="95169-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="95169-160">ApiManagement 為 Nullable "1 [PsApiManagementApiType，，ServiceManagement，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））））））</span><span class="sxs-lookup"><span data-stu-id="95169-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="95169-161">輸出</span><span class="sxs-lookup"><span data-stu-id="95169-161">OUTPUTS</span></span>

### <span data-ttu-id="95169-162">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="95169-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="95169-163">筆記</span><span class="sxs-lookup"><span data-stu-id="95169-163">NOTES</span></span>

## <span data-ttu-id="95169-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="95169-164">RELATED LINKS</span></span>

[<span data-ttu-id="95169-165">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="95169-165">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="95169-166">AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="95169-166">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="95169-167">新-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="95169-167">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="95169-168">移除-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="95169-168">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="95169-169">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="95169-169">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


