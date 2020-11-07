---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 190dfb075e16b6b7eaaa0cb6fafd0145b3211654
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788797"
---
# <span data-ttu-id="8b449-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8b449-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="8b449-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8b449-102">SYNOPSIS</span></span>
<span data-ttu-id="8b449-103">修改 API。</span><span class="sxs-lookup"><span data-stu-id="8b449-103">Modifies an API.</span></span>

## <span data-ttu-id="8b449-104">句法</span><span class="sxs-lookup"><span data-stu-id="8b449-104">SYNTAX</span></span>

### <span data-ttu-id="8b449-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="8b449-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b449-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8b449-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b449-107">說明</span><span class="sxs-lookup"><span data-stu-id="8b449-107">DESCRIPTION</span></span>
<span data-ttu-id="8b449-108">**AzApiManagementApi** Cmdlet 會修改 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="8b449-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="8b449-109">示例</span><span class="sxs-lookup"><span data-stu-id="8b449-109">EXAMPLES</span></span>

### <span data-ttu-id="8b449-110">範例1修改 API</span><span class="sxs-lookup"><span data-stu-id="8b449-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="8b449-111">參數</span><span class="sxs-lookup"><span data-stu-id="8b449-111">PARAMETERS</span></span>

### <span data-ttu-id="8b449-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8b449-112">-ApiId</span></span>
<span data-ttu-id="8b449-113">指定要修改的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b449-113">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="8b449-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="8b449-114">-AuthorizationScope</span></span>
<span data-ttu-id="8b449-115">指定 OAuth 作業範圍。</span><span class="sxs-lookup"><span data-stu-id="8b449-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="8b449-116">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="8b449-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="8b449-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="8b449-117">-AuthorizationServerId</span></span>
<span data-ttu-id="8b449-118">指定 OAuth 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b449-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="8b449-119">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="8b449-119">The default value is $Null.</span></span>
<span data-ttu-id="8b449-120">如果已指定 *AuthorizationScope* ，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="8b449-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="8b449-121">-內容</span><span class="sxs-lookup"><span data-stu-id="8b449-121">-Context</span></span>
<span data-ttu-id="8b449-122">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="8b449-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8b449-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b449-123">-DefaultProfile</span></span>
<span data-ttu-id="8b449-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8b449-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b449-125">-描述</span><span class="sxs-lookup"><span data-stu-id="8b449-125">-Description</span></span>
<span data-ttu-id="8b449-126">指定 web API 的描述。</span><span class="sxs-lookup"><span data-stu-id="8b449-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="8b449-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b449-127">-InputObject</span></span>
<span data-ttu-id="8b449-128">PsApiManagementApi 的實例。</span><span class="sxs-lookup"><span data-stu-id="8b449-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="8b449-129">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="8b449-129">This parameter is required.</span></span>

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

### <span data-ttu-id="8b449-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="8b449-130">-Name</span></span>
<span data-ttu-id="8b449-131">指定 web API 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b449-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="8b449-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b449-132">-PassThru</span></span>
<span data-ttu-id="8b449-133">passthru</span><span class="sxs-lookup"><span data-stu-id="8b449-133">passthru</span></span>

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

### <span data-ttu-id="8b449-134">-Path</span><span class="sxs-lookup"><span data-stu-id="8b449-134">-Path</span></span>
<span data-ttu-id="8b449-135">指定 web API 路徑，該路徑是 API 公用 URL 的最後一部分。</span><span class="sxs-lookup"><span data-stu-id="8b449-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="8b449-136">這個 URL 是由 API 消費者用來傳送要求至 web 服務的，而且必須是一個至400字元長。</span><span class="sxs-lookup"><span data-stu-id="8b449-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="8b449-137">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="8b449-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="8b449-138">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="8b449-138">-Protocols</span></span>
<span data-ttu-id="8b449-139">指定 web API 通訊協定的陣列。</span><span class="sxs-lookup"><span data-stu-id="8b449-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="8b449-140">psdx_paramvalues HTTP 和 HTTPs。</span><span class="sxs-lookup"><span data-stu-id="8b449-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="8b449-141">這些是可供使用 API 的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="8b449-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="8b449-142">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="8b449-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="8b449-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="8b449-143">-ServiceUrl</span></span>
<span data-ttu-id="8b449-144">指定公開 API 之 web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="8b449-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="8b449-145">這個 URL 只能由 Azure API 管理使用，而且不會公開。</span><span class="sxs-lookup"><span data-stu-id="8b449-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="8b449-146">URL 必須是一個至2000字元的長度。</span><span class="sxs-lookup"><span data-stu-id="8b449-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="8b449-147">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="8b449-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="8b449-148">指定訂閱金鑰標頭的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b449-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="8b449-149">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="8b449-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="8b449-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="8b449-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="8b449-151">指定訂閱金鑰查詢字串參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b449-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="8b449-152">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="8b449-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="8b449-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b449-153">CommonParameters</span></span>
<span data-ttu-id="8b449-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8b449-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b449-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8b449-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b449-156">輸入</span><span class="sxs-lookup"><span data-stu-id="8b449-156">INPUTS</span></span>

### <span data-ttu-id="8b449-157">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="8b449-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8b449-158">System.object</span><span class="sxs-lookup"><span data-stu-id="8b449-158">System.String</span></span>

### <span data-ttu-id="8b449-159">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="8b449-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="8b449-160">PsApiManagementSchema []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="8b449-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="8b449-161">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="8b449-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8b449-162">輸出</span><span class="sxs-lookup"><span data-stu-id="8b449-162">OUTPUTS</span></span>

### <span data-ttu-id="8b449-163">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="8b449-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="8b449-164">筆記</span><span class="sxs-lookup"><span data-stu-id="8b449-164">NOTES</span></span>

## <span data-ttu-id="8b449-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b449-165">RELATED LINKS</span></span>

[<span data-ttu-id="8b449-166">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8b449-166">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="8b449-167">AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8b449-167">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="8b449-168">匯入-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8b449-168">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="8b449-169">新-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8b449-169">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="8b449-170">移除-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8b449-170">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


