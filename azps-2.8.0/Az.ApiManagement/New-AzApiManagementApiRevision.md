---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 1a58c34aac272f6c8278833cd356de66774c5a4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614014"
---
# <span data-ttu-id="4c324-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="4c324-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="4c324-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c324-102">SYNOPSIS</span></span>
<span data-ttu-id="4c324-103">建立現有 API 的新修訂版本。</span><span class="sxs-lookup"><span data-stu-id="4c324-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="4c324-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c324-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c324-105">說明</span><span class="sxs-lookup"><span data-stu-id="4c324-105">DESCRIPTION</span></span>

<span data-ttu-id="4c324-106">**AzApiManagementApiRevision** Cmdlet 會在 api 管理內容中為現有 API 建立 api 修正。</span><span class="sxs-lookup"><span data-stu-id="4c324-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="4c324-107">示例</span><span class="sxs-lookup"><span data-stu-id="4c324-107">EXAMPLES</span></span>

### <span data-ttu-id="4c324-108">範例1：建立 API 的空白 API 修訂</span><span class="sxs-lookup"><span data-stu-id="4c324-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="4c324-109">這個命令會建立 api 的 API 版本 `2` `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="4c324-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="4c324-110">範例2：從現有的 Api 建立 API 修訂，並複製所有操作、標籤與原則</span><span class="sxs-lookup"><span data-stu-id="4c324-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
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

<span data-ttu-id="4c324-111">這個命令會建立 api 的 API 版本 `5` `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="4c324-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="4c324-112">參數</span><span class="sxs-lookup"><span data-stu-id="4c324-112">PARAMETERS</span></span>

### <span data-ttu-id="4c324-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4c324-113">-ApiId</span></span>
<span data-ttu-id="4c324-114">要建立其修正的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c324-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="4c324-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="4c324-115">-ApiRevision</span></span>
<span data-ttu-id="4c324-116">Api 的修訂識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c324-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="4c324-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="4c324-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="4c324-118">Api 修訂版說明。</span><span class="sxs-lookup"><span data-stu-id="4c324-118">Api Revision Description.</span></span> <span data-ttu-id="4c324-119">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="4c324-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="4c324-120">-內容</span><span class="sxs-lookup"><span data-stu-id="4c324-120">-Context</span></span>
<span data-ttu-id="4c324-121">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="4c324-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4c324-122">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="4c324-122">This parameter is required.</span></span>

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

### <span data-ttu-id="4c324-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c324-123">-DefaultProfile</span></span>
<span data-ttu-id="4c324-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c324-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c324-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="4c324-125">-ServiceUrl</span></span>
<span data-ttu-id="4c324-126">在後端服務中公開 API 之 web 服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="4c324-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="4c324-127">這個 URL 將只由 Azure API 管理使用，不會公開。</span><span class="sxs-lookup"><span data-stu-id="4c324-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="4c324-128">長度必須是1到2000個字元。</span><span class="sxs-lookup"><span data-stu-id="4c324-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="4c324-129">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="4c324-129">This parameter is required.</span></span>

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

### <span data-ttu-id="4c324-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="4c324-130">-SourceApiRevision</span></span>
<span data-ttu-id="4c324-131">來源 API 的 Api 修正版本識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c324-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="4c324-132">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="4c324-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="4c324-133">-確認</span><span class="sxs-lookup"><span data-stu-id="4c324-133">-Confirm</span></span>
<span data-ttu-id="4c324-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4c324-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c324-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c324-135">-WhatIf</span></span>
<span data-ttu-id="4c324-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4c324-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c324-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c324-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c324-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c324-138">CommonParameters</span></span>
<span data-ttu-id="4c324-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c324-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c324-140">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4c324-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c324-141">輸入</span><span class="sxs-lookup"><span data-stu-id="4c324-141">INPUTS</span></span>

### <span data-ttu-id="4c324-142">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="4c324-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4c324-143">System.object</span><span class="sxs-lookup"><span data-stu-id="4c324-143">System.String</span></span>

## <span data-ttu-id="4c324-144">輸出</span><span class="sxs-lookup"><span data-stu-id="4c324-144">OUTPUTS</span></span>

### <span data-ttu-id="4c324-145">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="4c324-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="4c324-146">筆記</span><span class="sxs-lookup"><span data-stu-id="4c324-146">NOTES</span></span>

## <span data-ttu-id="4c324-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c324-147">RELATED LINKS</span></span>

[<span data-ttu-id="4c324-148">AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4c324-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="4c324-149">移除-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4c324-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="4c324-150">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4c324-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)