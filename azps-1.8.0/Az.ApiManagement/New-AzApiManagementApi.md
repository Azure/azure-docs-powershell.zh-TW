---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 43793ef7d1d3f9a4e5e63687e1eaf785d237e86b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611592"
---
# <span data-ttu-id="f0535-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f0535-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="f0535-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0535-102">SYNOPSIS</span></span>
<span data-ttu-id="f0535-103">建立 API。</span><span class="sxs-lookup"><span data-stu-id="f0535-103">Creates an API.</span></span>

## <span data-ttu-id="f0535-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0535-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0535-105">說明</span><span class="sxs-lookup"><span data-stu-id="f0535-105">DESCRIPTION</span></span>
<span data-ttu-id="f0535-106">**新的-AzApiManagementApi** Cmdlet 會建立 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="f0535-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="f0535-107">示例</span><span class="sxs-lookup"><span data-stu-id="f0535-107">EXAMPLES</span></span>

### <span data-ttu-id="f0535-108">範例1：建立 API</span><span class="sxs-lookup"><span data-stu-id="f0535-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="f0535-109">這個命令會建立一個名為 EchoApi 且具有指定 URL 的 API。</span><span class="sxs-lookup"><span data-stu-id="f0535-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="f0535-110">參數</span><span class="sxs-lookup"><span data-stu-id="f0535-110">PARAMETERS</span></span>

### <span data-ttu-id="f0535-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f0535-111">-ApiId</span></span>
<span data-ttu-id="f0535-112">指定要建立的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0535-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="f0535-113">如果您沒有指定此參數，這個 Cmdlet 會為您產生識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0535-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="f0535-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="f0535-114">-AuthorizationScope</span></span>
<span data-ttu-id="f0535-115">指定 OAuth 作業範圍。</span><span class="sxs-lookup"><span data-stu-id="f0535-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="f0535-116">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="f0535-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="f0535-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="f0535-117">-AuthorizationServerId</span></span>
<span data-ttu-id="f0535-118">指定 OAuth 授權伺服器 ID。</span><span class="sxs-lookup"><span data-stu-id="f0535-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="f0535-119">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="f0535-119">The default value is $Null.</span></span>
<span data-ttu-id="f0535-120">如果已指定 *AuthorizationScope* ，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="f0535-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="f0535-121">-內容</span><span class="sxs-lookup"><span data-stu-id="f0535-121">-Context</span></span>
<span data-ttu-id="f0535-122">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="f0535-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f0535-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0535-123">-DefaultProfile</span></span>
<span data-ttu-id="f0535-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0535-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0535-125">-描述</span><span class="sxs-lookup"><span data-stu-id="f0535-125">-Description</span></span>
<span data-ttu-id="f0535-126">指定 web API 的描述。</span><span class="sxs-lookup"><span data-stu-id="f0535-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="f0535-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0535-127">-Name</span></span>
<span data-ttu-id="f0535-128">指定 web API 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0535-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="f0535-129">這是 API 在開發人員和管理入口網站上顯示的公用名稱。</span><span class="sxs-lookup"><span data-stu-id="f0535-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="f0535-130">-Path</span><span class="sxs-lookup"><span data-stu-id="f0535-130">-Path</span></span>
<span data-ttu-id="f0535-131">指定 web API 路徑，該路徑是 API 公用 URL 的最後一部分，並對應至管理入口網站中的 [Web API URL 尾碼] 欄位。</span><span class="sxs-lookup"><span data-stu-id="f0535-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="f0535-132">這個 URL 是由 API 消費者用來傳送要求至 web 服務的，而且必須是一個至400字元長。</span><span class="sxs-lookup"><span data-stu-id="f0535-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="f0535-133">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="f0535-133">The default value is $Null.</span></span>

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

### <span data-ttu-id="f0535-134">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="f0535-134">-ProductIds</span></span>
<span data-ttu-id="f0535-135">指定要將新 API 新增至其中的產品識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="f0535-135">Specifies an array of product IDs to which to add the new API.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0535-136">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="f0535-136">-Protocols</span></span>
<span data-ttu-id="f0535-137">指定 web API 通訊協定的陣列。</span><span class="sxs-lookup"><span data-stu-id="f0535-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="f0535-138">有效值為 HTTP、HTTPs。</span><span class="sxs-lookup"><span data-stu-id="f0535-138">Valid values are http, https.</span></span>
<span data-ttu-id="f0535-139">這些是可供使用 API 的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f0535-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="f0535-140">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="f0535-140">The default value is $Null.</span></span>

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

### <span data-ttu-id="f0535-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="f0535-141">-ServiceUrl</span></span>
<span data-ttu-id="f0535-142">指定公開 API 之 web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="f0535-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="f0535-143">這個 URL 只能由 Azure API 管理使用，而且不會公開。</span><span class="sxs-lookup"><span data-stu-id="f0535-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="f0535-144">URL 必須是一個至2000字元的長度。</span><span class="sxs-lookup"><span data-stu-id="f0535-144">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="f0535-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="f0535-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="f0535-146">指定訂閱金鑰標頭名稱。</span><span class="sxs-lookup"><span data-stu-id="f0535-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="f0535-147">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="f0535-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="f0535-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="f0535-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="f0535-149">指定訂閱金鑰查詢字串參數名稱。</span><span class="sxs-lookup"><span data-stu-id="f0535-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="f0535-150">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="f0535-150">The default value is $Null.</span></span>

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

### <span data-ttu-id="f0535-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0535-151">CommonParameters</span></span>
<span data-ttu-id="f0535-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0535-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0535-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f0535-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0535-154">輸入</span><span class="sxs-lookup"><span data-stu-id="f0535-154">INPUTS</span></span>

### <span data-ttu-id="f0535-155">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f0535-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f0535-156">System.object</span><span class="sxs-lookup"><span data-stu-id="f0535-156">System.String</span></span>

### <span data-ttu-id="f0535-157">PsApiManagementSchema []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="f0535-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="f0535-158">System.object []</span><span class="sxs-lookup"><span data-stu-id="f0535-158">System.String[]</span></span>

## <span data-ttu-id="f0535-159">輸出</span><span class="sxs-lookup"><span data-stu-id="f0535-159">OUTPUTS</span></span>

### <span data-ttu-id="f0535-160">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f0535-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="f0535-161">筆記</span><span class="sxs-lookup"><span data-stu-id="f0535-161">NOTES</span></span>

## <span data-ttu-id="f0535-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0535-162">RELATED LINKS</span></span>

[<span data-ttu-id="f0535-163">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f0535-163">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="f0535-164">AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f0535-164">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="f0535-165">匯入-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f0535-165">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="f0535-166">移除-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f0535-166">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="f0535-167">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f0535-167">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


