---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
ms.openlocfilehash: 3cba96c2b68a3045448aa6f6f6ccd011964c6e16
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287859"
---
# <span data-ttu-id="a2f07-101">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a2f07-101">New-AzApiManagementOperation</span></span>

## <span data-ttu-id="a2f07-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2f07-102">SYNOPSIS</span></span>
<span data-ttu-id="a2f07-103">建立 API 管理作業。</span><span class="sxs-lookup"><span data-stu-id="a2f07-103">Creates an API management operation.</span></span>

## <span data-ttu-id="a2f07-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2f07-104">SYNTAX</span></span>

```
New-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2f07-105">說明</span><span class="sxs-lookup"><span data-stu-id="a2f07-105">DESCRIPTION</span></span>
<span data-ttu-id="a2f07-106">**新的-AzApiManagementOperation** Cmdlet 會建立 API 操作。</span><span class="sxs-lookup"><span data-stu-id="a2f07-106">The **New-AzApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="a2f07-107">示例</span><span class="sxs-lookup"><span data-stu-id="a2f07-107">EXAMPLES</span></span>

### <span data-ttu-id="a2f07-108">範例1：建立 API 管理作業</span><span class="sxs-lookup"><span data-stu-id="a2f07-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="a2f07-109">這個命令會建立 API 管理作業。</span><span class="sxs-lookup"><span data-stu-id="a2f07-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="a2f07-110">範例2：使用要求與回應詳細資料建立 API 管理作業</span><span class="sxs-lookup"><span data-stu-id="a2f07-110">Example 2: Create an API management operation with request and response details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$RID = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$RID.Name = "RID"
$RID.Description = "Resource identifier"
$RID.Type = "string"
$Query = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Query.Name = "query"
$Query.Description = "Query string"
$Query.Type = 'string'
$Request = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
$Request.Description = "Create/update resource request"
$DummyQp = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$DummyQp.Name = 'dummy'
$DummyQp.Type = 'string'
$DummyQp.Required = $FALSE
$Request.QueryParameters = @($DummyQp)
$Header = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Header.Name = 'x-custom-header'
$Header.Type = 'string'
$Request.Headers = @($Header)
$RequestRepresentation = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRepresentation
$RequestRepresentation.ContentType = 'application/json'
$RequestRepresentation.Sample = '{ "propName": "propValue" }'
$Request.Representations = @($requestRepresentation)
$Response = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse
$Response.StatusCode = 204
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="a2f07-111">這個範例會使用 [要求] 與 [回應] 詳細資料建立 API 管理作業。</span><span class="sxs-lookup"><span data-stu-id="a2f07-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="a2f07-112">參數</span><span class="sxs-lookup"><span data-stu-id="a2f07-112">PARAMETERS</span></span>

### <span data-ttu-id="a2f07-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a2f07-113">-ApiId</span></span>
<span data-ttu-id="a2f07-114">指定 API 管理作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2f07-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="a2f07-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="a2f07-115">-ApiRevision</span></span>
<span data-ttu-id="a2f07-116">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2f07-116">Identifier of API Revision.</span></span> <span data-ttu-id="a2f07-117">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="a2f07-117">This parameter is optional.</span></span> <span data-ttu-id="a2f07-118">如果未指定，該作業將會附加到目前使用中的 api 修正程式。</span><span class="sxs-lookup"><span data-stu-id="a2f07-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="a2f07-119">-內容</span><span class="sxs-lookup"><span data-stu-id="a2f07-119">-Context</span></span>
<span data-ttu-id="a2f07-120">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="a2f07-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a2f07-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2f07-121">-DefaultProfile</span></span>
<span data-ttu-id="a2f07-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2f07-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2f07-123">-描述</span><span class="sxs-lookup"><span data-stu-id="a2f07-123">-Description</span></span>
<span data-ttu-id="a2f07-124">指定新 API 操作的描述。</span><span class="sxs-lookup"><span data-stu-id="a2f07-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="a2f07-125">-方法</span><span class="sxs-lookup"><span data-stu-id="a2f07-125">-Method</span></span>
<span data-ttu-id="a2f07-126">指定新 API 管理作業的 HTTP 方法。</span><span class="sxs-lookup"><span data-stu-id="a2f07-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="a2f07-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2f07-127">-Name</span></span>
<span data-ttu-id="a2f07-128">指定新 API 管理作業的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a2f07-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="a2f07-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a2f07-129">-OperationId</span></span>
<span data-ttu-id="a2f07-130">指定 API 管理作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2f07-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="a2f07-131">-要求</span><span class="sxs-lookup"><span data-stu-id="a2f07-131">-Request</span></span>
<span data-ttu-id="a2f07-132">指定 API 管理作業的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a2f07-132">Specifies the details of the API management operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2f07-133">-回復</span><span class="sxs-lookup"><span data-stu-id="a2f07-133">-Responses</span></span>
<span data-ttu-id="a2f07-134">指定可能的 API 管理操作回應陣列。</span><span class="sxs-lookup"><span data-stu-id="a2f07-134">Specifies an array of possible API management operation responses.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2f07-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="a2f07-135">-TemplateParameters</span></span>
<span data-ttu-id="a2f07-136">指定 [參數 *UrlTemplate*] 中定義的參數陣列。</span><span class="sxs-lookup"><span data-stu-id="a2f07-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="a2f07-137">如果您沒有指定此參數，則會根據 *UrlTemplate* 產生預設值。</span><span class="sxs-lookup"><span data-stu-id="a2f07-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2f07-138">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="a2f07-138">-UrlTemplate</span></span>
<span data-ttu-id="a2f07-139">指定 URL 範本。</span><span class="sxs-lookup"><span data-stu-id="a2f07-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="a2f07-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2f07-140">CommonParameters</span></span>
<span data-ttu-id="a2f07-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2f07-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2f07-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a2f07-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2f07-143">輸入</span><span class="sxs-lookup"><span data-stu-id="a2f07-143">INPUTS</span></span>

### <span data-ttu-id="a2f07-144">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a2f07-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a2f07-145">System.object</span><span class="sxs-lookup"><span data-stu-id="a2f07-145">System.String</span></span>

### <span data-ttu-id="a2f07-146">PsApiManagementParameter []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="a2f07-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="a2f07-147">ServiceManagement. PsApiManagementRequest （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a2f07-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="a2f07-148">PsApiManagementResponse []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="a2f07-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="a2f07-149">輸出</span><span class="sxs-lookup"><span data-stu-id="a2f07-149">OUTPUTS</span></span>

### <span data-ttu-id="a2f07-150">ServiceManagement. PsApiManagementOperation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a2f07-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="a2f07-151">筆記</span><span class="sxs-lookup"><span data-stu-id="a2f07-151">NOTES</span></span>

## <span data-ttu-id="a2f07-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2f07-152">RELATED LINKS</span></span>

[<span data-ttu-id="a2f07-153">AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a2f07-153">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="a2f07-154">移除-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a2f07-154">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="a2f07-155">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a2f07-155">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


