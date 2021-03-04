---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
ms.openlocfilehash: 44eb7ef52782f6a00a81385f7b1a87b0292bec33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903886"
---
# <span data-ttu-id="f6a14-101">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f6a14-101">New-AzApiManagementOperation</span></span>

## <span data-ttu-id="f6a14-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f6a14-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a14-103">建立 API 管理作業。</span><span class="sxs-lookup"><span data-stu-id="f6a14-103">Creates an API management operation.</span></span>

## <span data-ttu-id="f6a14-104">語法</span><span class="sxs-lookup"><span data-stu-id="f6a14-104">SYNTAX</span></span>

```
New-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6a14-105">描述</span><span class="sxs-lookup"><span data-stu-id="f6a14-105">DESCRIPTION</span></span>
<span data-ttu-id="f6a14-106">**New-AzApiManagementOperation Cmdlet** 會建立 API 作業。</span><span class="sxs-lookup"><span data-stu-id="f6a14-106">The **New-AzApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="f6a14-107">例子</span><span class="sxs-lookup"><span data-stu-id="f6a14-107">EXAMPLES</span></span>

### <span data-ttu-id="f6a14-108">範例 1：建立 API 管理作業</span><span class="sxs-lookup"><span data-stu-id="f6a14-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="f6a14-109">此命令會建立 API 管理作業。</span><span class="sxs-lookup"><span data-stu-id="f6a14-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="f6a14-110">範例 2：建立包含要求和回應詳細資料之 API 管理作業</span><span class="sxs-lookup"><span data-stu-id="f6a14-110">Example 2: Create an API management operation with request and response details</span></span>
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

<span data-ttu-id="f6a14-111">此範例會建立包含要求和回應詳細資料之 API 管理作業。</span><span class="sxs-lookup"><span data-stu-id="f6a14-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="f6a14-112">參數</span><span class="sxs-lookup"><span data-stu-id="f6a14-112">PARAMETERS</span></span>

### <span data-ttu-id="f6a14-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f6a14-113">-ApiId</span></span>
<span data-ttu-id="f6a14-114">指定 API 管理作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6a14-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="f6a14-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f6a14-115">-ApiRevision</span></span>
<span data-ttu-id="f6a14-116">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6a14-116">Identifier of API Revision.</span></span> <span data-ttu-id="f6a14-117">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="f6a14-117">This parameter is optional.</span></span> <span data-ttu-id="f6a14-118">如果未指定，作業會附加至目前使用中的 api 修訂。</span><span class="sxs-lookup"><span data-stu-id="f6a14-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="f6a14-119">-內容</span><span class="sxs-lookup"><span data-stu-id="f6a14-119">-Context</span></span>
<span data-ttu-id="f6a14-120">指定 **PsApiManagementCoNtext 物件** 的實例。</span><span class="sxs-lookup"><span data-stu-id="f6a14-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f6a14-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a14-121">-DefaultProfile</span></span>
<span data-ttu-id="f6a14-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6a14-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6a14-123">-描述</span><span class="sxs-lookup"><span data-stu-id="f6a14-123">-Description</span></span>
<span data-ttu-id="f6a14-124">指定新 API 作業的描述。</span><span class="sxs-lookup"><span data-stu-id="f6a14-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="f6a14-125">-方法</span><span class="sxs-lookup"><span data-stu-id="f6a14-125">-Method</span></span>
<span data-ttu-id="f6a14-126">指定新 API 管理作業的 HTTP 方法。</span><span class="sxs-lookup"><span data-stu-id="f6a14-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="f6a14-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6a14-127">-Name</span></span>
<span data-ttu-id="f6a14-128">指定新 API 管理作業的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f6a14-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="f6a14-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f6a14-129">-OperationId</span></span>
<span data-ttu-id="f6a14-130">指定 API 管理作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6a14-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="f6a14-131">-要求</span><span class="sxs-lookup"><span data-stu-id="f6a14-131">-Request</span></span>
<span data-ttu-id="f6a14-132">指定 API 管理作業的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f6a14-132">Specifies the details of the API management operation.</span></span>

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

### <span data-ttu-id="f6a14-133">-回復</span><span class="sxs-lookup"><span data-stu-id="f6a14-133">-Responses</span></span>
<span data-ttu-id="f6a14-134">指定可能的 API 管理作業回應陣列。</span><span class="sxs-lookup"><span data-stu-id="f6a14-134">Specifies an array of possible API management operation responses.</span></span>

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

### <span data-ttu-id="f6a14-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="f6a14-135">-TemplateParameters</span></span>
<span data-ttu-id="f6a14-136">指定參數 *UrlTemplate* 中定義的參數陣列。</span><span class="sxs-lookup"><span data-stu-id="f6a14-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="f6a14-137">如果您未指定此參數，將會根據 *UrlTemplate* 產生預設值。</span><span class="sxs-lookup"><span data-stu-id="f6a14-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

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

### <span data-ttu-id="f6a14-138">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="f6a14-138">-UrlTemplate</span></span>
<span data-ttu-id="f6a14-139">指定 URL 範本。</span><span class="sxs-lookup"><span data-stu-id="f6a14-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="f6a14-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a14-140">CommonParameters</span></span>
<span data-ttu-id="f6a14-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f6a14-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a14-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6a14-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a14-143">輸入</span><span class="sxs-lookup"><span data-stu-id="f6a14-143">INPUTS</span></span>

### <span data-ttu-id="f6a14-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="f6a14-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f6a14-145">System.String</span><span class="sxs-lookup"><span data-stu-id="f6a14-145">System.String</span></span>

### <span data-ttu-id="f6a14-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementParameter[]</span><span class="sxs-lookup"><span data-stu-id="f6a14-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="f6a14-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="f6a14-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="f6a14-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementResponse[]</span><span class="sxs-lookup"><span data-stu-id="f6a14-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="f6a14-149">輸出</span><span class="sxs-lookup"><span data-stu-id="f6a14-149">OUTPUTS</span></span>

### <span data-ttu-id="f6a14-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f6a14-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="f6a14-151">筆記</span><span class="sxs-lookup"><span data-stu-id="f6a14-151">NOTES</span></span>

## <span data-ttu-id="f6a14-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6a14-152">RELATED LINKS</span></span>

[<span data-ttu-id="f6a14-153">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f6a14-153">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="f6a14-154">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f6a14-154">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="f6a14-155">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f6a14-155">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


