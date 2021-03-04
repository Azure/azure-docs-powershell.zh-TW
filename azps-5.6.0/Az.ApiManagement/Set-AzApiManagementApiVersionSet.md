---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 125e349fd2644fcfcd4cf2b6758fe45c40f323b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917113"
---
# <span data-ttu-id="28928-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="28928-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="28928-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28928-102">SYNOPSIS</span></span>
<span data-ttu-id="28928-103">更新 API 管理內容中的 API 版本集。</span><span class="sxs-lookup"><span data-stu-id="28928-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="28928-104">語法</span><span class="sxs-lookup"><span data-stu-id="28928-104">SYNTAX</span></span>

### <span data-ttu-id="28928-105">展開Parameter (預設) </span><span class="sxs-lookup"><span data-stu-id="28928-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28928-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="28928-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28928-107">描述</span><span class="sxs-lookup"><span data-stu-id="28928-107">DESCRIPTION</span></span>

<span data-ttu-id="28928-108">**Set-AzApiManagementApiVersionSet** Cmdlet 會修改 Azure API 管理 API 版本集。</span><span class="sxs-lookup"><span data-stu-id="28928-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="28928-109">例子</span><span class="sxs-lookup"><span data-stu-id="28928-109">EXAMPLES</span></span>

### <span data-ttu-id="28928-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="28928-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="28928-111">此命令會使用版本配置和 Header 參數更新現有的 API 版本 `Header` 集 `api-version` 。</span><span class="sxs-lookup"><span data-stu-id="28928-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="28928-112">參數</span><span class="sxs-lookup"><span data-stu-id="28928-112">PARAMETERS</span></span>

### <span data-ttu-id="28928-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="28928-113">-ApiVersionSetId</span></span>
<span data-ttu-id="28928-114">新 API 版本集的識別碼。</span><span class="sxs-lookup"><span data-stu-id="28928-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="28928-115">-內容</span><span class="sxs-lookup"><span data-stu-id="28928-115">-Context</span></span>
<span data-ttu-id="28928-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="28928-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="28928-117">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="28928-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28928-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28928-118">-DefaultProfile</span></span>
<span data-ttu-id="28928-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="28928-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28928-120">-描述</span><span class="sxs-lookup"><span data-stu-id="28928-120">-Description</span></span>
<span data-ttu-id="28928-121">Api 版本集的描述。</span><span class="sxs-lookup"><span data-stu-id="28928-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="28928-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="28928-122">-HeaderName</span></span>
<span data-ttu-id="28928-123">包含版本資訊的標題值。</span><span class="sxs-lookup"><span data-stu-id="28928-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="28928-124">如果已選擇版本設計方案 HEADER，則必須指定此值。</span><span class="sxs-lookup"><span data-stu-id="28928-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="28928-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28928-125">-InputObject</span></span>
<span data-ttu-id="28928-126">PsApiManagementApiVersionSet 實例。</span><span class="sxs-lookup"><span data-stu-id="28928-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="28928-127">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="28928-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28928-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="28928-128">-Name</span></span>
<span data-ttu-id="28928-129">ApiVersion 集的名稱。</span><span class="sxs-lookup"><span data-stu-id="28928-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="28928-130">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="28928-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="28928-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28928-131">-PassThru</span></span>
<span data-ttu-id="28928-132">如果指定的話，代表已修改 apiVersionSet 的 Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet 類型就會寫入輸出。</span><span class="sxs-lookup"><span data-stu-id="28928-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28928-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="28928-133">-QueryName</span></span>
<span data-ttu-id="28928-134">包含版本資訊之查詢值。</span><span class="sxs-lookup"><span data-stu-id="28928-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="28928-135">如果選擇版本設計方案查詢，則必須指定此值。</span><span class="sxs-lookup"><span data-stu-id="28928-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="28928-136">-方案</span><span class="sxs-lookup"><span data-stu-id="28928-136">-Scheme</span></span>
<span data-ttu-id="28928-137">要針對 Api 版本設定集選取的版本設定設定。</span><span class="sxs-lookup"><span data-stu-id="28928-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="28928-138">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="28928-138">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28928-139">-確認</span><span class="sxs-lookup"><span data-stu-id="28928-139">-Confirm</span></span>
<span data-ttu-id="28928-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="28928-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28928-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28928-141">-WhatIf</span></span>
<span data-ttu-id="28928-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28928-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28928-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28928-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28928-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28928-144">CommonParameters</span></span>
<span data-ttu-id="28928-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28928-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28928-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28928-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28928-147">輸入</span><span class="sxs-lookup"><span data-stu-id="28928-147">INPUTS</span></span>

### <span data-ttu-id="28928-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="28928-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="28928-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="28928-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="28928-150">System.String</span><span class="sxs-lookup"><span data-stu-id="28928-150">System.String</span></span>

### <span data-ttu-id="28928-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementVersioningS方體</span><span class="sxs-lookup"><span data-stu-id="28928-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="28928-152">輸出</span><span class="sxs-lookup"><span data-stu-id="28928-152">OUTPUTS</span></span>

### <span data-ttu-id="28928-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="28928-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="28928-154">筆記</span><span class="sxs-lookup"><span data-stu-id="28928-154">NOTES</span></span>

## <span data-ttu-id="28928-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="28928-155">RELATED LINKS</span></span>

[<span data-ttu-id="28928-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="28928-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="28928-157">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="28928-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="28928-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="28928-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
