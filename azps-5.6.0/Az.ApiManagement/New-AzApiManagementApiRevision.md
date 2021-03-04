---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: d03253a608469ac111d04b837497375028b48fe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916602"
---
# <span data-ttu-id="d524b-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="d524b-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="d524b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d524b-102">SYNOPSIS</span></span>
<span data-ttu-id="d524b-103">建立現有 API 的新修訂。</span><span class="sxs-lookup"><span data-stu-id="d524b-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="d524b-104">語法</span><span class="sxs-lookup"><span data-stu-id="d524b-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d524b-105">描述</span><span class="sxs-lookup"><span data-stu-id="d524b-105">DESCRIPTION</span></span>

<span data-ttu-id="d524b-106">**New-AzApiManagementApiRevision** Cmdlet 會針對 API 管理內容中現有的 API 建立 API 修訂。</span><span class="sxs-lookup"><span data-stu-id="d524b-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="d524b-107">例子</span><span class="sxs-lookup"><span data-stu-id="d524b-107">EXAMPLES</span></span>

### <span data-ttu-id="d524b-108">範例 1：建立 API 的空白 API 修訂</span><span class="sxs-lookup"><span data-stu-id="d524b-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="d524b-109">此命令會建立 API `2` 的 API 修訂 `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="d524b-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="d524b-110">範例 2：從現有 Api 建立 API 修訂，並複製所有作業、標記和策略</span><span class="sxs-lookup"><span data-stu-id="d524b-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5" -SourceApiRevision "1" -ServiceUrl "https://echoapi.cloudapp.net/rev4"


ApiId                         : echo-api;rev=5
Name                          : Echo API
Description                   :
ServiceUrl                    : http://echoapi.cloudapp.net/api
Path                          : echo
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 5
ApiVersion                    :
IsCurrent                     : False
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/apimService1/providers/Microsoft.ApiManagement/service/sdktestapim4163/apis/echo-api;rev=5
ResourceGroupName             : apimService1
ServiceName                   : sdktestapim4163
```

<span data-ttu-id="d524b-111">此命令會建立 API `5` 的 API 修訂 `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="d524b-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="d524b-112">參數</span><span class="sxs-lookup"><span data-stu-id="d524b-112">PARAMETERS</span></span>

### <span data-ttu-id="d524b-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d524b-113">-ApiId</span></span>
<span data-ttu-id="d524b-114">要建立修訂的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="d524b-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="d524b-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d524b-115">-ApiRevision</span></span>
<span data-ttu-id="d524b-116">Api 的修訂識別碼。</span><span class="sxs-lookup"><span data-stu-id="d524b-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="d524b-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="d524b-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="d524b-118">Api 修訂說明。</span><span class="sxs-lookup"><span data-stu-id="d524b-118">Api Revision Description.</span></span> <span data-ttu-id="d524b-119">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="d524b-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="d524b-120">-內容</span><span class="sxs-lookup"><span data-stu-id="d524b-120">-Context</span></span>
<span data-ttu-id="d524b-121">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="d524b-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d524b-122">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="d524b-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d524b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d524b-123">-DefaultProfile</span></span>
<span data-ttu-id="d524b-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d524b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d524b-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="d524b-125">-ServiceUrl</span></span>
<span data-ttu-id="d524b-126">在後端服務中公開 API 的網頁服務 URL。</span><span class="sxs-lookup"><span data-stu-id="d524b-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="d524b-127">此 URL 將僅由 Azure API 管理使用，不會公開。</span><span class="sxs-lookup"><span data-stu-id="d524b-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="d524b-128">必須長 1 到 2000 個字元。</span><span class="sxs-lookup"><span data-stu-id="d524b-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="d524b-129">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="d524b-129">This parameter is required.</span></span>

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

### <span data-ttu-id="d524b-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="d524b-130">-SourceApiRevision</span></span>
<span data-ttu-id="d524b-131">來源 API 的 Api 修訂識別碼。</span><span class="sxs-lookup"><span data-stu-id="d524b-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="d524b-132">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="d524b-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="d524b-133">-確認</span><span class="sxs-lookup"><span data-stu-id="d524b-133">-Confirm</span></span>
<span data-ttu-id="d524b-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d524b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d524b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d524b-135">-WhatIf</span></span>
<span data-ttu-id="d524b-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d524b-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d524b-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d524b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d524b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d524b-138">CommonParameters</span></span>
<span data-ttu-id="d524b-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d524b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d524b-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d524b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d524b-141">輸入</span><span class="sxs-lookup"><span data-stu-id="d524b-141">INPUTS</span></span>

### <span data-ttu-id="d524b-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="d524b-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d524b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="d524b-143">System.String</span></span>

## <span data-ttu-id="d524b-144">輸出</span><span class="sxs-lookup"><span data-stu-id="d524b-144">OUTPUTS</span></span>

### <span data-ttu-id="d524b-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d524b-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="d524b-146">筆記</span><span class="sxs-lookup"><span data-stu-id="d524b-146">NOTES</span></span>

## <span data-ttu-id="d524b-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="d524b-147">RELATED LINKS</span></span>

[<span data-ttu-id="d524b-148">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d524b-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="d524b-149">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d524b-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="d524b-150">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d524b-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
