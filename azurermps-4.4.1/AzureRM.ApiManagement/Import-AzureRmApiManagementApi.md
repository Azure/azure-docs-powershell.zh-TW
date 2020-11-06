---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
ms.openlocfilehash: a95aa5cf5d78d2540fe2816cfa4b044502c69b0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450125"
---
# <span data-ttu-id="25842-101">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="25842-101">Import-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="25842-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25842-102">SYNOPSIS</span></span>
<span data-ttu-id="25842-103">從檔案或 URL 匯入 API。</span><span class="sxs-lookup"><span data-stu-id="25842-103">Imports an API from a file or a URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25842-104">句法</span><span class="sxs-lookup"><span data-stu-id="25842-104">SYNTAX</span></span>

### <span data-ttu-id="25842-105">從本機檔案 (預設) </span><span class="sxs-lookup"><span data-stu-id="25842-105">From Local File (Default)</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25842-106">從 URL</span><span class="sxs-lookup"><span data-stu-id="25842-106">From URL</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25842-107">說明</span><span class="sxs-lookup"><span data-stu-id="25842-107">DESCRIPTION</span></span>
<span data-ttu-id="25842-108">匯 **入-AzureRmApiManagementApi** Cmdlet 會從 Web 應用程式描述語言 (WADL) 、Web 服務描述語言 (WSDL) 或 Swagger 格式），從檔案或 URL 中匯入 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="25842-108">The **Import-AzureRmApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="25842-109">示例</span><span class="sxs-lookup"><span data-stu-id="25842-109">EXAMPLES</span></span>

### <span data-ttu-id="25842-110">範例1從 WADL 檔案匯入 API</span><span class="sxs-lookup"><span data-stu-id="25842-110">Example 1 Import an API from a WADL file</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="25842-111">這個命令會從指定的 WADL 檔案匯入 API。</span><span class="sxs-lookup"><span data-stu-id="25842-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="25842-112">範例2從 Swagger 檔案匯入 API</span><span class="sxs-lookup"><span data-stu-id="25842-112">Example 2 Import an API from a Swagger file</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="25842-113">這個命令會從指定的 Swagger 檔案匯入 API。</span><span class="sxs-lookup"><span data-stu-id="25842-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="25842-114">範例3：從 WADL 連結匯入 API</span><span class="sxs-lookup"><span data-stu-id="25842-114">Example 3: Import an API from a WADL link</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="25842-115">這個命令會從指定的 WADL 連結匯入 API。</span><span class="sxs-lookup"><span data-stu-id="25842-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="25842-116">參數</span><span class="sxs-lookup"><span data-stu-id="25842-116">PARAMETERS</span></span>

### <span data-ttu-id="25842-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="25842-117">-ApiId</span></span>
<span data-ttu-id="25842-118">指定要匯入的 API ID。</span><span class="sxs-lookup"><span data-stu-id="25842-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="25842-119">如果您沒有指定此參數，系統會為您產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="25842-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="25842-120">-ApiType</span><span class="sxs-lookup"><span data-stu-id="25842-120">-ApiType</span></span>
<span data-ttu-id="25842-121">這個參數是預設值 Http 的選用。</span><span class="sxs-lookup"><span data-stu-id="25842-121">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="25842-122">Soap 選項只適用于匯入 WSDL，且將建立 SOAP 直通 API。</span><span class="sxs-lookup"><span data-stu-id="25842-122">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="25842-123">-內容</span><span class="sxs-lookup"><span data-stu-id="25842-123">-Context</span></span>
<span data-ttu-id="25842-124">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="25842-124">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="25842-125">-Path</span><span class="sxs-lookup"><span data-stu-id="25842-125">-Path</span></span>
<span data-ttu-id="25842-126">將 web API 路徑指定為 API 公用 URL 的最後一部分。</span><span class="sxs-lookup"><span data-stu-id="25842-126">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="25842-127">這個 URL 是由 API 消費者用來傳送要求至 web 服務的。</span><span class="sxs-lookup"><span data-stu-id="25842-127">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="25842-128">長度必須是1到400個字元。</span><span class="sxs-lookup"><span data-stu-id="25842-128">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="25842-129">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="25842-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="25842-130">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="25842-130">-SpecificationFormat</span></span>
<span data-ttu-id="25842-131">指定規格格式。</span><span class="sxs-lookup"><span data-stu-id="25842-131">Specifies the specification format.</span></span>
<span data-ttu-id="25842-132">psdx_paramvalues Wadl、Wsdl 和 Swagger。</span><span class="sxs-lookup"><span data-stu-id="25842-132">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

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

### <span data-ttu-id="25842-133">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="25842-133">-SpecificationPath</span></span>
<span data-ttu-id="25842-134">指定規格檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="25842-134">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: From Local File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25842-135">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="25842-135">-SpecificationUrl</span></span>
<span data-ttu-id="25842-136">指定規格 URL。</span><span class="sxs-lookup"><span data-stu-id="25842-136">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: From URL
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25842-137">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="25842-137">-WsdlEndpointName</span></span>
<span data-ttu-id="25842-138">要匯入 (埠) 的 WSDL 端點本機名稱。</span><span class="sxs-lookup"><span data-stu-id="25842-138">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="25842-139">長度必須是1到400個字元。</span><span class="sxs-lookup"><span data-stu-id="25842-139">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="25842-140">這個參數是選擇性的，只有在匯入 Wsdl 時才需要。</span><span class="sxs-lookup"><span data-stu-id="25842-140">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="25842-141">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="25842-141">Default value is $null.</span></span>

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

### <span data-ttu-id="25842-142">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="25842-142">-WsdlServiceName</span></span>
<span data-ttu-id="25842-143">要匯入之 WSDL 服務的本機名稱。</span><span class="sxs-lookup"><span data-stu-id="25842-143">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="25842-144">長度必須是1到400個字元。</span><span class="sxs-lookup"><span data-stu-id="25842-144">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="25842-145">這個參數是選擇性的，只有在匯入 Wsdl 時才需要。</span><span class="sxs-lookup"><span data-stu-id="25842-145">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="25842-146">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="25842-146">Default value is $null.</span></span>

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

### <span data-ttu-id="25842-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25842-147">-DefaultProfile</span></span>
<span data-ttu-id="25842-148">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="25842-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25842-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25842-149">CommonParameters</span></span>
<span data-ttu-id="25842-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25842-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25842-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="25842-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25842-152">輸入</span><span class="sxs-lookup"><span data-stu-id="25842-152">INPUTS</span></span>

## <span data-ttu-id="25842-153">輸出</span><span class="sxs-lookup"><span data-stu-id="25842-153">OUTPUTS</span></span>

### <span data-ttu-id="25842-154">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="25842-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="25842-155">這個 Cmdlet 會將匯入的 API 傳回為 **PsApiManagementApi** 物件。</span><span class="sxs-lookup"><span data-stu-id="25842-155">This cmdlet returns the imported API as a **PsApiManagementApi** object.</span></span>

## <span data-ttu-id="25842-156">筆記</span><span class="sxs-lookup"><span data-stu-id="25842-156">NOTES</span></span>

## <span data-ttu-id="25842-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="25842-157">RELATED LINKS</span></span>

[<span data-ttu-id="25842-158">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="25842-158">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="25842-159">AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="25842-159">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="25842-160">新-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="25842-160">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="25842-161">移除-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="25842-161">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="25842-162">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="25842-162">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


