---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 126f30e732bc9c55c78c94d6c802b05a18ce29db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912506"
---
# <span data-ttu-id="ef80c-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ef80c-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="ef80c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ef80c-102">SYNOPSIS</span></span>
<span data-ttu-id="ef80c-103">建立 API 版本集。</span><span class="sxs-lookup"><span data-stu-id="ef80c-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="ef80c-104">語法</span><span class="sxs-lookup"><span data-stu-id="ef80c-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef80c-105">描述</span><span class="sxs-lookup"><span data-stu-id="ef80c-105">DESCRIPTION</span></span>
<span data-ttu-id="ef80c-106">**New-AzApiManagementApiVersionSet** Cmdlet 在 Azure API 管理內容中建立 API 版本集實體。</span><span class="sxs-lookup"><span data-stu-id="ef80c-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="ef80c-107">例子</span><span class="sxs-lookup"><span data-stu-id="ef80c-107">EXAMPLES</span></span>

### <span data-ttu-id="ef80c-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="ef80c-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

ApiVersionSetId   : ea9a87cd-a699-4a75-bf7d-909846b91268
Description       : version by xmsversion
VersionQueryName  :
VersionHeaderName : x-ms-version
DisplayName       : newversion
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/ea9a87cd-a699-4a75-bf7d-909846b91268
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="ef80c-109">此命令會建立 API 版本集，其中的版本設定配置 `Query` 和查詢參數 `api-version` 。</span><span class="sxs-lookup"><span data-stu-id="ef80c-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="ef80c-110">參數</span><span class="sxs-lookup"><span data-stu-id="ef80c-110">PARAMETERS</span></span>

### <span data-ttu-id="ef80c-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="ef80c-111">-ApiVersionSetId</span></span>
<span data-ttu-id="ef80c-112">新 API 版本集的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef80c-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="ef80c-113">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="ef80c-113">This parameter is optional.</span></span>
<span data-ttu-id="ef80c-114">如果未指定，將會產生識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef80c-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="ef80c-115">-內容</span><span class="sxs-lookup"><span data-stu-id="ef80c-115">-Context</span></span>
<span data-ttu-id="ef80c-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="ef80c-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ef80c-117">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="ef80c-117">This parameter is required.</span></span>

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

### <span data-ttu-id="ef80c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef80c-118">-DefaultProfile</span></span>
<span data-ttu-id="ef80c-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef80c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef80c-120">-描述</span><span class="sxs-lookup"><span data-stu-id="ef80c-120">-Description</span></span>
<span data-ttu-id="ef80c-121">Api 版本集的描述。</span><span class="sxs-lookup"><span data-stu-id="ef80c-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="ef80c-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="ef80c-122">-HeaderName</span></span>
<span data-ttu-id="ef80c-123">包含版本資訊的標題值。</span><span class="sxs-lookup"><span data-stu-id="ef80c-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="ef80c-124">如果已選擇版本設計方案 HEADER，則必須指定此值。</span><span class="sxs-lookup"><span data-stu-id="ef80c-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="ef80c-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef80c-125">-Name</span></span>
<span data-ttu-id="ef80c-126">ApiVersion 集的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef80c-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="ef80c-127">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="ef80c-127">This parameter is required.</span></span>

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

### <span data-ttu-id="ef80c-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="ef80c-128">-QueryName</span></span>
<span data-ttu-id="ef80c-129">包含版本資訊之查詢值。</span><span class="sxs-lookup"><span data-stu-id="ef80c-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="ef80c-130">如果選擇版本設計方案查詢，則必須指定此值。</span><span class="sxs-lookup"><span data-stu-id="ef80c-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="ef80c-131">-方案</span><span class="sxs-lookup"><span data-stu-id="ef80c-131">-Scheme</span></span>
<span data-ttu-id="ef80c-132">要針對 Api 版本設定集選取的版本設定設定。</span><span class="sxs-lookup"><span data-stu-id="ef80c-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="ef80c-133">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="ef80c-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef80c-134">-確認</span><span class="sxs-lookup"><span data-stu-id="ef80c-134">-Confirm</span></span>
<span data-ttu-id="ef80c-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ef80c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef80c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef80c-136">-WhatIf</span></span>
<span data-ttu-id="ef80c-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef80c-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef80c-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef80c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef80c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef80c-139">CommonParameters</span></span>
<span data-ttu-id="ef80c-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ef80c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef80c-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef80c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef80c-142">輸入</span><span class="sxs-lookup"><span data-stu-id="ef80c-142">INPUTS</span></span>

### <span data-ttu-id="ef80c-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="ef80c-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ef80c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ef80c-144">System.String</span></span>

### <span data-ttu-id="ef80c-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementVersioningS方體</span><span class="sxs-lookup"><span data-stu-id="ef80c-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="ef80c-146">輸出</span><span class="sxs-lookup"><span data-stu-id="ef80c-146">OUTPUTS</span></span>

### <span data-ttu-id="ef80c-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ef80c-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="ef80c-148">筆記</span><span class="sxs-lookup"><span data-stu-id="ef80c-148">NOTES</span></span>

## <span data-ttu-id="ef80c-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef80c-149">RELATED LINKS</span></span>

[<span data-ttu-id="ef80c-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ef80c-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="ef80c-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ef80c-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="ef80c-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ef80c-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)