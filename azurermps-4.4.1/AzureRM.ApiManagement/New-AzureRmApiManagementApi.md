---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 295551f9d4ddf751980ec81626e3714a37aa47a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450122"
---
# <span data-ttu-id="2a712-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2a712-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="2a712-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a712-102">SYNOPSIS</span></span>
<span data-ttu-id="2a712-103">建立 API。</span><span class="sxs-lookup"><span data-stu-id="2a712-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a712-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a712-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a712-105">說明</span><span class="sxs-lookup"><span data-stu-id="2a712-105">DESCRIPTION</span></span>
<span data-ttu-id="2a712-106">**新的-AzureRmApiManagementApi** Cmdlet 會建立 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="2a712-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="2a712-107">示例</span><span class="sxs-lookup"><span data-stu-id="2a712-107">EXAMPLES</span></span>

### <span data-ttu-id="2a712-108">範例1：建立 API</span><span class="sxs-lookup"><span data-stu-id="2a712-108">Example 1: Create an API</span></span>
```
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="2a712-109">這個命令會建立一個名為 EchoApi 且具有指定 URL 的 API。</span><span class="sxs-lookup"><span data-stu-id="2a712-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="2a712-110">參數</span><span class="sxs-lookup"><span data-stu-id="2a712-110">PARAMETERS</span></span>

### <span data-ttu-id="2a712-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2a712-111">-ApiId</span></span>
<span data-ttu-id="2a712-112">指定要建立的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="2a712-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="2a712-113">如果您沒有指定此參數，這個 Cmdlet 會為您產生識別碼。</span><span class="sxs-lookup"><span data-stu-id="2a712-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="2a712-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="2a712-114">-AuthorizationScope</span></span>
<span data-ttu-id="2a712-115">指定 OAuth 作業範圍。</span><span class="sxs-lookup"><span data-stu-id="2a712-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="2a712-116">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="2a712-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="2a712-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="2a712-117">-AuthorizationServerId</span></span>
<span data-ttu-id="2a712-118">指定 OAuth 授權伺服器 ID。</span><span class="sxs-lookup"><span data-stu-id="2a712-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="2a712-119">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="2a712-119">The default value is $Null.</span></span>
<span data-ttu-id="2a712-120">如果已指定 *AuthorizationScope* ，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="2a712-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="2a712-121">-內容</span><span class="sxs-lookup"><span data-stu-id="2a712-121">-Context</span></span>
<span data-ttu-id="2a712-122">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="2a712-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2a712-123">-描述</span><span class="sxs-lookup"><span data-stu-id="2a712-123">-Description</span></span>
<span data-ttu-id="2a712-124">指定 web API 的描述。</span><span class="sxs-lookup"><span data-stu-id="2a712-124">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="2a712-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a712-125">-Name</span></span>
<span data-ttu-id="2a712-126">指定 web API 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a712-126">Specifies the name of the web API.</span></span>
<span data-ttu-id="2a712-127">這是 API 在開發人員和管理入口網站上顯示的公用名稱。</span><span class="sxs-lookup"><span data-stu-id="2a712-127">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="2a712-128">-Path</span><span class="sxs-lookup"><span data-stu-id="2a712-128">-Path</span></span>
<span data-ttu-id="2a712-129">指定 web API 路徑，該路徑是 API 公用 URL 的最後一部分，並對應至管理入口網站中的 [Web API URL 尾碼] 欄位。</span><span class="sxs-lookup"><span data-stu-id="2a712-129">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="2a712-130">這個 URL 是由 API 消費者用來傳送要求至 web 服務的，而且必須是一個至400字元長。</span><span class="sxs-lookup"><span data-stu-id="2a712-130">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="2a712-131">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="2a712-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="2a712-132">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="2a712-132">-ProductIds</span></span>
<span data-ttu-id="2a712-133">指定要將新 API 新增至其中的產品識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="2a712-133">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="2a712-134">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="2a712-134">-Protocols</span></span>
<span data-ttu-id="2a712-135">指定 web API 通訊協定的陣列。</span><span class="sxs-lookup"><span data-stu-id="2a712-135">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="2a712-136">有效值為 HTTP、HTTPs。</span><span class="sxs-lookup"><span data-stu-id="2a712-136">Valid values are http, https.</span></span>
<span data-ttu-id="2a712-137">這些是可供使用 API 的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="2a712-137">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="2a712-138">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="2a712-138">The default value is $Null.</span></span>

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

### <span data-ttu-id="2a712-139">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="2a712-139">-ServiceUrl</span></span>
<span data-ttu-id="2a712-140">指定公開 API 之 web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="2a712-140">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="2a712-141">這個 URL 只能由 Azure API 管理使用，而且不會公開。</span><span class="sxs-lookup"><span data-stu-id="2a712-141">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="2a712-142">URL 必須是一個至2000字元的長度。</span><span class="sxs-lookup"><span data-stu-id="2a712-142">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="2a712-143">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="2a712-143">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="2a712-144">指定訂閱金鑰標頭名稱。</span><span class="sxs-lookup"><span data-stu-id="2a712-144">Specifies the subscription key header name.</span></span>
<span data-ttu-id="2a712-145">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="2a712-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="2a712-146">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="2a712-146">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="2a712-147">指定訂閱金鑰查詢字串參數名稱。</span><span class="sxs-lookup"><span data-stu-id="2a712-147">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="2a712-148">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="2a712-148">The default value is $Null.</span></span>

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

### <span data-ttu-id="2a712-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a712-149">-DefaultProfile</span></span>
<span data-ttu-id="2a712-150">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a712-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a712-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a712-151">CommonParameters</span></span>
<span data-ttu-id="2a712-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a712-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a712-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a712-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a712-154">輸入</span><span class="sxs-lookup"><span data-stu-id="2a712-154">INPUTS</span></span>

## <span data-ttu-id="2a712-155">輸出</span><span class="sxs-lookup"><span data-stu-id="2a712-155">OUTPUTS</span></span>

### <span data-ttu-id="2a712-156">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="2a712-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="2a712-157">筆記</span><span class="sxs-lookup"><span data-stu-id="2a712-157">NOTES</span></span>

## <span data-ttu-id="2a712-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a712-158">RELATED LINKS</span></span>

[<span data-ttu-id="2a712-159">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2a712-159">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="2a712-160">AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2a712-160">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="2a712-161">匯入-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2a712-161">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="2a712-162">移除-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2a712-162">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="2a712-163">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2a712-163">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


