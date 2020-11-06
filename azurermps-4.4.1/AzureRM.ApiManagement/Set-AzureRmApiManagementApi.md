---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 4c9dc60ad1c531a5da9f32abc0090475c32a7ad5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454947"
---
# <span data-ttu-id="8412f-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8412f-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="8412f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8412f-102">SYNOPSIS</span></span>
<span data-ttu-id="8412f-103">修改 API。</span><span class="sxs-lookup"><span data-stu-id="8412f-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8412f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8412f-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8412f-105">說明</span><span class="sxs-lookup"><span data-stu-id="8412f-105">DESCRIPTION</span></span>
<span data-ttu-id="8412f-106">**AzureRmApiManagementApi** Cmdlet 會修改 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="8412f-106">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="8412f-107">示例</span><span class="sxs-lookup"><span data-stu-id="8412f-107">EXAMPLES</span></span>

### <span data-ttu-id="8412f-108">範例1修改 API</span><span class="sxs-lookup"><span data-stu-id="8412f-108">Example 1 Modify an API</span></span>
```
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="8412f-109">參數</span><span class="sxs-lookup"><span data-stu-id="8412f-109">PARAMETERS</span></span>

### <span data-ttu-id="8412f-110">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8412f-110">-ApiId</span></span>
<span data-ttu-id="8412f-111">指定要修改的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="8412f-111">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="8412f-112">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="8412f-112">-AuthorizationScope</span></span>
<span data-ttu-id="8412f-113">指定 OAuth 作業範圍。</span><span class="sxs-lookup"><span data-stu-id="8412f-113">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="8412f-114">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="8412f-114">The default value is $Null.</span></span>

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

### <span data-ttu-id="8412f-115">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="8412f-115">-AuthorizationServerId</span></span>
<span data-ttu-id="8412f-116">指定 OAuth 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="8412f-116">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="8412f-117">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="8412f-117">The default value is $Null.</span></span>
<span data-ttu-id="8412f-118">如果已指定 *AuthorizationScope* ，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="8412f-118">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="8412f-119">-內容</span><span class="sxs-lookup"><span data-stu-id="8412f-119">-Context</span></span>
<span data-ttu-id="8412f-120">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="8412f-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8412f-121">-描述</span><span class="sxs-lookup"><span data-stu-id="8412f-121">-Description</span></span>
<span data-ttu-id="8412f-122">指定 web API 的描述。</span><span class="sxs-lookup"><span data-stu-id="8412f-122">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="8412f-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="8412f-123">-Name</span></span>
<span data-ttu-id="8412f-124">指定 web API 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8412f-124">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="8412f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8412f-125">-PassThru</span></span>
<span data-ttu-id="8412f-126">passthru</span><span class="sxs-lookup"><span data-stu-id="8412f-126">passthru</span></span>

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

### <span data-ttu-id="8412f-127">-Path</span><span class="sxs-lookup"><span data-stu-id="8412f-127">-Path</span></span>
<span data-ttu-id="8412f-128">指定 web API 路徑，該路徑是 API 公用 URL 的最後一部分。</span><span class="sxs-lookup"><span data-stu-id="8412f-128">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="8412f-129">這個 URL 是由 API 消費者用來傳送要求至 web 服務的，而且必須是一個至400字元長。</span><span class="sxs-lookup"><span data-stu-id="8412f-129">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="8412f-130">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="8412f-130">The default value is $Null.</span></span>

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

### <span data-ttu-id="8412f-131">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="8412f-131">-Protocols</span></span>
<span data-ttu-id="8412f-132">指定 web API 通訊協定的陣列。</span><span class="sxs-lookup"><span data-stu-id="8412f-132">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="8412f-133">psdx_paramvalues HTTP 和 HTTPs。</span><span class="sxs-lookup"><span data-stu-id="8412f-133">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="8412f-134">這些是可供使用 API 的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="8412f-134">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="8412f-135">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="8412f-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="8412f-136">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="8412f-136">-ServiceUrl</span></span>
<span data-ttu-id="8412f-137">指定公開 API 之 web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="8412f-137">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="8412f-138">這個 URL 只能由 Azure API 管理使用，而且不會公開。</span><span class="sxs-lookup"><span data-stu-id="8412f-138">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="8412f-139">URL 必須是一個至2000字元的長度。</span><span class="sxs-lookup"><span data-stu-id="8412f-139">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="8412f-140">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="8412f-140">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="8412f-141">指定訂閱金鑰標頭的名稱。</span><span class="sxs-lookup"><span data-stu-id="8412f-141">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="8412f-142">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="8412f-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="8412f-143">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="8412f-143">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="8412f-144">指定訂閱金鑰查詢字串參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="8412f-144">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="8412f-145">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="8412f-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="8412f-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8412f-146">-DefaultProfile</span></span>
<span data-ttu-id="8412f-147">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8412f-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8412f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8412f-148">CommonParameters</span></span>
<span data-ttu-id="8412f-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8412f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8412f-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8412f-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8412f-151">輸入</span><span class="sxs-lookup"><span data-stu-id="8412f-151">INPUTS</span></span>

## <span data-ttu-id="8412f-152">輸出</span><span class="sxs-lookup"><span data-stu-id="8412f-152">OUTPUTS</span></span>

### <span data-ttu-id="8412f-153">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="8412f-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="8412f-154">筆記</span><span class="sxs-lookup"><span data-stu-id="8412f-154">NOTES</span></span>

## <span data-ttu-id="8412f-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="8412f-155">RELATED LINKS</span></span>

[<span data-ttu-id="8412f-156">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8412f-156">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="8412f-157">AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8412f-157">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="8412f-158">匯入-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8412f-158">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="8412f-159">新-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8412f-159">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="8412f-160">移除-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8412f-160">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


