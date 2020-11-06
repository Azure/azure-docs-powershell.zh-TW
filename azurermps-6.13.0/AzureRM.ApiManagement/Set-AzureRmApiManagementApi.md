---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 10df1034b414260cb618c7de0b31b8ad93d30d0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452883"
---
# <span data-ttu-id="e0169-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e0169-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="e0169-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0169-102">SYNOPSIS</span></span>
<span data-ttu-id="e0169-103">修改 API。</span><span class="sxs-lookup"><span data-stu-id="e0169-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0169-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0169-104">SYNTAX</span></span>

### <span data-ttu-id="e0169-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="e0169-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0169-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e0169-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0169-107">說明</span><span class="sxs-lookup"><span data-stu-id="e0169-107">DESCRIPTION</span></span>
<span data-ttu-id="e0169-108">**AzureRmApiManagementApi** Cmdlet 會修改 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="e0169-108">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="e0169-109">示例</span><span class="sxs-lookup"><span data-stu-id="e0169-109">EXAMPLES</span></span>

### <span data-ttu-id="e0169-110">範例1修改 API</span><span class="sxs-lookup"><span data-stu-id="e0169-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="e0169-111">參數</span><span class="sxs-lookup"><span data-stu-id="e0169-111">PARAMETERS</span></span>

### <span data-ttu-id="e0169-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e0169-112">-ApiId</span></span>
<span data-ttu-id="e0169-113">指定要修改的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0169-113">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="e0169-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="e0169-114">-AuthorizationScope</span></span>
<span data-ttu-id="e0169-115">指定 OAuth 作業範圍。</span><span class="sxs-lookup"><span data-stu-id="e0169-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="e0169-116">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="e0169-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="e0169-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="e0169-117">-AuthorizationServerId</span></span>
<span data-ttu-id="e0169-118">指定 OAuth 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0169-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="e0169-119">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="e0169-119">The default value is $Null.</span></span>
<span data-ttu-id="e0169-120">如果已指定 *AuthorizationScope* ，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="e0169-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="e0169-121">-內容</span><span class="sxs-lookup"><span data-stu-id="e0169-121">-Context</span></span>
<span data-ttu-id="e0169-122">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="e0169-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0169-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0169-123">-DefaultProfile</span></span>
<span data-ttu-id="e0169-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0169-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0169-125">-描述</span><span class="sxs-lookup"><span data-stu-id="e0169-125">-Description</span></span>
<span data-ttu-id="e0169-126">指定 web API 的描述。</span><span class="sxs-lookup"><span data-stu-id="e0169-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="e0169-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0169-127">-InputObject</span></span>
<span data-ttu-id="e0169-128">PsApiManagementApi 的實例。</span><span class="sxs-lookup"><span data-stu-id="e0169-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="e0169-129">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="e0169-129">This parameter is required.</span></span>

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

### <span data-ttu-id="e0169-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="e0169-130">-Name</span></span>
<span data-ttu-id="e0169-131">指定 web API 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0169-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="e0169-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0169-132">-PassThru</span></span>
<span data-ttu-id="e0169-133">passthru</span><span class="sxs-lookup"><span data-stu-id="e0169-133">passthru</span></span>

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

### <span data-ttu-id="e0169-134">-Path</span><span class="sxs-lookup"><span data-stu-id="e0169-134">-Path</span></span>
<span data-ttu-id="e0169-135">指定 web API 路徑，該路徑是 API 公用 URL 的最後一部分。</span><span class="sxs-lookup"><span data-stu-id="e0169-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="e0169-136">這個 URL 是由 API 消費者用來傳送要求至 web 服務的，而且必須是一個至400字元長。</span><span class="sxs-lookup"><span data-stu-id="e0169-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="e0169-137">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="e0169-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="e0169-138">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="e0169-138">-Protocols</span></span>
<span data-ttu-id="e0169-139">指定 web API 通訊協定的陣列。</span><span class="sxs-lookup"><span data-stu-id="e0169-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="e0169-140">psdx_paramvalues HTTP 和 HTTPs。</span><span class="sxs-lookup"><span data-stu-id="e0169-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="e0169-141">這些是可供使用 API 的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="e0169-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="e0169-142">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="e0169-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="e0169-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="e0169-143">-ServiceUrl</span></span>
<span data-ttu-id="e0169-144">指定公開 API 之 web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="e0169-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="e0169-145">這個 URL 只能由 Azure API 管理使用，而且不會公開。</span><span class="sxs-lookup"><span data-stu-id="e0169-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="e0169-146">URL 必須是一個至2000字元的長度。</span><span class="sxs-lookup"><span data-stu-id="e0169-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="e0169-147">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="e0169-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="e0169-148">指定訂閱金鑰標頭的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0169-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="e0169-149">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="e0169-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="e0169-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="e0169-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="e0169-151">指定訂閱金鑰查詢字串參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0169-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="e0169-152">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="e0169-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="e0169-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0169-153">CommonParameters</span></span>
<span data-ttu-id="e0169-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0169-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0169-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0169-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0169-156">輸入</span><span class="sxs-lookup"><span data-stu-id="e0169-156">INPUTS</span></span>

### <span data-ttu-id="e0169-157">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e0169-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e0169-158">System.object</span><span class="sxs-lookup"><span data-stu-id="e0169-158">System.String</span></span>

### <span data-ttu-id="e0169-159">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e0169-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="e0169-160">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e0169-160">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e0169-161">PsApiManagementSchema []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="e0169-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="e0169-162">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="e0169-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e0169-163">輸出</span><span class="sxs-lookup"><span data-stu-id="e0169-163">OUTPUTS</span></span>

### <span data-ttu-id="e0169-164">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e0169-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="e0169-165">筆記</span><span class="sxs-lookup"><span data-stu-id="e0169-165">NOTES</span></span>

## <span data-ttu-id="e0169-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0169-166">RELATED LINKS</span></span>

[<span data-ttu-id="e0169-167">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e0169-167">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="e0169-168">AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e0169-168">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="e0169-169">匯入-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e0169-169">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="e0169-170">新-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e0169-170">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="e0169-171">移除-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e0169-171">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


