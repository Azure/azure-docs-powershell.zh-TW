---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
ms.openlocfilehash: 545c1f57d269b8cdb36e006a07c754811e0f2b04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450099"
---
# <span data-ttu-id="12f06-101">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="12f06-101">New-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="12f06-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12f06-102">SYNOPSIS</span></span>
<span data-ttu-id="12f06-103">建立 API 管理作業。</span><span class="sxs-lookup"><span data-stu-id="12f06-103">Creates an API management operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12f06-104">句法</span><span class="sxs-lookup"><span data-stu-id="12f06-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-OperationId <String>]
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12f06-105">說明</span><span class="sxs-lookup"><span data-stu-id="12f06-105">DESCRIPTION</span></span>
<span data-ttu-id="12f06-106">**新的-AzureRmApiManagementOperation** Cmdlet 會建立 API 操作。</span><span class="sxs-lookup"><span data-stu-id="12f06-106">The **New-AzureRmApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="12f06-107">示例</span><span class="sxs-lookup"><span data-stu-id="12f06-107">EXAMPLES</span></span>

### <span data-ttu-id="12f06-108">範例1：建立 API 管理作業</span><span class="sxs-lookup"><span data-stu-id="12f06-108">Example 1: Create an API management operation</span></span>
```
PS C:\>New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="12f06-109">這個命令會建立 API 管理作業。</span><span class="sxs-lookup"><span data-stu-id="12f06-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="12f06-110">範例2：使用要求與回應詳細資料建立 API 管理作業</span><span class="sxs-lookup"><span data-stu-id="12f06-110">Example 2: Create an API management operation with request and response details</span></span>
```
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
New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="12f06-111">這個範例會使用 [要求] 與 [回應] 詳細資料建立 API 管理作業。</span><span class="sxs-lookup"><span data-stu-id="12f06-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="12f06-112">參數</span><span class="sxs-lookup"><span data-stu-id="12f06-112">PARAMETERS</span></span>

### <span data-ttu-id="12f06-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="12f06-113">-ApiId</span></span>
<span data-ttu-id="12f06-114">指定 API 管理作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="12f06-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="12f06-115">-內容</span><span class="sxs-lookup"><span data-stu-id="12f06-115">-Context</span></span>
<span data-ttu-id="12f06-116">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="12f06-116">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="12f06-117">-描述</span><span class="sxs-lookup"><span data-stu-id="12f06-117">-Description</span></span>
<span data-ttu-id="12f06-118">指定新 API 操作的描述。</span><span class="sxs-lookup"><span data-stu-id="12f06-118">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="12f06-119">-方法</span><span class="sxs-lookup"><span data-stu-id="12f06-119">-Method</span></span>
<span data-ttu-id="12f06-120">指定新 API 管理作業的 HTTP 方法。</span><span class="sxs-lookup"><span data-stu-id="12f06-120">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="12f06-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="12f06-121">-Name</span></span>
<span data-ttu-id="12f06-122">指定新 API 管理作業的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="12f06-122">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="12f06-123">-OperationId</span><span class="sxs-lookup"><span data-stu-id="12f06-123">-OperationId</span></span>
<span data-ttu-id="12f06-124">指定 API 管理作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="12f06-124">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="12f06-125">-要求</span><span class="sxs-lookup"><span data-stu-id="12f06-125">-Request</span></span>
<span data-ttu-id="12f06-126">指定 API 管理作業的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="12f06-126">Specifies the details of the API management operation.</span></span>

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

### <span data-ttu-id="12f06-127">-回復</span><span class="sxs-lookup"><span data-stu-id="12f06-127">-Responses</span></span>
<span data-ttu-id="12f06-128">指定可能的 API 管理操作回應陣列。</span><span class="sxs-lookup"><span data-stu-id="12f06-128">Specifies an array of possible API management operation responses.</span></span>

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

### <span data-ttu-id="12f06-129">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="12f06-129">-TemplateParameters</span></span>
<span data-ttu-id="12f06-130">指定 [參數 *UrlTemplate* ] 中定義的參數陣列。</span><span class="sxs-lookup"><span data-stu-id="12f06-130">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="12f06-131">如果您沒有指定此參數，則會根據 *UrlTemplate* 產生預設值。</span><span class="sxs-lookup"><span data-stu-id="12f06-131">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

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

### <span data-ttu-id="12f06-132">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="12f06-132">-UrlTemplate</span></span>
<span data-ttu-id="12f06-133">指定 URL 範本。</span><span class="sxs-lookup"><span data-stu-id="12f06-133">Specifies the URL template.</span></span>

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

### <span data-ttu-id="12f06-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f06-134">-DefaultProfile</span></span>
<span data-ttu-id="12f06-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12f06-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12f06-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f06-136">CommonParameters</span></span>
<span data-ttu-id="12f06-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12f06-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f06-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12f06-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f06-139">輸入</span><span class="sxs-lookup"><span data-stu-id="12f06-139">INPUTS</span></span>

## <span data-ttu-id="12f06-140">輸出</span><span class="sxs-lookup"><span data-stu-id="12f06-140">OUTPUTS</span></span>

### <span data-ttu-id="12f06-141">ServiceManagement. PsApiManagementOperation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="12f06-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="12f06-142">筆記</span><span class="sxs-lookup"><span data-stu-id="12f06-142">NOTES</span></span>

## <span data-ttu-id="12f06-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="12f06-143">RELATED LINKS</span></span>

[<span data-ttu-id="12f06-144">AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="12f06-144">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="12f06-145">移除-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="12f06-145">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="12f06-146">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="12f06-146">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


