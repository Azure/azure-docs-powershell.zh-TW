---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: fe709b560c790ad010469bf2f0a2043231124138
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452880"
---
# <span data-ttu-id="fcfca-101">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="fcfca-101">Set-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="fcfca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fcfca-102">SYNOPSIS</span></span>
<span data-ttu-id="fcfca-103">修改 API 修訂</span><span class="sxs-lookup"><span data-stu-id="fcfca-103">Modifies an API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcfca-104">句法</span><span class="sxs-lookup"><span data-stu-id="fcfca-104">SYNTAX</span></span>

### <span data-ttu-id="fcfca-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="fcfca-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcfca-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fcfca-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcfca-107">說明</span><span class="sxs-lookup"><span data-stu-id="fcfca-107">DESCRIPTION</span></span>
<span data-ttu-id="fcfca-108">**AzureRmApiManagementApiRevision** Cmdlet 會修改 Azure API 管理 API 修正。</span><span class="sxs-lookup"><span data-stu-id="fcfca-108">The **Set-AzureRmApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="fcfca-109">示例</span><span class="sxs-lookup"><span data-stu-id="fcfca-109">EXAMPLES</span></span>

### <span data-ttu-id="fcfca-110">範例1修改 API 修訂版本</span><span class="sxs-lookup"><span data-stu-id="fcfca-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="fcfca-111">此 Cmdlet 會 `2` `echo-api` 使用新的描述、通訊協定和路徑來更新 API 的修訂版本。</span><span class="sxs-lookup"><span data-stu-id="fcfca-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="fcfca-112">參數</span><span class="sxs-lookup"><span data-stu-id="fcfca-112">PARAMETERS</span></span>

### <span data-ttu-id="fcfca-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fcfca-113">-ApiId</span></span>
<span data-ttu-id="fcfca-114">現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fcfca-114">Identifier of existing API.</span></span>
<span data-ttu-id="fcfca-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="fcfca-115">This parameter is required.</span></span>

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

### <span data-ttu-id="fcfca-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="fcfca-116">-ApiRevision</span></span>
<span data-ttu-id="fcfca-117">現有 API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fcfca-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="fcfca-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="fcfca-118">This parameter is required.</span></span>

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

### <span data-ttu-id="fcfca-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="fcfca-119">-AuthorizationScope</span></span>
<span data-ttu-id="fcfca-120">OAuth 作業範圍。</span><span class="sxs-lookup"><span data-stu-id="fcfca-120">OAuth operations scope.</span></span>
<span data-ttu-id="fcfca-121">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="fcfca-121">This parameter is optional.</span></span>
<span data-ttu-id="fcfca-122">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="fcfca-122">Default value is $null.</span></span>

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

### <span data-ttu-id="fcfca-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="fcfca-123">-AuthorizationServerId</span></span>
<span data-ttu-id="fcfca-124">OAuth 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="fcfca-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="fcfca-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="fcfca-125">This parameter is optional.</span></span>
<span data-ttu-id="fcfca-126">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="fcfca-126">Default value is $null.</span></span>
<span data-ttu-id="fcfca-127">如果已指定 AuthorizationScope，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="fcfca-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="fcfca-128">-內容</span><span class="sxs-lookup"><span data-stu-id="fcfca-128">-Context</span></span>
<span data-ttu-id="fcfca-129">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="fcfca-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fcfca-130">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="fcfca-130">This parameter is required.</span></span>

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

### <span data-ttu-id="fcfca-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcfca-131">-DefaultProfile</span></span>
<span data-ttu-id="fcfca-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fcfca-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcfca-133">-描述</span><span class="sxs-lookup"><span data-stu-id="fcfca-133">-Description</span></span>
<span data-ttu-id="fcfca-134">Web API 說明。</span><span class="sxs-lookup"><span data-stu-id="fcfca-134">Web API description.</span></span>
<span data-ttu-id="fcfca-135">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="fcfca-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="fcfca-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcfca-136">-InputObject</span></span>
<span data-ttu-id="fcfca-137">PsApiManagementApi 的實例。</span><span class="sxs-lookup"><span data-stu-id="fcfca-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="fcfca-138">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="fcfca-138">This parameter is required.</span></span>

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

### <span data-ttu-id="fcfca-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="fcfca-139">-Name</span></span>
<span data-ttu-id="fcfca-140">Web API 名稱。</span><span class="sxs-lookup"><span data-stu-id="fcfca-140">Web API name.</span></span>
<span data-ttu-id="fcfca-141">API 在開發人員和管理入口網站上顯示的公用名稱。</span><span class="sxs-lookup"><span data-stu-id="fcfca-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="fcfca-142">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="fcfca-142">This parameter is required.</span></span>

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

### <span data-ttu-id="fcfca-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcfca-143">-PassThru</span></span>
<span data-ttu-id="fcfca-144">如果已指定，則 ServiceManagement 代表 set API 的 PsApiManagementApi 類型的 ApiManagement 的實例。</span><span class="sxs-lookup"><span data-stu-id="fcfca-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="fcfca-145">-Path</span><span class="sxs-lookup"><span data-stu-id="fcfca-145">-Path</span></span>
<span data-ttu-id="fcfca-146">Web API 路徑。</span><span class="sxs-lookup"><span data-stu-id="fcfca-146">Web API Path.</span></span>
<span data-ttu-id="fcfca-147">API 公用 URL 的最後一部分。</span><span class="sxs-lookup"><span data-stu-id="fcfca-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="fcfca-148">此 URL 將由 API 消費者用來傳送要求至 web 服務。</span><span class="sxs-lookup"><span data-stu-id="fcfca-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="fcfca-149">長度必須是1到400個字元。</span><span class="sxs-lookup"><span data-stu-id="fcfca-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="fcfca-150">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="fcfca-150">This parameter is optional.</span></span>
<span data-ttu-id="fcfca-151">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="fcfca-151">Default value is $null.</span></span>

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

### <span data-ttu-id="fcfca-152">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="fcfca-152">-Protocols</span></span>
<span data-ttu-id="fcfca-153">Web API 通訊協定 (HTTP、HTTPs) 。</span><span class="sxs-lookup"><span data-stu-id="fcfca-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="fcfca-154">提供可用 API 的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="fcfca-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="fcfca-155">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="fcfca-155">This parameter is required.</span></span>
<span data-ttu-id="fcfca-156">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="fcfca-156">Default value is $null.</span></span>

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

### <span data-ttu-id="fcfca-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="fcfca-157">-ServiceUrl</span></span>
<span data-ttu-id="fcfca-158">公開 API 之 web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="fcfca-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="fcfca-159">這個 URL 將只由 Azure API 管理使用，不會公開。</span><span class="sxs-lookup"><span data-stu-id="fcfca-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="fcfca-160">長度必須是1到2000個字元。</span><span class="sxs-lookup"><span data-stu-id="fcfca-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="fcfca-161">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="fcfca-161">This parameter is required.</span></span>

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

### <span data-ttu-id="fcfca-162">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="fcfca-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="fcfca-163">訂閱金鑰標頭名稱。</span><span class="sxs-lookup"><span data-stu-id="fcfca-163">Subscription key header name.</span></span>
<span data-ttu-id="fcfca-164">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="fcfca-164">This parameter is optional.</span></span>
<span data-ttu-id="fcfca-165">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="fcfca-165">Default value is $null.</span></span>

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

### <span data-ttu-id="fcfca-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="fcfca-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="fcfca-167">訂閱金鑰查詢字串參數名稱。</span><span class="sxs-lookup"><span data-stu-id="fcfca-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="fcfca-168">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="fcfca-168">This parameter is optional.</span></span>
<span data-ttu-id="fcfca-169">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="fcfca-169">Default value is $null.</span></span>

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

### <span data-ttu-id="fcfca-170">-確認</span><span class="sxs-lookup"><span data-stu-id="fcfca-170">-Confirm</span></span>
<span data-ttu-id="fcfca-171">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fcfca-171">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcfca-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcfca-172">-WhatIf</span></span>
<span data-ttu-id="fcfca-173">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fcfca-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcfca-174">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fcfca-174">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcfca-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcfca-175">CommonParameters</span></span>
<span data-ttu-id="fcfca-176">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fcfca-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcfca-177">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fcfca-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcfca-178">輸入</span><span class="sxs-lookup"><span data-stu-id="fcfca-178">INPUTS</span></span>

### <span data-ttu-id="fcfca-179">System.object</span><span class="sxs-lookup"><span data-stu-id="fcfca-179">System.String</span></span>

### <span data-ttu-id="fcfca-180">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fcfca-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fcfca-181">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fcfca-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="fcfca-182">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="fcfca-182">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="fcfca-183">PsApiManagementSchema []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="fcfca-183">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="fcfca-184">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="fcfca-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fcfca-185">輸出</span><span class="sxs-lookup"><span data-stu-id="fcfca-185">OUTPUTS</span></span>

### <span data-ttu-id="fcfca-186">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fcfca-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="fcfca-187">筆記</span><span class="sxs-lookup"><span data-stu-id="fcfca-187">NOTES</span></span>

## <span data-ttu-id="fcfca-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="fcfca-188">RELATED LINKS</span></span>

[<span data-ttu-id="fcfca-189">AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="fcfca-189">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="fcfca-190">新-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="fcfca-190">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="fcfca-191">移除-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="fcfca-191">Remove-AzureRmApiManagementApiRevision</span></span>](./Remove-AzureRmApiManagementApiRevision.md)
