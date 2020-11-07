---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: 8b2e29da3c3f6140cbab422e74d09656c921c16c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788786"
---
# <span data-ttu-id="76b47-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="76b47-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="76b47-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76b47-102">SYNOPSIS</span></span>
<span data-ttu-id="76b47-103">修改 API 修訂</span><span class="sxs-lookup"><span data-stu-id="76b47-103">Modifies an API Revision</span></span>

## <span data-ttu-id="76b47-104">句法</span><span class="sxs-lookup"><span data-stu-id="76b47-104">SYNTAX</span></span>

### <span data-ttu-id="76b47-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="76b47-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76b47-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="76b47-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76b47-107">說明</span><span class="sxs-lookup"><span data-stu-id="76b47-107">DESCRIPTION</span></span>
<span data-ttu-id="76b47-108">**AzApiManagementApiRevision** Cmdlet 會修改 Azure API 管理 API 修正。</span><span class="sxs-lookup"><span data-stu-id="76b47-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="76b47-109">示例</span><span class="sxs-lookup"><span data-stu-id="76b47-109">EXAMPLES</span></span>

### <span data-ttu-id="76b47-110">範例1修改 API 修訂版本</span><span class="sxs-lookup"><span data-stu-id="76b47-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="76b47-111">此 Cmdlet 會 `2` `echo-api` 使用新的描述、通訊協定和路徑來更新 API 的修訂版本。</span><span class="sxs-lookup"><span data-stu-id="76b47-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="76b47-112">參數</span><span class="sxs-lookup"><span data-stu-id="76b47-112">PARAMETERS</span></span>

### <span data-ttu-id="76b47-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="76b47-113">-ApiId</span></span>
<span data-ttu-id="76b47-114">現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="76b47-114">Identifier of existing API.</span></span>
<span data-ttu-id="76b47-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="76b47-115">This parameter is required.</span></span>

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

### <span data-ttu-id="76b47-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="76b47-116">-ApiRevision</span></span>
<span data-ttu-id="76b47-117">現有 API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="76b47-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="76b47-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="76b47-118">This parameter is required.</span></span>

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

### <span data-ttu-id="76b47-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="76b47-119">-AuthorizationScope</span></span>
<span data-ttu-id="76b47-120">OAuth 作業範圍。</span><span class="sxs-lookup"><span data-stu-id="76b47-120">OAuth operations scope.</span></span>
<span data-ttu-id="76b47-121">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="76b47-121">This parameter is optional.</span></span>
<span data-ttu-id="76b47-122">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="76b47-122">Default value is $null.</span></span>

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

### <span data-ttu-id="76b47-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="76b47-123">-AuthorizationServerId</span></span>
<span data-ttu-id="76b47-124">OAuth 授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="76b47-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="76b47-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="76b47-125">This parameter is optional.</span></span>
<span data-ttu-id="76b47-126">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="76b47-126">Default value is $null.</span></span>
<span data-ttu-id="76b47-127">如果已指定 AuthorizationScope，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="76b47-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="76b47-128">-內容</span><span class="sxs-lookup"><span data-stu-id="76b47-128">-Context</span></span>
<span data-ttu-id="76b47-129">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="76b47-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="76b47-130">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="76b47-130">This parameter is required.</span></span>

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

### <span data-ttu-id="76b47-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76b47-131">-DefaultProfile</span></span>
<span data-ttu-id="76b47-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="76b47-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76b47-133">-描述</span><span class="sxs-lookup"><span data-stu-id="76b47-133">-Description</span></span>
<span data-ttu-id="76b47-134">Web API 說明。</span><span class="sxs-lookup"><span data-stu-id="76b47-134">Web API description.</span></span>
<span data-ttu-id="76b47-135">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="76b47-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="76b47-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76b47-136">-InputObject</span></span>
<span data-ttu-id="76b47-137">PsApiManagementApi 的實例。</span><span class="sxs-lookup"><span data-stu-id="76b47-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="76b47-138">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="76b47-138">This parameter is required.</span></span>

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

### <span data-ttu-id="76b47-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="76b47-139">-Name</span></span>
<span data-ttu-id="76b47-140">Web API 名稱。</span><span class="sxs-lookup"><span data-stu-id="76b47-140">Web API name.</span></span>
<span data-ttu-id="76b47-141">API 在開發人員和管理入口網站上顯示的公用名稱。</span><span class="sxs-lookup"><span data-stu-id="76b47-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="76b47-142">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="76b47-142">This parameter is required.</span></span>

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

### <span data-ttu-id="76b47-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76b47-143">-PassThru</span></span>
<span data-ttu-id="76b47-144">如果已指定，則 ServiceManagement 代表 set API 的 PsApiManagementApi 類型的 ApiManagement 的實例。</span><span class="sxs-lookup"><span data-stu-id="76b47-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="76b47-145">-Path</span><span class="sxs-lookup"><span data-stu-id="76b47-145">-Path</span></span>
<span data-ttu-id="76b47-146">Web API 路徑。</span><span class="sxs-lookup"><span data-stu-id="76b47-146">Web API Path.</span></span>
<span data-ttu-id="76b47-147">API 公用 URL 的最後一部分。</span><span class="sxs-lookup"><span data-stu-id="76b47-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="76b47-148">此 URL 將由 API 消費者用來傳送要求至 web 服務。</span><span class="sxs-lookup"><span data-stu-id="76b47-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="76b47-149">長度必須是1到400個字元。</span><span class="sxs-lookup"><span data-stu-id="76b47-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="76b47-150">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="76b47-150">This parameter is optional.</span></span>
<span data-ttu-id="76b47-151">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="76b47-151">Default value is $null.</span></span>

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

### <span data-ttu-id="76b47-152">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="76b47-152">-Protocols</span></span>
<span data-ttu-id="76b47-153">Web API 通訊協定 (HTTP、HTTPs) 。</span><span class="sxs-lookup"><span data-stu-id="76b47-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="76b47-154">提供可用 API 的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="76b47-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="76b47-155">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="76b47-155">This parameter is required.</span></span>
<span data-ttu-id="76b47-156">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="76b47-156">Default value is $null.</span></span>

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

### <span data-ttu-id="76b47-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="76b47-157">-ServiceUrl</span></span>
<span data-ttu-id="76b47-158">公開 API 之 web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="76b47-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="76b47-159">這個 URL 將只由 Azure API 管理使用，不會公開。</span><span class="sxs-lookup"><span data-stu-id="76b47-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="76b47-160">長度必須是1到2000個字元。</span><span class="sxs-lookup"><span data-stu-id="76b47-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="76b47-161">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="76b47-161">This parameter is required.</span></span>

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

### <span data-ttu-id="76b47-162">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="76b47-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="76b47-163">訂閱金鑰標頭名稱。</span><span class="sxs-lookup"><span data-stu-id="76b47-163">Subscription key header name.</span></span>
<span data-ttu-id="76b47-164">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="76b47-164">This parameter is optional.</span></span>
<span data-ttu-id="76b47-165">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="76b47-165">Default value is $null.</span></span>

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

### <span data-ttu-id="76b47-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="76b47-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="76b47-167">訂閱金鑰查詢字串參數名稱。</span><span class="sxs-lookup"><span data-stu-id="76b47-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="76b47-168">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="76b47-168">This parameter is optional.</span></span>
<span data-ttu-id="76b47-169">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="76b47-169">Default value is $null.</span></span>

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

### <span data-ttu-id="76b47-170">-確認</span><span class="sxs-lookup"><span data-stu-id="76b47-170">-Confirm</span></span>
<span data-ttu-id="76b47-171">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="76b47-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76b47-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76b47-172">-WhatIf</span></span>
<span data-ttu-id="76b47-173">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76b47-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76b47-174">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76b47-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76b47-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b47-175">CommonParameters</span></span>
<span data-ttu-id="76b47-176">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76b47-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b47-177">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="76b47-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b47-178">輸入</span><span class="sxs-lookup"><span data-stu-id="76b47-178">INPUTS</span></span>

### <span data-ttu-id="76b47-179">System.object</span><span class="sxs-lookup"><span data-stu-id="76b47-179">System.String</span></span>

### <span data-ttu-id="76b47-180">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="76b47-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="76b47-181">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="76b47-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="76b47-182">PsApiManagementSchema []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="76b47-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="76b47-183">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="76b47-183">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="76b47-184">輸出</span><span class="sxs-lookup"><span data-stu-id="76b47-184">OUTPUTS</span></span>

### <span data-ttu-id="76b47-185">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="76b47-185">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="76b47-186">筆記</span><span class="sxs-lookup"><span data-stu-id="76b47-186">NOTES</span></span>

## <span data-ttu-id="76b47-187">相關連結</span><span class="sxs-lookup"><span data-stu-id="76b47-187">RELATED LINKS</span></span>

[<span data-ttu-id="76b47-188">AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="76b47-188">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="76b47-189">新-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="76b47-189">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="76b47-190">移除-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="76b47-190">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)