---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 75a6dbf480e8b2f2f3d9f7524db4e57e5ed88f69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625940"
---
# <span data-ttu-id="1f439-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1f439-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="1f439-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f439-102">SYNOPSIS</span></span>
<span data-ttu-id="1f439-103">建立 API。</span><span class="sxs-lookup"><span data-stu-id="1f439-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f439-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f439-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f439-105">說明</span><span class="sxs-lookup"><span data-stu-id="1f439-105">DESCRIPTION</span></span>
<span data-ttu-id="1f439-106">**新的-AzureRmApiManagementApi** Cmdlet 會建立 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="1f439-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="1f439-107">示例</span><span class="sxs-lookup"><span data-stu-id="1f439-107">EXAMPLES</span></span>

### <span data-ttu-id="1f439-108">範例1：建立 API</span><span class="sxs-lookup"><span data-stu-id="1f439-108">Example 1: Create an API</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="1f439-109">這個命令會建立一個名為 EchoApi 且具有指定 URL 的 API。</span><span class="sxs-lookup"><span data-stu-id="1f439-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="1f439-110">參數</span><span class="sxs-lookup"><span data-stu-id="1f439-110">PARAMETERS</span></span>

### <span data-ttu-id="1f439-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1f439-111">-ApiId</span></span>
<span data-ttu-id="1f439-112">指定要建立的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="1f439-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="1f439-113">如果您沒有指定此參數，這個 Cmdlet 會為您產生識別碼。</span><span class="sxs-lookup"><span data-stu-id="1f439-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f439-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="1f439-114">-AuthorizationScope</span></span>
<span data-ttu-id="1f439-115">指定 OAuth 作業範圍。</span><span class="sxs-lookup"><span data-stu-id="1f439-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="1f439-116">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="1f439-116">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f439-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="1f439-117">-AuthorizationServerId</span></span>
<span data-ttu-id="1f439-118">指定 OAuth 授權伺服器 ID。</span><span class="sxs-lookup"><span data-stu-id="1f439-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="1f439-119">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="1f439-119">The default value is $Null.</span></span>
<span data-ttu-id="1f439-120">如果已指定 *AuthorizationScope* ，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="1f439-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f439-121">-內容</span><span class="sxs-lookup"><span data-stu-id="1f439-121">-Context</span></span>
<span data-ttu-id="1f439-122">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="1f439-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f439-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f439-123">-DefaultProfile</span></span>
<span data-ttu-id="1f439-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f439-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f439-125">-描述</span><span class="sxs-lookup"><span data-stu-id="1f439-125">-Description</span></span>
<span data-ttu-id="1f439-126">指定 web API 的描述。</span><span class="sxs-lookup"><span data-stu-id="1f439-126">Specifies a description for the web API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f439-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f439-127">-Name</span></span>
<span data-ttu-id="1f439-128">指定 web API 的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f439-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="1f439-129">這是 API 在開發人員和管理入口網站上顯示的公用名稱。</span><span class="sxs-lookup"><span data-stu-id="1f439-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f439-130">-Path</span><span class="sxs-lookup"><span data-stu-id="1f439-130">-Path</span></span>
<span data-ttu-id="1f439-131">指定 web API 路徑，該路徑是 API 公用 URL 的最後一部分，並對應至管理入口網站中的 [Web API URL 尾碼] 欄位。</span><span class="sxs-lookup"><span data-stu-id="1f439-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="1f439-132">這個 URL 是由 API 消費者用來傳送要求至 web 服務的，而且必須是一個至400字元長。</span><span class="sxs-lookup"><span data-stu-id="1f439-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="1f439-133">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="1f439-133">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f439-134">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="1f439-134">-ProductIds</span></span>
<span data-ttu-id="1f439-135">指定要將新 API 新增至其中的產品識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="1f439-135">Specifies an array of product IDs to which to add the new API.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f439-136">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="1f439-136">-Protocols</span></span>
<span data-ttu-id="1f439-137">指定 web API 通訊協定的陣列。</span><span class="sxs-lookup"><span data-stu-id="1f439-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="1f439-138">有效值為 HTTP、HTTPs。</span><span class="sxs-lookup"><span data-stu-id="1f439-138">Valid values are http, https.</span></span>
<span data-ttu-id="1f439-139">這些是可供使用 API 的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1f439-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="1f439-140">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="1f439-140">The default value is $Null.</span></span>

```yaml
Type: PsApiManagementSchema[]
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f439-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="1f439-141">-ServiceUrl</span></span>
<span data-ttu-id="1f439-142">指定公開 API 之 web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="1f439-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="1f439-143">這個 URL 只能由 Azure API 管理使用，而且不會公開。</span><span class="sxs-lookup"><span data-stu-id="1f439-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="1f439-144">URL 必須是一個至2000字元的長度。</span><span class="sxs-lookup"><span data-stu-id="1f439-144">The URL must be one to 2000 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f439-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="1f439-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="1f439-146">指定訂閱金鑰標頭名稱。</span><span class="sxs-lookup"><span data-stu-id="1f439-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="1f439-147">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="1f439-147">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f439-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="1f439-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="1f439-149">指定訂閱金鑰查詢字串參數名稱。</span><span class="sxs-lookup"><span data-stu-id="1f439-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="1f439-150">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="1f439-150">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f439-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f439-151">CommonParameters</span></span>
<span data-ttu-id="1f439-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f439-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f439-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f439-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f439-154">輸入</span><span class="sxs-lookup"><span data-stu-id="1f439-154">INPUTS</span></span>

### <span data-ttu-id="1f439-155">所有</span><span class="sxs-lookup"><span data-stu-id="1f439-155">None</span></span>
<span data-ttu-id="1f439-156">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="1f439-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f439-157">輸出</span><span class="sxs-lookup"><span data-stu-id="1f439-157">OUTPUTS</span></span>

### <span data-ttu-id="1f439-158">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="1f439-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="1f439-159">筆記</span><span class="sxs-lookup"><span data-stu-id="1f439-159">NOTES</span></span>

## <span data-ttu-id="1f439-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f439-160">RELATED LINKS</span></span>

[<span data-ttu-id="1f439-161">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1f439-161">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="1f439-162">AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1f439-162">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="1f439-163">匯入-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1f439-163">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="1f439-164">移除-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1f439-164">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="1f439-165">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1f439-165">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


