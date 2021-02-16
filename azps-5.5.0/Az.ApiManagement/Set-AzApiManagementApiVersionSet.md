---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: d85d480adc5d6c588c7da2f03c514258dc96a9e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141655"
---
# <span data-ttu-id="9e993-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9e993-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="9e993-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e993-102">SYNOPSIS</span></span>
<span data-ttu-id="9e993-103">更新 API 管理內容中設定的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="9e993-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="9e993-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e993-104">SYNTAX</span></span>

### <span data-ttu-id="9e993-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="9e993-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e993-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9e993-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e993-107">說明</span><span class="sxs-lookup"><span data-stu-id="9e993-107">DESCRIPTION</span></span>

<span data-ttu-id="9e993-108">**AzApiManagementApiVersionSet** Cmdlet 會修改 Azure API 管理 API 版本設定。</span><span class="sxs-lookup"><span data-stu-id="9e993-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="9e993-109">示例</span><span class="sxs-lookup"><span data-stu-id="9e993-109">EXAMPLES</span></span>

### <span data-ttu-id="9e993-110">範例1</span><span class="sxs-lookup"><span data-stu-id="9e993-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="9e993-111">這個命令會更新現有的 API 版本集與版本設定配置 `Header` 和標頭參數 `api-version` 。</span><span class="sxs-lookup"><span data-stu-id="9e993-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="9e993-112">參數</span><span class="sxs-lookup"><span data-stu-id="9e993-112">PARAMETERS</span></span>

### <span data-ttu-id="9e993-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="9e993-113">-ApiVersionSetId</span></span>
<span data-ttu-id="9e993-114">新 API 版本集的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e993-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="9e993-115">-內容</span><span class="sxs-lookup"><span data-stu-id="9e993-115">-Context</span></span>
<span data-ttu-id="9e993-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="9e993-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9e993-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="9e993-117">This parameter is required.</span></span>

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

### <span data-ttu-id="9e993-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e993-118">-DefaultProfile</span></span>
<span data-ttu-id="9e993-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e993-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e993-120">-描述</span><span class="sxs-lookup"><span data-stu-id="9e993-120">-Description</span></span>
<span data-ttu-id="9e993-121">Api 版本集的描述。</span><span class="sxs-lookup"><span data-stu-id="9e993-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="9e993-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="9e993-122">-HeaderName</span></span>
<span data-ttu-id="9e993-123">將包含版本設定資訊的標頭值。</span><span class="sxs-lookup"><span data-stu-id="9e993-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="9e993-124">如果選擇 [版本配置] 標題，則必須指定此值。</span><span class="sxs-lookup"><span data-stu-id="9e993-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="9e993-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e993-125">-InputObject</span></span>
<span data-ttu-id="9e993-126">PsApiManagementApiVersionSet 的實例。</span><span class="sxs-lookup"><span data-stu-id="9e993-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="9e993-127">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="9e993-127">This parameter is required.</span></span>

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

### <span data-ttu-id="9e993-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e993-128">-Name</span></span>
<span data-ttu-id="9e993-129">ApiVersion 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e993-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="9e993-130">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9e993-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="9e993-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e993-131">-PassThru</span></span>
<span data-ttu-id="9e993-132">如果已指定，則會將代表已修改之 apiVersionSet 的 PsApiManagementApiVersionSet 類型的 ServiceManagement 類型 ApiManagement 寫入輸出。</span><span class="sxs-lookup"><span data-stu-id="9e993-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="9e993-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="9e993-133">-QueryName</span></span>
<span data-ttu-id="9e993-134">會包含版本設定資訊的查詢值。</span><span class="sxs-lookup"><span data-stu-id="9e993-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="9e993-135">如果選擇 [版本設定模式] 查詢，則必須指定此值。</span><span class="sxs-lookup"><span data-stu-id="9e993-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="9e993-136">-配置</span><span class="sxs-lookup"><span data-stu-id="9e993-136">-Scheme</span></span>
<span data-ttu-id="9e993-137">針對 Api 版本設定選取的版本設定配置。</span><span class="sxs-lookup"><span data-stu-id="9e993-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="9e993-138">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9e993-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="9e993-139">-確認</span><span class="sxs-lookup"><span data-stu-id="9e993-139">-Confirm</span></span>
<span data-ttu-id="9e993-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9e993-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e993-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e993-141">-WhatIf</span></span>
<span data-ttu-id="9e993-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9e993-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e993-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e993-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e993-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e993-144">CommonParameters</span></span>
<span data-ttu-id="9e993-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e993-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e993-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9e993-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e993-147">輸入</span><span class="sxs-lookup"><span data-stu-id="9e993-147">INPUTS</span></span>

### <span data-ttu-id="9e993-148">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9e993-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9e993-149">ServiceManagement. PsApiManagementApiVersionSet （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9e993-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="9e993-150">System.object</span><span class="sxs-lookup"><span data-stu-id="9e993-150">System.String</span></span>

### <span data-ttu-id="9e993-151">ServiceManagement. PsApiManagementVersioningScheme （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9e993-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="9e993-152">輸出</span><span class="sxs-lookup"><span data-stu-id="9e993-152">OUTPUTS</span></span>

### <span data-ttu-id="9e993-153">ServiceManagement. PsApiManagementApiVersionSet （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9e993-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="9e993-154">筆記</span><span class="sxs-lookup"><span data-stu-id="9e993-154">NOTES</span></span>

## <span data-ttu-id="9e993-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e993-155">RELATED LINKS</span></span>

[<span data-ttu-id="9e993-156">AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9e993-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="9e993-157">新-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9e993-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="9e993-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9e993-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
